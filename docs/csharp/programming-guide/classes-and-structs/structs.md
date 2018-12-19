---
title: Structures - Guide de programmation C#
ms.custom: seodec18
ms.date: 08/21/2018
helpviewer_keywords:
- C# language, structs
- structs [C#]
ms.assetid: b7cf4ff2-0eb7-4e5c-93d5-b2196b4f5d89
ms.openlocfilehash: 3f19d0485939e1923c479c1c9fdeb06572a11e14
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53240383"
---
# <a name="structs-c-programming-guide"></a><span data-ttu-id="90a03-102">Structures (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="90a03-102">Structs (C# Programming Guide)</span></span>

<span data-ttu-id="90a03-103">Les structs sont définis à l’aide du mot clé [struct](../../language-reference/keywords/struct.md), par exemple :</span><span class="sxs-lookup"><span data-stu-id="90a03-103">Structs are defined by using the [struct](../../language-reference/keywords/struct.md) keyword, for example:</span></span>  
  
[!code-csharp[csProgGuideObjects#39](./codesnippet/CSharp/structs_1.cs)]  
  
<span data-ttu-id="90a03-104">Les structs partagent quasiment la même syntaxe que les classes.</span><span class="sxs-lookup"><span data-stu-id="90a03-104">Structs share most of the same syntax as classes.</span></span> <span data-ttu-id="90a03-105">Le nom du struct doit être un [nom d’identificateur](../inside-a-program/identifier-names.md) C# valide.</span><span class="sxs-lookup"><span data-stu-id="90a03-105">The name of the struct must be a valid C# [identifier name](../inside-a-program/identifier-names.md).</span></span> <span data-ttu-id="90a03-106">Les structs sont plus limités que les classes des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="90a03-106">Structs are more limited than classes in the following ways:</span></span>  
  
- <span data-ttu-id="90a03-107">Au sein d’une déclaration de struct, les champs ne peuvent pas être initialisés à moins d’être déclarés comme étant de type const ou static.</span><span class="sxs-lookup"><span data-stu-id="90a03-107">Within a struct declaration, fields cannot be initialized unless they are declared as const or static.</span></span>  
- <span data-ttu-id="90a03-108">Un struct ne peut pas déclarer de constructeur par défaut (un constructeur sans paramètre) ni de finaliseur.</span><span class="sxs-lookup"><span data-stu-id="90a03-108">A struct cannot declare a default constructor (a constructor without parameters) or a finalizer.</span></span>  
- <span data-ttu-id="90a03-109">Les structs sont copiés lors de l'assignation.</span><span class="sxs-lookup"><span data-stu-id="90a03-109">Structs are copied on assignment.</span></span> <span data-ttu-id="90a03-110">Lorsqu'un struct est assigné à une nouvelle variable, toutes les données sont copiées et les modifications apportées à la nouvelle copie ne changent pas les données de la copie d'origine.</span><span class="sxs-lookup"><span data-stu-id="90a03-110">When a struct is assigned to a new variable, all the data is copied, and any modification to the new copy does not change the data for the original copy.</span></span> <span data-ttu-id="90a03-111">Il est important de vous en souvenir quand vous utilisez des collections de types valeur telles que `Dictionary<string, myStruct>`.</span><span class="sxs-lookup"><span data-stu-id="90a03-111">This is important to remember when working with collections of value types such as `Dictionary<string, myStruct>`.</span></span>  
- <span data-ttu-id="90a03-112">Les structs sont des types valeur, contrairement aux classes, qui sont des types référence.</span><span class="sxs-lookup"><span data-stu-id="90a03-112">Structs are value types, unlike classes, which are reference types.</span></span>  
- <span data-ttu-id="90a03-113">Contrairement aux classes, il est possible d’instancier les structs sans avoir recours à un opérateur `new`.</span><span class="sxs-lookup"><span data-stu-id="90a03-113">Unlike classes, structs can be instantiated without using a `new` operator.</span></span>  
- <span data-ttu-id="90a03-114">Les structs peuvent déclarer des constructeurs qui ont des paramètres.</span><span class="sxs-lookup"><span data-stu-id="90a03-114">Structs can declare constructors that have parameters.</span></span> 
- <span data-ttu-id="90a03-115">Un struct ne peut pas hériter d'un autre struct ou d'une classe ; il ne peut pas non plus servir de base à une classe.</span><span class="sxs-lookup"><span data-stu-id="90a03-115">A struct cannot inherit from another struct or class, and it cannot be the base of a class.</span></span> <span data-ttu-id="90a03-116">Tous les structs héritent directement de <xref:System.ValueType>, qui hérite de <xref:System.Object>.</span><span class="sxs-lookup"><span data-stu-id="90a03-116">All structs inherit directly from <xref:System.ValueType>, which inherits from <xref:System.Object>.</span></span>  
- <span data-ttu-id="90a03-117">Un struct peut implémenter des interfaces.</span><span class="sxs-lookup"><span data-stu-id="90a03-117">A struct can implement interfaces.</span></span>  
- <span data-ttu-id="90a03-118">Un struct peut être utilisé comme un type Nullable et peut avoir une valeur null.</span><span class="sxs-lookup"><span data-stu-id="90a03-118">A struct can be used as a nullable type and can be assigned a null value.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="90a03-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90a03-119">Related sections</span></span>  

<span data-ttu-id="90a03-120">Pour plus d'informations :</span><span class="sxs-lookup"><span data-stu-id="90a03-120">For more information:</span></span>  
  
- [<span data-ttu-id="90a03-121">Utilisation de structs</span><span class="sxs-lookup"><span data-stu-id="90a03-121">Using Structs</span></span>](using-structs.md)
- [<span data-ttu-id="90a03-122">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="90a03-122">Constructors</span></span>](constructors.md)
- [<span data-ttu-id="90a03-123">Types Nullable</span><span class="sxs-lookup"><span data-stu-id="90a03-123">Nullable Types</span></span>](../nullable-types/index.md)
- [<span data-ttu-id="90a03-124">Guide pratique pour différencier le passage d’un struct et le passage d’une référence de classe à une méthode</span><span class="sxs-lookup"><span data-stu-id="90a03-124">How to: Know the Difference Between Passing a Struct and Passing a Class Reference to a Method</span></span>](how-to-know-the-difference-passing-a-struct-and-passing-a-class-to-a-method.md)
- [<span data-ttu-id="90a03-125">Guide pratique pour implémenter des conversions définies par l’utilisateur entre des structs</span><span class="sxs-lookup"><span data-stu-id="90a03-125">How to: Implement User-Defined Conversions Between Structs</span></span>](../statements-expressions-operators/how-to-implement-user-defined-conversions-between-structs.md)

## <a name="see-also"></a><span data-ttu-id="90a03-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90a03-126">See also</span></span>

- [<span data-ttu-id="90a03-127">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="90a03-127">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="90a03-128">Classes et structs</span><span class="sxs-lookup"><span data-stu-id="90a03-128">Classes and Structs</span></span>](index.md)
- [<span data-ttu-id="90a03-129">Classes</span><span class="sxs-lookup"><span data-stu-id="90a03-129">Classes</span></span>](classes.md)
- [<span data-ttu-id="90a03-130">Noms d’identificateur</span><span class="sxs-lookup"><span data-stu-id="90a03-130">Identifier names</span></span>](../inside-a-program/identifier-names.md)
