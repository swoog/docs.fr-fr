---
title: Sceller
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- limiting extensibility
- classes [.NET Framework], sealing
- preventing customization
- sealed classes
ms.assetid: cc42267f-bb7a-427a-845e-df97408528d4
author: KrzysztofCwalina
ms.openlocfilehash: fd1abdb4ff6f4850eea96bcfc3afbfe00a4ae56a
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53127691"
---
# <a name="sealing"></a>Sceller
L’une des fonctionnalités d’infrastructures et orienté objet est que les développeurs peuvent étendre et personnaliser les manières imprévus par les concepteurs de framework. Il s’agit la puissance et le risque de conception extensible. Lorsque vous concevez votre infrastructure, il est donc très important de concevoir soigneusement pour l’extensibilité lorsqu’il est nécessaire et pour limiter l’extensibilité lorsqu’il est dangereux.  
  
 Scellement d’un mécanisme puissant qui empêche d’extensibilité. Vous pouvez sceller la classe ou des membres individuels. Sceller une classe empêche les utilisateurs d’en hériter de la classe. Le fait de sceller un membre empêche les utilisateurs de remplacer un membre particulier.  
  
 **X DO NOT** sceller des classes sans avoir une bonne raison de le faire.  
  
 Le fait de sceller une classe, car vous ne pouvez pas considérer un scénario d’extensibilité n’est pas une bonne raison. Framework d’utilisateurs apprécient de hériter de classes pour diverses raisons identifiable, comme l’ajout de membres de commodité. Consultez [Classes Unsealed](../../../docs/standard/design-guidelines/unsealed-classes.md) pour obtenir des exemples de raisons identifiable les utilisateurs souhaitent hériter d’un type.  
  
 Bonnes raisons pour sceller une classe sont les suivantes :  
  
-   La classe est une classe statique. Consultez [conception de classes statiques](../../../docs/standard/design-guidelines/static-class.md).  
  
-   La classe stocke les clés secrètes sensibles à la sécurité dans les membres protégés hérités.  
  
-   La classe hérite de nombreux membres virtuels et le coût de leur scellement individuellement serait dépassent les avantages de la classe non scellés.  
  
-   La classe est un attribut qui nécessite la recherche d’exécution très rapide. Attributs sealed ont des niveaux de performances légèrement plus élevés que ceux non scellé. consultez [attributs](../../../docs/standard/design-guidelines/attributes.md).  
  
 **X DO NOT** déclarer les membres virtuels ou protégés sur les types sealed.  
  
 Par définition, les types sealed ne peut pas être héritées. Cela signifie que les membres protégés sur les types sealed ne peut pas être appelées, et les méthodes virtuelles sur les types sealed ne peut pas être substituées.  
  
 **✓ CONSIDER** sceller les membres que vous substituez.  
  
 Les problèmes qui peuvent résulter de présentation de membres virtuels (abordées dans [membres virtuels](../../../docs/standard/design-guidelines/virtual-members.md)) s’appliquent aux remplacements de même, bien qu’à un degré légèrement moindre. Le fait de sceller un remplacement vous protège ces problèmes à partir de ce point dans la hiérarchie d’héritage.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
- [Classes unsealed](../../../docs/standard/design-guidelines/unsealed-classes.md)
