---
title: Génériques - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- C# language, generics
- generics [C#]
ms.assetid: 75ea8509-a4ea-4e7a-a2b3-cf72482e9282
ms.openlocfilehash: fcc905353ada734e50fd56f50c4f705aa400f70d
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64608485"
---
# <a name="generics-c-programming-guide"></a><span data-ttu-id="9915e-102">Génériques (guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="9915e-102">Generics (C# Programming Guide)</span></span>
<span data-ttu-id="9915e-103">Les génériques ont été ajoutés à la version 2.0 du langage C# et du Common Language Runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="9915e-103">Generics were added to version 2.0 of the C# language and the common language runtime (CLR).</span></span> <span data-ttu-id="9915e-104">Les génériques introduisent le concept des paramètres de type dans .NET Framework, qui permettent de concevoir des classes et des méthodes qui diffèrent la spécification d’un ou de plusieurs types jusqu’à ce que la classe ou la méthode soit déclarée et instanciée par le code client.</span><span class="sxs-lookup"><span data-stu-id="9915e-104">Generics introduce to the .NET Framework the concept of type parameters, which make it possible to design classes and methods that defer the specification of one or more types until the class or method is declared and instantiated by client code.</span></span> <span data-ttu-id="9915e-105">Par exemple, à l’aide d’un paramètre de type générique T, vous pouvez écrire une seule classe qui peut être utilisée par un autre code client sans impliquer le coût ou le risque des casts ou des opérations de boxing à l’exécution, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="9915e-105">For example, by using a generic type parameter T you can write a single class that other client code can use without incurring the cost or risk of runtime casts or boxing operations, as shown here:</span></span>  
  
 [!code-csharp[csProgGuideGenerics#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideGenerics/CS/Generics.cs#1)]  
  
## <a name="generics-overview"></a><span data-ttu-id="9915e-106">Vue d’ensemble des génériques</span><span class="sxs-lookup"><span data-stu-id="9915e-106">Generics Overview</span></span>  
  
- <span data-ttu-id="9915e-107">Utilisez des types génériques pour optimiser la réutilisation de code, la sécurité des types et les performances.</span><span class="sxs-lookup"><span data-stu-id="9915e-107">Use generic types to maximize code reuse, type safety, and performance.</span></span>  
  
- <span data-ttu-id="9915e-108">L’utilisation la plus courante des génériques est de créer des classes de collection.</span><span class="sxs-lookup"><span data-stu-id="9915e-108">The most common use of generics is to create collection classes.</span></span>  
  
- <span data-ttu-id="9915e-109">La bibliothèque de classes du .NET Framework contient plusieurs nouvelles classes de collection génériques dans l’espace de noms <xref:System.Collections.Generic>.</span><span class="sxs-lookup"><span data-stu-id="9915e-109">The .NET Framework class library contains several new generic collection classes in the <xref:System.Collections.Generic> namespace.</span></span> <span data-ttu-id="9915e-110">Celles-ci doivent être utilisées chaque fois que c’est possible, à la place de classes comme <xref:System.Collections.ArrayList> dans l’espace de noms <xref:System.Collections>.</span><span class="sxs-lookup"><span data-stu-id="9915e-110">These should be used whenever possible instead of classes such as <xref:System.Collections.ArrayList> in the <xref:System.Collections> namespace.</span></span>  
  
- <span data-ttu-id="9915e-111">Vous pouvez créer vos propres interfaces, classes, méthodes, événements et délégués génériques.</span><span class="sxs-lookup"><span data-stu-id="9915e-111">You can create your own generic interfaces, classes, methods, events and delegates.</span></span>  
  
- <span data-ttu-id="9915e-112">Les classes génériques peuvent être contraintes pour permettre l’accès à des méthodes sur des types de données particuliers.</span><span class="sxs-lookup"><span data-stu-id="9915e-112">Generic classes may be constrained to enable access to methods on particular data types.</span></span>  
  
- <span data-ttu-id="9915e-113">Des informations sur les types qui sont utilisés dans un type de données générique peuvent être obtenues à l’exécution à l’aide de la réflexion.</span><span class="sxs-lookup"><span data-stu-id="9915e-113">Information on the types that are used in a generic data type may be obtained at run-time by using reflection.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="9915e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9915e-114">Related Sections</span></span>  
 <span data-ttu-id="9915e-115">Pour plus d'informations :</span><span class="sxs-lookup"><span data-stu-id="9915e-115">For more information:</span></span>  
  
- [<span data-ttu-id="9915e-116">Introduction aux génériques</span><span class="sxs-lookup"><span data-stu-id="9915e-116">Introduction to Generics</span></span>](../../../csharp/programming-guide/generics/introduction-to-generics.md)  
  
- [<span data-ttu-id="9915e-117">Avantages des génériques</span><span class="sxs-lookup"><span data-stu-id="9915e-117">Benefits of Generics</span></span>](../../../csharp/programming-guide/generics/benefits-of-generics.md)  
  
- [<span data-ttu-id="9915e-118">Paramètres de type générique</span><span class="sxs-lookup"><span data-stu-id="9915e-118">Generic Type Parameters</span></span>](../../../csharp/programming-guide/generics/generic-type-parameters.md)  
  
- [<span data-ttu-id="9915e-119">Contraintes sur les paramètres de type</span><span class="sxs-lookup"><span data-stu-id="9915e-119">Constraints on Type Parameters</span></span>](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md)  
  
- [<span data-ttu-id="9915e-120">Classes génériques</span><span class="sxs-lookup"><span data-stu-id="9915e-120">Generic Classes</span></span>](../../../csharp/programming-guide/generics/generic-classes.md)  
  
- [<span data-ttu-id="9915e-121">Interfaces génériques</span><span class="sxs-lookup"><span data-stu-id="9915e-121">Generic Interfaces</span></span>](../../../csharp/programming-guide/generics/generic-interfaces.md)  
  
- [<span data-ttu-id="9915e-122">Méthodes génériques</span><span class="sxs-lookup"><span data-stu-id="9915e-122">Generic Methods</span></span>](../../../csharp/programming-guide/generics/generic-methods.md)  
  
- [<span data-ttu-id="9915e-123">Délégués génériques</span><span class="sxs-lookup"><span data-stu-id="9915e-123">Generic Delegates</span></span>](../../../csharp/programming-guide/generics/generic-delegates.md)  
  
- [<span data-ttu-id="9915e-124">Différences entre les modèles C++ et les génériques C#</span><span class="sxs-lookup"><span data-stu-id="9915e-124">Differences Between C++ Templates and C# Generics</span></span>](../../../csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics.md)  
  
- [<span data-ttu-id="9915e-125">Génériques et réflexion</span><span class="sxs-lookup"><span data-stu-id="9915e-125">Generics and Reflection</span></span>](../../../csharp/programming-guide/generics/generics-and-reflection.md)  
  
- [<span data-ttu-id="9915e-126">Génériques dans le runtime</span><span class="sxs-lookup"><span data-stu-id="9915e-126">Generics in the Run Time</span></span>](../../../csharp/programming-guide/generics/generics-in-the-run-time.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="9915e-127">Spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9915e-127">C# Language Specification</span></span>  
 <span data-ttu-id="9915e-128">Pour plus d'informations, voir la [spécification du langage C#](~/_csharplang/spec/types.md#constructed-types).</span><span class="sxs-lookup"><span data-stu-id="9915e-128">For more information, see the [C# Language Specification](~/_csharplang/spec/types.md#constructed-types).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9915e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9915e-129">See also</span></span>

- <xref:System.Collections.Generic>
- [<span data-ttu-id="9915e-130">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9915e-130">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="9915e-131">Types</span><span class="sxs-lookup"><span data-stu-id="9915e-131">Types</span></span>](../../../csharp/programming-guide/types/index.md)
- [<span data-ttu-id="9915e-132">\<typeparam></span><span class="sxs-lookup"><span data-stu-id="9915e-132">\<typeparam></span></span>](../../../csharp/programming-guide/xmldoc/typeparam.md)
- [<span data-ttu-id="9915e-133">\<typeparamref></span><span class="sxs-lookup"><span data-stu-id="9915e-133">\<typeparamref></span></span>](../../../csharp/programming-guide/xmldoc/typeparamref.md)
- [<span data-ttu-id="9915e-134">Génériques en .NET</span><span class="sxs-lookup"><span data-stu-id="9915e-134">Generics in .NET</span></span>](../../../standard/generics/index.md)
