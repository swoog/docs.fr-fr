---
title: 'Comment : accéder à des éléments descendants XML (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- XML descendent axis property [Visual Basic]
- XML axis [Visual Basic], descendent
- descendent axis property [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: aabfa258-4112-4e7e-bab9-403f96072ef7
ms.openlocfilehash: 6d41844b540631df96740ce56818c125cf85e928
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33648484"
---
# <a name="how-to-access-xml-descendant-elements-visual-basic"></a>Comment : accéder à des éléments descendants XML (Visual Basic)
Cet exemple montre comment utiliser une propriété d’axe descendant pour accéder à tous les éléments XML qui ont un nom spécifié et qui sont contenus sous un élément XML. En particulier, il utilise le `Value` propriété à obtenir la valeur du premier élément dans la collection qui le `name` retourne de propriété d’axe descendant. Le `name` propriété d’axe descendant Obtient tous les éléments nommés `name` qui sont contenues dans le `contacts` objet. Cet exemple utilise également la `phone` propriété d’axe descendant pour accéder à tous les descendants nommés `phone` qui sont contenues dans le `contacts` objet.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbXMLSamples#31](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-access-xml-descendant-elements_1.vb)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   une référence à l'espace de noms <xref:System.Xml.Linq>.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Xml.Linq.XContainer.Descendants%2A?displayProperty=nameWithType>  
 [Propriété d’axe descendant XML](../../../../visual-basic/language-reference/xml-axis/xml-descendant-axis-property.md)  
 [Propriété de valeur XML](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md)  
 [Accès au code XML dans Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)  
 [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)
