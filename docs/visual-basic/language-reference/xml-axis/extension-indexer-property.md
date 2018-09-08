---
title: Propriété d’indexeur d’extension (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlPropertyExtensionIndexer
helpviewer_keywords:
- Visual Basic code, accessing XML
- XML extension indexer [Visual Basic]
- extension indexer [Visual Basic]
- XML [Visual Basic], accessing
ms.assetid: a16a4b13-54be-432c-82b3-a87091464ada
ms.openlocfilehash: ab9eacc3fb3796139d8ed8382146a4a6c2b28a97
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44189499"
---
# <a name="extension-indexer-property-visual-basic"></a>Propriété d’indexeur d’extension (Visual Basic)
Fournit un accès aux différents éléments d’une collection.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
object(index)  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`object`|Obligatoire. Une collection peut être interrogée. Autrement dit, une collection qui implémente <xref:System.Collections.Generic.IEnumerable%601> ou <xref:System.Linq.IQueryable%601>.|  
|(|Obligatoire. Indique le début de la propriété d’indexeur.|  
|`index`|Obligatoire. Expression entière qui spécifie la position de base zéro d’un élément de la collection.|  
|)|Obligatoire. Indique la fin de la propriété d’indexeur.|  
  
## <a name="return-value"></a>Valeur de retour  
 L’objet à partir de l’emplacement spécifié dans la collection, ou `Nothing` si l’index est hors limites.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser la propriété d’indexeur d’extension pour accéder aux éléments individuels dans une collection. Cette propriété d’indexeur est généralement utilisée sur la sortie de propriétés d’axe XML. L’enfant XML et les propriétés d’axe descendant XML retournent des collections de <xref:System.Xml.Linq.XElement> objets ou une valeur d’attribut.  
  
 Le compilateur Visual Basic convertit les propriétés de l’indexeur extension en appels à la `ElementAtOrDefault` (méthode). Contrairement à un indexeur de tableau, le `ElementAtOrDefault` retourne de la méthode `Nothing` si l’index est hors limites. Ce comportement est utile lorsque vous ne pouvez pas facilement déterminer le nombre d’éléments dans une collection.  
  
 Cette propriété d’indexeur est semblable à une propriété d’extension pour les collections qui implémentent <xref:System.Collections.Generic.IEnumerable%601> ou <xref:System.Linq.IQueryable%601>: il est utilisé uniquement si la collection n’a pas d’un indexeur ou une propriété par défaut.  
  
 Pour accéder à la valeur du premier élément dans une collection de <xref:System.Xml.Linq.XElement> ou <xref:System.Xml.Linq.XAttribute> objets, vous pouvez utiliser le code XML `Value` propriété. Pour plus d’informations, consultez [propriété de valeur XML](../../../visual-basic/language-reference/xml-axis/xml-value-property.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment utiliser l’indexeur d’extension pour accéder au deuxième nœud enfant dans une collection de <xref:System.Xml.Linq.XElement> objets. La collection est accessible à l’aide de la propriété d’axe enfant, qui obtient tous les éléments enfants nommés `phone` dans le `contact` objet.  
  
 [!code-vb[VbXMLSamples#24](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/extension-indexer-property_1.vb)]  
  
 Ce code affiche le texte suivant :  
  
 `Second phone number: 425-555-0145`  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Xml.Linq.XElement>  
 [Propriétés d’axe XML](../../../visual-basic/language-reference/xml-axis/index.md)  
 [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)  
 [Création de code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 [Propriété de valeur XML](../../../visual-basic/language-reference/xml-axis/xml-value-property.md)
