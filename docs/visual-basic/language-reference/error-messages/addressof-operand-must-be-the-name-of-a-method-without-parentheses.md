---
title: '&#39;AddressOf&#39; opérande doit être le nom d’une méthode (sans parenthèses)'
ms.date: 07/20/2015
f1_keywords:
- vbc30577
- bc30577
helpviewer_keywords:
- BC30577
ms.assetid: c2c55640-5c61-4e66-97a4-4322020c6001
ms.openlocfilehash: 701d86e03d9b14236eec8436d99ec40cebbbcd44
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33583810"
---
# <a name="39addressof39-operand-must-be-the-name-of-a-method-without-parentheses"></a><span data-ttu-id="f0ef1-102">&#39;AddressOf&#39; opérande doit être le nom d’une méthode (sans parenthèses)</span><span class="sxs-lookup"><span data-stu-id="f0ef1-102">&#39;AddressOf&#39; operand must be the name of a method (without parentheses)</span></span>
<span data-ttu-id="f0ef1-103">L’opérateur `AddressOf` crée une instance de délégué de procédure qui fait référence à une procédure spécifique.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-103">The `AddressOf` operator creates a procedure delegate instance that references a specific procedure.</span></span> <span data-ttu-id="f0ef1-104">La syntaxe est la suivante.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-104">The syntax is as follows.</span></span>  
  
 <span data-ttu-id="f0ef1-105">`AddressOf` `procedurename`</span><span class="sxs-lookup"><span data-stu-id="f0ef1-105">`AddressOf` `procedurename`</span></span>  
  
 <span data-ttu-id="f0ef1-106">Vous avez inséré des parenthèses autour de l’argument qui suit `AddressOf`, où aucune n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-106">You inserted parentheses around the argument following `AddressOf`, where none are needed.</span></span>  
  
 <span data-ttu-id="f0ef1-107">**ID d’erreur :** BC30577</span><span class="sxs-lookup"><span data-stu-id="f0ef1-107">**Error ID:** BC30577</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="f0ef1-108">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="f0ef1-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="f0ef1-109">Supprimez les parenthèses autour de l’argument qui suit `AddressOf`.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-109">Remove the parentheses around the argument following `AddressOf`.</span></span>  
  
2.  <span data-ttu-id="f0ef1-110">Assurez-vous que l’argument est un nom de méthode.</span><span class="sxs-lookup"><span data-stu-id="f0ef1-110">Make sure the argument is a method name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0ef1-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0ef1-111">See Also</span></span>  
 [<span data-ttu-id="f0ef1-112">AddressOf (opérateur)</span><span class="sxs-lookup"><span data-stu-id="f0ef1-112">AddressOf Operator</span></span>](../../../visual-basic/language-reference/operators/addressof-operator.md)  
 [<span data-ttu-id="f0ef1-113">Délégués</span><span class="sxs-lookup"><span data-stu-id="f0ef1-113">Delegates</span></span>](../../../visual-basic/programming-guide/language-features/delegates/index.md)
