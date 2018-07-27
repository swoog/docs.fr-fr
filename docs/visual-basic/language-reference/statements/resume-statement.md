---
title: Resume, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Resume
- vb.ResumeNext
helpviewer_keywords:
- Next statement [Visual Basic], Resume
- Resume Next statement [Visual Basic]
- execution [Visual Basic], resuming
- run-time errors [Visual Basic], resuming after
- Resume statement [Visual Basic], syntax
- errors [Visual Basic], resuming after
- Error statement [Visual Basic], and Resume statement
- execution
- Resume statement [Visual Basic]
ms.assetid: e24d058b-1a5c-4274-acb9-7d295d3ea537
ms.openlocfilehash: 853f3fe060b70c8a43957d3c843fb95539981679
ms.sourcegitcommit: 70c76a12449439bac0f7a359866be5a0311ce960
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/27/2018
ms.locfileid: "39296154"
---
# <a name="resume-statement"></a><span data-ttu-id="2b4b4-102">Resume, instruction</span><span class="sxs-lookup"><span data-stu-id="2b4b4-102">Resume Statement</span></span>
<span data-ttu-id="2b4b4-103">Reprend l’exécution une fois une routine de gestion des erreurs est terminée.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-103">Resumes execution after an error-handling routine is finished.</span></span>  
  
 <span data-ttu-id="2b4b4-104">Nous vous suggérons d’utiliser Gestion structurée des exceptions dans votre code autant que possible, plutôt que d’à l’aide de la gestion non structurée et `On Error` et `Resume` instructions.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-104">We suggest that you use structured exception handling in your code whenever possible, rather than using unstructured exception handling and the `On Error` and `Resume` statements.</span></span> <span data-ttu-id="2b4b4-105">Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span><span class="sxs-lookup"><span data-stu-id="2b4b4-105">For more information, see [Try...Catch...Finally Statement](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2b4b4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b4b4-106">Syntax</span></span>  
  
```  
Resume [ Next | line ]  
```  
  
## <a name="parts"></a><span data-ttu-id="2b4b4-107">Composants</span><span class="sxs-lookup"><span data-stu-id="2b4b4-107">Parts</span></span>  
 `Resume`  
 <span data-ttu-id="2b4b4-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-108">Required.</span></span> <span data-ttu-id="2b4b4-109">Si l’erreur s’est produite dans la même procédure que le Gestionnaire d’erreurs, l’exécution reprend avec l’instruction qui a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-109">If the error occurred in the same procedure as the error handler, execution resumes with the statement that caused the error.</span></span> <span data-ttu-id="2b4b4-110">Si l’erreur s’est produite dans une procédure appelée, l’exécution reprend à l’instruction qui a appelé la procédure contenant la routine de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-110">If the error occurred in a called procedure, execution resumes at the statement that last called out of the procedure containing the error-handling routine.</span></span>  
  
 `Next`  
 <span data-ttu-id="2b4b4-111">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-111">Optional.</span></span> <span data-ttu-id="2b4b4-112">Si l’erreur s’est produite dans la même procédure que le Gestionnaire d’erreurs, l’exécution reprend avec l’instruction qui suit immédiatement l’instruction ayant provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-112">If the error occurred in the same procedure as the error handler, execution resumes with the statement immediately following the statement that caused the error.</span></span> <span data-ttu-id="2b4b4-113">Si l’erreur s’est produite dans une procédure appelée, l’exécution se poursuit avec l’instruction qui suit immédiatement l’instruction qui a appelé la procédure contenant la routine de gestion des erreurs (ou `On Error Resume Next` instruction).</span><span class="sxs-lookup"><span data-stu-id="2b4b4-113">If the error occurred in a called procedure, execution resumes with the statement immediately following the statement that last called out of the procedure containing the error-handling routine (or `On Error Resume Next` statement).</span></span>  
  
 `line`  
 <span data-ttu-id="2b4b4-114">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-114">Optional.</span></span> <span data-ttu-id="2b4b4-115">L’exécution reprend à la ligne spécifiée dans le champ obligatoire `line` argument.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-115">Execution resumes at the line specified in the required `line` argument.</span></span> <span data-ttu-id="2b4b4-116">Le `line` argument est une étiquette de ligne ou un numéro de ligne et doit se trouver dans la même procédure que le Gestionnaire d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-116">The `line` argument is a line label or line number and must be in the same procedure as the error handler.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2b4b4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2b4b4-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2b4b4-118">Nous vous recommandons d’utiliser Gestion structurée des exceptions dans votre code autant que possible, plutôt que d’à l’aide de la gestion non structurée et `On Error` et `Resume` instructions.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-118">We recommend that you use structured exception handling in your code whenever possible, rather than using unstructured exception handling and the `On Error` and `Resume` statements.</span></span> <span data-ttu-id="2b4b4-119">Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span><span class="sxs-lookup"><span data-stu-id="2b4b4-119">For more information, see [Try...Catch...Finally Statement](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span></span>  
  
 <span data-ttu-id="2b4b4-120">Si vous utilisez un `Resume` instruction n’importe où autre que dans une routine de gestion des erreurs, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-120">If you use a `Resume` statement anywhere other than in an error-handling routine, an error occurs.</span></span>  
  
 <span data-ttu-id="2b4b4-121">Le `Resume` instruction ne peut pas être utilisée dans une procédure qui contient un `Try...Catch...Finally` instruction.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-121">The `Resume` statement cannot be used in any procedure that contains a `Try...Catch...Finally` statement.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2b4b4-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="2b4b4-122">Example</span></span>  
 <span data-ttu-id="2b4b4-123">Cet exemple utilise la `Resume` instruction à la fin dans une procédure de gestion des erreurs et de reprendre l’exécution avec l’instruction qui a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-123">This example uses the `Resume` statement to end error handling in a procedure and then resume execution with the statement that caused the error.</span></span> <span data-ttu-id="2b4b4-124">Erreur numéro 55 est générée pour illustrer l’utilisation de la `Resume` instruction.</span><span class="sxs-lookup"><span data-stu-id="2b4b4-124">Error number 55 is generated to illustrate use of the `Resume` statement.</span></span>  
  
 [!code-vb[VbVbalrErrorHandling#16](../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/resume-statement_1.vb)]  
  
## <a name="requirements"></a><span data-ttu-id="2b4b4-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b4b4-125">Requirements</span></span>  
 <span data-ttu-id="2b4b4-126">**Namespace :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span><span class="sxs-lookup"><span data-stu-id="2b4b4-126">**Namespace:** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span></span>  
  
 <span data-ttu-id="2b4b4-127">**Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)</span><span class="sxs-lookup"><span data-stu-id="2b4b4-127">**Assembly:** Visual Basic Runtime Library (in Microsoft.VisualBasic.dll)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b4b4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b4b4-128">See Also</span></span>  
 [<span data-ttu-id="2b4b4-129">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="2b4b4-129">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
 [<span data-ttu-id="2b4b4-130">Error (instruction)</span><span class="sxs-lookup"><span data-stu-id="2b4b4-130">Error Statement</span></span>](../../../visual-basic/language-reference/statements/error-statement.md)  
 [<span data-ttu-id="2b4b4-131">On Error (instruction)</span><span class="sxs-lookup"><span data-stu-id="2b4b4-131">On Error Statement</span></span>](../../../visual-basic/language-reference/statements/on-error-statement.md)
