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
ms.openlocfilehash: f58c1365e145166dfe122d455854d44526300a1e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58814625"
---
# <a name="xml-document-literal-visual-basic"></a><span data-ttu-id="5537a-102">Littéral de document XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5537a-102">XML Document Literal (Visual Basic)</span></span>
<span data-ttu-id="5537a-103">Littéral représentant un <xref:System.Xml.Linq.XDocument> objet.</span><span class="sxs-lookup"><span data-stu-id="5537a-103">A literal representing an <xref:System.Xml.Linq.XDocument> object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5537a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5537a-104">Syntax</span></span>  
  
```xml  
<?xml version="1.0" [encoding="encoding"] [standalone="standalone"] ?>  
[ piCommentList ]  
rootElement  
[ piCommentList ]  
```  
  
## <a name="parts"></a><span data-ttu-id="5537a-105">Composants</span><span class="sxs-lookup"><span data-stu-id="5537a-105">Parts</span></span>  
  
|<span data-ttu-id="5537a-106">Terme</span><span class="sxs-lookup"><span data-stu-id="5537a-106">Term</span></span>|<span data-ttu-id="5537a-107">Définition</span><span class="sxs-lookup"><span data-stu-id="5537a-107">Definition</span></span>|  
|---|---|  
|`encoding`|<span data-ttu-id="5537a-108">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="5537a-108">Optional.</span></span> <span data-ttu-id="5537a-109">Utilise du texte littéral qui déclare l’encodage du document.</span><span class="sxs-lookup"><span data-stu-id="5537a-109">Literal text declaring which encoding the document uses.</span></span>|  
|`standalone`|<span data-ttu-id="5537a-110">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="5537a-110">Optional.</span></span> <span data-ttu-id="5537a-111">Texte littéral.</span><span class="sxs-lookup"><span data-stu-id="5537a-111">Literal text.</span></span> <span data-ttu-id="5537a-112">Doit être « yes » ou « non ».</span><span class="sxs-lookup"><span data-stu-id="5537a-112">Must be "yes" or "no".</span></span>|  
|`piCommentList`|<span data-ttu-id="5537a-113">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="5537a-113">Optional.</span></span> <span data-ttu-id="5537a-114">Liste des instructions de traitement XML et les commentaires XML.</span><span class="sxs-lookup"><span data-stu-id="5537a-114">List of XML processing instructions and XML comments.</span></span> <span data-ttu-id="5537a-115">Prend le format suivant :</span><span class="sxs-lookup"><span data-stu-id="5537a-115">Takes the following format:</span></span><br /><br /> <span data-ttu-id="5537a-116">`piComment [` `piComment` `... ]`</span><span class="sxs-lookup"><span data-stu-id="5537a-116">`piComment [` `piComment` `... ]`</span></span><br /><br /> <span data-ttu-id="5537a-117">Chaque `piComment` peut prendre l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5537a-117">Each `piComment` can be one of the following:</span></span><br /><br /> <span data-ttu-id="5537a-118">-   [Littéral d’Instruction de traitement XML](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md).</span><span class="sxs-lookup"><span data-stu-id="5537a-118">-   [XML Processing Instruction Literal](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md).</span></span><br /><span data-ttu-id="5537a-119">-   [Littéral de commentaire XML](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md).</span><span class="sxs-lookup"><span data-stu-id="5537a-119">-   [XML Comment Literal](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md).</span></span>|  
|`rootElement`|<span data-ttu-id="5537a-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5537a-120">Required.</span></span> <span data-ttu-id="5537a-121">Élément racine du document.</span><span class="sxs-lookup"><span data-stu-id="5537a-121">Root element of the document.</span></span> <span data-ttu-id="5537a-122">Le format est une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5537a-122">The format is one of the following:</span></span><br /><br /> <ul><li><span data-ttu-id="5537a-123">[Littéral d’élément XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md).</span><span class="sxs-lookup"><span data-stu-id="5537a-123">[XML Element Literal](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md).</span></span></li><li><span data-ttu-id="5537a-124">Expression sous la forme incorporée `<%=` `elementExp` `%>`.</span><span class="sxs-lookup"><span data-stu-id="5537a-124">Embedded expression of the form `<%=` `elementExp` `%>`.</span></span> <span data-ttu-id="5537a-125">Le `elementExp` retourne une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5537a-125">The `elementExp` returns one of the following:</span></span><br /><br /> <ul><li><span data-ttu-id="5537a-126">Objet <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="5537a-126">An <xref:System.Xml.Linq.XElement> object.</span></span></li><li><span data-ttu-id="5537a-127">Une collection qui contient un <xref:System.Xml.Linq.XElement> objet et un nombre quelconque de <xref:System.Xml.Linq.XProcessingInstruction> et <xref:System.Xml.Linq.XComment> objets.</span><span class="sxs-lookup"><span data-stu-id="5537a-127">A collection that contains one <xref:System.Xml.Linq.XElement> object and any number of <xref:System.Xml.Linq.XProcessingInstruction> and <xref:System.Xml.Linq.XComment> objects.</span></span></li></ul></li></ul><br /> <span data-ttu-id="5537a-128">Pour plus d’informations, consultez [Expressions incorporées en XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).</span><span class="sxs-lookup"><span data-stu-id="5537a-128">For more information, see [Embedded Expressions in XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).</span></span>|  
  
## <a name="return-value"></a><span data-ttu-id="5537a-129">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5537a-129">Return Value</span></span>  
 <span data-ttu-id="5537a-130">Objet <xref:System.Xml.Linq.XDocument>.</span><span class="sxs-lookup"><span data-stu-id="5537a-130">An <xref:System.Xml.Linq.XDocument> object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5537a-131">Notes</span><span class="sxs-lookup"><span data-stu-id="5537a-131">Remarks</span></span>  
 <span data-ttu-id="5537a-132">Un littéral de document XML est identifié par la déclaration XML au début du littéral.</span><span class="sxs-lookup"><span data-stu-id="5537a-132">An XML document literal is identified by the XML declaration at the start of the literal.</span></span> <span data-ttu-id="5537a-133">Bien que chaque littéral de document XML doit avoir exactement un élément XML racine, il peut avoir n’importe quel nombre d’instructions de traitement XML et les commentaires XML.</span><span class="sxs-lookup"><span data-stu-id="5537a-133">Although each XML document literal must have exactly one root XML element, it can have any number of XML processing instructions and XML comments.</span></span>  
  
 <span data-ttu-id="5537a-134">Un littéral de document XML ne peut pas apparaître dans un élément XML.</span><span class="sxs-lookup"><span data-stu-id="5537a-134">An XML document literal cannot appear in an XML element.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5537a-135">Un littéral XML peut couvrir plusieurs lignes sans utiliser de caractères de continuation de ligne.</span><span class="sxs-lookup"><span data-stu-id="5537a-135">An XML literal can span multiple lines without using line continuation characters.</span></span> <span data-ttu-id="5537a-136">Cela vous permet de copier le contenu d’un document XML et la coller directement dans un programme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5537a-136">This enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>  
  
 <span data-ttu-id="5537a-137">Le compilateur Visual Basic convertit le littéral de document XML en appels à la <xref:System.Xml.Linq.XDocument.%23ctor%2A> et <xref:System.Xml.Linq.XDeclaration.%23ctor%2A> constructeurs.</span><span class="sxs-lookup"><span data-stu-id="5537a-137">The Visual Basic compiler converts the XML document literal into calls to the <xref:System.Xml.Linq.XDocument.%23ctor%2A> and <xref:System.Xml.Linq.XDeclaration.%23ctor%2A> constructors.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5537a-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="5537a-138">Example</span></span>  
 <span data-ttu-id="5537a-139">L’exemple suivant crée un document XML qui a une déclaration XML, une instruction de traitement, un commentaire et un élément qui contient un autre élément.</span><span class="sxs-lookup"><span data-stu-id="5537a-139">The following example creates an XML document that has an XML declaration, a processing instruction, a comment, and an element that contains another element.</span></span>  
  
 [!code-vb[VbXMLSamples#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples13.vb#30)]  
  
## <a name="see-also"></a><span data-ttu-id="5537a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5537a-140">See also</span></span>

- <xref:System.Xml.Linq.XElement>
- <xref:System.Xml.Linq.XProcessingInstruction>
- <xref:System.Xml.Linq.XComment>
- <xref:System.Xml.Linq.XDocument>
- [<span data-ttu-id="5537a-141">Littéral d’instruction de traitement XML</span><span class="sxs-lookup"><span data-stu-id="5537a-141">XML Processing Instruction Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md)
- [<span data-ttu-id="5537a-142">Littéraux de commentaires XML</span><span class="sxs-lookup"><span data-stu-id="5537a-142">XML Comment Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md)
- [<span data-ttu-id="5537a-143">Littéral d’élément XML</span><span class="sxs-lookup"><span data-stu-id="5537a-143">XML Element Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [<span data-ttu-id="5537a-144">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="5537a-144">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)
- [<span data-ttu-id="5537a-145">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5537a-145">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
- [<span data-ttu-id="5537a-146">Expressions incorporées en XML</span><span class="sxs-lookup"><span data-stu-id="5537a-146">Embedded Expressions in XML</span></span>](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)
