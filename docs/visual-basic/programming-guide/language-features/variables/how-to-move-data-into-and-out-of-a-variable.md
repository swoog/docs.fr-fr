---
title: 'Procédure : Déplacer des données dans et hors d’une Variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], retrieving values
- variables [Visual Basic], storing data
ms.assetid: 93744f46-bf78-4fa0-9640-1de01bc38d9a
ms.openlocfilehash: 30d1c0ab91724ac556e59b272782513ee8b8067b
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58818530"
---
# <a name="how-to-move-data-into-and-out-of-a-variable-visual-basic"></a><span data-ttu-id="fca79-102">Procédure : Déplacer des données dans et hors d’une Variable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fca79-102">How to: Move Data Into and Out of a Variable (Visual Basic)</span></span>
<span data-ttu-id="fca79-103">Vous stockez une valeur dans une variable en plaçant le nom de variable sur le côté gauche d’une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="fca79-103">You store a value in a variable by putting the variable name on the left side of an assignment statement.</span></span>  
  
## <a name="putting-data-in-a-variable"></a><span data-ttu-id="fca79-104">Placer des données dans une Variable</span><span class="sxs-lookup"><span data-stu-id="fca79-104">Putting Data in a Variable</span></span>  
  
#### <a name="to-store-a-value-in-a-variable"></a><span data-ttu-id="fca79-105">Pour stocker une valeur dans une variable</span><span class="sxs-lookup"><span data-stu-id="fca79-105">To store a value in a variable</span></span>  
  
-   <span data-ttu-id="fca79-106">Utilisez le nom de variable sur le côté gauche d’une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="fca79-106">Use the variable name on the left side of an assignment statement.</span></span>  
  
     <span data-ttu-id="fca79-107">L’exemple suivant définit la valeur de la variable `alpha`.</span><span class="sxs-lookup"><span data-stu-id="fca79-107">The following example sets the value of the variable `alpha`.</span></span>  
  
    ```  
    alpha = (beta * 6.27) / (gamma + 2.1)  
    ```  
  
     <span data-ttu-id="fca79-108">La valeur générée sur le côté droit de l’instruction d’assignation est stockée dans la variable.</span><span class="sxs-lookup"><span data-stu-id="fca79-108">The value generated on the right side of the assignment statement is stored in the variable.</span></span>  
  
## <a name="getting-data-from-a-variable"></a><span data-ttu-id="fca79-109">Obtention de données à partir d’une Variable</span><span class="sxs-lookup"><span data-stu-id="fca79-109">Getting Data from a Variable</span></span>  
 <span data-ttu-id="fca79-110">Vous récupérez une valeur variable en incluant le nom de variable dans une expression.</span><span class="sxs-lookup"><span data-stu-id="fca79-110">You retrieve a variable's value by including the variable name in an expression.</span></span>  
  
#### <a name="to-retrieve-a-value-from-a-variable"></a><span data-ttu-id="fca79-111">Pour récupérer une valeur dans une variable</span><span class="sxs-lookup"><span data-stu-id="fca79-111">To retrieve a value from a variable</span></span>  
  
-   <span data-ttu-id="fca79-112">Utilisez le nom de variable dans une expression.</span><span class="sxs-lookup"><span data-stu-id="fca79-112">Use the variable name in an expression.</span></span> <span data-ttu-id="fca79-113">Vous pouvez utiliser une variable de n’importe où vous pouvez utiliser une constante ou un littéral, sauf dans une expression qui définit la valeur d’une constante.</span><span class="sxs-lookup"><span data-stu-id="fca79-113">You can use a variable anywhere you can use a constant or a literal, except in an expression that defines the value of a constant.</span></span>  
  
     <span data-ttu-id="fca79-114">- ou -</span><span class="sxs-lookup"><span data-stu-id="fca79-114">-or-</span></span>  
  
-   <span data-ttu-id="fca79-115">Utiliser le nom de variable suivant égaux (`=`) connectez-vous à une instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="fca79-115">Use the variable name following the equal (`=`) sign in an assignment statement.</span></span>  
  
     <span data-ttu-id="fca79-116">L’exemple suivant lit la valeur de la variable `startValue` , puis utilise la valeur de la variable `counter` dans une expression.</span><span class="sxs-lookup"><span data-stu-id="fca79-116">The following example reads the value of the variable `startValue` and then uses the value of the variable `counter` in an expression.</span></span>  
  
    ```  
    counter = startValue  
    cellValue = (counter + 5) ^ 2  
    ```  
  
     <span data-ttu-id="fca79-117">La valeur de la variable participe à l’expression comme une constante serait, puis il est stocké dans la variable ou la propriété sur le côté gauche de l’instruction d’assignation.</span><span class="sxs-lookup"><span data-stu-id="fca79-117">The value of the variable participates in the expression just as a constant would, and then it is stored in the variable or property on the left side of the assignment statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fca79-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fca79-118">See also</span></span>

- [<span data-ttu-id="fca79-119">Variables</span><span class="sxs-lookup"><span data-stu-id="fca79-119">Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/index.md)
- [<span data-ttu-id="fca79-120">Déclaration de variable</span><span class="sxs-lookup"><span data-stu-id="fca79-120">Variable Declaration</span></span>](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [<span data-ttu-id="fca79-121">Variables objets</span><span class="sxs-lookup"><span data-stu-id="fca79-121">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
