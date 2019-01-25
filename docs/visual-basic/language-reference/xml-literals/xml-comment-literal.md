---
title: Littéraux de commentaires XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralComment
helpviewer_keywords:
- comment literal [Visual Basic]
- XML comments, adding [Visual Basic]
- XML comment literal [Visual Basic]
- XML literals [Visual Basic], comment
ms.assetid: 634c1cee-5e01-48d0-88d7-2dd55e4a9e52
ms.openlocfilehash: 96a7281cde546c3077cf15c625c6e09d2d0ee46f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624676"
---
# <a name="xml-comment-literal-visual-basic"></a>Littéraux de commentaires XML (Visual Basic)
Littéral représentant un <xref:System.Xml.Linq.XComment> objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<!-- content -->  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`<!--`|Obligatoire. Indique le début du commentaire XML.|  
|`content`|Obligatoire. Texte à afficher dans le commentaire XML. Ne peut pas contenir une série de deux traits d’union (-) ou se terminer par un trait d’union adjacent à la balise de fermeture.|  
|`-->`|Obligatoire. Indique la fin du commentaire XML.|  
  
## <a name="return-value"></a>Valeur de retour  
 Objet <xref:System.Xml.Linq.XComment>.  
  
## <a name="remarks"></a>Notes  
 Littéraux de commentaire XML ne contiennent pas de contenu de document ; ils contiennent des informations sur le document. La section de commentaire XML se termine par la séquence «--> ». Cela implique les points suivants :  
  
-   Vous ne pouvez pas utiliser une expression incorporée dans un littéral de commentaire XML, car les délimiteurs d’expression sont le contenu du commentaire XML valide.  
  
-   Sections de commentaire XML ne peut pas être imbriquées, étant donné que `content` ne peut pas contenir la valeur de «--> ».  
  
 Vous pouvez assigner un littéral de commentaire XML à une variable, ou vous pouvez l’inclure dans un littéral d’élément XML.  
  
> [!NOTE]
>  Un littéral XML peut couvrir plusieurs lignes sans utiliser de caractères de continuation de ligne. Cette fonctionnalité vous permet de copier le contenu d’un document XML et la coller directement dans un programme Visual Basic.  
  
 Le compilateur Visual Basic convertit le littéral de commentaire XML en un appel à la <xref:System.Xml.Linq.XComment.%23ctor%2A> constructeur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un commentaire XML qui contient le texte « Il s’agit d’un commentaire ».  
  
 [!code-vb[VbXMLSamples#9](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-comment-literal_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Xml.Linq.XComment>
- [Littéral d’élément XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)
- [Création de code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
