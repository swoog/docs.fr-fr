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
ms.openlocfilehash: 3c63c5613b40cb2014c77a0a996e3acb2cc304d4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61783931"
---
# <a name="rem-statement-visual-basic"></a><span data-ttu-id="de599-102">REM, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="de599-102">REM Statement (Visual Basic)</span></span>
<span data-ttu-id="de599-103">Permet d’inclure des notes explicatives dans le code source d’un programme.</span><span class="sxs-lookup"><span data-stu-id="de599-103">Used to include explanatory remarks in the source code of a program.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de599-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de599-104">Syntax</span></span>  
  
```  
REM comment  
' comment  
```  
  
## <a name="parts"></a><span data-ttu-id="de599-105">Composants</span><span class="sxs-lookup"><span data-stu-id="de599-105">Parts</span></span>  
 `comment`  
 <span data-ttu-id="de599-106">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="de599-106">Optional.</span></span> <span data-ttu-id="de599-107">Le texte des commentaires que vous souhaitez inclure.</span><span class="sxs-lookup"><span data-stu-id="de599-107">The text of any comment you want to include.</span></span> <span data-ttu-id="de599-108">Un espace est nécessaire entre le `REM` mot clé et `comment`.</span><span class="sxs-lookup"><span data-stu-id="de599-108">A space is required between the `REM` keyword and `comment`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="de599-109">Notes</span><span class="sxs-lookup"><span data-stu-id="de599-109">Remarks</span></span>  
 <span data-ttu-id="de599-110">Vous pouvez placer un `REM` instruction seule sur une ligne, ou vous pouvez le placer sur une ligne qui suit une autre instruction.</span><span class="sxs-lookup"><span data-stu-id="de599-110">You can put a `REM` statement alone on a line, or you can put it on a line following another statement.</span></span> <span data-ttu-id="de599-111">La `REM` instruction doit être la dernière instruction sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="de599-111">The `REM` statement must be the last statement on the line.</span></span> <span data-ttu-id="de599-112">Si elle suit une autre instruction, le `REM` doivent être séparés de cette instruction par un espace.</span><span class="sxs-lookup"><span data-stu-id="de599-112">If it follows another statement, the `REM` must be separated from that statement by a space.</span></span>  
  
 <span data-ttu-id="de599-113">Vous pouvez utiliser un guillemet unique (`'`) au lieu de `REM`.</span><span class="sxs-lookup"><span data-stu-id="de599-113">You can use a single quotation mark (`'`) instead of `REM`.</span></span> <span data-ttu-id="de599-114">Cela est vrai si votre commentaire suit une autre instruction sur la même ligne ou se trouve uniquement sur une ligne.</span><span class="sxs-lookup"><span data-stu-id="de599-114">This is true whether your comment follows another statement on the same line or sits alone on a line.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="de599-115">Vous ne pouvez pas continuer une `REM` instruction à l’aide d’une séquence de continuation de ligne (`_`).</span><span class="sxs-lookup"><span data-stu-id="de599-115">You cannot continue a `REM` statement by using a line-continuation sequence (`_`).</span></span> <span data-ttu-id="de599-116">Une fois un commentaire démarré, le compilateur n’examine pas les caractères pour une signification spéciale.</span><span class="sxs-lookup"><span data-stu-id="de599-116">Once a comment begins, the compiler does not examine the characters for special meaning.</span></span> <span data-ttu-id="de599-117">Un commentaire de plusieurs lignes, utilisez un autre `REM` instruction ou un symbole de commentaire (`'`) sur chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="de599-117">For a multiple-line comment, use another `REM` statement or a comment symbol (`'`) on each line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="de599-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="de599-118">Example</span></span>  
 <span data-ttu-id="de599-119">L’exemple suivant illustre la `REM` instruction, qui est utilisée pour inclure des notes explicatives dans un programme.</span><span class="sxs-lookup"><span data-stu-id="de599-119">The following example illustrates the `REM` statement, which is used to include explanatory remarks in a program.</span></span> <span data-ttu-id="de599-120">Il montre également d’utiliser le caractère guillemet simple (`'`) au lieu de `REM`.</span><span class="sxs-lookup"><span data-stu-id="de599-120">It also shows the alternative of using the single quotation-mark character (`'`) instead of `REM`.</span></span>  
  
 [!code-vb[VbVbalrStatements#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="de599-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de599-121">See also</span></span>

- [<span data-ttu-id="de599-122">Commentaires dans le code</span><span class="sxs-lookup"><span data-stu-id="de599-122">Comments in Code</span></span>](../../../visual-basic/programming-guide/program-structure/comments-in-code.md)
- [<span data-ttu-id="de599-123">Guide pratique pour diviser et combiner des instructions dans le code</span><span class="sxs-lookup"><span data-stu-id="de599-123">How to: Break and Combine Statements in Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
