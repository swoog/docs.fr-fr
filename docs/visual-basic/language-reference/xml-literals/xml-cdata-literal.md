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
# <a name="xml-cdata-literal-visual-basic"></a><span data-ttu-id="82f2d-102">Littéral CDATA XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="82f2d-102">XML CDATA Literal (Visual Basic)</span></span>
<span data-ttu-id="82f2d-103">Littéral représentant un <xref:System.Xml.Linq.XCData> objet.</span><span class="sxs-lookup"><span data-stu-id="82f2d-103">A literal representing an <xref:System.Xml.Linq.XCData> object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82f2d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82f2d-104">Syntax</span></span>  
  
```xml  
<![CDATA[content]]>  
```  
  
## <a name="parts"></a><span data-ttu-id="82f2d-105">Composants</span><span class="sxs-lookup"><span data-stu-id="82f2d-105">Parts</span></span>  
 `<![CDATA[`  
 <span data-ttu-id="82f2d-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="82f2d-106">Required.</span></span> <span data-ttu-id="82f2d-107">Indique le début de la section CDATA XML.</span><span class="sxs-lookup"><span data-stu-id="82f2d-107">Denotes the start of the XML CDATA section.</span></span>  
  
 `content`  
 <span data-ttu-id="82f2d-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="82f2d-108">Required.</span></span> <span data-ttu-id="82f2d-109">Contenu de texte à afficher dans la section CDATA XML.</span><span class="sxs-lookup"><span data-stu-id="82f2d-109">Text content to appear in the XML CDATA section.</span></span>  
  
 `]]>`  
 <span data-ttu-id="82f2d-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="82f2d-110">Required.</span></span> <span data-ttu-id="82f2d-111">Indique la fin de la section.</span><span class="sxs-lookup"><span data-stu-id="82f2d-111">Denotes the end of the section.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="82f2d-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="82f2d-112">Return Value</span></span>  
 <span data-ttu-id="82f2d-113">Objet <xref:System.Xml.Linq.XCData>.</span><span class="sxs-lookup"><span data-stu-id="82f2d-113">An <xref:System.Xml.Linq.XCData> object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="82f2d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="82f2d-114">Remarks</span></span>  
 <span data-ttu-id="82f2d-115">Les sections CDATA XML contiennent du texte brut qui doit être inclus, mais non analysé, avec le code XML qui le contient.</span><span class="sxs-lookup"><span data-stu-id="82f2d-115">XML CDATA sections contain raw text that should be included, but not parsed, with the XML that contains it.</span></span> <span data-ttu-id="82f2d-116">Une section CDATA XML peut contenir n’importe quel texte.</span><span class="sxs-lookup"><span data-stu-id="82f2d-116">A XML CDATA section can contain any text.</span></span> <span data-ttu-id="82f2d-117">Cela inclut les caractères XML réservés.</span><span class="sxs-lookup"><span data-stu-id="82f2d-117">This includes reserved XML characters.</span></span> <span data-ttu-id="82f2d-118">La section CDATA XML se termine par la séquence »]] > ».</span><span class="sxs-lookup"><span data-stu-id="82f2d-118">The XML CDATA section ends with the sequence "]]>".</span></span> <span data-ttu-id="82f2d-119">Cela implique les points suivants :</span><span class="sxs-lookup"><span data-stu-id="82f2d-119">This implies the following points:</span></span>  
  
-   <span data-ttu-id="82f2d-120">Vous ne pouvez pas utiliser une expression incorporée dans un littéral XML CDATA, car les délimiteurs d’expression sont contenu CDATA XML valide.</span><span class="sxs-lookup"><span data-stu-id="82f2d-120">You cannot use an embedded expression in an XML CDATA literal because the embedded expression delimiters are valid XML CDATA content.</span></span>  
  
-   <span data-ttu-id="82f2d-121">Les sections CDATA XML ne peut pas être imbriquées, étant donné que `content` ne peut pas contenir la valeur «]] > ».</span><span class="sxs-lookup"><span data-stu-id="82f2d-121">XML CDATA sections cannot be nested, because `content` cannot contain the value "]]>".</span></span>  
  
 <span data-ttu-id="82f2d-122">Vous pouvez assigner un littéral XML CDATA à une variable ou l’inclure dans un littéral d’élément XML.</span><span class="sxs-lookup"><span data-stu-id="82f2d-122">You can assign an XML CDATA literal to a variable, or include it in an XML element literal.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="82f2d-123">Un littéral XML peut couvrir plusieurs lignes, mais n’utilise pas de caractères de continuation de ligne.</span><span class="sxs-lookup"><span data-stu-id="82f2d-123">An XML literal can span multiple lines but does not use line continuation characters.</span></span> <span data-ttu-id="82f2d-124">Cela vous permet de copier le contenu d’un document XML et la coller directement dans un programme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="82f2d-124">This enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>  
  
 <span data-ttu-id="82f2d-125">Le compilateur Visual Basic convertit le littéral XML CDATA en un appel à la <xref:System.Xml.Linq.XCData.%23ctor%2A> constructeur.</span><span class="sxs-lookup"><span data-stu-id="82f2d-125">The Visual Basic compiler converts the XML CDATA literal to a call to the <xref:System.Xml.Linq.XCData.%23ctor%2A> constructor.</span></span>  
  
## <a name="example"></a><span data-ttu-id="82f2d-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="82f2d-126">Example</span></span>  
 <span data-ttu-id="82f2d-127">L’exemple suivant crée une section CDATA qui contient le texte « peut contenir un littéral \<XML > balises ».</span><span class="sxs-lookup"><span data-stu-id="82f2d-127">The following example creates a CDATA section that contains the text "Can contain literal \<XML> tags".</span></span>  
  
 [!code-vb[VbXMLSamples#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples11.vb#23)]  
  
## <a name="see-also"></a><span data-ttu-id="82f2d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82f2d-128">See also</span></span>

- <xref:System.Xml.Linq.XCData>
- [<span data-ttu-id="82f2d-129">Littéral d’élément XML</span><span class="sxs-lookup"><span data-stu-id="82f2d-129">XML Element Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [<span data-ttu-id="82f2d-130">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="82f2d-130">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)
- [<span data-ttu-id="82f2d-131">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="82f2d-131">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
