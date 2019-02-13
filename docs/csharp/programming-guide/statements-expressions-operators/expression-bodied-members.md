---
title: Membres expression-bodied - Guide de programmation C#
ms.custom: seodec18
ms.date: 02/06/2019
helpviewer_keywords:
- expression-bodied members[C#]
- C# language, expresion-bodied members
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d7c282157639a6a60270ce8dbebbc91dd0e0a3f3
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55826614"
---
# <a name="expression-bodied-members-c-programming-guide"></a><span data-ttu-id="99c3c-102">Membres expression-bodied (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="99c3c-102">Expression-bodied members (C# programming guide)</span></span>

<span data-ttu-id="99c3c-103">Les définitions de corps d’expression vous permettent de fournir l’implémentation d’un membre sous une forme lisible et très concise.</span><span class="sxs-lookup"><span data-stu-id="99c3c-103">Expression body definitions let you provide a member's implementation in a very concise, readable form.</span></span> <span data-ttu-id="99c3c-104">Vous pouvez utiliser une définition de corps d’expression chaque fois que la logique d’un membre pris en charge, comme une méthode ou une propriété, se compose d’une seule expression.</span><span class="sxs-lookup"><span data-stu-id="99c3c-104">You can use an expression body definition whenever the logic for any supported member, such as a method or property, consists of a single expression.</span></span> <span data-ttu-id="99c3c-105">La syntaxe générale d’une définition de corps d’expression est la suivante :</span><span class="sxs-lookup"><span data-stu-id="99c3c-105">An expression body definition has the following general syntax:</span></span>

```csharp
member => expression;
```

<span data-ttu-id="99c3c-106">où *expression* est une expression valide.</span><span class="sxs-lookup"><span data-stu-id="99c3c-106">where *expression* is a valid expression.</span></span>

<span data-ttu-id="99c3c-107">La prise en charge des définitions de corps d’expression a été introduite pour les méthodes et les propriétés en lecture seule dans C# 6 et a été étendue dans C# 7.0.</span><span class="sxs-lookup"><span data-stu-id="99c3c-107">Support for expression body definitions was introduced for methods and read-only properties in C# 6 and was expanded in C# 7.0.</span></span> <span data-ttu-id="99c3c-108">Vous pouvez utiliser des définitions de corps d’expression avec les membres de type listés dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="99c3c-108">Expression body definitions can be used with the type members listed in the following table:</span></span>

|<span data-ttu-id="99c3c-109">Membre</span><span class="sxs-lookup"><span data-stu-id="99c3c-109">Member</span></span>  |<span data-ttu-id="99c3c-110">Prise en charge à compter de</span><span class="sxs-lookup"><span data-stu-id="99c3c-110">Supported as of...</span></span> |
|---------|---------|
|[<span data-ttu-id="99c3c-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="99c3c-111">Method</span></span>](#methods)  |<span data-ttu-id="99c3c-112">C# 6</span><span class="sxs-lookup"><span data-stu-id="99c3c-112">C# 6</span></span> |
|[<span data-ttu-id="99c3c-113">Propriété en lecture seule</span><span class="sxs-lookup"><span data-stu-id="99c3c-113">Read-only property</span></span>](#read-only-properties)   |<span data-ttu-id="99c3c-114">C# 6</span><span class="sxs-lookup"><span data-stu-id="99c3c-114">C# 6</span></span>  |
|[<span data-ttu-id="99c3c-115">Property</span><span class="sxs-lookup"><span data-stu-id="99c3c-115">Property</span></span>](#properties)  |<span data-ttu-id="99c3c-116">C# 7.0</span><span class="sxs-lookup"><span data-stu-id="99c3c-116">C# 7.0</span></span> |
|[<span data-ttu-id="99c3c-117">Constructeur</span><span class="sxs-lookup"><span data-stu-id="99c3c-117">Constructor</span></span>](#constructors)   |<span data-ttu-id="99c3c-118">C# 7.0</span><span class="sxs-lookup"><span data-stu-id="99c3c-118">C# 7.0</span></span> |
|[<span data-ttu-id="99c3c-119">Finaliseur</span><span class="sxs-lookup"><span data-stu-id="99c3c-119">Finalizer</span></span>](#finalizers)     |<span data-ttu-id="99c3c-120">C# 7.0</span><span class="sxs-lookup"><span data-stu-id="99c3c-120">C# 7.0</span></span> |
|[<span data-ttu-id="99c3c-121">Indexeur</span><span class="sxs-lookup"><span data-stu-id="99c3c-121">Indexer</span></span>](#indexers)       |<span data-ttu-id="99c3c-122">C# 7.0</span><span class="sxs-lookup"><span data-stu-id="99c3c-122">C# 7.0</span></span> |

## <a name="methods"></a><span data-ttu-id="99c3c-123">Méthodes</span><span class="sxs-lookup"><span data-stu-id="99c3c-123">Methods</span></span>

<span data-ttu-id="99c3c-124">Une méthode expression-bodied se compose d’une seule expression qui retourne une valeur dont le type correspond au type de retour de la méthode ou, pour les méthodes qui retournent `void`, qui effectue une opération.</span><span class="sxs-lookup"><span data-stu-id="99c3c-124">An expression-bodied method consists of a single expression that returns a value whose type matches the method's return type, or, for methods that return `void`, that performs some operation.</span></span> <span data-ttu-id="99c3c-125">Par exemple, les types qui substituent la méthode <xref:System.Object.ToString%2A> incluent généralement une expression unique qui retourne la représentation sous forme de chaîne de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="99c3c-125">For example, types that override the <xref:System.Object.ToString%2A> method typically include a single expression that returns the string representation of the current object.</span></span>

<span data-ttu-id="99c3c-126">L’exemple suivant définit une classe `Person` qui substitue la méthode <xref:System.Object.ToString%2A> avec une définition de corps d’expression.</span><span class="sxs-lookup"><span data-stu-id="99c3c-126">The following example defines a `Person` class that overrides the <xref:System.Object.ToString%2A> method with an expression body definition.</span></span> <span data-ttu-id="99c3c-127">Il définit également une méthode `DisplayName` qui affiche un nom sur la console.</span><span class="sxs-lookup"><span data-stu-id="99c3c-127">It also defines a `DisplayName` method that displays a name to the console.</span></span> <span data-ttu-id="99c3c-128">Notez que le mot clé `return` n’est pas utilisé dans la définition de corps d’expression `ToString`.</span><span class="sxs-lookup"><span data-stu-id="99c3c-128">Note that the `return` keyword is not used in the `ToString` expression body definition.</span></span>

[!code-csharp[expression-bodied-methods](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/expr-bodied-methods.cs)]  

<span data-ttu-id="99c3c-129">Pour plus d’informations, consultez [Méthodes (Guide de programmation C#)](../classes-and-structs/methods.md).</span><span class="sxs-lookup"><span data-stu-id="99c3c-129">For more information, see [Methods (C# Programming Guide)](../classes-and-structs/methods.md).</span></span>

## <a name="read-only-properties"></a><span data-ttu-id="99c3c-130">Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="99c3c-130">Read-only properties</span></span>

<span data-ttu-id="99c3c-131">Depuis C# 6, vous pouvez utiliser une définition de corps d’expression pour implémenter une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="99c3c-131">Starting with C# 6, you can use expression body definition to implement a read-only property.</span></span> <span data-ttu-id="99c3c-132">Pour ce faire, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="99c3c-132">To do that, use the following syntax:</span></span>

```csharp
PropertyType PropertyName => expression;
```

<span data-ttu-id="99c3c-133">L’exemple suivant définit une classe `Location` dont la propriété en lecture seule `Name` est implémentée comme une définition de corps d’expression qui retourne la valeur du champ privé `locationName` :</span><span class="sxs-lookup"><span data-stu-id="99c3c-133">The following example defines a `Location` class whose read-only `Name` property is implemented as an expression body definition that returns the value of the private `locationName` field:</span></span>

[!code-csharp[expression-bodied-read-only-property](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/expr-bodied-readonly.cs#1)]  

<span data-ttu-id="99c3c-134">Pour plus d’informations sur les propriétés, consultez [Propriétés (Guide de programmation C#)](../classes-and-structs/properties.md).</span><span class="sxs-lookup"><span data-stu-id="99c3c-134">For more information about properties, see [Properties (C# Programming Guide)](../classes-and-structs/properties.md).</span></span>

## <a name="properties"></a><span data-ttu-id="99c3c-135">Propriétés</span><span class="sxs-lookup"><span data-stu-id="99c3c-135">Properties</span></span>

<span data-ttu-id="99c3c-136">Depuis C# 7.0, vous pouvez utiliser des définitions de corps d’expression pour implémenter la propriété `get` et les accesseurs `set`.</span><span class="sxs-lookup"><span data-stu-id="99c3c-136">Starting with C# 7.0, you can use expression body definitions to implement property `get` and `set` accessors.</span></span> <span data-ttu-id="99c3c-137">L’exemple suivant montre comment faire :</span><span class="sxs-lookup"><span data-stu-id="99c3c-137">The following example demonstrates how to do that:</span></span>

[!code-csharp[expression-bodied-property-get-set](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/expr-bodied-ctor.cs#1)]

<span data-ttu-id="99c3c-138">Pour plus d’informations sur les propriétés, consultez [Propriétés (Guide de programmation C#)](../classes-and-structs/properties.md).</span><span class="sxs-lookup"><span data-stu-id="99c3c-138">For more information about properties, see [Properties (C# Programming Guide)](../classes-and-structs/properties.md).</span></span>

## <a name="constructors"></a><span data-ttu-id="99c3c-139">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="99c3c-139">Constructors</span></span>

<span data-ttu-id="99c3c-140">Une définition de corps d’expression pour un constructeur se compose généralement d’une seule expression d’assignation ou d’un appel de méthode qui gère les arguments du constructeur ou qui initialise l’état de l’instance.</span><span class="sxs-lookup"><span data-stu-id="99c3c-140">An expression body definition for a constructor typically consists of a single assignment expression or a method call that handles the constructor's arguments or initializes instance state.</span></span>

<span data-ttu-id="99c3c-141">L’exemple suivant définit une classe `Location` dont le constructeur a un seul paramètre de chaîne nommé *name*.</span><span class="sxs-lookup"><span data-stu-id="99c3c-141">The following example defines a `Location` class whose constructor has a single string parameter named *name*.</span></span> <span data-ttu-id="99c3c-142">La définition de corps d’expression assigne l’argument à la propriété `Name`.</span><span class="sxs-lookup"><span data-stu-id="99c3c-142">The expression body definition assigns the argument to the `Name` property.</span></span>

[!code-csharp[expression-bodied-constructor](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/expr-bodied-ctor.cs#1)]  

<span data-ttu-id="99c3c-143">Pour plus d’informations, consultez [Constructeurs (Guide de programmation C#)](../classes-and-structs/constructors.md).</span><span class="sxs-lookup"><span data-stu-id="99c3c-143">For more information, see [Constructors (C# Programming Guide)](../classes-and-structs/constructors.md).</span></span>

## <a name="finalizers"></a><span data-ttu-id="99c3c-144">Finaliseurs</span><span class="sxs-lookup"><span data-stu-id="99c3c-144">Finalizers</span></span>

<span data-ttu-id="99c3c-145">Une définition de corps d’expression pour un finaliseur contient généralement des instructions de nettoyage, telles que des instructions qui libèrent les ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="99c3c-145">An expression body definition for a finalizer typically contains cleanup statements, such as statements that release unmanaged resources.</span></span>

<span data-ttu-id="99c3c-146">L’exemple suivant définit un finaliseur qui utilise une définition de corps d’expression pour indiquer que le finaliseur a été appelé.</span><span class="sxs-lookup"><span data-stu-id="99c3c-146">The following example defines a finalizer that uses an expression body definition to indicate that the finalizer has been called.</span></span>

[!code-csharp[expression-bodied-finalizer](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/expr-bodied-destructor.cs#1)]  

<span data-ttu-id="99c3c-147">Pour plus d’informations, consultez [Finaliseurs (Guide de programmation C#)](../classes-and-structs/destructors.md).</span><span class="sxs-lookup"><span data-stu-id="99c3c-147">For more information, see [Finalizers (C# Programming Guide)](../classes-and-structs/destructors.md).</span></span>

## <a name="indexers"></a><span data-ttu-id="99c3c-148">Indexeurs</span><span class="sxs-lookup"><span data-stu-id="99c3c-148">Indexers</span></span>

<span data-ttu-id="99c3c-149">Comme les propriétés, les accesseurs get et set d’un indexeur sont composés de définitions de corps d’expression si l’accesseur get est constitué d’une seule instruction qui retourne une valeur ou si l’accesseur set effectue une assignation simple.</span><span class="sxs-lookup"><span data-stu-id="99c3c-149">Like properties, an indexer's get and set accessors consist of expression body definitions if the get accessor consists of a single statement that returns a value or the set accessor performs a simple assignment.</span></span>

<span data-ttu-id="99c3c-150">L’exemple suivant définit une classe nommée `Sports` qui inclut un tableau <xref:System.String> interne contenant les noms de plusieurs sports.</span><span class="sxs-lookup"><span data-stu-id="99c3c-150">The following example defines a class named `Sports` that includes an internal <xref:System.String> array that contains the names of a number of sports.</span></span> <span data-ttu-id="99c3c-151">Les accesseurs get et set de l’indexeur sont implémentés en tant que définitions de corps d’expression.</span><span class="sxs-lookup"><span data-stu-id="99c3c-151">Both the indexer's get and set accessors are implemented as expression body definitions.</span></span>

[!code-csharp[expression-bodied-indexer](../../../../samples/snippets/csharp/programming-guide/classes-and-structs/expr-bodied-indexers.cs#1)]

<span data-ttu-id="99c3c-152">Pour plus d’informations, consultez [Indexeurs (Guide de programmation C#)](../indexers/index.md).</span><span class="sxs-lookup"><span data-stu-id="99c3c-152">For more information, see [Indexers (C# Programming Guide)](../indexers/index.md).</span></span>
