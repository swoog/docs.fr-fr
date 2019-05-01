---
title: Conception d'interfaces
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- interfaces [.NET Framework], design guidelines
- type design guidelines, interfaces
- class library design guidelines [.NET Framework], interfaces
ms.assetid: a016bd18-6710-4358-9438-9f190a295392
author: KrzysztofCwalina
ms.openlocfilehash: 1f982aa37f92b7270725574d949989ca120297d5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62026365"
---
# <a name="interface-design"></a>Conception d'interfaces
Bien que la plupart des API sont mieux modélisées au moyen des classes et structs, il existe des cas dans lequel les interfaces sont plus appropriées ou sont la seule option.  
  
 Le CLR ne prend pas en charge l’héritage multiple (par exemple, les classes CLR ne peut pas hériter plusieurs classes de base), mais il n’autorise pas les types d’implémenter une ou plusieurs interfaces en plus de l’héritage d’une classe de base. Par conséquent, les interfaces sont souvent utilisées pour obtenir l’effet de l’héritage multiple. Par exemple, <xref:System.IDisposable> est une interface qui permet aux types prendre en charge disposability indépendant de toute autre hiérarchie d’héritage dans lequel ils souhaitent participer.  
  
 L’autre situation en les définissant une interface est appropriée est dans la création d’une interface commune pouvant être pris en charge par plusieurs types, y compris certains types de valeur. Types valeur ne peut pas hériter de types autres que <xref:System.ValueType>, mais ils peuvent implémenter des interfaces, par conséquent, à l’aide d’une interface est la seule option afin de fournir un type de base commun.  
  
 **✓ DO** définir une interface si vous avez besoin de certaines API courantes pour être pris en charge par un ensemble de types qui inclut les types de valeur.  
  
 **✓ CONSIDER** définissant une interface si vous avez besoin prendre en charge ses fonctionnalités sur les types qui héritent déjà d’un autre type.  
  
 **X AVOID** à l’aide des interfaces de marqueur (interfaces sans membres).  
  
 Si vous avez besoin marquer une classe comme ayant une caractéristique spécifique (marqueur), utilisez en général, un attribut personnalisé plutôt que d’une interface.  
  
 **✓ DO** fournir au moins un type qui est une implémentation d’une interface.  
  
 Ceci permet de valider la conception de l’interface. Par exemple, <xref:System.Collections.Generic.List%601> est une implémentation de la <xref:System.Collections.Generic.IList%601> interface.  
  
 **✓ DO** fournissent au moins une API qui consomme chaque interface que vous définissez (une méthode qui prend l’interface comme paramètre ou une propriété de type interface).  
  
 Ceci permet de valider la conception de l’interface. Par exemple, <xref:System.Collections.Generic.List%601.Sort%2A?displayProperty=nameWithType> consomme la <xref:System.Collections.Generic.IComparer%601?displayProperty=nameWithType> interface.  
  
 **X DO NOT** ajouter des membres à une interface qui existait précédemment.  
  
 Cela compromettrait les implémentations de l’interface. Vous devez créer une nouvelle interface afin d’éviter les problèmes de versioning.  
  
 À l’exception des situations décrites dans ces instructions, vous devez, en général, choisir les classes plutôt que des interfaces dans la conception de bibliothèques réutilisables de code managé.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
