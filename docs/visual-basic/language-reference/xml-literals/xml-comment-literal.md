---
title: Littéraux de commentaires XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.XmlLiteralComment
helpviewer_keywords:
- comment literal [Visual Basic]
- XML comments, adding [Visual Basic]
- XML comment literal [Visual Basic]
- XML literals [Visual Basic], comment
ms.assetid: 634c1cee-5e01-48d0-88d7-2dd55e4a9e52
ms.openlocfilehash: 1f8526c4b67b7d975b11f6ef5dada2b45bb6b1df
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56964178"
---
# <a name="xml-comment-literal-visual-basic"></a><span data-ttu-id="a4197-102">Littéraux de commentaires XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a4197-102">XML Comment Literal (Visual Basic)</span></span>
<span data-ttu-id="a4197-103">Littéral représentant un <xref:System.Xml.Linq.XComment> objet.</span><span class="sxs-lookup"><span data-stu-id="a4197-103">A literal representing an <xref:System.Xml.Linq.XComment> object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4197-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4197-104">Syntax</span></span>  
  
```xml  
<!-- content -->  
```  
  
## <a name="parts"></a><span data-ttu-id="a4197-105">Composants</span><span class="sxs-lookup"><span data-stu-id="a4197-105">Parts</span></span>  
  
|<span data-ttu-id="a4197-106">Terme</span><span class="sxs-lookup"><span data-stu-id="a4197-106">Term</span></span>|<span data-ttu-id="a4197-107">Définition</span><span class="sxs-lookup"><span data-stu-id="a4197-107">Definition</span></span>|  
|---|---|  
|`<!--`|<span data-ttu-id="a4197-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4197-108">Required.</span></span> <span data-ttu-id="a4197-109">Indique le début du commentaire XML.</span><span class="sxs-lookup"><span data-stu-id="a4197-109">Denotes the start of the XML comment.</span></span>|  
|`content`|<span data-ttu-id="a4197-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4197-110">Required.</span></span> <span data-ttu-id="a4197-111">Texte à afficher dans le commentaire XML.</span><span class="sxs-lookup"><span data-stu-id="a4197-111">Text to appear in the XML comment.</span></span> <span data-ttu-id="a4197-112">Ne peut pas contenir une série de deux traits d’union (-) ou se terminer par un trait d’union adjacent à la balise de fermeture.</span><span class="sxs-lookup"><span data-stu-id="a4197-112">Cannot contain a series of two hyphens (--) or end with a hyphen adjacent to the closing tag.</span></span>|  
|`-->`|<span data-ttu-id="a4197-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4197-113">Required.</span></span> <span data-ttu-id="a4197-114">Indique la fin du commentaire XML.</span><span class="sxs-lookup"><span data-stu-id="a4197-114">Denotes the end of the XML comment.</span></span>|  
  
## <a name="return-value"></a><span data-ttu-id="a4197-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a4197-115">Return Value</span></span>  
 <span data-ttu-id="a4197-116">Objet <xref:System.Xml.Linq.XComment>.</span><span class="sxs-lookup"><span data-stu-id="a4197-116">An <xref:System.Xml.Linq.XComment> object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a4197-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a4197-117">Remarks</span></span>  
 <span data-ttu-id="a4197-118">Littéraux de commentaire XML ne contiennent pas de contenu de document ; ils contiennent des informations sur le document.</span><span class="sxs-lookup"><span data-stu-id="a4197-118">XML comment literals do not contain document content; they contain information about the document.</span></span> <span data-ttu-id="a4197-119">La section de commentaire XML se termine par la séquence «--> ».</span><span class="sxs-lookup"><span data-stu-id="a4197-119">The XML comment section ends with the sequence "-->".</span></span> <span data-ttu-id="a4197-120">Cela implique les points suivants :</span><span class="sxs-lookup"><span data-stu-id="a4197-120">This implies the following points:</span></span>  
  
-   <span data-ttu-id="a4197-121">Vous ne pouvez pas utiliser une expression incorporée dans un littéral de commentaire XML, car les délimiteurs d’expression sont le contenu du commentaire XML valide.</span><span class="sxs-lookup"><span data-stu-id="a4197-121">You cannot use an embedded expression in an XML comment literal because the embedded expression delimiters are valid XML comment content.</span></span>  
  
-   <span data-ttu-id="a4197-122">Sections de commentaire XML ne peut pas être imbriquées, étant donné que `content` ne peut pas contenir la valeur de «--> ».</span><span class="sxs-lookup"><span data-stu-id="a4197-122">XML comment sections cannot be nested, because `content` cannot contain the value "-->".</span></span>  
  
 <span data-ttu-id="a4197-123">Vous pouvez assigner un littéral de commentaire XML à une variable, ou vous pouvez l’inclure dans un littéral d’élément XML.</span><span class="sxs-lookup"><span data-stu-id="a4197-123">You can assign an XML comment literal to a variable, or you can include it in an XML element literal.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a4197-124">Un littéral XML peut couvrir plusieurs lignes sans utiliser de caractères de continuation de ligne.</span><span class="sxs-lookup"><span data-stu-id="a4197-124">An XML literal can span multiple lines without using line continuation characters.</span></span> <span data-ttu-id="a4197-125">Cette fonctionnalité vous permet de copier le contenu d’un document XML et la coller directement dans un programme Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a4197-125">This feature enables you to copy content from an XML document and paste it directly into a Visual Basic program.</span></span>  
  
 <span data-ttu-id="a4197-126">Le compilateur Visual Basic convertit le littéral de commentaire XML en un appel à la <xref:System.Xml.Linq.XComment.%23ctor%2A> constructeur.</span><span class="sxs-lookup"><span data-stu-id="a4197-126">The Visual Basic compiler converts the XML comment literal to a call to the <xref:System.Xml.Linq.XComment.%23ctor%2A> constructor.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a4197-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="a4197-127">Example</span></span>  
 <span data-ttu-id="a4197-128">L’exemple suivant crée un commentaire XML qui contient le texte « Il s’agit d’un commentaire ».</span><span class="sxs-lookup"><span data-stu-id="a4197-128">The following example creates an XML comment that contains the text "This is a comment".</span></span>  
  
 [!code-vb[VbXMLSamples#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples4.vb#9)]  
  
## <a name="see-also"></a><span data-ttu-id="a4197-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4197-129">See also</span></span>
- <xref:System.Xml.Linq.XComment>
- [<span data-ttu-id="a4197-130">Littéral d’élément XML</span><span class="sxs-lookup"><span data-stu-id="a4197-130">XML Element Literal</span></span>](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [<span data-ttu-id="a4197-131">Littéraux XML</span><span class="sxs-lookup"><span data-stu-id="a4197-131">XML Literals</span></span>](../../../visual-basic/language-reference/xml-literals/index.md)
- [<span data-ttu-id="a4197-132">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a4197-132">Creating XML in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
