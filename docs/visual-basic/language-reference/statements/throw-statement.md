---
title: Throw, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Throw
helpviewer_keywords:
- structured exception handling, throw statements
- try-catch exception handling, throw statements
- throw statement [Visual Basic], about throw statements
- throwing exceptions, throw statement
- exception handling, throw statement
- On Error statement [Visual Basic], throwing exceptions
- throwing exceptions
- exception handling, unstructured
- throw statement [Visual Basic]
ms.assetid: a6e07406-5c8a-4498-87a2-8339f3651d62
ms.openlocfilehash: cfa53b3585846da25711739fb7af4bde21746b29
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602851"
---
# <a name="throw-statement-visual-basic"></a><span data-ttu-id="3b3eb-102">Throw, instruction (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3b3eb-102">Throw Statement (Visual Basic)</span></span>
<span data-ttu-id="3b3eb-103">Lève une exception dans une procédure.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-103">Throws an exception within a procedure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b3eb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b3eb-104">Syntax</span></span>  
  
```  
Throw [ expression ]  
```  
  
## <a name="part"></a><span data-ttu-id="3b3eb-105">Élément</span><span class="sxs-lookup"><span data-stu-id="3b3eb-105">Part</span></span>  
 `expression`  
 <span data-ttu-id="3b3eb-106">Fournit des informations relatives à l’exception levée.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-106">Provides information about the exception to be thrown.</span></span> <span data-ttu-id="3b3eb-107">Facultatif lorsqu’il réside dans un `Catch` instruction, requise dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-107">Optional when residing in a `Catch` statement, otherwise required.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3b3eb-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3b3eb-108">Remarks</span></span>  
 <span data-ttu-id="3b3eb-109">Le `Throw` instruction lève une exception que vous pouvez gérer à l’aide du code de gestion des exceptions structurée (`Try`... `Catch`... `Finally`) ou le code de gestion des exceptions structurée (`On Error GoTo`).</span><span class="sxs-lookup"><span data-stu-id="3b3eb-109">The `Throw` statement throws an exception that you can handle with structured exception-handling code (`Try`...`Catch`...`Finally`) or unstructured exception-handling code (`On Error GoTo`).</span></span> <span data-ttu-id="3b3eb-110">Vous pouvez utiliser la `Throw` instruction pour intercepter les erreurs dans votre code, car Visual Basic monte dans la pile des appels jusqu'à ce qu’il trouve le code de gestion des exceptions approprié.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-110">You can use the `Throw` statement to trap errors within your code because Visual Basic moves up the call stack until it finds the appropriate exception-handling code.</span></span>  
  
 <span data-ttu-id="3b3eb-111">A `Throw` instruction sans expression peut uniquement être utilisée dans un `Catch` instruction, dans lequel cas l’instruction lève à nouveau l’exception qui est gérée par le `Catch` instruction.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-111">A `Throw` statement with no expression can only be used in a `Catch` statement, in which case the statement rethrows the exception currently being handled by the `Catch` statement.</span></span>  
  
 <span data-ttu-id="3b3eb-112">Le `Throw` instruction rétablit la pile des appels pour le `expression` exception.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-112">The `Throw` statement resets the call stack for the `expression` exception.</span></span> <span data-ttu-id="3b3eb-113">Si `expression` n’est pas fourni, la pile des appels reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-113">If `expression` is not provided, the call stack is left unchanged.</span></span> <span data-ttu-id="3b3eb-114">Vous pouvez accéder à la pile des appels de l’exception via la <xref:System.Exception.StackTrace%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="3b3eb-114">You can access the call stack for the exception through the <xref:System.Exception.StackTrace%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3b3eb-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="3b3eb-115">Example</span></span>  
 <span data-ttu-id="3b3eb-116">Le code suivant utilise la `Throw` instruction pour lever une exception :</span><span class="sxs-lookup"><span data-stu-id="3b3eb-116">The following code uses the `Throw` statement to throw an exception:</span></span>  
  
 [!code-vb[VbVbalrStatements#84](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/throw-statement_1.vb)]  
  
## <a name="requirements"></a><span data-ttu-id="3b3eb-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b3eb-117">Requirements</span></span>  
 <span data-ttu-id="3b3eb-118">**Namespace :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span><span class="sxs-lookup"><span data-stu-id="3b3eb-118">**Namespace:** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span></span>  
  
 <span data-ttu-id="3b3eb-119">**Module :** `Interaction`</span><span class="sxs-lookup"><span data-stu-id="3b3eb-119">**Module:** `Interaction`</span></span>  
  
 <span data-ttu-id="3b3eb-120">**Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)</span><span class="sxs-lookup"><span data-stu-id="3b3eb-120">**Assembly:** Visual Basic Runtime Library (in Microsoft.VisualBasic.dll)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b3eb-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b3eb-121">See Also</span></span>  
 [<span data-ttu-id="3b3eb-122">Try...Catch...Finally (instruction)</span><span class="sxs-lookup"><span data-stu-id="3b3eb-122">Try...Catch...Finally Statement</span></span>](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)  
 [<span data-ttu-id="3b3eb-123">On Error (instruction)</span><span class="sxs-lookup"><span data-stu-id="3b3eb-123">On Error Statement</span></span>](../../../visual-basic/language-reference/statements/on-error-statement.md)
