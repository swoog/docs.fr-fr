---
title: La fonction '<procedurename>' ne retourne pas une valeur pour tous les chemins de code
ms.date: 07/20/2015
f1_keywords:
- bc42105
- vbc42105
helpviewer_keywords:
- BC42105
ms.assetid: b6929bf4-a365-4a70-8dc9-6b0fc09e1468
ms.openlocfilehash: badcfea4f24ba3858071e02ba47b8f77ab557f88
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61802373"
---
# <a name="function-procedurename-doesnt-return-a-value-on-all-code-paths"></a><span data-ttu-id="fd289-102">Fonction '\<nom_procédure >' ne retourne pas une valeur pour tous les chemins de code</span><span class="sxs-lookup"><span data-stu-id="fd289-102">Function '\<procedurename>' doesn't return a value on all code paths</span></span>
<span data-ttu-id="fd289-103">Fonction '\<nom_procédure >' ne retourne pas une valeur pour tous les chemins de code.</span><span class="sxs-lookup"><span data-stu-id="fd289-103">Function '\<procedurename>' doesn't return a value on all code paths.</span></span> <span data-ttu-id="fd289-104">Une instruction 'Return' est-elle manquante ?</span><span class="sxs-lookup"><span data-stu-id="fd289-104">Are you missing a 'Return' statement?</span></span>  
  
 <span data-ttu-id="fd289-105">Un `Function` procédure a au moins un chemin d’accès possible via son code qui ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fd289-105">A `Function` procedure has at least one possible path through its code that does not return a value.</span></span>  
  
 <span data-ttu-id="fd289-106">Vous pouvez retourner une valeur à partir d’un `Function` procédure dans une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd289-106">You can return a value from a `Function` procedure in any of the following ways:</span></span>  
  
- <span data-ttu-id="fd289-107">Inclure la valeur dans un [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md).</span><span class="sxs-lookup"><span data-stu-id="fd289-107">Include the value in a [Return Statement](../../../visual-basic/language-reference/statements/return-statement.md).</span></span>  
  
- <span data-ttu-id="fd289-108">Affectez la valeur pour le `Function` procédure nommez, puis effectuez une `Exit Function` instruction.</span><span class="sxs-lookup"><span data-stu-id="fd289-108">Assign the value to the `Function` procedure name and then perform an `Exit Function` statement.</span></span>  
  
- <span data-ttu-id="fd289-109">Affectez la valeur pour le `Function` procédure nommez, puis effectuez la `End Function` instruction.</span><span class="sxs-lookup"><span data-stu-id="fd289-109">Assign the value to the `Function` procedure name and then perform the `End Function` statement.</span></span>  
  
 <span data-ttu-id="fd289-110">Si le contrôle passe à `Exit Function` ou `End Function` et vous n’avez pas affectés n’importe quelle valeur pour le nom de la procédure, la procédure retourne la valeur par défaut du type de retour de données.</span><span class="sxs-lookup"><span data-stu-id="fd289-110">If control passes to `Exit Function` or `End Function` and you have not assigned any value to the procedure name, the procedure returns the default value of the return data type.</span></span> <span data-ttu-id="fd289-111">Pour plus d’informations, consultez « Comportement » dans [Function, instruction](../../../visual-basic/language-reference/statements/function-statement.md).</span><span class="sxs-lookup"><span data-stu-id="fd289-111">For more information, see "Behavior" in [Function Statement](../../../visual-basic/language-reference/statements/function-statement.md).</span></span>  
  
 <span data-ttu-id="fd289-112">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="fd289-112">By default, this message is a warning.</span></span> <span data-ttu-id="fd289-113">Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="fd289-113">For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="fd289-114">**ID d’erreur :** BC42105</span><span class="sxs-lookup"><span data-stu-id="fd289-114">**Error ID:** BC42105</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="fd289-115">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="fd289-115">To correct this error</span></span>  
  
- <span data-ttu-id="fd289-116">Vérifiez votre logique de flux de contrôle et assurez-vous que vous assignez une valeur avant chaque instruction qui provoque un retour.</span><span class="sxs-lookup"><span data-stu-id="fd289-116">Check your control flow logic and make sure you assign a value before every statement that causes a return.</span></span>  
  
     <span data-ttu-id="fd289-117">Il est plus facile de garantir que chaque retour de la procédure retourne une valeur si vous utilisez toujours la `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="fd289-117">It is easier to guarantee that every return from the procedure returns a value if you always use the `Return` statement.</span></span> <span data-ttu-id="fd289-118">Si vous le faites, la dernière instruction avant `End Function` doit être un `Return` instruction.</span><span class="sxs-lookup"><span data-stu-id="fd289-118">If you do this, the last statement before `End Function` should be a `Return` statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd289-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd289-119">See also</span></span>

- [<span data-ttu-id="fd289-120">Procédures Function</span><span class="sxs-lookup"><span data-stu-id="fd289-120">Function Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/function-procedures.md)
- [<span data-ttu-id="fd289-121">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="fd289-121">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
- [<span data-ttu-id="fd289-122">Page Compiler, Concepteur de projet (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fd289-122">Compile Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/compile-page-project-designer-visual-basic)
