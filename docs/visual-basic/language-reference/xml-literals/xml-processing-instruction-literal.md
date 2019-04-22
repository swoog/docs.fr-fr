---
title: Littéral d'instruction de traitement XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralProcessingInstruction
helpviewer_keywords:
- XML literals [Visual Basic], processing instruction
- XML processing instruction literal [Visual Basic]
- processing instruction literal [Visual Basic]
ms.assetid: cef4f7f8-0011-4f64-8602-795077ad4f15
ms.openlocfilehash: 3fbb16a4d47801b671d37566573215d3a57afff1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58820150"
---
# <a name="xml-processing-instruction-literal-visual-basic"></a><span data-ttu-id="8bd33-102">Littéral d'instruction de traitement XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8bd33-102">XML Processing Instruction Literal (Visual Basic)</span></span>
<span data-ttu-id="8bd33-103">Littéral représentant un <xref:System.Xml.Linq.XProcessingInstruction> objet.</span><span class="sxs-lookup"><span data-stu-id="8bd33-103">A literal representing an <xref:System.Xml.Linq.XProcessingInstruction> object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8bd33-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8bd33-104">Syntax</span></span>  
  
```xml  
<?piName [ = piData ] ?>  
```  
  
## <a name="parts"></a><span data-ttu-id="8bd33-105">Composants</span><span class="sxs-lookup"><span data-stu-id="8bd33-105">Parts</span></span>  
 `<?`  
 <span data-ttu-id="8bd33-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8bd33-106">Required.</span></span> <span data-ttu-id="8bd33-107">Indique le début de l’instruction de traitement XML littéral.</span><span class="sxs-lookup"><span data-stu-id="8bd33-107">Denotes the start of the XML processing instruction literal.</span></span>  
  
 `piName`  
 <span data-ttu-id="8bd33-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8bd33-108">Required.</span></span> <span data-ttu-id="8bd33-109">Nom indiquant l’application les cibles d’instruction de traitement.</span><span class="sxs-lookup"><span data-stu-id="8bd33-109">Name indicating which application the processing instruction targets.</span></span> <span data-ttu-id="8bd33-110">Ne peut pas commencer par « xml » ou « XML ».</span><span class="sxs-lookup"><span data-stu-id="8bd33-110">Cannot begin with "xml" or "XML".</span></span>  
  
 `piData`  
 <span data-ttu-id="8bd33-111">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="8bd33-111">Optional.</span></span> <span data-ttu-id="8bd33-112">Chaîne indiquant la façon dont l’application ciblée par `piName` doit traiter le document XML.</span><span class="sxs-lookup"><span data-stu-id="8bd33-112">String indicating how the application targeted by `piName` should process the XML document.</span></span>  
  
 `?>`  
 <span data-ttu-id="8bd33-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8bd33-113">Required.</span></span> <span data-ttu-id="8bd33-114">Indique la fin de l’instruction de traitement.</span><span class="sxs-lookup"><span data-stu-id="8bd33-114">Denotes the end of the processing instruction.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8bd33-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8bd33-115">Return Value</span></span>  
 <span data-ttu-id="8bd33-116">Objet <xref:System.Xml.Linq.XProcessingInstruction>.</span><span class="sxs-lookup"><span data-stu-id="8bd33-116">An <xref:System.Xml.Linq.XProcessingInstruction> object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8bd33-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8bd33-117">Remarks</span></span>  
 <span data-ttu-id="8bd33-118">Littéraux d’instruction de traitement XML indiquent la façon dont les applications doivent traiter un document XML.</span><span class="sxs-lookup"><span data-stu-id="8bd33-118">XML processing instruction literals indicate how applications should process an XML document.</span></span> <span data-ttu-id="8bd33-119">Lorsqu’une application charge un document XML, l’application peut vérifier les instructions de traitement XML pour déterminer comment traiter le document.</span><span class="sxs-lookup"><span data-stu-id="8bd33-119">When an application loads an XML document, the application can check the XML processing instructions to determine how to process the document.</span></span> <span data-ttu-id="8bd33-120">L’application interprète la signification de `piName` et `piData`.</span><span class="sxs-lookup"><span data-stu-id="8bd33-120">The application interprets the meaning of `piName` and `piData`.</span></span>  
  
 <span data-ttu-id="8bd33-121">Le littéral de document XML utilise la syntaxe qui est similaire à celle de l’instruction de traitement XML.</span><span class="sxs-lookup"><span data-stu-id="8bd33-121">The XML document literal uses syntax that is similar to that of the XML processing instruction.</span></span> <span data-ttu-id="8bd33-122">Pour plus d’informations, consultez [littéral de Document XML](../../../visual-basic/language-reference/xml-literals/xml-document-literal.md).</span><span class="sxs-lookup"><span data-stu-id="8bd33-122">For more information, see [XML Document Literal](../../../visual-basic/language-reference/xml-literals/xml-document-literal.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8bd33-123">Le `piName` élément ne peut pas commencer par les chaînes « xml » ou « XML », car la spécification XML 1.0 réserve ces identificateurs.</span><span class="sxs-lookup"><span data-stu-id="8bd33-123">The `piName` element cannot begin with the strings "xml" or "XML", because the XML 1.0 specification reserves those identifiers.</span></span>  
  
 <span data-ttu-id="8bd33-124">Vous pouvez assigner un littéral d’instruction de traitement XML à une variable ou l’inclure dans un littéral de document XML.</span><span class="sxs-lookup"><span data-stu-id="8bd33-124">You can assign an XML processing instruction literal to a variable or include it in an XML document literal.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8bd33-125">Un littéral XML peut couvrir plusieurs lignes sans avoir besoin de caractères de continuation de ligne.</span><span class="sxs-lookup"><span data-stu-id="8bd33-125">An XML literal can span multiple lines without needing line continuation characters.</span></span> <span data-ttu-id="8bd33-126">Cela vous permet de copier le contenu d’un document XML et la coller directement dans un programme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8bd33-126">This enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>  
  
 <span data-ttu-id="8bd33-127">Le compilateur Visual Basic convertit le littéral d’instruction de traitement XML en un appel à la <xref:System.Xml.Linq.XProcessingInstruction.%23ctor%2A> constructeur.</span><span class="sxs-lookup"><span data-stu-id="8bd33-127">The Visual Basic compiler converts the XML processing instruction literal to a call to the <xref:System.Xml.Linq.XProcessingInstruction.%23ctor%2A> constructor.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8bd33-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="8bd33-128">Example</span></span>  
 <span data-ttu-id="8bd33-129">L’exemple suivant crée une instruction de traitement identifiant une feuille de style pour un document XML.</span><span class="sxs-lookup"><span data-stu-id="8bd33-129">The following example creates a processing instruction identifying a style-sheet for an XML document.</span></span>  
  
 [!code-vb[VbXMLSamples#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples13.vb#28)]  
  
## <a name="see-also"></a><span data-ttu-id="8bd33-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8bd33-130">See also</span></span>

- <xref:System.Xml.Linq.XProcessingInstruction>
- [<span data-ttu-id="8bd33-131">Littéral de document XML</span><span class="sxs-lookup"><span data-stu-id="8bd33-131">XML Document Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-document-literal.md)
- [<span data-ttu-id="8bd33-132">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="8bd33-132">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)
- [<span data-ttu-id="8bd33-133">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="8bd33-133">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
