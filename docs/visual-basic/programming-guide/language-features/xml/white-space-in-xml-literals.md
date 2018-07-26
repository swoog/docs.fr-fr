---
title: Espaces blancs dans les littéraux XML (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- white space [XML in Visual Basic]
- XML literals [Visual Basic], white space
ms.assetid: dfe3a9ff-d69a-418e-a6b5-476f4ed84219
ms.openlocfilehash: 60ee90c69aeda38f95107a6043801a4994972079
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2018
ms.locfileid: "39245157"
---
# <a name="white-space-in-xml-literals-visual-basic"></a><span data-ttu-id="7ff55-102">Espaces blancs dans les littéraux XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7ff55-102">White Space in XML Literals (Visual Basic)</span></span>
<span data-ttu-id="7ff55-103">Le compilateur Visual Basic incorpore uniquement les caractères d’espace blanc significatif à partir d’un littéral XML lorsqu’il crée un [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objet.</span><span class="sxs-lookup"><span data-stu-id="7ff55-103">The Visual Basic compiler incorporates only the significant white space characters from an XML literal when it creates a [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] object.</span></span> <span data-ttu-id="7ff55-104">Les caractères d’espaces blancs non significatifs ne sont pas incorporées.</span><span class="sxs-lookup"><span data-stu-id="7ff55-104">The insignificant white space characters are not incorporated.</span></span>  
  
## <a name="significant-and-insignificant-white-space"></a><span data-ttu-id="7ff55-105">Espaces blancs significatifs et non significatifs</span><span class="sxs-lookup"><span data-stu-id="7ff55-105">Significant and Insignificant White Space</span></span>  
 <span data-ttu-id="7ff55-106">Caractères d’espace blanc dans les littéraux XML sont significatifs que dans trois zones :</span><span class="sxs-lookup"><span data-stu-id="7ff55-106">White space characters in XML literals are significant in only three areas:</span></span>  
  
-   <span data-ttu-id="7ff55-107">Lorsqu’ils sont dans une valeur d’attribut.</span><span class="sxs-lookup"><span data-stu-id="7ff55-107">When they are in an attribute value.</span></span>  
  
-   <span data-ttu-id="7ff55-108">Quand ils font partie d’un élément contenu de texte et le texte contient également d’autres caractères.</span><span class="sxs-lookup"><span data-stu-id="7ff55-108">When they are part of an element's text content and the text also contains other characters.</span></span>  
  
-   <span data-ttu-id="7ff55-109">Lorsqu’ils sont dans une expression incorporée pour le contenu de texte d’un élément.</span><span class="sxs-lookup"><span data-stu-id="7ff55-109">When they are in an embedded expression for an element's text content.</span></span>  
  
 <span data-ttu-id="7ff55-110">Sinon, le compilateur traite les caractères d’espace blanc comme insignifiants et ne les inclut pas dans le [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] objet pour le littéral.</span><span class="sxs-lookup"><span data-stu-id="7ff55-110">Otherwise, the compiler treats white space characters as insignificant and does not include then in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] object for the literal.</span></span>  
  
 <span data-ttu-id="7ff55-111">Pour inclure des espaces blancs non significatifs dans un littéral XML, utilisez une expression incorporée qui contient un littéral de chaîne avec les espaces blancs.</span><span class="sxs-lookup"><span data-stu-id="7ff55-111">To include insignificant white space in an XML literal, use an embedded expression that contains a string literal with the white space.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7ff55-112">Si le `xml:space` attribut apparaît dans un littéral d’élément XML, le compilateur Visual Basic inclut l’attribut dans le <xref:System.Xml.Linq.XElement> objet, mais l’ajout de cet attribut ne modifie pas la façon dont le compilateur traite l’espace blanc.</span><span class="sxs-lookup"><span data-stu-id="7ff55-112">If the `xml:space` attribute appears in an XML element literal, the Visual Basic compiler includes the attribute in the <xref:System.Xml.Linq.XElement> object, but adding this attribute does not change how the compiler treats white space.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="7ff55-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="7ff55-113">Examples</span></span>  
 <span data-ttu-id="7ff55-114">L’exemple suivant contient deux éléments XML, externes et internes.</span><span class="sxs-lookup"><span data-stu-id="7ff55-114">The following example contains two XML elements, outer and inner.</span></span> <span data-ttu-id="7ff55-115">Les deux éléments contiennent un espace blanc dans leur contenu de texte.</span><span class="sxs-lookup"><span data-stu-id="7ff55-115">Both elements contain white space in their text content.</span></span> <span data-ttu-id="7ff55-116">L’espace blanc dans l’élément externe est insignifiant, car il contient uniquement un espace blanc et un élément XML.</span><span class="sxs-lookup"><span data-stu-id="7ff55-116">The white space in the outer element is insignificant because it contains only white space and an XML element.</span></span> <span data-ttu-id="7ff55-117">L’espace blanc dans l’élément interne est significatif, car elle contient un espace blanc et texte.</span><span class="sxs-lookup"><span data-stu-id="7ff55-117">The white space in the inner element is significant because it contains white space and text.</span></span>  
  
 [!code-vb[VbXMLSamples#29](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/white-space-in-xml-literals_1.vb)]  
  
 <span data-ttu-id="7ff55-118">Lorsque vous exécutez, ce code affiche le texte suivant.</span><span class="sxs-lookup"><span data-stu-id="7ff55-118">When run, this code displays the following text.</span></span>  
  
```xml  
<outer>  
  <inner>  
                                          Inner text  
                                      </inner>  
</outer>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7ff55-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ff55-119">See Also</span></span>  
 [<span data-ttu-id="7ff55-120">Création de code XML dans Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7ff55-120">Creating XML in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)
