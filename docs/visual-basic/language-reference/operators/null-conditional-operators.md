---
title: Opérateurs conditionnels null (Visual Basic)
ms.date: 10/19/2018
helpviewer_keywords:
- null-conditional operators [Visual Basic]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.openlocfilehash: c29362a1e335e18b66821919e266b1ce57774692
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195990"
---
# <a name="-and--null-conditional-operators-visual-basic"></a><span data-ttu-id="59857-102">?.</span><span class="sxs-lookup"><span data-stu-id="59857-102">?.</span></span> <span data-ttu-id="59857-103">et ? opérateurs de condition null () (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="59857-103">and ?() null-conditional operators (Visual Basic)</span></span>

<span data-ttu-id="59857-104">Teste la valeur de l’opérande de gauche pour la valeur null (`Nothing`) avant d’effectuer un accès au membre (`?.`) ou d’un index (`?()`) de l’opération ; retourne `Nothing` si l’opérande de gauche a la valeur `Nothing`.</span><span class="sxs-lookup"><span data-stu-id="59857-104">Tests the value of the left-hand operand for null (`Nothing`) before performing a member access (`?.`) or index (`?()`) operation; returns `Nothing` if the left-hand operand evaluates to `Nothing`.</span></span> <span data-ttu-id="59857-105">Notez que, dans les expressions qui renverrait habituellement des types valeur, l’opérateur conditionnel null renvoie un <xref:System.Nullable%601>.</span><span class="sxs-lookup"><span data-stu-id="59857-105">Note that, in the expressions that would ordinarily return value types, the null-conditional operator returns a <xref:System.Nullable%601>.</span></span>

<span data-ttu-id="59857-106">Ces opérateurs permettent d’écrire moins de code pour gérer les vérifications « null », en particulier lors de la descente dans les structures de données.</span><span class="sxs-lookup"><span data-stu-id="59857-106">These operators help you write less code to handle null checks, especially when descending into data structures.</span></span> <span data-ttu-id="59857-107">Exemple :</span><span class="sxs-lookup"><span data-stu-id="59857-107">For example:</span></span>

```vb
Dim length As Integer? = customers?.Length  ' Nothing if customers is Nothing  
Dim first As Customer = customers?(0)  ' Nothing if customers is Nothing  
Dim count As Integer? = customers?(0)?.Orders?.Count()  ' Nothing if customers, the first customer, or Orders is Nothing  
```

<span data-ttu-id="59857-108">Pour la comparaison, le code de remplacement pour la première de ces expressions sans opérateur conditionnel null est :</span><span class="sxs-lookup"><span data-stu-id="59857-108">For comparison, the alternative code for the first of these expressions without a null-conditional operator is:</span></span>

```vb
Dim length As Integer
If customers IsNot Nothing Then
   length = customers.Length
End If
```

<span data-ttu-id="59857-109">Les opérateurs conditionnels Null ont un effet de court-circuit.</span><span class="sxs-lookup"><span data-stu-id="59857-109">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="59857-110">Si une opération dans une chaîne d’opérations d’accès et des index membre conditionnel ne retourne rien, le reste de l’exécution de la chaîne s’arrête.</span><span class="sxs-lookup"><span data-stu-id="59857-110">If one operation in a chain of conditional member access and index operations returns Nothing, the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="59857-111">Dans l’exemple suivant, c (e) n’est pas évaluée si `A`, `B`, ou `C` a la valeur Nothing.</span><span class="sxs-lookup"><span data-stu-id="59857-111">In the following example, C(E) isn't evaluated if `A`, `B`, or `C` evaluates to Nothing.</span></span>

```vb
A?.B?.C?(E);
```

<span data-ttu-id="59857-112">Utilisez un autre pour l’accès aux membres conditionnels null consiste à appeler des délégués de façon thread-safe avec beaucoup moins de code.</span><span class="sxs-lookup"><span data-stu-id="59857-112">Another use for null-conditional member access is to invoke delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="59857-113">Avec l'ancienne méthode, vous deviez utiliser un code similaire au suivant :</span><span class="sxs-lookup"><span data-stu-id="59857-113">The old way requires code like the following:</span></span>  

```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```

<span data-ttu-id="59857-114">La nouvelle méthode est beaucoup plus simple :</span><span class="sxs-lookup"><span data-stu-id="59857-114">The new way is much simpler:</span></span>  

```vb
PropertyChanged?.Invoke(…)
```

<span data-ttu-id="59857-115">La nouvelle méthode est thread-safe, car le compilateur génère du code qui évalue `PropertyChanged` une seule fois, en conservant le résultat dans une variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="59857-115">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="59857-116">Vous devez explicitement appeler la méthode `Invoke`, car il n'existe pas de syntaxe d'appel de délégué conditionnel Null `PropertyChanged?(e)`.</span><span class="sxs-lookup"><span data-stu-id="59857-116">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>  

## <a name="see-also"></a><span data-ttu-id="59857-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59857-117">See also</span></span>

- [<span data-ttu-id="59857-118">Opérateurs (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="59857-118">Operators (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="59857-119">Guide de programmation Visual Basic</span><span class="sxs-lookup"><span data-stu-id="59857-119">Visual Basic Programming Guide</span></span>](../../../visual-basic/programming-guide/index.md)
- [<span data-ttu-id="59857-120">Informations de référence sur le langage Visual Basic</span><span class="sxs-lookup"><span data-stu-id="59857-120">Visual Basic Language Reference</span></span>](../../../visual-basic/language-reference/index.md)  
