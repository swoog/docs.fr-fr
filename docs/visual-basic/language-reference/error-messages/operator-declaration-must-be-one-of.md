---
title: 'Déclaration d’opérateur doit être de type : +,-, *,-, -, ^, &amp;, Like, Mod et, Or, Xor, pas &lt; &lt;, &gt; &gt;, =, &lt; &gt;, &lt;, &lt;=, &gt; , &gt;=, CType, IsTrue ou IsFalse'
ms.date: 07/20/2015
f1_keywords:
- bc33000
- vbc33000
helpviewer_keywords:
- BC33000
ms.assetid: 15c5d8eb-3a8c-4141-8f41-33151afabf97
ms.openlocfilehash: eb1e7e8088ec8661be2469aff043c0f1a96e4d01
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33595018"
---
# <a name="operator-declaration-must-be-one-of----amp-like-mod-and-or-xor-not-ltlt-gtgt"></a><span data-ttu-id="b3a7c-102">Déclaration d’opérateur doit être de type : +,-, \*,\,/, ^, &amp;, Like, Mod et, Or, Xor, pas &lt; &lt;, &gt; &gt;...</span><span class="sxs-lookup"><span data-stu-id="b3a7c-102">Operator declaration must be one of:  +,-,\*,\,/,^, &amp;, Like, Mod, And, Or, Xor, Not, &lt;&lt;, &gt;&gt;...</span></span>
<span data-ttu-id="b3a7c-103">Vous pouvez déclarer uniquement un opérateur qui n’est éligible pour la surcharge.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-103">You can declare only an operator that is eligible for overloading.</span></span> <span data-ttu-id="b3a7c-104">Le tableau suivant répertorie les opérateurs que vous pouvez déclarer.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-104">The following table lists the operators you can declare.</span></span>  
  
|<span data-ttu-id="b3a7c-105">Type</span><span class="sxs-lookup"><span data-stu-id="b3a7c-105">Type</span></span>|<span data-ttu-id="b3a7c-106">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="b3a7c-106">Operators</span></span>|  
|----------|---------------|  
|<span data-ttu-id="b3a7c-107">Unaire</span><span class="sxs-lookup"><span data-stu-id="b3a7c-107">Unary</span></span>|<span data-ttu-id="b3a7c-108">`+`, `-`, `IsFalse`, `IsTrue`, `Not`</span><span class="sxs-lookup"><span data-stu-id="b3a7c-108">`+`, `-`, `IsFalse`, `IsTrue`, `Not`</span></span>|  
|<span data-ttu-id="b3a7c-109">Binaire</span><span class="sxs-lookup"><span data-stu-id="b3a7c-109">Binary</span></span>|<span data-ttu-id="b3a7c-110">`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`</span><span class="sxs-lookup"><span data-stu-id="b3a7c-110">`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`</span></span>|  
|<span data-ttu-id="b3a7c-111">Conversion (unaire)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-111">Conversion (unary)</span></span>|`CType`|  
  
 <span data-ttu-id="b3a7c-112">Notez que le `=` opérateur dans la liste binaire est l’opérateur de comparaison, pas l’opérateur d’assignation.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-112">Note that the `=` operator in the binary list is the comparison operator, not the assignment operator.</span></span>  
  
 <span data-ttu-id="b3a7c-113">**ID d’erreur :** BC33000</span><span class="sxs-lookup"><span data-stu-id="b3a7c-113">**Error ID:** BC33000</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b3a7c-114">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b3a7c-114">To correct this error</span></span>  
  
1.  <span data-ttu-id="b3a7c-115">Sélectionnez un opérateur dans le jeu d’opérateurs surchargeables.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-115">Select an operator from the set of overloadable operators.</span></span>  
  
2.  <span data-ttu-id="b3a7c-116">Si vous avez besoin des fonctionnalités de surcharge d’un opérateur que vous ne pouvez pas surcharger directement, créez une procédure `Function` qui accepte les paramètres appropriés et retourne la valeur adéquate.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-116">If you need the functionality of overloading an operator that you cannot overload directly, create a `Function` procedure that takes the appropriate parameters and returns the appropriate value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3a7c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3a7c-117">See Also</span></span>  
 [<span data-ttu-id="b3a7c-118">Operator (instruction)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-118">Operator Statement</span></span>](../../../visual-basic/language-reference/statements/operator-statement.md)  
 [<span data-ttu-id="b3a7c-119">Procédures d’opérateur</span><span class="sxs-lookup"><span data-stu-id="b3a7c-119">Operator Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)  
 [<span data-ttu-id="b3a7c-120">Guide pratique : définir un opérateur</span><span class="sxs-lookup"><span data-stu-id="b3a7c-120">How to: Define an Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)  
 [<span data-ttu-id="b3a7c-121">Guide pratique : définir un opérateur de conversion</span><span class="sxs-lookup"><span data-stu-id="b3a7c-121">How to: Define a Conversion Operator</span></span>](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)  
 [<span data-ttu-id="b3a7c-122">Function (instruction)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-122">Function Statement</span></span>](../../../visual-basic/language-reference/statements/function-statement.md)
