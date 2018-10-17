---
title: Modifications avec rupture et les bibliothèques .NET
description: Meilleures pratiques recommandées pour parcourir les modifications avec rupture lors de la création de bibliothèques .NET.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 83c01fdad7d836877bf692b87eeb0230219ded36
ms.sourcegitcommit: fd8d4587cc26e53f0e27e230d6e27d828ef4306b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370061"
---
# <a name="breaking-changes"></a>Modifications avec rupture

Il est important pour une bibliothèque .NET trouver un équilibre entre la stabilité pour les utilisateurs existants et l’innovation pour l’avenir. Les auteurs de bibliothèque au plus juste pour la refactorisation et à repenser le code jusqu'à ce qu’il est parfait, mais avec rupture de vos utilisateurs existants a un impact négatif, en particulier pour les bibliothèques de bas niveau.

## <a name="project-types-and-breaking-changes"></a>Types de projets et des modifications avec rupture

Comment une bibliothèque est utilisée par la Communauté .NET modifie l’effet des changements sur les développeurs de l’utilisateur final.

* **Faible et des bibliothèques de niveau intermédiaire** comme un analyseur sérialiseur, HTML, mappeur relationnel objet de base de données ou infrastructure web sont plus affectés par les modifications avec rupture.

  Packages de bloc de construction sont utilisés par les développeurs de l’utilisateur final de créer des applications et par d’autres bibliothèques comme dépendances NuGet. Par exemple, vous créez une application et que vous utilisez un client open source pour appeler un service web. Une mise à jour avec rupture à une dépendance qu'utilise le client n’est pas quelque chose que vous pouvez résoudre. C’est le client open source qui doit être modifiée et que vous n’avez aucun contrôle dessus. Vous devez déterminer les versions compatibles des bibliothèques ou soumettre un correctif à la bibliothèque cliente et attendre une nouvelle version. La situation pire est si vous souhaitez utiliser les deux bibliothèques qui dépendent de versions mutuellement incompatibles d’une bibliothèque de tiers.

* **Bibliothèques de haut niveau** comme une suite de l’interface utilisateur des contrôles sont moins sensibles aux modifications avec rupture.

  Bibliothèques de haut niveau sont directement référencés dans une application de l’utilisateur final. En cas de modifications avec rupture, le développeur peut choisir de mettre à jour vers la dernière version, ou permettre modifier leur application de fonctionner avec la modification avec rupture.

**FAIRE ✔️** réflexion sur l’utilisation de votre bibliothèque. Effet des modifications avec rupture aura sur les applications et les bibliothèques qui l’utilisent ?

**FAIRE ✔️** minimiser les modifications avec rupture lors du développement d’une bibliothèque .NET de bas niveau.

**ENVISAGEZ de ✔️** publication majeur de réécriture d’une bibliothèque en tant qu’un nouveau package NuGet.

## <a name="types-of-breaking-changes"></a>Types de modifications avec rupture

Modifications avec rupture se répartissent en différentes catégories et ne sont pas aussi efficaces.

### <a name="source-breaking-change"></a>Modification avec rupture de code source

Une source de modification avec rupture n’affecte pas l’exécution du programme mais provoquera des erreurs de compilation la prochaine fois que l’application est recompilée. Par exemple, une nouvelle surcharge peut créer une ambiguïté dans les appels de méthode qui étaient précédemment non équivoque, ou un paramètre renommé interrompra les appelants qui utilisent des paramètres nommés.

```csharp
public class Task
{
    // Adding a type called Task could conflict with System.Threading.Tasks.Task at compilation
}
```

Étant une source de modification avec rupture uniquement dangereuse lorsque les développeurs recompiler leurs applications, il est la moins perturbatrices modification avec rupture. Les développeurs peuvent résoudre leur propre code source rompu facilement.

### <a name="behavior-breaking-change"></a>Changement de comportement

Changements de comportement sont le type le plus courant de modification avec rupture : une personne peut inhiber les presque n’importe quel changement de comportement. Modifications à votre bibliothèque, telles que les signatures de méthode, les exceptions levées ou d’entrée ou de sortie des formats de données, tout impact négatif sur vos consommateurs de bibliothèque. Même un correctif de bogue peut considéré comme une modification avec rupture Si les utilisateurs s’appuyaient sur le comportement précédemment interrompue.

Ajout de fonctionnalités et l’amélioration de mauvais comportements sont une bonne chose, mais sans les soins il peut rendre très difficile pour les utilisateurs existants à mettre à niveau. Une approche pour aider les développeurs à gérer avec les dernières modifications de comportement consiste à les masquer derrière les paramètres. Paramètres permettent aux développeurs de mettre à jour vers la dernière version de votre bibliothèque tout en choisissant d’accepter ou refuser de modifications avec rupture. Cette stratégie permet aux développeurs de rester à jour tout en permettant à leur code de consommation de s’adapter au fil du temps.

Par exemple, ASP.NET Core MVC a le concept d’un [version compatibilité](/aspnet/core/mvc/compatibility-version) qui modifie les fonctionnalités activées et désactivées sur `MvcOptions`.

**ENVISAGEZ de ✔️** si vous omettez nouvelles fonctionnalités par défaut, si elles affectent les utilisateurs existants et permettent aux développeurs de s’abonner à la fonctionnalité avec un paramètre.

### <a name="binary-breaking-change"></a>Modification avec rupture binaire

Un fichier binaire modification avec rupture qui se produit lorsque vous modifiez l’API publique de votre bibliothèque, afin des assemblys compilés par rapport à des versions antérieures de votre bibliothèque ne sont plus en mesure d’appeler l’API. Par exemple, la modification de signature d’une méthode en ajoutant un nouveau paramètre entraîne assemblys compilés avec l’ancienne version de la bibliothèque lever une <xref:System.MissingMethodException>.

Un fichier binaire modification avec rupture peut également être rompus un **assembly entier**. Modification du nom d’un assembly avec `AssemblyName` changera identité de l’assembly, de même que l’ajout, suppression ou modification d’une clé forte d’affectation de noms de l’assembly. Une modification de l’identité d’un assembly va interrompre tout le code compilé qui l’utilise.

**N’est pas le cas de ❌** modifier un nom d’assembly.

**N’est pas le cas de ❌** ajouter, supprimer ou modifier la clé d’affectation de noms forte.

**ENVISAGEZ de ✔️** à l’aide des classes de base abstraites au lieu d’interfaces.

> Ajouter quoi que ce soit à une interface entraîne des types existants qui implémentent son échec. Classe de base abstraite permet de vous permet d’ajouter une implémentation virtuel par défaut.

**✔️ Envisagez** placer le <xref:System.ObsoleteAttribute> sur les types et membres que vous souhaitez supprimer. L’attribut doit avoir des instructions pour la mise à jour de code de ne plus utiliser l’API obsolète.

> Code qui appelle des types et méthodes avec les <xref:System.ObsoleteAttribute> génère un avertissement de build avec le message fourni à l’attribut. Les personnes de donnent des avertissements qui utilisent l’heure de surface d’API obsolète pour migrer afin que lors de l’API obsolète est supprimé, la plupart n’est plus l’utiliser.

```csharp
public class Document
{
    [Obsolete("LoadDocument(string) is obsolete. Use LoadDocument(Uri) instead.")]
    public static Document LoadDocument(string uri)
    {
        return LoadDocument(new Uri(uri));
    }

    public static Document LoadDocument(Uri uri)
    {
        // Load the document
    }
}
```

## <a name="see-also"></a>Voir aussi

* [Considérations relatives à la version et de mise à jour pour les développeurs c#](../../csharp/whats-new/version-update-considerations.md)
* [Un guide de référence pour les modifications avec rupture des API dans .NET](https://stackoverflow.com/questions/1456785/a-definitive-guide-to-api-breaking-changes-in-net)
* [Règles de modification avec rupture CoreFX](https://github.com/dotnet/corefx/blob/master/Documentation/coding-guidelines/breaking-change-rules.md)

>[!div class="step-by-step"]
[Précédent](./versioning.md)
