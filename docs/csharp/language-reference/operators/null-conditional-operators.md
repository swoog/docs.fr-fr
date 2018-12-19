---
title: Opérateurs conditionnels Null - Référence C#
ms.custom: seodec18
ms.date: 04/03/2015
helpviewer_keywords:
- null-conditional operators [C#]
- ?. operator [C#]
- ?[] operator [C#]
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
ms.openlocfilehash: 4189b07fd280192a4cb39400e4e77cef702c9d08
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239551"
---
# <a name="-and--null-conditional-operators-c-and-visual-basic"></a><span data-ttu-id="c92e5-102">?.</span><span class="sxs-lookup"><span data-stu-id="c92e5-102">?.</span></span> <span data-ttu-id="c92e5-103">et ?[] (C# et Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="c92e5-103">and ?[] null-conditional Operators (C# and Visual Basic)</span></span>
<span data-ttu-id="c92e5-104">Teste si l’opérande de gauche a une valeur Null avant d’effectuer une opération d’accès au membre (`?.`) ou d’index (`?[]`) ; retourne `null` si l’opérande de gauche s’évalue à `null`.</span><span class="sxs-lookup"><span data-stu-id="c92e5-104">Tests the value of the left-hand operand for null before performing a member access (`?.`) or index (`?[]`) operation; returns `null` if the left-hand operand evaluates to `null`.</span></span> 

<span data-ttu-id="c92e5-105">Ces opérateurs permettent d’écrire moins de code pour gérer les vérifications Null, notamment pour l’exploration des structures de données.</span><span class="sxs-lookup"><span data-stu-id="c92e5-105">These operators help you write less code to handle null checks, especially for descending into data structures.</span></span>  
  
```csharp  
int? length = customers?.Length; // null if customers is null   
Customer first = customers?[0];  // null if customers is null  
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null  
```  
  
 <span data-ttu-id="c92e5-106">Les opérateurs conditionnels Null ont un effet de court-circuit.</span><span class="sxs-lookup"><span data-stu-id="c92e5-106">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="c92e5-107">Si une opération dans une chaîne d'opérations d'accès au membre et d'indexation conditionnelles retourne une valeur Null, l'exécution du reste de la chaîne s'arrête.</span><span class="sxs-lookup"><span data-stu-id="c92e5-107">If one operation in a chain of conditional member access and index operations returns null, the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="c92e5-108">Dans l’exemple ci-dessous, `E` ne s’exécute pas si `A`, `B` ou `C` a une valeur Null.</span><span class="sxs-lookup"><span data-stu-id="c92e5-108">In the following example, `E` doesn't execute if `A`, `B`, or `C` evaluates to null.</span></span>
  
```csharp
A?.B?.C?.Do(E);
A?.B?.C?[E];
```

 <span data-ttu-id="c92e5-109">L’accès au membre conditionnel Null s’utilise également pour appeler des délégués de façon thread-safe, avec beaucoup moins de code.</span><span class="sxs-lookup"><span data-stu-id="c92e5-109">Another use for the null-conditional member access is invoking delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="c92e5-110">Avec l'ancienne méthode, vous deviez utiliser un code similaire au suivant :</span><span class="sxs-lookup"><span data-stu-id="c92e5-110">The old way requires code like the following:</span></span>  
  
```csharp  
var handler = this.PropertyChanged;  
if (handler != null)  
    handler(…);
```  
  
  
 <span data-ttu-id="c92e5-111">La nouvelle méthode est beaucoup plus simple :</span><span class="sxs-lookup"><span data-stu-id="c92e5-111">The new way is much simpler:</span></span>  
  
```csharp
PropertyChanged?.Invoke(…)  
```  

 <span data-ttu-id="c92e5-112">La nouvelle méthode est thread-safe, car le compilateur génère du code qui évalue `PropertyChanged` une seule fois, en conservant le résultat dans une variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="c92e5-112">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="c92e5-113">Vous devez explicitement appeler la méthode `Invoke`, car il n'existe pas de syntaxe d'appel de délégué conditionnel Null `PropertyChanged?(e)`.</span><span class="sxs-lookup"><span data-stu-id="c92e5-113">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>  
  
## <a name="language-specifications"></a><span data-ttu-id="c92e5-114">Spécifications du langage</span><span class="sxs-lookup"><span data-stu-id="c92e5-114">Language Specifications</span></span>  

<span data-ttu-id="c92e5-115">Pour plus d’informations, consultez [Opérateur de condition Null](~/_csharplang/spec/expressions.md#null-conditional-operator) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="c92e5-115">For more information, see [Null-conditional operator](~/_csharplang/spec/expressions.md#null-conditional-operator) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="c92e5-116">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="c92e5-116">The language specification is the definitive source for C# syntax and usage.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c92e5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c92e5-117">See Also</span></span>

- [<span data-ttu-id="c92e5-118">?? (opérateur de fusion Null)</span><span class="sxs-lookup"><span data-stu-id="c92e5-118">?? (null-coalescing operator)</span></span>](null-coalescing-operator.md)  
- [<span data-ttu-id="c92e5-119">Référence C#</span><span class="sxs-lookup"><span data-stu-id="c92e5-119">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="c92e5-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="c92e5-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
