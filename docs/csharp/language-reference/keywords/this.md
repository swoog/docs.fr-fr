---
title: this (référence C#)
description: this, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- this
- this_CSharpKeyword
helpviewer_keywords:
- this keyword [C#]
ms.assetid: d4f827fe-4710-410b-89b8-867dad44b8a3
ms.openlocfilehash: df1bf6a3e6d24b231bf5e3c7a960f49084c4e53a
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2018
ms.locfileid: "46577358"
---
# <a name="this-c-reference"></a><span data-ttu-id="f25a5-103">this (référence C#)</span><span class="sxs-lookup"><span data-stu-id="f25a5-103">this (C# Reference)</span></span>
<span data-ttu-id="f25a5-104">Le mot clé `this` fait référence à l’instance actuelle de la classe et est également utilisé comme modificateur du premier paramètre d’une méthode d’extension.</span><span class="sxs-lookup"><span data-stu-id="f25a5-104">The `this` keyword refers to the current instance of the class and is also used as a modifier of the first parameter of an extension method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f25a5-105">Cet article traite de l’utilisation de `this` avec des instances de classe.</span><span class="sxs-lookup"><span data-stu-id="f25a5-105">This article discusses the use of `this` with class instances.</span></span> <span data-ttu-id="f25a5-106">Pour plus d’informations sur son utilisation dans les méthodes d’extension, consultez [Méthodes d’extension](../../../csharp/programming-guide/classes-and-structs/extension-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f25a5-106">For more information about its use in extension methods, see [Extension Methods](../../../csharp/programming-guide/classes-and-structs/extension-methods.md).</span></span>  
  
 <span data-ttu-id="f25a5-107">Voici quelques utilisations courantes de `this` :</span><span class="sxs-lookup"><span data-stu-id="f25a5-107">The following are common uses of `this`:</span></span>  
  
-   <span data-ttu-id="f25a5-108">Pour qualifier des membres masqués par des noms similaires, par exemple :</span><span class="sxs-lookup"><span data-stu-id="f25a5-108">To qualify members hidden by similar names, for example:</span></span>  
  
 [!code-csharp[csrefKeywordsAccess#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_1.cs)]  
  
-   <span data-ttu-id="f25a5-109">Pour passer un objet comme paramètre à d’autres méthodes, par exemple :</span><span class="sxs-lookup"><span data-stu-id="f25a5-109">To pass an object as a parameter to other methods, for example:</span></span>  
  
    ```csharp  
    CalcTax(this);  
    ```  
  
-   <span data-ttu-id="f25a5-110">Pour déclarer des indexeurs, par exemple :</span><span class="sxs-lookup"><span data-stu-id="f25a5-110">To declare indexers, for example:</span></span>  
  
 [!code-csharp[csrefKeywordsAccess#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_2.cs)]  
  
 <span data-ttu-id="f25a5-111">Les fonctions membres statiques, car ils existent au niveau de la classe et non comme faisant partie d’un objet, n’ont pas de pointeur `this`.</span><span class="sxs-lookup"><span data-stu-id="f25a5-111">Static member functions, because they exist at the class level and not as part of an object, do not have a `this` pointer.</span></span> <span data-ttu-id="f25a5-112">Une erreur consiste à faire référence à `this` dans une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="f25a5-112">It is an error to refer to `this` in a static method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f25a5-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="f25a5-113">Example</span></span>  
 <span data-ttu-id="f25a5-114">Dans cet exemple, `this` est utilisé pour qualifier les membres de la classe `Employee`, `name` et `alias`, qui sont masqués par des noms similaires.</span><span class="sxs-lookup"><span data-stu-id="f25a5-114">In this example, `this` is used to qualify the `Employee` class members, `name` and `alias`, which are hidden by similar names.</span></span> <span data-ttu-id="f25a5-115">Il est également utilisé pour passer un objet à la méthode `CalcTax`, qui appartient à une autre classe.</span><span class="sxs-lookup"><span data-stu-id="f25a5-115">It is also used to pass an object to the method `CalcTax`, which belongs to another class.</span></span>  
  
 [!code-csharp[csrefKeywordsAccess#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/this_3.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="f25a5-116">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="f25a5-116">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f25a5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f25a5-117">See Also</span></span>

- [<span data-ttu-id="f25a5-118">Référence C#</span><span class="sxs-lookup"><span data-stu-id="f25a5-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="f25a5-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f25a5-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="f25a5-120">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="f25a5-120">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
- [<span data-ttu-id="f25a5-121">base</span><span class="sxs-lookup"><span data-stu-id="f25a5-121">base</span></span>](../../../csharp/language-reference/keywords/base.md)  
- [<span data-ttu-id="f25a5-122">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f25a5-122">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)
