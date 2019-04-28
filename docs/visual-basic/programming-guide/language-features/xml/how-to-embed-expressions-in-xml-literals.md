---
title: 'Procédure : Incorporer des Expressions dans des littéraux XML (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- embedded expressions [Visual Basic]
- XML literals [Visual Basic], embedded expressions
ms.assetid: 75016fad-0141-42de-8564-5051be29487e
ms.openlocfilehash: 31e79a8787978ffab2e35cd2827b80a8f1ed843e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61861359"
---
# <a name="how-to-embed-expressions-in-xml-literals-visual-basic"></a><span data-ttu-id="4432e-102">Procédure : Incorporer des Expressions dans des littéraux XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4432e-102">How to: Embed Expressions in XML Literals (Visual Basic)</span></span>
<span data-ttu-id="4432e-103">Vous pouvez combiner des littéraux XML avec des expressions incorporées pour créer un document XML, un fragment ou un élément qui contient le contenu créé au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4432e-103">You can combine XML literals with embedded expressions to create an XML document, fragment, or element that contains content created at run time.</span></span> <span data-ttu-id="4432e-104">Les exemples suivants montrent comment utiliser des expressions incorporées pour remplir le contenu de l’élément, des attributs et des noms d’élément en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4432e-104">The following examples demonstrate how to use embedded expressions to populate element content, attributes, and element names at run time.</span></span>  
  
 <span data-ttu-id="4432e-105">La syntaxe pour une expression incorporée est `<%=` `exp` `%>`, qui est la même syntaxe que [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] utilise.</span><span class="sxs-lookup"><span data-stu-id="4432e-105">The syntax for an embedded expression is `<%=` `exp` `%>`, which is the same syntax that [!INCLUDE[vstecasp](~/includes/vstecasp-md.md)] uses.</span></span> <span data-ttu-id="4432e-106">Pour plus d’informations, consultez [Expressions incorporées en XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).</span><span class="sxs-lookup"><span data-stu-id="4432e-106">For more information, see [Embedded Expressions in XML](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).</span></span>  
  
 <span data-ttu-id="4432e-107">Vous pouvez également utiliser le [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] API pour créer [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objets.</span><span class="sxs-lookup"><span data-stu-id="4432e-107">You can also use the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] APIs to create [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objects.</span></span> <span data-ttu-id="4432e-108">Pour plus d'informations, consultez <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="4432e-108">For more information, see <xref:System.Xml.Linq.XElement>.</span></span>  
  
## <a name="procedures"></a><span data-ttu-id="4432e-109">Procédures</span><span class="sxs-lookup"><span data-stu-id="4432e-109">Procedures</span></span>  
  
#### <a name="to-insert-text-as-element-content"></a><span data-ttu-id="4432e-110">Pour insérer du texte en tant que contenu de l’élément</span><span class="sxs-lookup"><span data-stu-id="4432e-110">To insert text as element content</span></span>  
  
- <span data-ttu-id="4432e-111">L’exemple suivant montre comment insérer le texte qui est contenu dans le `contactName` variable entre les éléments de nom d’ouverture et de fermeture.</span><span class="sxs-lookup"><span data-stu-id="4432e-111">The following example shows how to insert the text that is contained in the `contactName` variable between the opening and closing name elements.</span></span>  
  
     [!code-vb[VbXMLSamples#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples14.vb#39)]  
  
     <span data-ttu-id="4432e-112">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="4432e-112">This example produces the following output:</span></span>  
  
    ```xml  
    <contact>  
      <name>Patrick Hines</name>  
    </contact>  
    ```  
  
#### <a name="to-insert-text-as-an-attribute-value"></a><span data-ttu-id="4432e-113">Pour insérer du texte comme valeur d’attribut</span><span class="sxs-lookup"><span data-stu-id="4432e-113">To insert text as an attribute value</span></span>  
  
- <span data-ttu-id="4432e-114">L’exemple suivant montre comment insérer le texte qui est contenu dans le `phoneType` variable comme valeur de la `type` attribut.</span><span class="sxs-lookup"><span data-stu-id="4432e-114">The following example shows how to insert the text that is contained in the `phoneType` variable as the value of the `type` attribute.</span></span>  
  
     [!code-vb[VbXMLSamples#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples14.vb#40)]  
  
     <span data-ttu-id="4432e-115">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="4432e-115">This example produces the following output:</span></span>  
  
    ```xml  
    <contact>  
      <phone type="home">206-555-0144</phone>  
    </contact>  
    ```  
  
#### <a name="to-insert-text-for-an-element-name"></a><span data-ttu-id="4432e-116">Pour insérer du texte pour un nom d’élément</span><span class="sxs-lookup"><span data-stu-id="4432e-116">To insert text for an element name</span></span>  
  
- <span data-ttu-id="4432e-117">L’exemple suivant montre comment insérer le texte qui est contenu dans le `elementName` variable en tant que le nom d’un élément.</span><span class="sxs-lookup"><span data-stu-id="4432e-117">The following example shows how to insert the text that is contained in the `elementName` variable as the name of an element.</span></span>  
  
     <span data-ttu-id="4432e-118">Lorsque vous créez des éléments à l’aide de cette technique, vous devez les fermer avec la \</ > balise.</span><span class="sxs-lookup"><span data-stu-id="4432e-118">When creating elements by using this technique, you must close them with the \</> tag.</span></span>  
  
     [!code-vb[VbXMLSamples#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples14.vb#41)]  
  
     <span data-ttu-id="4432e-119">Cet exemple génère la sortie suivante :</span><span class="sxs-lookup"><span data-stu-id="4432e-119">This example produces the following output:</span></span>  
  
    ```xml  
    <contact>  
      <name>Patrick Hines</name>  
    </contact>  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="4432e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4432e-120">See also</span></span>

- [<span data-ttu-id="4432e-121">Guide pratique pour Créer des littéraux XML</span><span class="sxs-lookup"><span data-stu-id="4432e-121">How to: Create XML Literals</span></span>](../../../../visual-basic/programming-guide/language-features/xml/how-to-create-xml-literals.md)
- [<span data-ttu-id="4432e-122">Expressions incorporées en XML</span><span class="sxs-lookup"><span data-stu-id="4432e-122">Embedded Expressions in XML</span></span>](../../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)
- [<span data-ttu-id="4432e-123">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4432e-123">Creating XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [<span data-ttu-id="4432e-124">XML</span><span class="sxs-lookup"><span data-stu-id="4432e-124">XML</span></span>](../../../../visual-basic/programming-guide/language-features/xml/index.md)
