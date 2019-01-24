---
title: Attribution d'un nom à des paramètres
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- parameters, names
- names [.NET Framework], parameters
ms.assetid: ca3c956e-725a-441b-b4e3-eab5d472f41c
author: KrzysztofCwalina
ms.openlocfilehash: 0e5b33839372e303b96bd6b84949f9a82da2f689
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54646618"
---
# <a name="naming-parameters"></a>Attribution d'un nom à des paramètres
Au-delà de la raison évidente de lisibilité, il est important de suivre les instructions pour les noms de paramètre, car les paramètres sont affichés dans la documentation et dans le concepteur lorsque les outils de conception visuelle fournissent Intellisense et la classe de fonctionnalités de navigation.  
  
 **✓ DO** utilisez la casse mixte dans les noms de paramètre.  
  
 **✓ DO** utiliser des noms de paramètres descriptifs.  
  
 **✓ CONSIDER** à l’aide de noms basés sur la signification du paramètre plutôt que le type de paramètre.  
  
### <a name="naming-operator-overload-parameters"></a>Paramètres de surcharge d’opérateur d’affectation de noms  
 **✓ DO** utiliser `left` et `right` opérateur binaire surchargé aux noms de paramètres s’il n’a aucune signification pour les paramètres.  
  
 **✓ DO** utiliser `value` pour unaire surcharge d’opérateur les noms de paramètres s’il n’a aucune signification pour les paramètres.  
  
 **✓ CONSIDER** des noms explicites pour l’opérateur de paramètres de surcharge si cela ajoute une valeur significative.  
  
 **X DO NOT** les noms de paramètres de surcharge des abréviations d’utilisation ou un index numérique pour l’opérateur.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)
