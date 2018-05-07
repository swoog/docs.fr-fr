---
title: Littéral CDATA XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralCdata
helpviewer_keywords:
- CDATA literal [Visual Basic]
- XML CDATA literal [Visual Basic]
- XML literals [Visual Basic], CDATA
ms.assetid: 9eafb6a4-dd9d-4866-85e8-0654c65abc44
ms.openlocfilehash: 999531d8146748fe491255663f0d2d17d056bcd4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="xml-cdata-literal-visual-basic"></a>Littéral CDATA XML (Visual Basic)
Littéral représentant un <xref:System.Xml.Linq.XCData> objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<![CDATA[content]]>  
```  
  
## <a name="parts"></a>Composants  
 `<![CDATA[`  
 Obligatoire. Indique le début de la section CDATA XML.  
  
 `content`  
 Obligatoire. Contenu de texte s’affichent dans la section CDATA XML.  
  
 `]]>`  
 Obligatoire. Indique la fin de la section.  
  
## <a name="return-value"></a>Valeur de retour  
 Objet <xref:System.Xml.Linq.XCData>.  
  
## <a name="remarks"></a>Notes  
 Les sections XML CDATA contiennent du texte brut qui doit être inclus, mais non analysé, avec le code XML qui le contient. Une section CDATA XML peut contenir n’importe quel texte. Cela inclut les caractères XML réservés. La section CDATA XML se termine par la séquence «]] > ». Cela implique les points suivants :  
  
-   Vous ne pouvez pas utiliser une expression incorporée dans un littéral XML CDATA, car les délimiteurs d’expression sont contenus XML CDATA valides.  
  
-   Les sections XML CDATA ne peuvent pas être imbriquées, parce que `content` ne peut pas contenir la valeur «]] > ».  
  
 Vous pouvez assigner un littéral XML CDATA à une variable ou l’inclure dans un littéral d’élément XML.  
  
> [!NOTE]
>  Un littéral XML peut couvrir plusieurs lignes, mais n’utilise pas de caractères de continuation de ligne. Cela vous permet de copier le contenu d’un document XML et le coller directement dans un programme Visual Basic.  
  
 Le compilateur Visual Basic convertit le littéral XML CDATA à un appel à la <xref:System.Xml.Linq.XCData.%23ctor%2A> constructeur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une section CDATA qui contient le texte « peut contenir des littéraux \<XML > balises ».  
  
 [!code-vb[VbXMLSamples#23](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-cdata-literal_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Xml.Linq.XCData>  
 [Littéral d’élément XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)  
 [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)  
 [Création de code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
