---
title: 'Procédure : Incorporer des Expressions dans des littéraux XML (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- embedded expressions [Visual Basic]
- XML literals [Visual Basic], embedded expressions
ms.assetid: 75016fad-0141-42de-8564-5051be29487e
ms.openlocfilehash: 31e79a8787978ffab2e35cd2827b80a8f1ed843e
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58841579"
---
# <a name="how-to-embed-expressions-in-xml-literals-visual-basic"></a>Procédure : Incorporer des Expressions dans des littéraux XML (Visual Basic)
Vous pouvez combiner des littéraux XML avec des expressions incorporées pour créer un document XML, un fragment ou un élément qui contient le contenu créé au moment de l’exécution. Les exemples suivants montrent comment utiliser des expressions incorporées pour remplir le contenu de l’élément, des attributs et des noms d’élément en cours d’exécution.  
  
 La syntaxe pour une expression incorporée est `<%=` `exp` `%>`, qui est la même syntaxe que [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] utilise. Pour plus d’informations, consultez [Expressions incorporées en XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).  
  
 Vous pouvez également utiliser le [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] API pour créer [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objets. Pour plus d'informations, consultez <xref:System.Xml.Linq.XElement>.  
  
## <a name="procedures"></a>Procédures  
  
#### <a name="to-insert-text-as-element-content"></a>Pour insérer du texte en tant que contenu de l’élément  
  
-   L’exemple suivant montre comment insérer le texte qui est contenu dans le `contactName` variable entre les éléments de nom d’ouverture et de fermeture.  
  
     [!code-vb[VbXMLSamples#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples14.vb#39)]  
  
     Cet exemple génère la sortie suivante :  
  
    ```xml  
    <contact>  
      <name>Patrick Hines</name>  
    </contact>  
    ```  
  
#### <a name="to-insert-text-as-an-attribute-value"></a>Pour insérer du texte comme valeur d’attribut  
  
-   L’exemple suivant montre comment insérer le texte qui est contenu dans le `phoneType` variable comme valeur de la `type` attribut.  
  
     [!code-vb[VbXMLSamples#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples14.vb#40)]  
  
     Cet exemple génère la sortie suivante :  
  
    ```xml  
    <contact>  
      <phone type="home">206-555-0144</phone>  
    </contact>  
    ```  
  
#### <a name="to-insert-text-for-an-element-name"></a>Pour insérer du texte pour un nom d’élément  
  
-   L’exemple suivant montre comment insérer le texte qui est contenu dans le `elementName` variable en tant que le nom d’un élément.  
  
     Lorsque vous créez des éléments à l’aide de cette technique, vous devez les fermer avec la \</ > balise.  
  
     [!code-vb[VbXMLSamples#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples14.vb#41)]  
  
     Cet exemple génère la sortie suivante :  
  
    ```xml  
    <contact>  
      <name>Patrick Hines</name>  
    </contact>  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Guide pratique pour Créer des littéraux XML](../../../../visual-basic/programming-guide/language-features/xml/how-to-create-xml-literals.md)
- [Expressions incorporées en XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)
- [Création de code XML dans Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md)
