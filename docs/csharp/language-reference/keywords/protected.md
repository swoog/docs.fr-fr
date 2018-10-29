---
title: protected, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- protected
- protected_CSharpKeyword
helpviewer_keywords:
- protected keyword [C#]
ms.assetid: 05ce3794-6675-4025-bddb-eaaa0ec22892
ms.openlocfilehash: cc3c8f81edb68fb26be560c8635e30dfd6e7b372
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50183176"
---
# <a name="protected-c-reference"></a><span data-ttu-id="0a8ec-102">protected (référence C#)</span><span class="sxs-lookup"><span data-stu-id="0a8ec-102">protected (C# Reference)</span></span>

<span data-ttu-id="0a8ec-103">Le mot clé `protected` est un modificateur d’accès de membre.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-103">The `protected` keyword is a member access modifier.</span></span>

 > <span data-ttu-id="0a8ec-104">Cette page traite de l’accès `protected`.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-104">This page covers `protected` access.</span></span> <span data-ttu-id="0a8ec-105">Le mot clé `protected` fait également partie des modificateurs d’accès [`protected internal`](protected-internal.md) et [`private protected`](private-protected.md).</span><span class="sxs-lookup"><span data-stu-id="0a8ec-105">The `protected` keyword is also part of the [`protected internal`](protected-internal.md) and [`private protected`](private-protected.md) access modifiers.</span></span>

<span data-ttu-id="0a8ec-106">Un membre protégé est accessible dans sa classe et par les instances de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-106">A protected member is accessible within its class and by derived class instances.</span></span>

<span data-ttu-id="0a8ec-107">Pour obtenir une comparaison de `protected` et des autres modificateurs d’accès, consultez [Niveaux d’accessibilité](accessibility-levels.md).</span><span class="sxs-lookup"><span data-stu-id="0a8ec-107">For a comparison of `protected` with the other access modifiers, see [Accessibility Levels](accessibility-levels.md).</span></span>

## <a name="example"></a><span data-ttu-id="0a8ec-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="0a8ec-108">Example</span></span>

<span data-ttu-id="0a8ec-109">Un membre protégé d’une classe de base est accessible dans une classe dérivée uniquement si l’accès s’effectue par le biais du type de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-109">A protected member of a base class is accessible in a derived class only if the access occurs through the derived class type.</span></span> <span data-ttu-id="0a8ec-110">Prenons l’exemple de l’extrait de code suivant :</span><span class="sxs-lookup"><span data-stu-id="0a8ec-110">For example, consider the following code segment:</span></span>

[!code-csharp[csrefKeywordsModifiers#11](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#11)]

<span data-ttu-id="0a8ec-111">L’instruction `a.x = 10` génère une erreur, car elle est appelée dans la méthode statique Main, et pas dans une instance de la classe B.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-111">The statement `a.x = 10` generates an error because it is made within the static method Main, and not an instance of class B.</span></span>

<span data-ttu-id="0a8ec-112">Les membres de struct ne peuvent pas être protégés, car le struct ne peut pas être hérité.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-112">Struct members cannot be protected because the struct cannot be inherited.</span></span>

## <a name="example"></a><span data-ttu-id="0a8ec-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="0a8ec-113">Example</span></span>

<span data-ttu-id="0a8ec-114">Dans cet exemple, la classe `DerivedPoint` est dérivée de `Point`.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-114">In this example, the class `DerivedPoint` is derived from `Point`.</span></span> <span data-ttu-id="0a8ec-115">Vous pouvez donc accéder aux membres protégés de la classe de base directement à partir de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="0a8ec-115">Therefore, you can access the protected members of the base class directly from the derived class.</span></span>

[!code-csharp[csrefKeywordsModifiers#12](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsModifiers/CS/csrefKeywordsModifiers.cs#12)]  

<span data-ttu-id="0a8ec-116">Si vous changez les niveaux d’accès de `x` et `y` à [private](private.md), le compilateur affiche les messages d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="0a8ec-116">If you change the access levels of `x` and `y` to [private](private.md), the compiler will issue the error messages:</span></span>

`'Point.y' is inaccessible due to its protection level.`

`'Point.x' is inaccessible due to its protection level.`

## <a name="c-language-specification"></a><span data-ttu-id="0a8ec-117">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="0a8ec-117">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="0a8ec-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a8ec-118">See also</span></span>

- [<span data-ttu-id="0a8ec-119">Référence C#</span><span class="sxs-lookup"><span data-stu-id="0a8ec-119">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="0a8ec-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0a8ec-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="0a8ec-121">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="0a8ec-121">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="0a8ec-122">Modificateurs d’accès</span><span class="sxs-lookup"><span data-stu-id="0a8ec-122">Access Modifiers</span></span>](access-modifiers.md)
- [<span data-ttu-id="0a8ec-123">Niveaux d’accessibilité</span><span class="sxs-lookup"><span data-stu-id="0a8ec-123">Accessibility Levels</span></span>](accessibility-levels.md)
- [<span data-ttu-id="0a8ec-124">Modificateurs</span><span class="sxs-lookup"><span data-stu-id="0a8ec-124">Modifiers</span></span>](modifiers.md)
- [<span data-ttu-id="0a8ec-125">public</span><span class="sxs-lookup"><span data-stu-id="0a8ec-125">public</span></span>](public.md)
- [<span data-ttu-id="0a8ec-126">private</span><span class="sxs-lookup"><span data-stu-id="0a8ec-126">private</span></span>](private.md)
- [<span data-ttu-id="0a8ec-127">internal</span><span class="sxs-lookup"><span data-stu-id="0a8ec-127">internal</span></span>](internal.md)
- <span data-ttu-id="0a8ec-128">[Problèmes de sécurité pour les mots clés virtuels internes](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/heyd8kky(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="0a8ec-128">[Security concerns for internal virtual keywords](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/heyd8kky(v=vs.100))</span></span>