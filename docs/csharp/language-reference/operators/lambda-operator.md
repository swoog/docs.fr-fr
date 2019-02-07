---
title: =>, opérateur - Référence C#
ms.custom: seodec18
ms.date: 01/22/2019
f1_keywords:
- =>_CSharpKeyword
helpviewer_keywords:
- lambda operator [C#]
- => operator [C#]
- lambda expressions [C#], => operator
ms.openlocfilehash: 0cded9d23d67e6afc8b01d6711e42759b4b51fab
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55275858"
---
# <a name="-operator-c-reference"></a><span data-ttu-id="7a278-102">=>, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="7a278-102">=> operator (C# Reference)</span></span>

<span data-ttu-id="7a278-103">Le jeton `=>` est pris en charge sous deux formes : comme opérateur lambda, et comme séparateur d’un nom de membre et de l’implémentation de membre dans une définition de corps d’expression.</span><span class="sxs-lookup"><span data-stu-id="7a278-103">The `=>` token is supported in two forms: as the lambda operator and as a separator of a member name and the member implementation in an expression body definition.</span></span>

## <a name="lambda-operator"></a><span data-ttu-id="7a278-104">Opérateur lamdba</span><span class="sxs-lookup"><span data-stu-id="7a278-104">Lambda operator</span></span>

<span data-ttu-id="7a278-105">Dans les [expressions lambda](../../programming-guide/statements-expressions-operators/lambda-expressions.md), l’opérateur lambda `=>` sépare les variables d’entrée du côté gauche et le corps lambda du côté droit.</span><span class="sxs-lookup"><span data-stu-id="7a278-105">In [lambda expressions](../../programming-guide/statements-expressions-operators/lambda-expressions.md), the lambda operator `=>` separates the input variables on the left side from the lambda body on the right side.</span></span>

<span data-ttu-id="7a278-106">L’exemple suivant utilise la fonctionnalité [LINQ](../../programming-guide/concepts/linq/index.md) avec la syntaxe de méthode pour illustrer l’utilisation d’expressions lambda :</span><span class="sxs-lookup"><span data-stu-id="7a278-106">The following example uses the [LINQ](../../programming-guide/concepts/linq/index.md) feature with method syntax to demonstrate the usage of lambda expressions:</span></span>

[!code-csharp-interactive[infer types of input variables](~/samples/snippets/csharp/language-reference/operators/LambdaOperatorExamples.cs#InferredTypes)]

<span data-ttu-id="7a278-107">Les variables d’entrée des expressions lambda sont fortement typées au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="7a278-107">Input variables of lambda expressions are strongly typed at compile time.</span></span> <span data-ttu-id="7a278-108">Quand le compilateur peut déduire les types des variables d’entrée, comme dans l’exemple précédent, vous pouvez omettre les déclarations de type.</span><span class="sxs-lookup"><span data-stu-id="7a278-108">When the compiler can infer the types of input variables, like in the preceding example, you may omit type declarations.</span></span> <span data-ttu-id="7a278-109">Si vous avez besoin de spécifier le type des variables d’entrée, vous devez le faire pour chaque variable, comme le montre l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="7a278-109">If you need to specify the type of input variables, you must do that for each variable, as the following example shows:</span></span>

[!code-csharp-interactive[specify types of input variables](~/samples/snippets/csharp/language-reference/operators/LambdaOperatorExamples.cs#ExplicitTypes)]

<span data-ttu-id="7a278-110">L’exemple suivant illustre comment définir une expression lambda sans variable d’entrée :</span><span class="sxs-lookup"><span data-stu-id="7a278-110">The following example shows how to define a lambda expression without input variables:</span></span>

[!code-csharp-interactive[without input variables](~/samples/snippets/csharp/language-reference/operators/LambdaOperatorExamples.cs#WithoutInput)]

<span data-ttu-id="7a278-111">Pour plus d’informations, consultez [Expressions lambda](../../programming-guide/statements-expressions-operators/lambda-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="7a278-111">For more information, see [Lambda expressions](../../programming-guide/statements-expressions-operators/lambda-expressions.md).</span></span>

## <a name="expression-body-definition"></a><span data-ttu-id="7a278-112">Définition de corps d’expression</span><span class="sxs-lookup"><span data-stu-id="7a278-112">Expression body definition</span></span>

<span data-ttu-id="7a278-113">La syntaxe générale d’une définition de corps d’expression est la suivante :</span><span class="sxs-lookup"><span data-stu-id="7a278-113">An expression body definition has the following general syntax:</span></span>

```csharp
member => expression;
```

<span data-ttu-id="7a278-114">où *expression* est une expression valide.</span><span class="sxs-lookup"><span data-stu-id="7a278-114">where *expression* is a valid expression.</span></span> <span data-ttu-id="7a278-115">Notez que *expression* peut être une *expression d’instruction* seulement si le type de retour du membre est `void`, ou si le membre est un constructeur, un finaliseur ou un accesseur de propriété `set`.</span><span class="sxs-lookup"><span data-stu-id="7a278-115">Note that *expression* can be a *statement expression* only if the member's return type is `void`, or if the member is a constructor, a finalizer, or a property `set` accessor.</span></span>

<span data-ttu-id="7a278-116">L’exemple suivant montre une définition de corps d’expression pour une méthode `Person.ToString` :</span><span class="sxs-lookup"><span data-stu-id="7a278-116">The following example shows an expression body definition for a `Person.ToString` method:</span></span>

```csharp
public override string ToString() => $"{fname} {lname}".Trim();
```

<span data-ttu-id="7a278-117">Il s’agit d’une version raccourcie de la définition de méthode suivante :</span><span class="sxs-lookup"><span data-stu-id="7a278-117">It's a shorthand version of the following method definition:</span></span>

```csharp
public override string ToString()
{
   return $"{fname} {lname}".Trim();
}
```

<span data-ttu-id="7a278-118">Les définitions de corps d’expression pour les méthodes et les propriétés en lecture seule sont prises en charge à compter de C# 6.</span><span class="sxs-lookup"><span data-stu-id="7a278-118">Expression body definitions for methods and read-only properties are supported starting with C# 6.</span></span> <span data-ttu-id="7a278-119">Les définitions de corps d’expression pour les constructeurs, les finaliseurs, les accesseurs de propriétés et les indexeurs sont prises en charge à compter de C# 7.0.</span><span class="sxs-lookup"><span data-stu-id="7a278-119">Expression body definitions for constructors, finalizers, property accessors, and indexers are supported starting with C# 7.0.</span></span>

<span data-ttu-id="7a278-120">Pour plus d’informations, consultez [Membres expression-bodied](../../programming-guide/statements-expressions-operators/expression-bodied-members.md).</span><span class="sxs-lookup"><span data-stu-id="7a278-120">For more information, see [Expression-bodied members](../../programming-guide/statements-expressions-operators/expression-bodied-members.md).</span></span>

## <a name="operator-overloadability"></a><span data-ttu-id="7a278-121">Capacité de surcharge de l’opérateur</span><span class="sxs-lookup"><span data-stu-id="7a278-121">Operator overloadability</span></span>

<span data-ttu-id="7a278-122">L’opérateur `=>` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="7a278-122">The `=>` operator cannot be overloaded.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="7a278-123">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="7a278-123">C# language specification</span></span>

<span data-ttu-id="7a278-124">Pour plus d’informations, consultez la section [Expressions de fonction anonyme](~/_csharplang/spec/expressions.md#anonymous-function-expressions) de la [spécification du langage C#](../language-specification/index.md).</span><span class="sxs-lookup"><span data-stu-id="7a278-124">For more information, see the [Anonymous function expressions](~/_csharplang/spec/expressions.md#anonymous-function-expressions) section of the [C# language specification](../language-specification/index.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7a278-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a278-125">See also</span></span>

- [<span data-ttu-id="7a278-126">Référence C#</span><span class="sxs-lookup"><span data-stu-id="7a278-126">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="7a278-127">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="7a278-127">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="7a278-128">Opérateurs C#</span><span class="sxs-lookup"><span data-stu-id="7a278-128">C# Operators</span></span>](index.md)
- [<span data-ttu-id="7a278-129">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="7a278-129">Lambda expressions</span></span>](../../programming-guide/statements-expressions-operators/lambda-expressions.md)
- [<span data-ttu-id="7a278-130">Membres expression-bodied</span><span class="sxs-lookup"><span data-stu-id="7a278-130">Expression-bodied members</span></span>](../../programming-guide/statements-expressions-operators/expression-bodied-members.md)