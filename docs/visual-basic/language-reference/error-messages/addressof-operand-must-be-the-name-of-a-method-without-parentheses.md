---
title: L'opérande 'AddressOf' doit être le nom d'une méthode (sans parenthèses)
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: b8c67c2390df91c6a4af66e020365544e6bf369b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61751629"
---
# <a name="addressof-operand-must-be-the-name-of-a-method-without-parentheses"></a><span data-ttu-id="203be-102">L'opérande 'AddressOf' doit être le nom d'une méthode (sans parenthèses)</span><span class="sxs-lookup"><span data-stu-id="203be-102">'AddressOf' operand must be the name of a method (without parentheses)</span></span>
<span data-ttu-id="203be-103">L’opérateur `AddressOf` crée une instance de délégué de procédure qui fait référence à une procédure spécifique.</span><span class="sxs-lookup"><span data-stu-id="203be-103">The `AddressOf` operator creates a procedure delegate instance that references a specific procedure.</span></span> <span data-ttu-id="203be-104">La syntaxe est la suivante.</span><span class="sxs-lookup"><span data-stu-id="203be-104">The syntax is as follows.</span></span>  
  
 <span data-ttu-id="203be-105">`AddressOf` `procedurename`</span><span class="sxs-lookup"><span data-stu-id="203be-105">`AddressOf` `procedurename`</span></span>  
  
 <span data-ttu-id="203be-106">Vous avez inséré des parenthèses autour de l’argument qui suit `AddressOf`, où aucune n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="203be-106">You inserted parentheses around the argument following `AddressOf`, where none are needed.</span></span>  
  
 <span data-ttu-id="203be-107">**ID d’erreur :** BC30577</span><span class="sxs-lookup"><span data-stu-id="203be-107">**Error ID:** BC30577</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="203be-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="203be-108">To correct this error</span></span>  
  
1. <span data-ttu-id="203be-109">Supprimez les parenthèses autour de l’argument qui suit `AddressOf`.</span><span class="sxs-lookup"><span data-stu-id="203be-109">Remove the parentheses around the argument following `AddressOf`.</span></span>  
  
2. <span data-ttu-id="203be-110">Assurez-vous que l’argument est un nom de méthode.</span><span class="sxs-lookup"><span data-stu-id="203be-110">Make sure the argument is a method name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="203be-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="203be-111">See also</span></span>

- [<span data-ttu-id="203be-112">AddressOf (opérateur)</span><span class="sxs-lookup"><span data-stu-id="203be-112">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="203be-113">Délégués</span><span class="sxs-lookup"><span data-stu-id="203be-113">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
