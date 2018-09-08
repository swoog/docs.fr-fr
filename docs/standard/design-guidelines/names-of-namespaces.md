---
title: Noms d'espaces de noms
ms.date: 03/30/2017
helpviewer_keywords:
- names [.NET Framework], conflicts
- names [.NET Framework], namespaces
- type names, conflicts
- namespaces [.NET Framework], names
- names [.NET Framework], type names
ms.assetid: a49058d2-0276-43a7-9502-04adddf857b2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6d68966f60c5039fd67195a03facc1586b9ed154
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44183260"
---
# <a name="names-of-namespaces"></a>Noms d'espaces de noms
Comme avec les autres instructions d’affectation de noms, l’objectif lorsque vous nommez des espaces de noms consiste à créer suffisamment claire pour le programmeur immédiatement savoir qui est le contenu de l’espace de noms susceptible d’être à l’aide de l’infrastructure. Le modèle suivant spécifie la règle générale pour nommer les espaces de noms :  
  
 `<Company>.(<Product>|<Technology>)[.<Feature>][.<Subnamespace>]`  
  
 Voici quelques exemples :  
  
 `Fabrikam.Math`  
 `Litware.Security`  
  
 **✓ DO** faites précéder les noms d’espace de noms avec un nom de société pour empêcher les espaces de noms provenant de différentes sociétés de ne pas avoir le même nom.  
  
 **✓ DO** utiliser un nom de produit indépendant de la version stable au deuxième niveau d’un espace de noms.  
  
 **X DO NOT** utiliser des hiérarchies d’organisation comme base pour les noms dans les hiérarchies de l’espace de noms, étant donné que les noms de groupe au sein des entreprises ont tendance à être de courte durée de vie. Organiser la hiérarchie d’espaces de noms autour des groupes de technologies associées.  
  
 **✓ DO** utilisent la casse Pascal et des composants de l’espace de noms distinct avec des périodes (par exemple, `Microsoft.Office.PowerPoint`). Si votre marque utilise une casse non traditionnelle, vous devez suivre la casse définie par votre marque, même s’il diffère de casse de l’espace de noms normal.  
  
 **✓ CONSIDER** à l’aide de noms au pluriel, le cas échéant.  
  
 Par exemple, utilisez `System.Collections` au lieu de `System.Collection`. Noms de marques et les acronymes sont toutefois des exceptions à cette règle. Par exemple, utilisez `System.IO` au lieu de `System.IOs`.  
  
 **X DO NOT** utiliser le même nom pour un espace de noms et un type dans cet espace de noms.  
  
 Par exemple, n’utilisez pas `Debug` comme un espace de noms nommer et fournissez également une classe nommée `Debug` dans le même espace de noms. Plusieurs compilateurs exigent que ces types doivent être qualifiés complets.  
  
### <a name="namespaces-and-type-name-conflicts"></a>Espaces de noms et nom de Type est en conflit  
 **X DO NOT** présentent des noms de type générique comme `Element`, `Node`, `Log`, et `Message`.  
  
 Il est fort probable que cela entraîne à taper le nom est en conflit en commun des scénarios. Vous devez qualifier les noms de type générique (`FormElement`, `XmlNode`, `EventLog`, `SoapMessage`).  
  
 Il existe des recommandations spécifiques pour éviter les conflits de nom de type pour différentes catégories d’espaces de noms.  
  
-   **Espaces de noms de modèle application**  
  
     Espaces de noms appartenant à un modèle d’application unique sont très souvent utilisés ensemble, mais ils sont presque jamais utilisés avec les espaces de noms des autres modèles d’application. Par exemple, le <xref:System.Windows.Forms?displayProperty=nameWithType> espace de noms est très rarement utilisée conjointement avec la <xref:System.Web.UI?displayProperty=nameWithType> espace de noms. Voici une liste connue modèle espace de noms de groupes d’applications :  
  
     `System.Windows*`   
     `System.Web.UI*`  
  
     **X DO NOT** donner le même nom aux types dans les espaces de noms dans un modèle d’application unique.  
  
     Par exemple, n’ajoutez pas d’un type nommé `Page` à la <xref:System.Web.UI.Adapters?displayProperty=nameWithType> espace de noms, car le <xref:System.Web.UI?displayProperty=nameWithType> espace de noms contient déjà un type nommé `Page`.  
  
-   **Espaces de noms infrastructure**  
  
     Ce groupe contient des espaces de noms qui sont rarement importées pendant le développement d’applications courantes. Par exemple, `.Design` espaces de noms sont utilisés principalement lorsque des outils de développement de programmation. Prévention des conflits avec les types dans ces espaces de noms n’est pas critique.  
  
-   **Espaces de noms principaux**  
  
     Espaces de noms Core incluent tous `System` espaces de noms, à l’exclusion des espaces de noms des modèles d’application et les espaces de noms d’Infrastructure. Espaces de noms Core incluent, entre autres, `System`, `System.IO`, `System.Xml`, et `System.Net`.  
  
     **X DO NOT** permettent de types de noms qui sont en conflit avec un type dans les espaces de noms de base.  
  
     Par exemple, n’utilisez jamais `Stream` comme nom de type. Elle serait en conflit avec <xref:System.IO.Stream?displayProperty=nameWithType>, un très couramment utilisés type.  
  
-   **Groupes d’espace de noms de technologies**  
  
     Cette catégorie inclut tous les espaces de noms avec les deux premiers nœuds d’espace de noms même `(<Company>.<Technology>*`), tel que `Microsoft.Build.Utilities` et `Microsoft.Build.Tasks`. Il est important que les types appartenant à une technologie unique ne sont pas en conflit entre eux.  
  
     **X DO NOT** affecter des noms de type qui sont en conflit avec d’autres types au sein d’une seule technologie.  
  
     **X DO NOT** présentent des conflits de nom de type entre les types dans les espaces de noms de technologie et un espace de noms de modèle d’application (à moins que la technologie n’est pas destinée à être utilisée avec le modèle d’application).  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)
