---
title: 'Comment : appeler une procédure qui ne retourne pas de valeur (Visual Basic)'
ms.custom: ''
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- procedure calls [Visual Basic], returning values
- Visual Basic code, procedures
- procedures [Visual Basic], calling
ms.assetid: 259b49a3-a3c1-4254-ba8c-73cdc4127703
caps.latest.revision: 17
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: bb9f13d5387f4a440a7fdd39c5e8f50cb8d56270
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-call-a-procedure-that-does-not-return-a-value-visual-basic"></a><span data-ttu-id="2797f-102">Comment : appeler une procédure qui ne retourne pas de valeur (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2797f-102">How to: Call a Procedure that Does Not Return a Value (Visual Basic)</span></span>
<span data-ttu-id="2797f-103">A `Sub` procédure ne retourne pas de valeur au code appelant.</span><span class="sxs-lookup"><span data-stu-id="2797f-103">A `Sub` procedure does not return a value to the calling code.</span></span> <span data-ttu-id="2797f-104">Vous appelez explicitement avec une instruction d’appel autonome.</span><span class="sxs-lookup"><span data-stu-id="2797f-104">You call it explicitly with a stand-alone calling statement.</span></span> <span data-ttu-id="2797f-105">Vous ne pouvez pas l’appeler en utilisant simplement son nom dans une expression.</span><span class="sxs-lookup"><span data-stu-id="2797f-105">You cannot call it by simply using its name within an expression.</span></span>  
  
### <a name="to-call-a-sub-procedure"></a><span data-ttu-id="2797f-106">Pour appeler une procédure Sub</span><span class="sxs-lookup"><span data-stu-id="2797f-106">To call a Sub procedure</span></span>  
  
1.  <span data-ttu-id="2797f-107">Spécifiez le nom de la `Sub` procédure.</span><span class="sxs-lookup"><span data-stu-id="2797f-107">Specify the name of the `Sub` procedure.</span></span>  
  
2.  <span data-ttu-id="2797f-108">Suivez le nom de la procédure avec des parenthèses pour encadrer la liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="2797f-108">Follow the procedure name with parentheses to enclose the argument list.</span></span> <span data-ttu-id="2797f-109">S’il n’y a pas d’arguments, vous pouvez éventuellement omettre les parenthèses.</span><span class="sxs-lookup"><span data-stu-id="2797f-109">If there are no arguments, you can optionally omit the parentheses.</span></span> <span data-ttu-id="2797f-110">Toutefois, à l’aide de parenthèses rend votre code plus facile à lire.</span><span class="sxs-lookup"><span data-stu-id="2797f-110">However, using the parentheses makes your code easier to read.</span></span>  
  
3.  <span data-ttu-id="2797f-111">Placez les arguments dans la liste d’arguments entre parenthèses, séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="2797f-111">Place the arguments in the argument list within the parentheses, separated by commas.</span></span> <span data-ttu-id="2797f-112">Assurez-vous de fournir les arguments dans le même ordre que les `Sub` procédure définit les paramètres correspondants.</span><span class="sxs-lookup"><span data-stu-id="2797f-112">Be sure you supply the arguments in the same order that the `Sub` procedure defines the corresponding parameters.</span></span>  
  
     <span data-ttu-id="2797f-113">L’exemple suivant appelle Visual Basic <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A> fonction pour activer une fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="2797f-113">The following example calls the Visual Basic <xref:Microsoft.VisualBasic.Interaction.AppActivate%2A> function to activate an application window.</span></span> <span data-ttu-id="2797f-114"><xref:Microsoft.VisualBasic.Interaction.AppActivate%2A> accepte le titre de la fenêtre comme unique argument.</span><span class="sxs-lookup"><span data-stu-id="2797f-114"><xref:Microsoft.VisualBasic.Interaction.AppActivate%2A> takes the window title as its sole argument.</span></span> <span data-ttu-id="2797f-115">Il ne retourne pas une valeur au code appelant.</span><span class="sxs-lookup"><span data-stu-id="2797f-115">It does not return a value to the calling code.</span></span> <span data-ttu-id="2797f-116">Si un processus Notepad n’est pas en cours d’exécution, l’exemple lève une <xref:System.ArgumentException>.</span><span class="sxs-lookup"><span data-stu-id="2797f-116">If a Notepad process is not running, the example throws an <xref:System.ArgumentException>.</span></span> <span data-ttu-id="2797f-117">Le `Shell` procédure suppose que les applications se trouvent dans les chemins d’accès spécifiés.</span><span class="sxs-lookup"><span data-stu-id="2797f-117">The `Shell` procedure assumes the applications are in the paths specified.</span></span>  
  
     [!code-vb[VbVbalrCatRef#11](./codesnippet/VisualBasic/how-to-call-a-procedure-that-does-not-return-a-value_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="2797f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2797f-118">See Also</span></span>  
 <xref:Microsoft.VisualBasic.Interaction.Shell%2A>  
 <xref:System.ArgumentException>  
 [<span data-ttu-id="2797f-119">Procédures</span><span class="sxs-lookup"><span data-stu-id="2797f-119">Procedures</span></span>](./index.md)  
 [<span data-ttu-id="2797f-120">Procédures Sub</span><span class="sxs-lookup"><span data-stu-id="2797f-120">Sub Procedures</span></span>](./sub-procedures.md)  
 [<span data-ttu-id="2797f-121">Paramètres et arguments d’une procédure</span><span class="sxs-lookup"><span data-stu-id="2797f-121">Procedure Parameters and Arguments</span></span>](./procedure-parameters-and-arguments.md)  
 [<span data-ttu-id="2797f-122">Sub (instruction)</span><span class="sxs-lookup"><span data-stu-id="2797f-122">Sub Statement</span></span>](../../../../visual-basic/language-reference/statements/sub-statement.md)  
 [<span data-ttu-id="2797f-123">Guide pratique : créer une procédure</span><span class="sxs-lookup"><span data-stu-id="2797f-123">How to: Create a Procedure</span></span>](./how-to-create-a-procedure.md)  
 [<span data-ttu-id="2797f-124">Guide pratique : appeler une procédure qui retourne une valeur</span><span class="sxs-lookup"><span data-stu-id="2797f-124">How to: Call a Procedure That Returns a Value</span></span>](./how-to-call-a-procedure-that-returns-a-value.md)  
 [<span data-ttu-id="2797f-125">Comment : appeler un gestionnaire d’événements en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2797f-125">How to: Call an Event Handler in Visual Basic</span></span>](./how-to-call-an-event-handler.md)
