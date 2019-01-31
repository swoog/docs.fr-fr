---
title: Les expressions lambda ne sont pas valides dans la première expression d’une instruction ’Select Case’
ms.date: 07/20/2015
f1_keywords:
- bc36635
- vbc36635
helpviewer_keywords:
- BC36635
ms.assetid: 74609979-9c03-4864-bbce-f588aa2e0917
ms.openlocfilehash: d56515093020a4c987d132491957ce6db9e21683
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55287792"
---
# <a name="lambda-expressions-are-not-valid-in-the-first-expression-of-a-select-case-statement"></a><span data-ttu-id="d34f6-102">Les expressions lambda ne sont pas valides dans la première expression d’une instruction ’Select Case’</span><span class="sxs-lookup"><span data-stu-id="d34f6-102">Lambda expressions are not valid in the first expression of a 'Select Case' statement</span></span>
<span data-ttu-id="d34f6-103">Vous ne pouvez pas utiliser une expression lambda pour l’expression de test dans un `Select Case` instruction.</span><span class="sxs-lookup"><span data-stu-id="d34f6-103">You cannot use a lambda expression for the test expression in a `Select Case` statement.</span></span> <span data-ttu-id="d34f6-104">Définitions d’expression lambda retournent des fonctions et l’expression de test d’un `Select Case` instruction doit être un type de données élémentaire.</span><span class="sxs-lookup"><span data-stu-id="d34f6-104">Lambda expression definitions return functions, and the test expression of a `Select Case` statement must be an elementary data type.</span></span>  
  
 <span data-ttu-id="d34f6-105">Le code suivant génère cette erreur :</span><span class="sxs-lookup"><span data-stu-id="d34f6-105">The following code causes this error:</span></span>  
  
```vb  
' Select Case (Function(arg) arg Is Nothing)  
    ' List of the cases.  
' End Select  
```  
  
 <span data-ttu-id="d34f6-106">**ID d’erreur :** BC36635</span><span class="sxs-lookup"><span data-stu-id="d34f6-106">**Error ID:** BC36635</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="d34f6-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="d34f6-107">To correct this error</span></span>  
  
-   <span data-ttu-id="d34f6-108">Examinez votre code pour déterminer si une construction conditionnelle différente, comme une instruction `If...Then...Else` , répond à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="d34f6-108">Examine your code to determine whether a different conditional construction, such as an `If...Then...Else` statement, would work for you.</span></span>  
  
-   <span data-ttu-id="d34f6-109">Vous aviez prévu appeler la fonction, comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d34f6-109">You may have intended to call the function, as shown in the following code:</span></span>  
  
```vb  
Dim num? As Integer  
Select Case ((Function(arg? As Integer) arg Is Nothing)(num))  
    ' List of the cases  
End Select  
```  
  
## <a name="see-also"></a><span data-ttu-id="d34f6-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d34f6-110">See also</span></span>
- [<span data-ttu-id="d34f6-111">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="d34f6-111">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="d34f6-112">If...Then...Else (instruction)</span><span class="sxs-lookup"><span data-stu-id="d34f6-112">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [<span data-ttu-id="d34f6-113">Select...Case (instruction)</span><span class="sxs-lookup"><span data-stu-id="d34f6-113">Select...Case Statement</span></span>](../../../visual-basic/language-reference/statements/select-case-statement.md)
