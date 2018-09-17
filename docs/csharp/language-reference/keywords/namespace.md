---
title: namespace, mot clé (référence C#)
ms.date: 07/20/2015
f1_keywords:
- namespace_CSharpKeyword
- namespace
helpviewer_keywords:
- namespace keyword [C#]
- scope [C#]
ms.assetid: 0a788423-9110-42e0-97d9-bda41ca4870f
ms.openlocfilehash: 2cdc1e33d86dae675411b571e553b467e5c1f891
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43856424"
---
# <a name="namespace-c-reference"></a><span data-ttu-id="9ecb8-102">namespace (référence C#)</span><span class="sxs-lookup"><span data-stu-id="9ecb8-102">namespace (C# Reference)</span></span>

<span data-ttu-id="9ecb8-103">Le mot clé `namespace` est utilisé pour déclarer une portée qui contient un ensemble d’objets connexes.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-103">The `namespace` keyword is used to declare a scope that contains a set of related objects.</span></span> <span data-ttu-id="9ecb8-104">Vous pouvez utiliser un espace de noms pour organiser les éléments de code et créer des types globaux uniques.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-104">You can use a namespace to organize code elements and to create globally unique types.</span></span>

[!code-csharp[csrefKeywordsNamespace#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsNamespace/CS/csrefKeywordsNamespace.cs#1)]

## <a name="remarks"></a><span data-ttu-id="9ecb8-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9ecb8-105">Remarks</span></span>

<span data-ttu-id="9ecb8-106">Dans un espace de noms, vous pouvez déclarer zéro ou plusieurs des types suivants :</span><span class="sxs-lookup"><span data-stu-id="9ecb8-106">Within a namespace, you can declare zero or more of the following types:</span></span>

- <span data-ttu-id="9ecb8-107">autre espace de noms</span><span class="sxs-lookup"><span data-stu-id="9ecb8-107">another namespace</span></span>

- [<span data-ttu-id="9ecb8-108">class</span><span class="sxs-lookup"><span data-stu-id="9ecb8-108">class</span></span>](class.md)

- [<span data-ttu-id="9ecb8-109">interface</span><span class="sxs-lookup"><span data-stu-id="9ecb8-109">interface</span></span>](interface.md)

- [<span data-ttu-id="9ecb8-110">struct</span><span class="sxs-lookup"><span data-stu-id="9ecb8-110">struct</span></span>](struct.md)

- [<span data-ttu-id="9ecb8-111">enum</span><span class="sxs-lookup"><span data-stu-id="9ecb8-111">enum</span></span>](enum.md)

- [<span data-ttu-id="9ecb8-112">delegate</span><span class="sxs-lookup"><span data-stu-id="9ecb8-112">delegate</span></span>](delegate.md)

<span data-ttu-id="9ecb8-113">Le compilateur ajoute un espace de noms par défaut, que vous déclariez ou non explicitement un espace de noms dans un fichier source C#.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-113">Whether or not you explicitly declare a namespace in a C# source file, the compiler adds a default namespace.</span></span> <span data-ttu-id="9ecb8-114">Cet espace de noms sans nom, parfois appelé espace de noms global, est présent dans chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-114">This unnamed namespace, sometimes referred to as the global namespace, is present in every file.</span></span> <span data-ttu-id="9ecb8-115">Tout identificateur dans l’espace de noms global peut être utilisé dans un espace de noms nommé.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-115">Any identifier in the global namespace is available for use in a named namespace.</span></span>

<span data-ttu-id="9ecb8-116">Les espaces de noms ont implicitement un accès public, et cela n’est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-116">Namespaces implicitly have public access and this is not modifiable.</span></span> <span data-ttu-id="9ecb8-117">Consultez [Modificateurs d’accès](access-modifiers.md) pour connaître les modificateurs d’accès que vous pouvez assigner à des éléments dans un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-117">For a discussion of the access modifiers you can assign to elements in a namespace, see [Access Modifiers](access-modifiers.md).</span></span>

<span data-ttu-id="9ecb8-118">Il est possible de définir un espace de noms dans deux déclarations ou plus.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-118">It is possible to define a namespace in two or more declarations.</span></span> <span data-ttu-id="9ecb8-119">Par exemple, l’exemple suivant définit deux classes comme appartenant à l’espace de noms `MyCompany` :</span><span class="sxs-lookup"><span data-stu-id="9ecb8-119">For example, the following example defines two classes as part of the `MyCompany` namespace:</span></span>

[!code-csharp[csrefKeywordsNamespace#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsNamespace/CS/csrefKeywordsNamespace.cs#2)]

## <a name="example"></a><span data-ttu-id="9ecb8-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="9ecb8-120">Example</span></span>

<span data-ttu-id="9ecb8-121">L’exemple suivant montre comment appeler une méthode statique dans un espace de noms imbriqué.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-121">The following example shows how to call a static method in a nested namespace.</span></span>

[!code-csharp[csrefKeywordsNamespace#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsNamespace/CS/csrefKeywordsNamespace.cs#3)]

## <a name="related-resources"></a><span data-ttu-id="9ecb8-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9ecb8-122">Related resources</span></span>

<span data-ttu-id="9ecb8-123">Pour plus d’informations sur l’utilisation des espaces de noms, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="9ecb8-123">For more information about using namespaces, see the following topics:</span></span>

- [<span data-ttu-id="9ecb8-124">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="9ecb8-124">Namespaces</span></span>](../../programming-guide/namespaces/index.md)

- [<span data-ttu-id="9ecb8-125">Utilisation d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="9ecb8-125">Using Namespaces</span></span>](../../programming-guide/namespaces/using-namespaces.md)

- [<span data-ttu-id="9ecb8-126">Comment : utiliser l’alias d’espace de noms global</span><span class="sxs-lookup"><span data-stu-id="9ecb8-126">How to: Use the Global Namespace Alias</span></span>](../../programming-guide/namespaces/how-to-use-the-global-namespace-alias.md)

## <a name="c-language-specification"></a><span data-ttu-id="9ecb8-127">spécification du langage C#</span><span class="sxs-lookup"><span data-stu-id="9ecb8-127">C# language specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="9ecb8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ecb8-128">See also</span></span>

- [<span data-ttu-id="9ecb8-129">Référence C#</span><span class="sxs-lookup"><span data-stu-id="9ecb8-129">C# Reference</span></span>](../../language-reference/index.md)
- [<span data-ttu-id="9ecb8-130">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9ecb8-130">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="9ecb8-131">Mots clés C#</span><span class="sxs-lookup"><span data-stu-id="9ecb8-131">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="9ecb8-132">Mots clés d’espaces de noms</span><span class="sxs-lookup"><span data-stu-id="9ecb8-132">Namespace Keywords</span></span>](namespace-keywords.md)
- [<span data-ttu-id="9ecb8-133">using</span><span class="sxs-lookup"><span data-stu-id="9ecb8-133">using</span></span>](using.md)