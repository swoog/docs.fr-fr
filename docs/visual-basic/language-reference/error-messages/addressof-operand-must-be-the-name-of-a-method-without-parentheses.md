---
title: L’opérande 'AddressOf' doit être le nom d’une méthode (sans parenthèses)
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 37b02ab76730458b757835fda37b8cb145ed93ad
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55262112"
---
# <a name="addressof-operand-must-be-the-name-of-a-method-without-parentheses"></a><span data-ttu-id="0897f-102">L’opérande 'AddressOf' doit être le nom d’une méthode (sans parenthèses)</span><span class="sxs-lookup"><span data-stu-id="0897f-102">'AddressOf' operand must be the name of a method (without parentheses)</span></span>
<span data-ttu-id="0897f-103">L’opérateur `AddressOf` crée une instance de délégué de procédure qui fait référence à une procédure spécifique.</span><span class="sxs-lookup"><span data-stu-id="0897f-103">The `AddressOf` operator creates a procedure delegate instance that references a specific procedure.</span></span> <span data-ttu-id="0897f-104">La syntaxe est la suivante.</span><span class="sxs-lookup"><span data-stu-id="0897f-104">The syntax is as follows.</span></span>  
  
 <span data-ttu-id="0897f-105">`AddressOf` `procedurename`</span><span class="sxs-lookup"><span data-stu-id="0897f-105">`AddressOf` `procedurename`</span></span>  
  
 <span data-ttu-id="0897f-106">Vous avez inséré des parenthèses autour de l’argument qui suit `AddressOf`, où aucune n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0897f-106">You inserted parentheses around the argument following `AddressOf`, where none are needed.</span></span>  
  
 <span data-ttu-id="0897f-107">**ID d’erreur :** BC30577</span><span class="sxs-lookup"><span data-stu-id="0897f-107">**Error ID:** BC30577</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0897f-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="0897f-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="0897f-109">Supprimez les parenthèses autour de l’argument qui suit `AddressOf`.</span><span class="sxs-lookup"><span data-stu-id="0897f-109">Remove the parentheses around the argument following `AddressOf`.</span></span>  
  
2.  <span data-ttu-id="0897f-110">Assurez-vous que l’argument est un nom de méthode.</span><span class="sxs-lookup"><span data-stu-id="0897f-110">Make sure the argument is a method name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0897f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0897f-111">See also</span></span>
- [<span data-ttu-id="0897f-112">AddressOf (opérateur)</span><span class="sxs-lookup"><span data-stu-id="0897f-112">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="0897f-113">Délégués</span><span class="sxs-lookup"><span data-stu-id="0897f-113">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
