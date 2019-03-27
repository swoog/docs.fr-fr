---
title: Opérateurs conditionnels Null - Référence C#
ms.custom: seodec18
ms.date: 04/03/2015
helpviewer_keywords:
- null-conditional operators [C#]
- ?. operator [C#]
- ?[] operator [C#]
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
ms.openlocfilehash: 9cbf8a0f860f0bc0328cd98e558b20b5e8e1bf8f
ms.sourcegitcommit: 344d82456f27d09a210671214a14cfd7daf1f97c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2019
ms.locfileid: "58348841"
---
# <a name="-and--null-conditional-operators-c-reference"></a><span data-ttu-id="0d11b-102">?.</span><span class="sxs-lookup"><span data-stu-id="0d11b-102">?.</span></span> <span data-ttu-id="0d11b-103">et ?[] - Opérateurs conditionnels Null - (Référence C#)</span><span class="sxs-lookup"><span data-stu-id="0d11b-103">and ?[] null-conditional operators (C# Reference)</span></span>

<span data-ttu-id="0d11b-104">Teste si l’opérande de gauche a une valeur Null avant d’effectuer une opération d’accès au membre (`?.`) ou d’index (`?[]`) ; retourne `null` si l’opérande de gauche s’évalue à `null`.</span><span class="sxs-lookup"><span data-stu-id="0d11b-104">Tests the value of the left-hand operand for null before performing a member access (`?.`) or index (`?[]`) operation; returns `null` if the left-hand operand evaluates to `null`.</span></span>

<span data-ttu-id="0d11b-105">Ces opérateurs permettent d’écrire moins de code pour gérer les vérifications Null, notamment pour l’exploration des structures de données.</span><span class="sxs-lookup"><span data-stu-id="0d11b-105">These operators help you write less code to handle null checks, especially for descending into data structures.</span></span>

```csharp
int? length = customers?.Length; // null if customers is null
Customer first = customers?[0];  // null if customers is null
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null
```

<span data-ttu-id="0d11b-106">Les opérateurs conditionnels Null ont un effet de court-circuit.</span><span class="sxs-lookup"><span data-stu-id="0d11b-106">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="0d11b-107">Si une opération dans une chaîne d'opérations d'accès au membre et d'indexation conditionnelles retourne une valeur Null, l'exécution du reste de la chaîne s'arrête.</span><span class="sxs-lookup"><span data-stu-id="0d11b-107">If one operation in a chain of conditional member access and index operations returns null, the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="0d11b-108">Dans l’exemple ci-dessous, `E` ne s’exécute pas si `A`, `B` ou `C` a une valeur Null.</span><span class="sxs-lookup"><span data-stu-id="0d11b-108">In the following example, `E` doesn't execute if `A`, `B`, or `C` evaluates to null.</span></span>

```csharp
A?.B?.C?.Do(E);
A?.B?.C?[E];
```

<span data-ttu-id="0d11b-109">L’accès au membre conditionnel Null s’utilise également pour appeler des délégués de façon thread-safe, avec beaucoup moins de code.</span><span class="sxs-lookup"><span data-stu-id="0d11b-109">Another use for the null-conditional member access is invoking delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="0d11b-110">Avec l'ancienne méthode, vous deviez utiliser un code similaire au suivant :</span><span class="sxs-lookup"><span data-stu-id="0d11b-110">The old way requires code like the following:</span></span>

```csharp
var handler = this.PropertyChanged;
if (handler != null)
    handler(…);
```

<span data-ttu-id="0d11b-111">La nouvelle méthode est beaucoup plus simple :</span><span class="sxs-lookup"><span data-stu-id="0d11b-111">The new way is much simpler:</span></span>

```csharp
PropertyChanged?.Invoke(…)
```

<span data-ttu-id="0d11b-112">La nouvelle méthode est thread-safe, car le compilateur génère du code qui évalue `PropertyChanged` une seule fois, en conservant le résultat dans une variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="0d11b-112">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="0d11b-113">Vous devez explicitement appeler la méthode `Invoke`, car il n'existe pas de syntaxe d'appel de délégué conditionnel Null `PropertyChanged?(e)`.</span><span class="sxs-lookup"><span data-stu-id="0d11b-113">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>

## <a name="language-specifications"></a><span data-ttu-id="0d11b-114">Spécifications du langage</span><span class="sxs-lookup"><span data-stu-id="0d11b-114">Language specifications</span></span>

<span data-ttu-id="0d11b-115">Pour plus d’informations, consultez [Opérateur de condition Null](~/_csharplang/spec/expressions.md#null-conditional-operator) dans la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="0d11b-115">For more information, see [Null-conditional operator](~/_csharplang/spec/expressions.md#null-conditional-operator) in the [C# Language Specification](../language-specification/index.md).</span></span> <span data-ttu-id="0d11b-116">La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.</span><span class="sxs-lookup"><span data-stu-id="0d11b-116">The language specification is the definitive source for C# syntax and usage.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d11b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d11b-117">See also</span></span>

- [<span data-ttu-id="0d11b-118">?? (opérateur de fusion Null)</span><span class="sxs-lookup"><span data-stu-id="0d11b-118">?? (null-coalescing operator)</span></span>](null-coalescing-operator.md)
- [<span data-ttu-id="0d11b-119">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0d11b-119">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="0d11b-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0d11b-120">C# Programming Guide</span></span>](../../programming-guide/index.md)