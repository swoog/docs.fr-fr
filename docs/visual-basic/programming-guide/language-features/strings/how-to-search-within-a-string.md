---
title: 'Comment : effectuer une recherche dans une chaîne (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], finding
- strings [Visual Basic], searching
- examples [Visual Basic], strings
ms.assetid: ae4c79e0-08ea-489f-bdb2-5eb6d355f284
ms.openlocfilehash: 08a005f2927a76c9b29c1ff0092ea8282188b2b2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647681"
---
# <a name="how-to-search-within-a-string-visual-basic"></a><span data-ttu-id="f8685-102">Comment : effectuer une recherche dans une chaîne (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f8685-102">How to: Search Within a String (Visual Basic)</span></span>
<span data-ttu-id="f8685-103">Cet exemple appelle la <xref:System.String.IndexOf%2A> méthode sur un <xref:System.String> objet à l’index de la première occurrence d’une sous-chaîne de rapports.</span><span class="sxs-lookup"><span data-stu-id="f8685-103">This example calls the <xref:System.String.IndexOf%2A> method on a <xref:System.String> object to report the index of the first occurrence of a substring.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f8685-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f8685-104">Example</span></span>  
 [!code-vb[VbVbalrStrings#71](../../../../visual-basic/language-reference/functions/codesnippet/VisualBasic/how-to-search-within-a-string_1.vb)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="f8685-105">Compilation du code</span><span class="sxs-lookup"><span data-stu-id="f8685-105">Compiling the Code</span></span>  
 <span data-ttu-id="f8685-106">Cet exemple nécessite :</span><span class="sxs-lookup"><span data-stu-id="f8685-106">This example requires:</span></span>  
  
-   <span data-ttu-id="f8685-107">Un `Imports` instruction en spécifiant le <xref:System> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="f8685-107">An `Imports` statement specifying the <xref:System> namespace.</span></span> <span data-ttu-id="f8685-108">Pour plus d’informations, consultez [Instruction Imports (espace de noms et type .NET)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).</span><span class="sxs-lookup"><span data-stu-id="f8685-108">For more information, see [Imports Statement (.NET Namespace and Type)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="f8685-109">Programmation fiable</span><span class="sxs-lookup"><span data-stu-id="f8685-109">Robust Programming</span></span>  
 <span data-ttu-id="f8685-110">Le <xref:System.String.IndexOf%2A> méthode signale l’emplacement du premier caractère de la première occurrence de la sous-chaîne.</span><span class="sxs-lookup"><span data-stu-id="f8685-110">The <xref:System.String.IndexOf%2A> method reports the location of the first character of the first occurrence of the substring.</span></span> <span data-ttu-id="f8685-111">L’index est basé sur 0, ce qui signifie que le premier caractère d’une chaîne est un index de 0.</span><span class="sxs-lookup"><span data-stu-id="f8685-111">The index is 0-based, which means the first character of a string has an index of 0.</span></span>  
  
 <span data-ttu-id="f8685-112">Si <xref:System.String.IndexOf%2A> ne trouve pas la sous-chaîne, elle retourne -1.</span><span class="sxs-lookup"><span data-stu-id="f8685-112">If <xref:System.String.IndexOf%2A> does not find the substring, it returns -1.</span></span>  
  
 <span data-ttu-id="f8685-113">Le <xref:System.String.IndexOf%2A> méthode respecte la casse et utilise la culture actuelle.</span><span class="sxs-lookup"><span data-stu-id="f8685-113">The <xref:System.String.IndexOf%2A> method is case-sensitive and uses the current culture.</span></span>  
  
 <span data-ttu-id="f8685-114">Pour un contrôle optimal des erreurs, vous pouvez souhaiter placez la recherche de chaîne dans le `Try` bloquer d’un [essayez... Catch... Instruction finally](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md) construction.</span><span class="sxs-lookup"><span data-stu-id="f8685-114">For optimal error control, you might want to enclose the string search in the `Try` block of a [Try...Catch...Finally Statement](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md) construction.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8685-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8685-115">See Also</span></span>  
 <xref:System.String.IndexOf%2A>  
 [<span data-ttu-id="f8685-116">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="f8685-116">Try...Catch...Finally Statement</span></span>](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
 [<span data-ttu-id="f8685-117">Introduction aux chaînes en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f8685-117">Introduction to Strings in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/strings/introduction-to-strings.md)  
 [<span data-ttu-id="f8685-118">Chaînes</span><span class="sxs-lookup"><span data-stu-id="f8685-118">Strings</span></span>](../../../../visual-basic/programming-guide/language-features/strings/index.md)
