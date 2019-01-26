---
title: Propriété d'axe descendant XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyDescendantsAxis
helpviewer_keywords:
- Visual Basic code, accessing XML
- XML descendant axis property [Visual Basic]
- descendant axis property [Visual Baisc]
- XML axis [Visual Basic], descendant
- XML [Visual Basic], accessing
ms.assetid: a178f85b-5d54-438f-8479-40b62af6fe76
ms.openlocfilehash: 862a9177d9e10e9561da389fdbffa3e35aa3b51a
ms.sourcegitcommit: d9a0071d0fd490ae006c816f78a563b9946e269a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55065932"
---
# <a name="xml-descendant-axis-property-visual-basic"></a>Propriété d'axe descendant XML (Visual Basic)
Fournit l’accès aux descendants des éléments suivants : un <xref:System.Xml.Linq.XElement> objet, un <xref:System.Xml.Linq.XDocument> objet, une collection de <xref:System.Xml.Linq.XElement> objets, ou une collection de <xref:System.Xml.Linq.XDocument> objets.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
object...<descendant>  
```  
  
## <a name="parts"></a>Composants  
 `object`  
 Obligatoire. Un objet <xref:System.Xml.Linq.XElement>, un objet <xref:System.Xml.Linq.XDocument>, une collection d’objets <xref:System.Xml.Linq.XElement> ou une collection d’objets <xref:System.Xml.Linq.XDocument>.  
  
 ...<  
 Obligatoire. Indique le début d’une propriété d’axe descendant.  
  
 `descendant`  
 Obligatoire. Nom des nœuds descendants d’accès, sous la forme [`prefix:]name`.  
  
|Élément|Description|  
|----------|-----------------|  
|`prefix`|Facultatif. Préfixe d’espace de noms XML pour le nœud descendant. Doit être un espace de noms XML global qui est défini à l’aide un `Imports` instruction.|  
|`name`|Obligatoire. Nom local du nœud descendant. Consultez [nom des attributs et éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).|  
  
 \>  
 Obligatoire. Indique la fin d’une propriété d’axe descendant.  
  
## <a name="return-value"></a>Valeur de retour  
 Collection d'objets <xref:System.Xml.Linq.XElement>.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser une propriété d’axe descendant XML pour accéder aux nœuds descendants par nom à partir d’un <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> objet, ou à partir d’une collection de <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XDocument> objets. Utilisez le code XML `Value` propriété pour accéder à la valeur du premier nœud descendant dans la collection retournée. Pour plus d’informations, consultez [propriété de valeur XML](../../../visual-basic/language-reference/xml-axis/xml-value-property.md).  
  
 Le compilateur Visual Basic convertit des propriétés d’axes descendants en appels à la <xref:System.Xml.Linq.XContainer.Descendants%2A> (méthode).  
  
## <a name="xml-namespaces"></a>Espaces de noms XML  
 Le nom dans une propriété d’axe descendant peut utiliser uniquement les espaces de noms XML déclarés globalement avec le `Imports` instruction. Il ne peut pas utiliser les espaces de noms XML déclarés localement dans les littéraux d’élément XML. Pour plus d’informations, consultez [instruction Imports (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment accéder à la valeur du premier nœud descendant nommé `name` et les valeurs de tous les nœuds descendants nommés `phone` à partir de la `contacts` objet.  
  
 [!code-vb[VbXMLSamples#25](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-descendant-axis-property_1.vb)]  
  
 Ce code affiche le texte suivant :  
  
 `Name: Patrick Hines`  
  
 `Home Phone = 206-555-0144`  
  
## <a name="example"></a>Exemple  
 L'exemple suivant déclare `ns` en tant que préfixe d'espace de noms XML. Il utilise ensuite le préfixe de l’espace de noms pour créer un littéral XML et accéder à la valeur du premier nœud enfant avec le nom qualifié `ns:name`.  
  
 [!code-vb[VbXMLSamples#26](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-descendant-axis-property_2.vb)]  
  
 Ce code affiche le texte suivant :  
  
 `Name: Patrick Hines`  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Xml.Linq.XElement>
- [Propriétés d’axe XML](../../../visual-basic/language-reference/xml-axis/index.md)
- [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)
- [Création de code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [Nom des attributs et des éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)
