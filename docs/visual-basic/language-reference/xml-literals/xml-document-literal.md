---
title: Littéral de document XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralDocument
helpviewer_keywords:
- XML document literal [Visual Basic]
- XML literals [Visual Basic], document
- XML documents [Visual Basic], creating
- document literal [Visual Basic]
ms.assetid: f7bbee56-0911-41de-b907-96f20450137b
ms.openlocfilehash: 09ab9d0bf3feeea70ddbc094183406a6fd646c1c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54690512"
---
# <a name="xml-document-literal-visual-basic"></a>Littéral de document XML (Visual Basic)
Littéral représentant un <xref:System.Xml.Linq.XDocument> objet.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<?xml version="1.0" [encoding="encoding"] [standalone="standalone"] ?>  
[ piCommentList ]  
rootElement  
[ piCommentList ]  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`encoding`|Facultatif. Utilise du texte littéral qui déclare l’encodage du document.|  
|`standalone`|Facultatif. Texte littéral. Doit être « yes » ou « non ».|  
|`piCommentList`|Facultatif. Liste des instructions de traitement XML et les commentaires XML. Prend le format suivant :<br /><br /> `piComment [` `piComment` `... ]`<br /><br /> Chaque `piComment` peut prendre l’une des opérations suivantes :<br /><br /> -   [Littéral d’Instruction de traitement XML](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md).<br />-   [Littéral de commentaire XML](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md).|  
|`rootElement`|Obligatoire. Élément racine du document. Le format est une des opérations suivantes :<br /><br /> <ul><li>[Littéral d’élément XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md).</li><li>Expression sous la forme incorporée `<%=` `elementExp` `%>`. Le `elementExp` retourne une des opérations suivantes :<br /><br /> <ul><li>Objet <xref:System.Xml.Linq.XElement>.</li><li>Une collection qui contient un <xref:System.Xml.Linq.XElement> objet et un nombre quelconque de <xref:System.Xml.Linq.XProcessingInstruction> et <xref:System.Xml.Linq.XComment> objets.</li></ul></li></ul><br /> Pour plus d’informations, consultez [Expressions incorporées en XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).|  
  
## <a name="return-value"></a>Valeur de retour  
 Objet <xref:System.Xml.Linq.XDocument>.  
  
## <a name="remarks"></a>Notes  
 Un littéral de document XML est identifié par la déclaration XML au début du littéral. Bien que chaque littéral de document XML doit avoir exactement un élément XML racine, il peut avoir n’importe quel nombre d’instructions de traitement XML et les commentaires XML.  
  
 Un littéral de document XML ne peut pas apparaître dans un élément XML.  
  
> [!NOTE]
>  Un littéral XML peut couvrir plusieurs lignes sans utiliser de caractères de continuation de ligne. Cela vous permet de copier le contenu d’un document XML et la coller directement dans un programme Visual Basic.  
  
 Le compilateur Visual Basic convertit le littéral de document XML en appels à la <xref:System.Xml.Linq.XDocument.%23ctor%2A> et <xref:System.Xml.Linq.XDeclaration.%23ctor%2A> constructeurs.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée un document XML qui a une déclaration XML, une instruction de traitement, un commentaire et un élément qui contient un autre élément.  
  
 [!code-vb[VbXMLSamples#30](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-document-literal_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Xml.Linq.XElement>
- <xref:System.Xml.Linq.XProcessingInstruction>
- <xref:System.Xml.Linq.XComment>
- <xref:System.Xml.Linq.XDocument>
- [Littéral d’instruction de traitement XML](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md)
- [Littéraux de commentaires XML](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md)
- [Littéral d’élément XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)
- [Création de code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [Expressions incorporées en XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)
