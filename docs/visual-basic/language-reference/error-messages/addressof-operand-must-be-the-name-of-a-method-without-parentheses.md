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
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59323822"
---
# <a name="addressof-operand-must-be-the-name-of-a-method-without-parentheses"></a><span data-ttu-id="750e1-102">L'opérande 'AddressOf' doit être le nom d'une méthode (sans parenthèses)</span><span class="sxs-lookup"><span data-stu-id="750e1-102">'AddressOf' operand must be the name of a method (without parentheses)</span></span>
<span data-ttu-id="750e1-103">L’opérateur `AddressOf` crée une instance de délégué de procédure qui fait référence à une procédure spécifique.</span><span class="sxs-lookup"><span data-stu-id="750e1-103">The `AddressOf` operator creates a procedure delegate instance that references a specific procedure.</span></span> <span data-ttu-id="750e1-104">La syntaxe est la suivante.</span><span class="sxs-lookup"><span data-stu-id="750e1-104">The syntax is as follows.</span></span>  
  
 `AddressOf` `procedurename`  
  
 <span data-ttu-id="750e1-105">Vous avez inséré des parenthèses autour de l’argument qui suit `AddressOf`, où aucune n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="750e1-105">You inserted parentheses around the argument following `AddressOf`, where none are needed.</span></span>  
  
 <span data-ttu-id="750e1-106">**ID d’erreur :** BC30577</span><span class="sxs-lookup"><span data-stu-id="750e1-106">**Error ID:** BC30577</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="750e1-107">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="750e1-107">To correct this error</span></span>  
  
1. <span data-ttu-id="750e1-108">Supprimez les parenthèses autour de l’argument qui suit `AddressOf`.</span><span class="sxs-lookup"><span data-stu-id="750e1-108">Remove the parentheses around the argument following `AddressOf`.</span></span>  
  
2. <span data-ttu-id="750e1-109">Assurez-vous que l’argument est un nom de méthode.</span><span class="sxs-lookup"><span data-stu-id="750e1-109">Make sure the argument is a method name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="750e1-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="750e1-110">See also</span></span>

- [<span data-ttu-id="750e1-111">AddressOf, opérateur</span><span class="sxs-lookup"><span data-stu-id="750e1-111">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="750e1-112">Délégués</span><span class="sxs-lookup"><span data-stu-id="750e1-112">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
