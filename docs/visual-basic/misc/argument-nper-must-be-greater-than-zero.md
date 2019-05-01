---
title: L’argument 'NPer' doit être supérieur à zéro
ms.date: 07/20/2015
f1_keywords:
- vbrRate_NPerMustBeGTZero
ms.assetid: d49242df-dbd1-4b26-bd8c-ed56d24fdfcd
ms.openlocfilehash: 6f54a2da0eb0c1cc31a4aa536fdcb59026240a25
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61977143"
---
# <a name="argument-nper-must-be-greater-than-zero"></a><span data-ttu-id="72446-102">L’argument 'NPer' doit être supérieur à zéro</span><span class="sxs-lookup"><span data-stu-id="72446-102">Argument 'NPer' must be greater than zero</span></span>
<span data-ttu-id="72446-103">La fonction `NPer` , qui retourne un `Double` spécifiant le nombre de périodes pour une annuité sur la base de versements fixes périodiques et d’un taux d’intérêt fixe, nécessite un argument supérieur à zéro.</span><span class="sxs-lookup"><span data-stu-id="72446-103">The `NPer` function, which returns a `Double` specifying the number of periods for an annuity based on periodic fixed payments and a fixed interest rate, requires an argument greater than zero.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="72446-104">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="72446-104">To correct this error</span></span>  
  
- <span data-ttu-id="72446-105">Vérifiez l’orthographe des arguments dans l’expression.</span><span class="sxs-lookup"><span data-stu-id="72446-105">Check the spelling of arguments in the expression.</span></span> <span data-ttu-id="72446-106">Un nom de variable mal orthographié peut créer implicitement une variable numérique dont la valeur est zéro.</span><span class="sxs-lookup"><span data-stu-id="72446-106">A misspelled variable name can implicitly create a numeric variable that is initialized to zero.</span></span>  
  
- <span data-ttu-id="72446-107">Vérifiez les opérations précédentes sur les variables de l’expression, surtout celles passées dans la procédure en tant qu’arguments à partir d’autres procédures.</span><span class="sxs-lookup"><span data-stu-id="72446-107">Check previous operations on variables in the expression, especially those passed into the procedure as arguments from other procedures.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72446-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72446-108">See also</span></span>

- [<span data-ttu-id="72446-109">Passage d’un argument par valeur et par référence</span><span class="sxs-lookup"><span data-stu-id="72446-109">Passing Arguments by Value and by Reference</span></span>](../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)
