---
title: Paramètres de type générique - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- generics [C#], type parameters
- type parameters [C#]
ms.assetid: a03b0ab2-0606-4b41-b7bf-e64d5bb4d18f
ms.openlocfilehash: 10feb47ce3dfe9e356da381e0d62e6d220c9452a
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57677420"
---
# <a name="generic-type-parameters-c-programming-guide"></a><span data-ttu-id="9a054-102">Paramètres de type générique (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="9a054-102">Generic type parameters (C# Programming Guide)</span></span>

<span data-ttu-id="9a054-103">Dans une définition de méthode ou de type générique, le paramètre de type représente un espace réservé pour un type spécifié par le client au moment de créer une instance du type générique.</span><span class="sxs-lookup"><span data-stu-id="9a054-103">In a generic type or method definition, a type parameter is a placeholder for a specific type that a client specifies when they create an instance of the generic type.</span></span> <span data-ttu-id="9a054-104">Une classe générique, telle que `GenericList<T>` répertoriée dans [Introduction aux génériques](../../../csharp/programming-guide/generics/introduction-to-generics.md), ne peut pas être utilisée en l’état car il ne s’agit pas vraiment d’un type, mais plutôt d’un modèle pour un type.</span><span class="sxs-lookup"><span data-stu-id="9a054-104">A generic class, such as `GenericList<T>` listed in [Introduction to Generics](../../../csharp/programming-guide/generics/introduction-to-generics.md), cannot be used as-is because it is not really a type; it is more like a blueprint for a type.</span></span> <span data-ttu-id="9a054-105">Pour utiliser `GenericList<T>`, le code client doit déclarer et instancier un type construit en spécifiant un argument de type à l’intérieur de crochets pointus.</span><span class="sxs-lookup"><span data-stu-id="9a054-105">To use `GenericList<T>`, client code must declare and instantiate a constructed type by specifying a type argument inside the angle brackets.</span></span> <span data-ttu-id="9a054-106">L’argument de type pour cette classe particulière peut être tout type reconnu par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="9a054-106">The type argument for this particular class can be any type recognized by the compiler.</span></span> <span data-ttu-id="9a054-107">Il est possible de créer un nombre quelconque d’instances de type construit, chacune avec un argument de type différent, comme suit :</span><span class="sxs-lookup"><span data-stu-id="9a054-107">Any number of constructed type instances can be created, each one using a different type argument, as follows:</span></span>  
  
[!code-csharp[csProgGuideGenerics#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideGenerics/CS/Generics.cs#7)]  
  
<span data-ttu-id="9a054-108">Dans chacune de ces instances de `GenericList<T>`, chaque occurrence de `T` dans la classe est remplacée à l’exécution par l’argument de type.</span><span class="sxs-lookup"><span data-stu-id="9a054-108">In each of these instances of `GenericList<T>`, every occurrence of `T` in the class is substituted at run time with the type argument.</span></span> <span data-ttu-id="9a054-109">Par cette substitution, nous avons créé trois objets distincts de type sécurisé et efficaces à l’aide d’une seule définition de classe.</span><span class="sxs-lookup"><span data-stu-id="9a054-109">By means of this substitution, we have created three separate type-safe and efficient objects using a single class definition.</span></span> <span data-ttu-id="9a054-110">Pour plus d’informations sur la façon dont cette substitution est exécutée par le CLR, consultez [Génériques dans le runtime](../../../csharp/programming-guide/generics/generics-in-the-run-time.md).</span><span class="sxs-lookup"><span data-stu-id="9a054-110">For more information on how this substitution is performed by the CLR, see [Generics in the Run Time](../../../csharp/programming-guide/generics/generics-in-the-run-time.md).</span></span>  
  
## <a name="type-parameter-naming-guidelines"></a><span data-ttu-id="9a054-111">Recommandations concernant le nom des paramètres de type</span><span class="sxs-lookup"><span data-stu-id="9a054-111">Type parameter naming guidelines</span></span>  
  
- <span data-ttu-id="9a054-112">**Nommez** les paramètres de type générique avec des noms descriptifs, sauf si un nom composé d’une seule lettre est suffisamment évocateur et qu’un nom descriptif n’apporte rien de plus.</span><span class="sxs-lookup"><span data-stu-id="9a054-112">**Do** name generic type parameters with descriptive names, unless a single letter name is completely self explanatory and a descriptive name would not add value.</span></span>  
  
   [!code-csharp[csProgGuideGenerics#8](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideGenerics/CS/Generics.cs#8)]  
  
- <span data-ttu-id="9a054-113">**Envisagez** l’utilisation de T comme nom de paramètre de type pour les types ayant un paramètre de type d’une seule lettre.</span><span class="sxs-lookup"><span data-stu-id="9a054-113">**Consider** using T as the type parameter name for types with one single letter type parameter.</span></span>  
  
   [!code-csharp[csProgGuideGenerics#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideGenerics/CS/Generics.cs#9)]  
  
- <span data-ttu-id="9a054-114">**Préfixez** les noms des paramètres de type descriptifs avec « T ».</span><span class="sxs-lookup"><span data-stu-id="9a054-114">**Do** prefix descriptive type parameter names with "T".</span></span>  
  
   [!code-csharp[csProgGuideGenerics#10](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideGenerics/CS/Generics.cs#10)]  
  
- <span data-ttu-id="9a054-115">**Pensez** à indiquer les contraintes placées sur un paramètre de type dans le nom de paramètre.</span><span class="sxs-lookup"><span data-stu-id="9a054-115">**Consider** indicating constraints placed on a type parameter in the name of parameter.</span></span> <span data-ttu-id="9a054-116">Par exemple, un paramètre limité à `ISession` peut être appelé `TSession`.</span><span class="sxs-lookup"><span data-stu-id="9a054-116">For example, a parameter constrained to `ISession` may be called `TSession`.</span></span>

<span data-ttu-id="9a054-117">La règle d’analyse du code [CA1715](/visualstudio/code-quality/ca1715-identifiers-should-have-correct-prefix) vérifie que les paramètres de type sont correctement nommés.</span><span class="sxs-lookup"><span data-stu-id="9a054-117">The code analysis rule [CA1715](/visualstudio/code-quality/ca1715-identifiers-should-have-correct-prefix) can be used to ensure that type parameters are named appropriately.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a054-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a054-118">See also</span></span>

- <xref:System.Collections.Generic>
- [<span data-ttu-id="9a054-119">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9a054-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="9a054-120">Génériques</span><span class="sxs-lookup"><span data-stu-id="9a054-120">Generics</span></span>](../../../csharp/programming-guide/generics/index.md)
- [<span data-ttu-id="9a054-121">Différences entre les modèles C++ et les génériques C#</span><span class="sxs-lookup"><span data-stu-id="9a054-121">Differences Between C++ Templates and C# Generics</span></span>](../../../csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics.md)
