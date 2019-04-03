---
title: Vue d'ensemble des littéraux XML (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- XML literals [Visual Basic], about XML literals
- declaring XML literals [Visual Basic]
- LINQ to XML [Visual Basic], XML literals
- literals [Visual Basic], XML
ms.assetid: 37987c15-4ab8-471b-bd45-399816bfb57f
ms.openlocfilehash: a7b70669131ae35135088418e4b33b3ae289d322
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58839884"
---
# <a name="xml-literals-overview-visual-basic"></a>Vue d'ensemble des littéraux XML (Visual Basic)
Un *littéral XML* vous permet d’incorporer du code XML directement dans votre code Visual Basic. La syntaxe des littéraux XML représente [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objets et il est similaire à la syntaxe XML 1.0. Cela rend plus facile de créer par programme des documents et éléments XML, car votre code possède la même structure que le XML final.  
  
 Visual Basic compile les littéraux XML en [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objets. [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] fournit un modèle d’objet simple pour la création et manipulation de XML et ce modèle s’intègre parfaitement aux [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)]. Pour plus d'informations, consultez <xref:System.Xml.Linq.XElement>.  
  
 Vous pouvez incorporer une expression Visual Basic dans un littéral XML. Au moment de l’exécution, votre application crée un [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objet pour chaque littéral, en intégrant les valeurs des expressions incorporées. Cela vous permet de spécifier le contenu dynamique à l’intérieur d’un littéral XML. Pour plus d’informations, consultez [Expressions incorporées en XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).  
  
 Pour plus d’informations sur les différences entre la syntaxe des littéraux XML et la syntaxe XML 1.0, consultez [littéraux XML et XML 1.0 Specification](../../../../visual-basic/programming-guide/language-features/xml/xml-literals-and-the-xml-1-0-specification.md).  
  
## <a name="simple-literals"></a>Littéraux simples  
 Vous pouvez créer un [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objet dans votre code Visual Basic en tapant ou collant dans un fichier XML valide. Un littéral d’élément XML retourne un <xref:System.Xml.Linq.XElement> objet. Pour plus d’informations, consultez [XML élément littéral](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md) et [littéraux XML et XML 1.0 Specification](../../../../visual-basic/programming-guide/language-features/xml/xml-literals-and-the-xml-1-0-specification.md). L’exemple suivant crée un élément XML qui a plusieurs éléments enfants.  
  
 [!code-vb[VbXMLSamples#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples2.vb#5)]  
  
 Vous pouvez créer un document XML en démarrant un littéral XML avec `<?xml version="1.0"?>`, comme illustré dans l’exemple suivant. Un littéral de document XML retourne un <xref:System.Xml.Linq.XDocument> objet. Pour plus d’informations, consultez [littéral de Document XML](../../../../visual-basic/language-reference/xml-literals/xml-document-literal.md).  
  
 [!code-vb[VbXMLSamples#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples2.vb#6)]  
  
> [!NOTE]
>  La syntaxe des littéraux XML en Visual Basic n’est pas identique à la syntaxe dans la spécification XML 1.0. Pour plus d’informations, consultez [littéraux XML et XML 1.0 Specification](../../../../visual-basic/programming-guide/language-features/xml/xml-literals-and-the-xml-1-0-specification.md).  
  
## <a name="line-continuation"></a>Continuation de ligne  
 Un littéral XML peut couvrir plusieurs lignes sans utiliser de caractères de continuation de ligne (la séquence espace-trait de soulignement-entrée). Cela facilite la comparaison des littéraux XML dans le code avec des documents XML.  
  
 Le compilateur traite les caractères de continuation de ligne dans le cadre d’un littéral XML. Par conséquent, vous devez utiliser la séquence espace-trait de soulignement-entrée uniquement lorsqu’elle appartient à la [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objet.  
  
 Toutefois, vous avez besoin des caractères de continuation de ligne si vous avez une expression multiligne dans une expression incorporée. Pour plus d’informations, consultez [Expressions incorporées en XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).  
  
## <a name="embedding-queries-in-xml-literals"></a>Incorporation de requêtes dans les littéraux XML  
 Vous pouvez utiliser une requête dans une expression incorporée. Lorsque vous effectuez cette opération, les éléments retournés par la requête sont ajoutés à l’élément XML. Cela vous permet d’ajouter du contenu dynamique, tel que le résultat de requête d’un utilisateur, à un littéral XML.  
  
 Par exemple, le code suivant utilise une requête incorporée pour créer des éléments XML à partir des membres de la `phoneNumbers2` de tableau, puis ajoutez ces éléments en tant qu’enfants de `contact2`.  
  
 [!code-vb[VbXMLSamples#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples2.vb#7)]  
  
## <a name="how-the-compiler-creates-objects-from-xml-literals"></a>Comment le compilateur crée des objets à partir des littéraux XML  
 Le compilateur Visual Basic traduit les littéraux XML en appels à l’équivalent [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] constructeurs pour créer le [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objet. Par exemple, le compilateur Visual Basic convertit l’exemple de code suivant dans un appel à la <xref:System.Xml.Linq.XProcessingInstruction> appels de constructeur pour l’instruction de version XML, à la <xref:System.Xml.Linq.XElement> constructeur pour le `<contact>`, `<name>`, et `<phone>` éléments et des appels à la <xref:System.Xml.Linq.XAttribute> constructeur pour le `type` attribut. En particulier, étant donné les attributs dans l’exemple suivant, le compilateur Visual Basic appelle le <xref:System.Xml.Linq.XAttribute.%23ctor%28System.Xml.Linq.XName%2CSystem.Object%29> constructeur à deux reprises. La première passe la valeur `type` pour le `name` et la valeur `home` pour le `value` paramètre. La deuxième passe également la valeur `type` pour le `name` paramètre, mais la valeur `work` pour le `value` paramètre.  
  
 [!code-vb[VbXMLSamples#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples2.vb#6)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Xml.Linq.XElement>
- [Création de code XML dans Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [Expressions incorporées en XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)
- [Littéral de document XML](../../../../visual-basic/language-reference/xml-literals/xml-document-literal.md)
- [Littéral d’élément XML](../../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [Littéraux XML](../../../../visual-basic/language-reference/xml-literals/index.md)
