---
title: REM, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.'
- vb.Rem
- Rem
- "'"
helpviewer_keywords:
- REM statement [Visual Basic]
- comments, Visual Basic code
- code comments, Visual Basic
- Visual Basic code, comments
- "' comment marker character [Visual Basic]"
ms.assetid: 34126d7f-e0f9-476d-91e6-b31b398615dc
ms.openlocfilehash: 3bd526b08e1ba3be856e1e823cf8ef49ea9b6c97
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33604274"
---
# <a name="rem-statement-visual-basic"></a><span data-ttu-id="b747b-102">REM, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b747b-102">REM Statement (Visual Basic)</span></span>
<span data-ttu-id="b747b-103">Permet d’inclure des notes explicatives dans le code source d’un programme.</span><span class="sxs-lookup"><span data-stu-id="b747b-103">Used to include explanatory remarks in the source code of a program.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b747b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b747b-104">Syntax</span></span>  
  
```  
REM comment  
' comment  
```  
  
## <a name="parts"></a><span data-ttu-id="b747b-105">Composants</span><span class="sxs-lookup"><span data-stu-id="b747b-105">Parts</span></span>  
 `comment`  
 <span data-ttu-id="b747b-106">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="b747b-106">Optional.</span></span> <span data-ttu-id="b747b-107">Le texte des commentaires que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="b747b-107">The text of any comment you want to include.</span></span> <span data-ttu-id="b747b-108">Un espace est requis entre le `REM` (mot clé) et `comment`.</span><span class="sxs-lookup"><span data-stu-id="b747b-108">A space is required between the `REM` keyword and `comment`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b747b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b747b-109">Remarks</span></span>  
 <span data-ttu-id="b747b-110">Vous pouvez placer un `REM` instruction seule sur une ligne, ou vous pouvez le placer sur une ligne qui suit une autre instruction.</span><span class="sxs-lookup"><span data-stu-id="b747b-110">You can put a `REM` statement alone on a line, or you can put it on a line following another statement.</span></span> <span data-ttu-id="b747b-111">La `REM` instruction doit être la dernière instruction de la ligne.</span><span class="sxs-lookup"><span data-stu-id="b747b-111">The `REM` statement must be the last statement on the line.</span></span> <span data-ttu-id="b747b-112">Si elle suit une autre instruction, la `REM` doit être séparée de cette instruction par un espace.</span><span class="sxs-lookup"><span data-stu-id="b747b-112">If it follows another statement, the `REM` must be separated from that statement by a space.</span></span>  
  
 <span data-ttu-id="b747b-113">Vous pouvez utiliser un guillemet simple (`'`) au lieu de `REM`.</span><span class="sxs-lookup"><span data-stu-id="b747b-113">You can use a single quotation mark (`'`) instead of `REM`.</span></span> <span data-ttu-id="b747b-114">Cela est vrai si votre commentaire suit une autre instruction sur la même ligne ou se situe seul sur une ligne.</span><span class="sxs-lookup"><span data-stu-id="b747b-114">This is true whether your comment follows another statement on the same line or sits alone on a line.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b747b-115">Vous ne pouvez pas continuer une `REM` instruction à l’aide d’une séquence de continuation de ligne (`_`).</span><span class="sxs-lookup"><span data-stu-id="b747b-115">You cannot continue a `REM` statement by using a line-continuation sequence (`_`).</span></span> <span data-ttu-id="b747b-116">Une fois qu’un commentaire commencé, le compilateur n’examine pas les caractères pour une signification particulière.</span><span class="sxs-lookup"><span data-stu-id="b747b-116">Once a comment begins, the compiler does not examine the characters for special meaning.</span></span> <span data-ttu-id="b747b-117">Un commentaire de plusieurs lignes, utilisez un autre `REM` instruction ou un symbole de commentaire (`'`) sur chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="b747b-117">For a multiple-line comment, use another `REM` statement or a comment symbol (`'`) on each line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b747b-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="b747b-118">Example</span></span>  
 <span data-ttu-id="b747b-119">L’exemple suivant illustre la `REM` instruction, qui est utilisée pour inclure des notes explicatives dans un programme.</span><span class="sxs-lookup"><span data-stu-id="b747b-119">The following example illustrates the `REM` statement, which is used to include explanatory remarks in a program.</span></span> <span data-ttu-id="b747b-120">Il montre également d’utiliser le guillemet simple (`'`) au lieu de `REM`.</span><span class="sxs-lookup"><span data-stu-id="b747b-120">It also shows the alternative of using the single quotation-mark character (`'`) instead of `REM`.</span></span>  
  
 [!code-vb[VbVbalrStatements#6](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/rem-statement_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="b747b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b747b-121">See Also</span></span>  
 [<span data-ttu-id="b747b-122">Commentaires dans le code</span><span class="sxs-lookup"><span data-stu-id="b747b-122">Comments in Code</span></span>](../../../visual-basic/programming-guide/program-structure/comments-in-code.md)  
 [<span data-ttu-id="b747b-123">Guide pratique : diviser et combiner des instructions dans le code</span><span class="sxs-lookup"><span data-stu-id="b747b-123">How to: Break and Combine Statements in Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
