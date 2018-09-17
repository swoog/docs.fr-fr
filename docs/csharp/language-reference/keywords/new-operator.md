---
title: new, opérateur (référence C#)
ms.date: 03/15/2018
helpviewer_keywords:
- new operator keyword [C#]
ms.assetid: a212b697-a79b-4105-9923-1f7b108036e8
ms.openlocfilehash: 362217b247bd2ab7a2eec2f86cbaaf1a0652a3ad
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45519407"
---
# <a name="new-operator-c-reference"></a><span data-ttu-id="9c44c-102">new, opérateur (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9c44c-102">new operator (C# Reference)</span></span>

<span data-ttu-id="9c44c-103">Cet opérateur s’utilise pour créer des objets et appeler des constructeurs.</span><span class="sxs-lookup"><span data-stu-id="9c44c-103">Used to create objects and invoke constructors.</span></span> <span data-ttu-id="9c44c-104">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9c44c-104">For example:</span></span>

```csharp
Class1 obj  = new Class1();
```

<span data-ttu-id="9c44c-105">Il est également utilisé pour créer des instances de types anonymes :</span><span class="sxs-lookup"><span data-stu-id="9c44c-105">It is also used to create instances of anonymous types:</span></span>

```csharp
var query = from cust in customers
            select new { Name = cust.Name, Address = cust.PrimaryAddress };
```

<span data-ttu-id="9c44c-106">L’opérateur `new` est aussi utilisé pour appeler le constructeur par défaut pour les types valeur.</span><span class="sxs-lookup"><span data-stu-id="9c44c-106">The `new` operator is also used to invoke the default constructor for value types.</span></span> <span data-ttu-id="9c44c-107">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9c44c-107">For example:</span></span>

```csharp
int i = new int();
```

<span data-ttu-id="9c44c-108">Dans l’instruction précédente, `i` est initialisé à `0`, qui est la valeur par défaut pour le type `int`.</span><span class="sxs-lookup"><span data-stu-id="9c44c-108">In the preceding statement, `i` is initialized to `0`, which is the default value for the type `int`.</span></span> <span data-ttu-id="9c44c-109">L’instruction produit le même résultat que ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="9c44c-109">The statement has the same effect as the following:</span></span>

```csharp
int i = 0;
```

<span data-ttu-id="9c44c-110">Pour obtenir une liste complète des valeurs par défaut, consultez [Tableau des valeurs par défaut](default-values-table.md).</span><span class="sxs-lookup"><span data-stu-id="9c44c-110">For a complete list of default values, see [Default Values Table](default-values-table.md).</span></span>

<span data-ttu-id="9c44c-111">N’oubliez pas qu’il est incorrect de déclarer un constructeur par défaut pour un [struct](struct.md), car chaque type valeur a implicitement un constructeur public par défaut.</span><span class="sxs-lookup"><span data-stu-id="9c44c-111">Remember that it is an error to declare a default constructor for a [struct](struct.md) because every value type implicitly has a public default constructor.</span></span> <span data-ttu-id="9c44c-112">Il est possible de déclarer des constructeurs paramétrables sur un type struct pour définir ses valeurs initiales, mais cela est nécessaire uniquement si d’autres valeurs que la valeur par défaut sont requises.</span><span class="sxs-lookup"><span data-stu-id="9c44c-112">It is possible to declare parameterized constructors on a struct type to set its initial values, but this is only necessary if values other than the default are required.</span></span>

<span data-ttu-id="9c44c-113">Les objets de type valeur, tels que les structs, et les objets de type référence, tels que les classes, sont détruits automatiquement, mais les objets de type valeur sont détruits quand leur contexte contenant est détruit alors que les objets de type référence sont détruits par le garbage collector à une heure non spécifiée une fois que la dernière référence à ceux-ci est supprimée.</span><span class="sxs-lookup"><span data-stu-id="9c44c-113">Both value-type objects such as structs and reference-type objects such as classes are destroyed automatically, but value-type objects are destroyed when their containing context is destroyed, whereas reference-type objects are destroyed by the garbage collector at an unspecified time after the last reference to them is removed.</span></span> <span data-ttu-id="9c44c-114">Pour les types qui contiennent des ressources telles que des handles de fichiers ou des connexions réseau, il est préférable d’employer le nettoyage déterministe pour vous assurer que les ressources qu’ils contiennent sont libérées dès que possible.</span><span class="sxs-lookup"><span data-stu-id="9c44c-114">For types that contain resources such as file handles, or network connections, it is desirable to employ deterministic cleanup to ensure that the resources they contain are released as soon as possible.</span></span> <span data-ttu-id="9c44c-115">Pour plus d’informations, consultez [using, instruction](using-statement.md).</span><span class="sxs-lookup"><span data-stu-id="9c44c-115">For more information, see [using Statement](using-statement.md).</span></span>

<span data-ttu-id="9c44c-116">L’opérateur `new` ne peut pas être surchargé.</span><span class="sxs-lookup"><span data-stu-id="9c44c-116">The `new` operator cannot be overloaded.</span></span>

<span data-ttu-id="9c44c-117">Si l’opérateur `new` ne réussit pas à allouer de la mémoire, il lève l’exception <xref:System.OutOfMemoryException>.</span><span class="sxs-lookup"><span data-stu-id="9c44c-117">If the `new` operator fails to allocate memory, it throws the exception, <xref:System.OutOfMemoryException>.</span></span>

## <a name="example"></a><span data-ttu-id="9c44c-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="9c44c-118">Example</span></span>

<span data-ttu-id="9c44c-119">Dans l’exemple suivant, un objet `struct` et un objet de classe sont créés et initialisés à l’aide de l’opérateur `new`, puis des valeurs leur sont assignées.</span><span class="sxs-lookup"><span data-stu-id="9c44c-119">In the following example, a `struct` object and a class object are created and initialized by using the `new` operator and then assigned values.</span></span> <span data-ttu-id="9c44c-120">La valeur par défaut et les valeurs assignées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="9c44c-120">The default and the assigned values are displayed.</span></span>

[!code-csharp[csrefKeywordsOperator#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsOperator/CS/csrefKeywordsOperators.cs#7)]

<span data-ttu-id="9c44c-121">Notez que, dans l’exemple, la valeur par défaut d’une chaîne est `null`.</span><span class="sxs-lookup"><span data-stu-id="9c44c-121">Notice in the example that the default value of a string is `null`.</span></span> <span data-ttu-id="9c44c-122">Elle n’est donc pas affichée.</span><span class="sxs-lookup"><span data-stu-id="9c44c-122">Therefore, it is not displayed.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="9c44c-123">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9c44c-123">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="9c44c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c44c-124">See also</span></span>

- [<span data-ttu-id="9c44c-125">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9c44c-125">C# Reference</span></span>](../../language-reference/index.md)
- [<span data-ttu-id="9c44c-126">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9c44c-126">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="9c44c-127">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="9c44c-127">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="9c44c-128">Mots clés des opérateurs</span><span class="sxs-lookup"><span data-stu-id="9c44c-128">Operator Keywords</span></span>](operator-keywords.md)
- [<span data-ttu-id="9c44c-129">new</span><span class="sxs-lookup"><span data-stu-id="9c44c-129">new</span></span>](new.md)
- [<span data-ttu-id="9c44c-130">Types anonymes</span><span class="sxs-lookup"><span data-stu-id="9c44c-130">Anonymous Types</span></span>](../../programming-guide/classes-and-structs/anonymous-types.md)