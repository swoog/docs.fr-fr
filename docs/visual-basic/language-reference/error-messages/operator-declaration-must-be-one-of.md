---
title: 'Déclaration d’opérateur doit être une des : +,-, *,-, -, ^, &amp;, Like, Mod et, Or, Xor, pas, <<>>,, =, <>, <, < =, >, > =, CType, IsTrue, IsFalse'
ms.date: 07/20/2015
f1_keywords:
- bc33000
- vbc33000
helpviewer_keywords:
- BC33000
ms.assetid: 15c5d8eb-3a8c-4141-8f41-33151afabf97
ms.openlocfilehash: dac8613d79e3262e4d1fd6ad1599fd01182e329b
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58819370"
---
# <a name="operator-declaration-must-be-one-of----amp-like-mod-and-or-xor-not--"></a><span data-ttu-id="0d8d3-102">Déclaration d’opérateur doit être une des : +,-, \*,\,/, ^, &amp;, Like, Mod et, Or, Xor, pas, \< \<, >>...</span><span class="sxs-lookup"><span data-stu-id="0d8d3-102">Operator declaration must be one of:  +,-,\*,\,/,^, &amp;, Like, Mod, And, Or, Xor, Not, \<\<, >>...</span></span>
<span data-ttu-id="0d8d3-103">Vous pouvez déclarer uniquement un opérateur qui est éligible pour la surcharge.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-103">You can declare only an operator that is eligible for overloading.</span></span> <span data-ttu-id="0d8d3-104">Le tableau suivant répertorie les opérateurs que vous pouvez déclarer.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-104">The following table lists the operators you can declare.</span></span>  
  
|<span data-ttu-id="0d8d3-105">Type</span><span class="sxs-lookup"><span data-stu-id="0d8d3-105">Type</span></span>|<span data-ttu-id="0d8d3-106">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="0d8d3-106">Operators</span></span>|  
|----------|---------------|  
|<span data-ttu-id="0d8d3-107">Unaire</span><span class="sxs-lookup"><span data-stu-id="0d8d3-107">Unary</span></span>|<span data-ttu-id="0d8d3-108">`+`, `-`, `IsFalse`, `IsTrue`, `Not`</span><span class="sxs-lookup"><span data-stu-id="0d8d3-108">`+`, `-`, `IsFalse`, `IsTrue`, `Not`</span></span>|  
|<span data-ttu-id="0d8d3-109">Binaire</span><span class="sxs-lookup"><span data-stu-id="0d8d3-109">Binary</span></span>|<span data-ttu-id="0d8d3-110">`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`</span><span class="sxs-lookup"><span data-stu-id="0d8d3-110">`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`</span></span>|  
|<span data-ttu-id="0d8d3-111">Conversion (unaire)</span><span class="sxs-lookup"><span data-stu-id="0d8d3-111">Conversion (unary)</span></span>|`CType`|  
  
 <span data-ttu-id="0d8d3-112">Notez que le `=` opérateur dans la liste binaire est l’opérateur de comparaison, pas l’opérateur d’assignation.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-112">Note that the `=` operator in the binary list is the comparison operator, not the assignment operator.</span></span>  
  
 <span data-ttu-id="0d8d3-113">**ID d’erreur :** BC33000</span><span class="sxs-lookup"><span data-stu-id="0d8d3-113">**Error ID:** BC33000</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="0d8d3-114">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="0d8d3-114">To correct this error</span></span>  
  
1.  <span data-ttu-id="0d8d3-115">Sélectionnez un opérateur dans le jeu d’opérateurs surchargeables.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-115">Select an operator from the set of overloadable operators.</span></span>  
  
2.  <span data-ttu-id="0d8d3-116">Si vous avez besoin des fonctionnalités de surcharge d’un opérateur que vous ne pouvez pas surcharger directement, créez une procédure `Function` qui accepte les paramètres appropriés et retourne la valeur adéquate.</span><span class="sxs-lookup"><span data-stu-id="0d8d3-116">If you need the functionality of overloading an operator that you cannot overload directly, create a `Function` procedure that takes the appropriate parameters and returns the appropriate value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d8d3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d8d3-117">See also</span></span>

- [<span data-ttu-id="0d8d3-118">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="0d8d3-118">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)
- [<span data-ttu-id="0d8d3-119">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="0d8d3-119">Operator Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)
- [<span data-ttu-id="0d8d3-120">Guide pratique pour Définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="0d8d3-120">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [<span data-ttu-id="0d8d3-121">Guide pratique pour Définir un opérateur de Conversion</span><span class="sxs-lookup"><span data-stu-id="0d8d3-121">How to: Define a Conversion Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [<span data-ttu-id="0d8d3-122">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="0d8d3-122">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
