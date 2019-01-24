---
title: 'Procédure : Accéder aux éléments d’enfant XML (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- XML axis [Visual Basic], child
- child axis property [Visual Basic]
- XML child axis property [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: 6689eb36-c471-469f-a82d-099ab8197b25
ms.openlocfilehash: 92ecea2c2e6e117add37b30498f5fb34adfeac6e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54626652"
---
# <a name="how-to-access-xml-child-elements-visual-basic"></a>Procédure : Accéder aux éléments d’enfant XML (Visual Basic)
Cet exemple montre comment utiliser un enfant de propriété d’axe pour accéder à tous les éléments enfants XML qui ont un nom spécifié dans un élément XML. En particulier, il utilise le <xref:System.Xml.Linq.XElement.Value%2A> propriété à obtenir la valeur du premier élément dans la collection qui le `name` retourne de propriété d’axe enfant. Le `name` propriété d’axe enfant obtient tous les éléments enfants nommés `phone` dans le `contact` objet. Cet exemple utilise également le `phone` propriété d’axe enfant pour accéder à tous les éléments enfants nommés `phone` qui sont contenus dans le `contact` objet.  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbXMLSamples#10](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-access-xml-child-elements_1.vb)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple nécessite :  
  
-   une référence à l'espace de noms <xref:System.Xml.Linq>.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Xml.Linq.XContainer.Elements%2A?displayProperty=nameWithType>
- [Propriété d’axe enfant XML](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md)
- [Propriété de valeur XML](../../../../visual-basic/language-reference/xml-axis/xml-value-property.md)
- [Accès au code XML dans Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)
- [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)
