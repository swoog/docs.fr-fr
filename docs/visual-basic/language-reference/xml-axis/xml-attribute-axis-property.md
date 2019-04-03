---
title: Propriété d'axe d'attribut XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyAttributeAxis
helpviewer_keywords:
- attribute axis property [Visual Basic]
- Visual Basic code, accessing XML
- XML attribute axis property [Visual Basic]
- XML axis [Visual Basic], attribute
- XML [Visual Basic], accessing
ms.assetid: 7a4777e1-0618-4de9-9510-fb9ace2bf4db
ms.openlocfilehash: a7a93608d14bcbec316228b59467b23e9247e043
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58828800"
---
# <a name="xml-attribute-axis-property-visual-basic"></a>Propriété d'axe d'attribut XML (Visual Basic)
Fournit l’accès à la valeur d’un attribut pour un <xref:System.Xml.Linq.XElement> objet ou vers le premier élément dans une collection de <xref:System.Xml.Linq.XElement> objets.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
      object.@attribute  
-or-  
object.@<attribute>  
```  
  
## <a name="parts"></a>Composants  
 `object`  
 Obligatoire. Un <xref:System.Xml.Linq.XElement> objet ou une collection de <xref:System.Xml.Linq.XElement> objets.  
  
 .@  
 Obligatoire. Indique le début de la propriété d’axe d’attribut.  
  
 <  
 Optionnel. Indique le début du nom de l’attribut lorsque `attribute` n’est pas un identificateur valide en Visual Basic.  
  
 `attribute`  
 Obligatoire. Nom de l’attribut d’accès, sous la forme [`prefix`:]`name`.  
  
|Élément|Description|  
|----------|-----------------|  
|`prefix`|Facultatif. Préfixe d’espace de noms XML pour l’attribut. Doit être un espace de noms XML global défini avec une instruction `Imports`.|  
|`name`|Obligatoire. Nom de l’attribut local. Consultez [nom des attributs et éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).|  
  
 \>  
 Optionnel. Indique la fin du nom de l’attribut lorsque `attribute` n’est pas un identificateur valide en Visual Basic.  
  
## <a name="return-value"></a>Valeur de retour  
 Chaîne qui contient la valeur de `attribute`. Si le nom d’attribut n’existe pas, `Nothing` est retournée.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser une propriété d’axe XML attribut pour accéder à la valeur d’un attribut par nom à partir d’un <xref:System.Xml.Linq.XElement> objet ou du premier élément dans une collection de <xref:System.Xml.Linq.XElement> objets. Vous pouvez récupérer une valeur d’attribut par nom, ou ajouter un nouvel attribut à un élément en spécifiant un nouveau nom précédé par l’identificateur @.  
  
 Lorsque vous faites référence à un attribut XML en utilisant l’identificateur @, la valeur d’attribut est retournée sous forme de chaîne et vous n’avez pas besoin de spécifier explicitement le <xref:System.Xml.Linq.XAttribute.Value%2A> propriété.  
  
 Les règles d’affectation de noms pour les attributs XML diffèrent des règles d’affectation de noms des identificateurs de Visual Basic. Pour accéder à un attribut XML qui a un nom qui n’est pas un identificateur Visual Basic valide, placez-la entre crochets pointus (\< et >).  
  
## <a name="xml-namespaces"></a>Espaces de noms XML  
 Le nom de propriété d’axe d’attribut peut utiliser uniquement des préfixes d’espace de noms XML, déclarés globalement à l’aide de la `Imports` instruction. Il ne peut pas utiliser des préfixes d'espace de noms XML déclarés localement dans des littéraux d'éléments XML. Pour plus d’informations, consultez [instruction Imports (XML Namespace)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment obtenir les valeurs des attributs XML nommés `type` à partir d’une collection d’éléments XML qui sont nommés `phone`.  
  
 [!code-vb[VbXMLSamples#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples5.vb#12)]  
  
 Ce code affiche le texte suivant :  
  
 `<phoneTypes>`  
  
 `<type>home</type>`  
  
 `<type>work</type>`  
  
 `</phoneTypes>`  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment créer des attributs pour un élément XML de façon déclarative, dans le cadre du XML et dynamiquement en ajoutant un attribut à une instance d’un <xref:System.Xml.Linq.XElement> objet. Le `type` attribut est créé de façon déclarative et la `owner` attribut est créé dynamiquement.  
  
 [!code-vb[VbXMLSamples#44](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples5.vb#44)]  
  
 Ce code affiche le texte suivant :  
  
```xml  
<phone type="home" owner="Harris, Phyllis">206-555-0144</phone>  
```  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise la syntaxe de crochets pointus pour obtenir la valeur de l’attribut XML nommé `number-type`, qui n’est pas un identificateur valide en Visual Basic.  
  
 [!code-vb[VbXMLSamples#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples5.vb#13)]  
  
 Ce code affiche le texte suivant :  
  
 `Phone type: work`  
  
## <a name="example"></a>Exemple  
 L'exemple suivant déclare `ns` en tant que préfixe d'espace de noms XML. Il utilise ensuite le préfixe de l’espace de noms pour créer un littéral XML et accéder au premier nœud enfant avec le nom qualifié «`ns:name`».  
  
 [!code-vb[VbXMLSamples#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples6.vb#14)]  
  
 Ce code affiche le texte suivant :  
  
 `Phone type: home`  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Xml.Linq.XElement>
- [Propriétés d’axe XML](../../../visual-basic/language-reference/xml-axis/index.md)
- [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)
- [Création de code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [Nom des attributs et des éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)
