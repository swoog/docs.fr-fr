---
title: Utilisation de noms forts et les bibliothèques .NET
description: Meilleures pratiques recommandées pour les bibliothèques .NET d’affectation de noms forts.
author: jamesnk
ms.author: mairaw
ms.date: 10/16/2018
ms.openlocfilehash: e3f7d443eb9acc84c800ea2611b803733085391c
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49372804"
---
# <a name="strong-naming"></a>Affectation de noms forts

Utilisation de noms forts fait référence à la signature d’un assembly avec une clé, produisant un [assembly avec nom fort](../../framework/app-domains/strong-named-assemblies.md). Lorsqu’un assembly est un nom fort, il crée une identité unique basée sur le numéro de version d’assembly et un nom, et il peut aider à éviter les conflits de l’assembly.

L’inconvénient de l’utilisation de noms forts est que le .NET Framework sur Windows permet strict lors du chargement des assemblys une fois qu’un assembly possède un nom fort. Une référence d’assembly avec nom fort doit correspondre exactement à la version référencée par un assembly, forcer les développeurs à [configurer des redirections de liaison](../../framework/configure-apps/redirect-assembly-versions.md) lors de l’utilisation de l’assembly :

```xml
<configuration>
   <runtime>
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
         <dependentAssembly>
            <assemblyIdentity name="myAssembly" publicKeyToken="32ab4ba45e0a69a1" culture="neutral" />
            <bindingRedirect oldVersion="1.0.0.0" newVersion="2.0.0.0"/>
         </dependentAssembly>
      </assemblyBinding>
   </runtime>
</configuration>
```

Lorsque les développeurs .NET se plaignent de noms forts, qu’ils sont généralement plaignent est strict chargement d’assembly. Heureusement, ce problème est isolé sur le .NET Framework. .NET core, Xamarin, UWP et la plupart des autres implémentations .NET n’avez pas le chargement des assemblys strict et supprime le principal inconvénient des noms forts.

Un aspect important des noms forts est qu’il s’agit viral : un nom fort référence qu’assembly autres fort nommé assemblys. Si votre bibliothèque n’est pas forte nommé, vous avez exclus des développeurs qui créent une application ou une bibliothèque qui a besoin des noms forts à partir de l’utiliser.

Les avantages de l’utilisation de noms forts sont :

1. L’assembly peut être référencé et utilisé par d’autres assemblys avec nom fort.
2. L’assembly peut être stocké dans le Global Assembly Cache (GAC).
3. L’assembly peut être chargé côte à côte avec d’autres versions de l’assembly. Le chargement des assemblys côte à côte sont généralement requise par les applications avec des architectures de plug-in.

## <a name="create-strong-named-net-libraries"></a>Créer fort nommé des bibliothèques .NET

Vous devez nommer strong vos bibliothèques de .NET open source. Un assembly de nom fort garantit le plupart des personnes puissent l’utiliser, et strict assembly en le chargeant uniquement affecte le .NET Framework.

> [!NOTE]
> Ce guide est spécifique aux seules bibliothèques .NET distribuées publiquement, telles que les bibliothèques .NET publiés sur NuGet.org. Utilisation de noms forts n’est pas requis par la plupart des applications .NET et ne doit pas être effectuée par défaut.

**ENVISAGEZ de ✔️** strong naming les assemblys de votre bibliothèque.

**ENVISAGEZ de ✔️** archiver la clé utilisée pour le nom fort dans votre système de contrôle de code source.

> Une clé disponible publiquement permet aux développeurs de modifier et recompiler votre code source de la bibliothèque avec la même clé.

> [!IMPORTANT]
> Lorsqu’une identité de chiffrement est souhaitée, [Authenticode](/windows-hardware/drivers/install/authenticode) et [la signature du Package NuGet](/nuget/create-packages/sign-a-package) sont recommandés. Utilisation de noms forts ne doit pas être utilisée pour les considérations de sécurité.

**ENVISAGEZ de ✔️** incrémentation de la version d’assembly sur les modifications de version principale uniquement pour aider les utilisateurs à réduire les redirections de liaison et la fréquence à laquelle ils sont mis à jour.

> En savoir plus sur [le contrôle de version et la version d’assembly](./versioning.md#assembly-version).

**N’est pas le cas de ❌** ajouter, supprimer ou modifier la clé d’affectation de noms forte.

> Modification de la clé d’affectation de noms forts d’un assembly modifie l’identité de l’assembly et altère le code compilé qui l’utilise. Pour plus d’informations, consultez [binaire de modifications avec rupture](./breaking-changes.md#binary-breaking-change).

**N’est pas le cas de ❌** publier avec nom fort et non-fort des versions de votre bibliothèque. Par exemple : `Contoso.Api` et `Contoso.Api.StrongNamed`.

> Publication deux branchements de packages de votre écosystème de développeur. En outre, si une application se retrouve selon les deux packages le développeur peut rencontrer des conflits de noms de type. Comme ce qui concerne .NET est qu’ils sont différents types dans des assemblys différents.

>[!div class="step-by-step"]
[Précédent](./cross-platform-targeting.md)
[Suivant](./nuget.md)
