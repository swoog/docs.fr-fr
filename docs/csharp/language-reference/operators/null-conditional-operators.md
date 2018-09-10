---
title: Opérateurs conditionnels Null (C# et Visual Basic)
ms.date: 04/03/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- null-conditional operators [C#]
- null-conditional operators [Visual Basic]
- ?. operator [C#]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
ms.openlocfilehash: f00d5e489931d9c1172a21ee5f0d3e3d0a6f4a4e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44192809"
---
# <a name="-and--null-conditional-operators-c-and-visual-basic"></a><span data-ttu-id="357a3-102">?.</span><span class="sxs-lookup"><span data-stu-id="357a3-102">?.</span></span> <span data-ttu-id="357a3-103">et ?[] (C# et Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="357a3-103">and ?[] null-conditional Operators (C# and Visual Basic)</span></span>
<span data-ttu-id="357a3-104">Teste si l’opérande de gauche a une valeur Null avant d’effectuer une opération d’accès au membre (`?.`) ou d’index (`?[]`) ; retourne `null` si l’opérande de gauche s’évalue à `null`.</span><span class="sxs-lookup"><span data-stu-id="357a3-104">Tests the value of the left-hand operand for null before performing a member access (`?.`) or index (`?[]`) operation; returns `null` if the left-hand operand evaluates to `null`.</span></span> 

<span data-ttu-id="357a3-105">Ces opérateurs permettent d’écrire moins de code pour gérer les vérifications Null, notamment pour l’exploration des structures de données.</span><span class="sxs-lookup"><span data-stu-id="357a3-105">These operators help you write less code to handle null checks, especially for descending into data structures.</span></span>  
  
```csharp  
int? length = customers?.Length; // null if customers is null   
Customer first = customers?[0];  // null if customers is null  
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null  
```  
  
```vb  
Dim length = customers?.Length  ' null if customers is null  
Dim first as Customer = customers?(0)  ' null if customers is null  
Dim count as Integer? = customers?(0)?.Orders?.Count()  ' null if customers, the first customer, or Orders is null  
```  
  
 <span data-ttu-id="357a3-106">Les opérateurs conditionnels Null ont un effet de court-circuit.</span><span class="sxs-lookup"><span data-stu-id="357a3-106">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="357a3-107">Si une opération dans une chaîne d'opérations d'accès au membre et d'indexation conditionnelles retourne une valeur Null, l'exécution du reste de la chaîne s'arrête.</span><span class="sxs-lookup"><span data-stu-id="357a3-107">If one operation in a chain of conditional member access and index operation returns null, then the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="357a3-108">Dans l’exemple ci-dessous, `E` ne s’exécute pas si `A`, `B` ou `C` a une valeur Null.</span><span class="sxs-lookup"><span data-stu-id="357a3-108">In the following example, `E` doesn't execute if `A`, `B`, or `C` evaluates to null.</span></span>
  
```csharp
A?.B?.C?.Do(E);
A?.B?.C?[E];
```

```vb
A?.B?.C?.Do(E);
A?.B?.C?(E);
```  
  
 <span data-ttu-id="357a3-109">L’accès au membre conditionnel Null s’utilise également pour appeler des délégués de façon thread-safe, avec beaucoup moins de code.</span><span class="sxs-lookup"><span data-stu-id="357a3-109">Another use for the null-conditional member access is invoking delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="357a3-110">Avec l'ancienne méthode, vous deviez utiliser un code similaire au suivant :</span><span class="sxs-lookup"><span data-stu-id="357a3-110">The old way requires code like the following:</span></span>  
  
```csharp  
var handler = this.PropertyChanged;  
if (handler != null)  
    handler(…);
```  
  
```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```  
  
 <span data-ttu-id="357a3-111">La nouvelle méthode est beaucoup plus simple :</span><span class="sxs-lookup"><span data-stu-id="357a3-111">The new way is much simpler:</span></span>  
  
```csharp
PropertyChanged?.Invoke(…)  
```  

```vb
PropertyChanged?.Invoke(…)
```  
  
 <span data-ttu-id="357a3-112">La nouvelle méthode est thread-safe, car le compilateur génère du code qui évalue `PropertyChanged` une seule fois, en conservant le résultat dans une variable temporaire.</span><span class="sxs-lookup"><span data-stu-id="357a3-112">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="357a3-113">Vous devez explicitement appeler la méthode `Invoke`, car il n'existe pas de syntaxe d'appel de délégué conditionnel Null `PropertyChanged?(e)`.</span><span class="sxs-lookup"><span data-stu-id="357a3-113">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>  
  
## <a name="language-specifications"></a><span data-ttu-id="357a3-114">Spécifications du langage</span><span class="sxs-lookup"><span data-stu-id="357a3-114">Language Specifications</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
 <span data-ttu-id="357a3-115">Pour plus d’informations, consultez [Informations de référence sur le langage Visual Basic](../../../visual-basic/language-reference/index.md).</span><span class="sxs-lookup"><span data-stu-id="357a3-115">For more information, see the [Visual Basic Language Reference](../../../visual-basic/language-reference/index.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="357a3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="357a3-116">See Also</span></span>

- [<span data-ttu-id="357a3-117">?? (opérateur de fusion Null)</span><span class="sxs-lookup"><span data-stu-id="357a3-117">?? (null-coalescing operator)</span></span>](null-coalescing-operator.md)  
- [<span data-ttu-id="357a3-118">Référence C#</span><span class="sxs-lookup"><span data-stu-id="357a3-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="357a3-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="357a3-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="357a3-120">Guide de programmation Visual Basic</span><span class="sxs-lookup"><span data-stu-id="357a3-120">Visual Basic Programming Guide</span></span>](../../../visual-basic/programming-guide/index.md)
