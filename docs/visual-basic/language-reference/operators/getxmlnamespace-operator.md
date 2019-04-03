---
title: Opérateur GetXmlNamespace (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.GetXmlNamespace
- GetXmlNamespace
helpviewer_keywords:
- GetXmlNamespace operator [Visual Basic]
- GetXmlNamespace keyword [Visual Basic]
ms.assetid: d0d28cfd-0755-4896-ae0b-4981aa35517c
ms.openlocfilehash: 757ca54e5ba370bf2cc48bc70499e7b43ec96ef6
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834749"
---
# <a name="getxmlnamespace-operator-visual-basic"></a>Opérateur GetXmlNamespace (Visual Basic)
Obtient le <xref:System.Xml.Linq.XNamespace> objet qui correspond au préfixe d’espace de noms XML spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
GetXmlNamespace(xmlNamespacePrefix)  
```  
  
## <a name="parts"></a>Composants  
 `xmlNamespacePrefix`  
 Facultatif. Chaîne qui identifie le préfixe d’espace de noms XML. S’il est fourni, cette chaîne doit être un identificateur XML valide. Pour plus d’informations, consultez [les attributs et les noms d’éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md). Si aucun préfixe n’est spécifié, l’espace de noms par défaut est retourné. Si aucun espace de noms par défaut n’est spécifié, l’espace de noms vide est retournée.  
  
## <a name="return-value"></a>Valeur de retour  
 Le <xref:System.Xml.Linq.XNamespace> objet qui correspond au préfixe d’espace de noms XML.  
  
## <a name="remarks"></a>Notes  
 Le `GetXmlNamespace` opérateur Obtient le <xref:System.Xml.Linq.XNamespace> objet qui correspond au préfixe d’espace de noms XML `xmlNamespacePrefix`.  
  
 Vous pouvez utiliser des préfixes d’espace de noms XML directement dans les littéraux XML et les propriétés d’axe XML. Toutefois, vous devez utiliser le `GetXmlNamespace` pour convertir un préfixe d’espace de noms à un <xref:System.Xml.Linq.XNamespace> de l’objet avant de pouvoir l’utiliser dans votre code. Vous pouvez ajouter un nom d’élément non qualifié à un <xref:System.Xml.Linq.XNamespace> objet pour lequel obtenir un complet <xref:System.Xml.Linq.XName> de l’objet, que de nombreuses [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] méthodes requièrent.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant importe `ns` comme un préfixe d’espace de noms XML. Il utilise ensuite le préfixe de l’espace de noms pour créer un littéral XML et accéder au premier nœud enfant qui a le nom qualifié `ns:phone`. Il passe alors ce nœud enfant à la `ShowName` sous-routine qui construit un nom qualifié à l’aide de la `GetXmlNamespace` opérateur. Le `ShowName` sous-routine transmet ensuite le nom qualifié à la <xref:System.Xml.Linq.XNode.Ancestors%2A> méthode pour obtenir le parent `ns:contact` nœud.  
  
 [!code-vb[VbXMLSamples#38](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/GetXmlNamespace.vb#38)]  
  
 Lorsque vous appelez `TestGetXmlNamespace.RunSample()`, il affiche un message qui contient le texte suivant :  
  
 `Name: Patrick Hines`  
  
## <a name="see-also"></a>Voir aussi

- [Imports (instruction) (espace de noms XML)](../../../visual-basic/language-reference/statements/imports-statement-xml-namespace.md)
- [Accès au code XML dans Visual Basic](../../../visual-basic/programming-guide/language-features/xml/accessing-xml.md)
