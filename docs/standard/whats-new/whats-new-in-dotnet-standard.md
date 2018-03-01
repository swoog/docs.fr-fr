---
title: "Nouveautés de .NET Standard"
ms.custom: updateeachrelease
ms.date: 11/08/2017
ms.prod: .net
ms.topic: article
ms.technology: dotnet-standard
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 3a5833bdfcf1e3433ea82403908e9a06a88cde27
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="whats-new-in-the-net-standard"></a>Nouveautés de .NET Standard

.NET Standard est une spécification formelle qui définit un ensemble par version de l’API qui doit être disponible sur des mises en œuvre .NET conformes à cette version de la norme. .NET Standard est destiné aux développeurs de bibliothèques. Une bibliothèque qui cible une version .NET Standard peut être utilisée sur n’importe quelle implémentation .NET Framework, .NET Core ou Xamarin prenant en charge cette version de la norme.

La version la plus récente de .NET Standard est 2.0. Elle est incluse dans le Kit SDK .NET Core 2.0 et dans Visual Studio 2017 version 15.3 avec la charge de travail .NET Core installée.

## <a name="supported-net-implementations"></a>Implémentations de .NET prises en charge

Les implémentations .NET suivantes prennent en charge la norme .NET Standard 2.0 :

- .NET Core 2.0
- .NET Framework 4.6.1
- Mono 5.4
- Xamarin.iOS 10.14
- Xamarin.Mac 3.8
- Xamarin.Android 8.0
- Plateforme Windows universelle 10.0.16299

## <a name="whats-new-in-the-net-standard-20"></a>Nouveautés de .NET Standard 2.0
 
.NET Standard 2.0 inclut les nouvelles fonctionnalités suivantes :

**Un ensemble d’API beaucoup plus complet**

Jusqu'à la version 1.6, .NET Standard incluait un sous-ensemble d’API relativement limité. Ce sous-ensemble excluait de nombreuses API utilisées dans .NET Framework ou Xamarin. Cela complique le développement en obligeant les développeurs à trouver des remplacements appropriés pour les API courantes lorsqu’ils développent des applications et des bibliothèques ciblant plusieurs implémentations .NET. .NET Standard 2.0 lève cette limitation en ajoutant plus de 20 000 API supplémentaires par rapport à .NET Standard 1.6, la version précédente de la norme. Pour obtenir la liste des API ajoutées à .NET Standard 2.0, voir [.NET Standard 2.0 vs 1.6](https://raw.githubusercontent.com/dotnet/standard/master/docs/versions/netstandard2.0_diff.md). 

Voici certains des ajouts à l’espace de noms <xref:System> dans .NET Standard 2.0 :

- Prise en charge de la classe <xref:System.AppDomain>.
- Meilleure prise en charge de l’utilisation de tableaux provenant d’autres membres de la classe <xref:System.Array>.
- Meilleure prise en charge de l’utilisation d’attributs provenant d’autres membres de la classe <xref:System.Attribute>.
- Meilleure prise en charge du calendrier et d’autres options de mise en forme pour les valeurs <xref:System.DateTime>.
- Ajout d’une fonctionnalité d’arrondi <xref:System.Decimal>.
- Ajout d’une fonctionnalité à la classe <xref:System.Environment>.
- Meilleur contrôle du récupérateur de mémoire via la classe <xref:System.GC>.
- Meilleure prise en charge de la comparaison de chaînes, de l’énumération et de la normalisation dans la classe <xref:System.String>.
- Prise en charge des ajustements à l’heure d’été et des durées de transition dans les classes <xref:System.TimeZoneInfo.AdjustmentRule> et <xref:System.TimeZoneInfo.TransitionTime>.
- Importante amélioration de la fonctionnalité dans la classe <xref:System.Type>.
- Meilleure prise en charge de la désérialisation des objets d’exception par ajout d’un constructeur d’exception avec les paramètres <xref:System.Runtime.Serialization.SerializationInfo> et <xref:System.Runtime.Serialization.StreamingContext>.

**Prise en charge des bibliothèques .NET Framework**

La très grande majorité des bibliothèques ciblent .NET Framework plutôt que .NET Standard. Toutefois, la plupart des appels dans ces bibliothèques sont dirigés vers les API incluses dans .NET Standard 2.0. À partir de .NET Standard 2.0, vous pouvez accéder aux bibliothèques .NET Framework depuis une bibliothèque .NET Standard en utilisant un [correctif de compatibilité](https://github.com/dotnet/standard/blob/master/docs/netstandard-20/README.md#assembly-unification). Cette couche de compatibilité est transparente pour les développeurs ; vous n’avez rien à faire pour tirer parti des bibliothèques .NET Framework.

La seule condition est que les API appelées par la bibliothèque de classes .NET Framework doivent être incluses dans .NET Standard 2.0.

**Prise en charge de Visual Basic**

Vous pouvez désormais développer des bibliothèques .NET Standard dans Visual Basic. Pour les développeurs Visual Basic qui utilisent Visual Studio 2017 version 15.3 ou ultérieure avec la charge de travail .NET Core installée, Visual Studio inclut désormais un modèle de bibliothèque de classe .NET Standard. Pour les développeurs Visual Basic qui utilisent d’autres outils de développement et environnements, vous pouvez utiliser la commande [dotnet new](../../core/tools/dotnet-new.md) pour créer un projet de bibliothèque .NET Standard. Pour plus d’informations, consultez [Prise en charge des outils pour les bibliothèques .NET Standard](#tooling).

<a name="tooling" />**Prise en charge des outils pour les bibliothèques .NET Standard**

Avec les versions .NET Core 2.0 et .NET Standard 2.0, Studio Visual 2017 et l[’interface de ligne de commande (CLI) .NET Core](../../core/tools/index.md) incluent la prise en charge des outils pour la création de bibliothèques .NET Standard. 

Si vous installez Visual Studio avec la charge de travail **Développement multiplateforme .NET Core**, vous pouvez créer un projet de bibliothèque .NET Standard 2.0 à l’aide d’un modèle de projet, comme le montre l’illustration suivante. 

# <a name="ctabcsharp"></a>[C#](#tab/csharp)
![Ajouter un nouveau projet de bibliothèque .NET Standard](./media/std-project-cs.png)
# <a name="visual-basictabvisual-basic"></a>[Visual Basic](#tab/visual-basic)
<a name="add-new-net-standard-library-projectmediastd-project-vbpng"></a>![Ajouter un nouveau projet de bibliothèque .NET Standard](./media/std-project-vb.png)
---

Si vous utilisez l’interface CLI .NET Core, la commande [dotnet new](../../core/tools/dotnet-new.md) suivante crée un projet de bibliothèque de classes qui cible .NET Standard 2.0.

```csharp
dotnet new classlib
```
```vb
dotnet new classlib -lang vb
```
  
## <a name="see-also"></a>Voir aussi
[.NET Standard](../net-standard.md)
[Présentation de .NET Standard](https://blogs.msdn.microsoft.com/dotnet/2016/09/26/introducing-net-standard/)
