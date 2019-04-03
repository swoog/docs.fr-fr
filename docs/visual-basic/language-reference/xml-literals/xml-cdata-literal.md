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
ms.openlocfilehash: ee269ca5cf9635fec35165d1ea65d6a6483cadef
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58828592"
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
 Obligatoire. Contenu de texte à afficher dans la section CDATA XML.  
  
 `]]>`  
 Obligatoire. Indique la fin de la section.  
  
## <a name="return-value"></a>Valeur de retour  
 Objet <xref:System.Xml.Linq.XCData>.  
  
## <a name="remarks"></a>Notes  
 Les sections CDATA XML contiennent du texte brut qui doit être inclus, mais non analysé, avec le code XML qui le contient. Une section CDATA XML peut contenir n’importe quel texte. Cela inclut les caractères XML réservés. La section CDATA XML se termine par la séquence »]] > ». Cela implique les points suivants :  
  
-   Vous ne pouvez pas utiliser une expression incorporée dans un littéral XML CDATA, car les délimiteurs d’expression sont contenu CDATA XML valide.  
  
-   Les sections CDATA XML ne peut pas être imbriquées, étant donné que `content` ne peut pas contenir la valeur «]] > ».  
  
 Vous pouvez assigner un littéral XML CDATA à une variable ou l’inclure dans un littéral d’élément XML.  
  
> [!NOTE]
>  Un littéral XML peut couvrir plusieurs lignes, mais n’utilise pas de caractères de continuation de ligne. Cela vous permet de copier le contenu d’un document XML et la coller directement dans un programme Visual Basic.  
  
 Le compilateur Visual Basic convertit le littéral XML CDATA en un appel à la <xref:System.Xml.Linq.XCData.%23ctor%2A> constructeur.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une section CDATA qui contient le texte « peut contenir un littéral \<XML > balises ».  
  
 [!code-vb[VbXMLSamples#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples11.vb#23)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Xml.Linq.XCData>
- [Littéral d’élément XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)
- [Création de code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
