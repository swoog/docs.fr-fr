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
ms.openlocfilehash: fcb50a9c7e36bab046be25d7f82f91cfe0f9be8e
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56966916"
---
# <a name="resume-statement"></a><span data-ttu-id="efd0c-102">Resume, instruction</span><span class="sxs-lookup"><span data-stu-id="efd0c-102">Resume Statement</span></span>
<span data-ttu-id="efd0c-103">Reprend l’exécution une fois une routine de gestion des erreurs est terminée.</span><span class="sxs-lookup"><span data-stu-id="efd0c-103">Resumes execution after an error-handling routine is finished.</span></span>  
  
 <span data-ttu-id="efd0c-104">Nous vous suggérons d’utiliser Gestion structurée des exceptions dans votre code autant que possible, plutôt que d’à l’aide de la gestion non structurée et `On Error` et `Resume` instructions.</span><span class="sxs-lookup"><span data-stu-id="efd0c-104">We suggest that you use structured exception handling in your code whenever possible, rather than using unstructured exception handling and the `On Error` and `Resume` statements.</span></span> <span data-ttu-id="efd0c-105">Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span><span class="sxs-lookup"><span data-stu-id="efd0c-105">For more information, see [Try...Catch...Finally Statement](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="efd0c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efd0c-106">Syntax</span></span>  
  
```  
Resume [ Next | line ]  
```  
  
## <a name="parts"></a><span data-ttu-id="efd0c-107">Composants</span><span class="sxs-lookup"><span data-stu-id="efd0c-107">Parts</span></span>  
 `Resume`  
 <span data-ttu-id="efd0c-108">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="efd0c-108">Required.</span></span> <span data-ttu-id="efd0c-109">Si l’erreur s’est produite dans la même procédure que le Gestionnaire d’erreurs, l’exécution reprend avec l’instruction qui a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="efd0c-109">If the error occurred in the same procedure as the error handler, execution resumes with the statement that caused the error.</span></span> <span data-ttu-id="efd0c-110">Si l’erreur s’est produite dans une procédure appelée, l’exécution reprend à l’instruction qui a appelé la procédure contenant la routine de gestion des erreurs.</span><span class="sxs-lookup"><span data-stu-id="efd0c-110">If the error occurred in a called procedure, execution resumes at the statement that last called out of the procedure containing the error-handling routine.</span></span>  
  
 `Next`  
 <span data-ttu-id="efd0c-111">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="efd0c-111">Optional.</span></span> <span data-ttu-id="efd0c-112">Si l’erreur s’est produite dans la même procédure que le Gestionnaire d’erreurs, l’exécution reprend avec l’instruction qui suit immédiatement l’instruction ayant provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="efd0c-112">If the error occurred in the same procedure as the error handler, execution resumes with the statement immediately following the statement that caused the error.</span></span> <span data-ttu-id="efd0c-113">Si l’erreur s’est produite dans une procédure appelée, l’exécution se poursuit avec l’instruction qui suit immédiatement l’instruction qui a appelé la procédure contenant la routine de gestion des erreurs (ou `On Error Resume Next` instruction).</span><span class="sxs-lookup"><span data-stu-id="efd0c-113">If the error occurred in a called procedure, execution resumes with the statement immediately following the statement that last called out of the procedure containing the error-handling routine (or `On Error Resume Next` statement).</span></span>  
  
 `line`  
 <span data-ttu-id="efd0c-114">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="efd0c-114">Optional.</span></span> <span data-ttu-id="efd0c-115">L’exécution reprend à la ligne spécifiée dans le champ obligatoire `line` argument.</span><span class="sxs-lookup"><span data-stu-id="efd0c-115">Execution resumes at the line specified in the required `line` argument.</span></span> <span data-ttu-id="efd0c-116">Le `line` argument est une étiquette de ligne ou un numéro de ligne et doit se trouver dans la même procédure que le Gestionnaire d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="efd0c-116">The `line` argument is a line label or line number and must be in the same procedure as the error handler.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="efd0c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="efd0c-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="efd0c-118">Nous vous recommandons d’utiliser Gestion structurée des exceptions dans votre code autant que possible, plutôt que d’à l’aide de la gestion non structurée et `On Error` et `Resume` instructions.</span><span class="sxs-lookup"><span data-stu-id="efd0c-118">We recommend that you use structured exception handling in your code whenever possible, rather than using unstructured exception handling and the `On Error` and `Resume` statements.</span></span> <span data-ttu-id="efd0c-119">Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span><span class="sxs-lookup"><span data-stu-id="efd0c-119">For more information, see [Try...Catch...Finally Statement](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).</span></span>  
  
 <span data-ttu-id="efd0c-120">Si vous utilisez un `Resume` instruction n’importe où autre que dans une routine de gestion des erreurs, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="efd0c-120">If you use a `Resume` statement anywhere other than in an error-handling routine, an error occurs.</span></span>  
  
 <span data-ttu-id="efd0c-121">Le `Resume` instruction ne peut pas être utilisée dans une procédure qui contient un `Try...Catch...Finally` instruction.</span><span class="sxs-lookup"><span data-stu-id="efd0c-121">The `Resume` statement cannot be used in any procedure that contains a `Try...Catch...Finally` statement.</span></span>  
  
## <a name="example"></a><span data-ttu-id="efd0c-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="efd0c-122">Example</span></span>  
 <span data-ttu-id="efd0c-123">Cet exemple utilise la `Resume` instruction à la fin dans une procédure de gestion des erreurs et de reprendre l’exécution avec l’instruction qui a provoqué l’erreur.</span><span class="sxs-lookup"><span data-stu-id="efd0c-123">This example uses the `Resume` statement to end error handling in a procedure and then resume execution with the statement that caused the error.</span></span> <span data-ttu-id="efd0c-124">Erreur numéro 55 est générée pour illustrer l’utilisation de la `Resume` instruction.</span><span class="sxs-lookup"><span data-stu-id="efd0c-124">Error number 55 is generated to illustrate use of the `Resume` statement.</span></span>  
  
 [!code-vb[VbVbalrErrorHandling#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrErrorHandling/VB/Class1.vb#16)]  
  
## <a name="requirements"></a><span data-ttu-id="efd0c-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="efd0c-125">Requirements</span></span>  
 <span data-ttu-id="efd0c-126">**Espace de noms :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span><span class="sxs-lookup"><span data-stu-id="efd0c-126">**Namespace:** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span></span>  
  
 <span data-ttu-id="efd0c-127">**Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)</span><span class="sxs-lookup"><span data-stu-id="efd0c-127">**Assembly:** Visual Basic Runtime Library (in Microsoft.VisualBasic.dll)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efd0c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efd0c-128">See also</span></span>
- [<span data-ttu-id="efd0c-129">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="efd0c-129">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [<span data-ttu-id="efd0c-130">Error (instruction)</span><span class="sxs-lookup"><span data-stu-id="efd0c-130">Error Statement</span></span>](../../../visual-basic/language-reference/statements/error-statement.md)
- [<span data-ttu-id="efd0c-131">On Error (instruction)</span><span class="sxs-lookup"><span data-stu-id="efd0c-131">On Error Statement</span></span>](../../../visual-basic/language-reference/statements/on-error-statement.md)
