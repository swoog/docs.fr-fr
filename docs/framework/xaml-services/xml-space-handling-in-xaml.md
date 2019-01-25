---
title: Gestion de xml:space en XAML
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [XAML Services], xml:space attribute
- XAML [XAML Services], white-space processing
- xml:space attribute [XAML Services]
- white-space processing [XAML Services]
ms.assetid: 5e1814f0-5b30-43d5-8c88-dede335a89d7
ms.openlocfilehash: a7c3775f2e49a80eabc61f24d086a94fcadfd574
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54617575"
---
# <a name="xmlspace-handling-in-xaml"></a>Gestion de xml:space en XAML
Le `xml:space` attribut est un attribut XML qui déclare le comportement de traitement des espaces blancs significatifs dans un élément objet. Ce comportement s’applique pour tout le contenu (texte interne) contenu dans l’élément où `xml:space` est déclaré et s’étend également aux éléments enfants.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xaml  
<object xml:space="preserve" />  
```  
  
 \- ou -  
  
```xaml  
<object xml:space="default" />  
```  
  
## <a name="remarks"></a>Notes  
 La définition de la `xml:space` attribut dans XAML, y compris ses deux valeurs possibles est dérivée de `xml:space` , défini comme un « attribut spécial » par les spécifications W3C pour XML.  
  
 La valeur par défaut de la `xml:space` attribut est la valeur littérale `"default"`. Pour la valeur `"default"`, ou si `xml:space` n’est pas indiqué, le comportement d’analyse d’espace blanc significatif est la gestion par défaut, comme défini dans la rubrique [blancs en XAML traitement](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).  
  
 Pour conserver les espaces blancs dans le contenu d’élément objet, spécifiez `xml:space="preserve"` sur cet élément objet.  
  
 Dans la plupart des interprétations le `xml:space` effets et la valeur de l’attribut sont limitées aux éléments enfants.  
  
 Pour obtenir une description complète de l’espace blanc-traitement dans XAML, consultez [blancs en XAML traitement](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md).  
  
## <a name="see-also"></a>Voir aussi
- [Espace blanc dans XAML de traitement](../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md)
- [Vue d’ensemble du langage XAML (WPF)](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)
