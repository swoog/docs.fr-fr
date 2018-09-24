---
title: Regrouper des résultats par clés contiguës (LINQ en C#)
description: Guide pratique pour regrouper des résultats par clés contiguës à l’aide de LINQ en C#.
ms.date: 08/14/2018
ms.assetid: cbda9c08-151b-4c9e-82f7-c3d7f3dac66b
ms.openlocfilehash: b5753c85bb07be4fc84b78a299eece961969ff9d
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46696952"
---
# <a name="group-results-by-contiguous-keys"></a><span data-ttu-id="1af66-103">Regrouper des résultats par clés contiguës</span><span class="sxs-lookup"><span data-stu-id="1af66-103">Group results by contiguous keys</span></span>

<span data-ttu-id="1af66-104">L’exemple suivant montre comment regrouper des éléments dans des blocs représentant des sous-séquences de clés contiguës.</span><span class="sxs-lookup"><span data-stu-id="1af66-104">The following example shows how to group elements into chunks that represent subsequences of contiguous keys.</span></span> <span data-ttu-id="1af66-105">Par exemple, supposons que vous disposiez de la séquence de paires clé-valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="1af66-105">For example, assume that you are given the following sequence of key-value pairs:</span></span>

|<span data-ttu-id="1af66-106">Touche</span><span class="sxs-lookup"><span data-stu-id="1af66-106">Key</span></span>|<span data-ttu-id="1af66-107">Value</span><span class="sxs-lookup"><span data-stu-id="1af66-107">Value</span></span>|
|---------|-----------|
|<span data-ttu-id="1af66-108">A</span><span class="sxs-lookup"><span data-stu-id="1af66-108">A</span></span>|<span data-ttu-id="1af66-109">Nous</span><span class="sxs-lookup"><span data-stu-id="1af66-109">We</span></span>|
|<span data-ttu-id="1af66-110">A</span><span class="sxs-lookup"><span data-stu-id="1af66-110">A</span></span>|<span data-ttu-id="1af66-111">pensons</span><span class="sxs-lookup"><span data-stu-id="1af66-111">think</span></span>|
|<span data-ttu-id="1af66-112">A</span><span class="sxs-lookup"><span data-stu-id="1af66-112">A</span></span>|<span data-ttu-id="1af66-113">que</span><span class="sxs-lookup"><span data-stu-id="1af66-113">that</span></span>|
|<span data-ttu-id="1af66-114">B</span><span class="sxs-lookup"><span data-stu-id="1af66-114">B</span></span>|<span data-ttu-id="1af66-115">Linq</span><span class="sxs-lookup"><span data-stu-id="1af66-115">Linq</span></span>|
|<span data-ttu-id="1af66-116">C</span><span class="sxs-lookup"><span data-stu-id="1af66-116">C</span></span>|<span data-ttu-id="1af66-117">est</span><span class="sxs-lookup"><span data-stu-id="1af66-117">is</span></span>|
|<span data-ttu-id="1af66-118">A</span><span class="sxs-lookup"><span data-stu-id="1af66-118">A</span></span>|<span data-ttu-id="1af66-119">vraiment</span><span class="sxs-lookup"><span data-stu-id="1af66-119">really</span></span>|
|<span data-ttu-id="1af66-120">B</span><span class="sxs-lookup"><span data-stu-id="1af66-120">B</span></span>|<span data-ttu-id="1af66-121">chouette</span><span class="sxs-lookup"><span data-stu-id="1af66-121">cool</span></span>|
|<span data-ttu-id="1af66-122">B</span><span class="sxs-lookup"><span data-stu-id="1af66-122">B</span></span>|<span data-ttu-id="1af66-123">!</span><span class="sxs-lookup"><span data-stu-id="1af66-123">!</span></span>|

<span data-ttu-id="1af66-124">Les groupes suivants seront créés dans cet ordre :</span><span class="sxs-lookup"><span data-stu-id="1af66-124">The following groups will be created in this order:</span></span>

1. <span data-ttu-id="1af66-125">Nous, pensons, que</span><span class="sxs-lookup"><span data-stu-id="1af66-125">We, think, that</span></span>

2. <span data-ttu-id="1af66-126">Linq</span><span class="sxs-lookup"><span data-stu-id="1af66-126">Linq</span></span>

3. <span data-ttu-id="1af66-127">est</span><span class="sxs-lookup"><span data-stu-id="1af66-127">is</span></span>

4. <span data-ttu-id="1af66-128">vraiment</span><span class="sxs-lookup"><span data-stu-id="1af66-128">really</span></span>

5. <span data-ttu-id="1af66-129">chouette, !</span><span class="sxs-lookup"><span data-stu-id="1af66-129">cool, !</span></span>

<span data-ttu-id="1af66-130">La solution est implémentée comme une méthode d’extension thread-safe qui retourne ses résultats en continu.</span><span class="sxs-lookup"><span data-stu-id="1af66-130">The solution is implemented as an extension method that is thread-safe and that returns its results in a streaming manner.</span></span> <span data-ttu-id="1af66-131">En d’autres termes, elle produit ses groupes à mesure qu’elle se déplace dans la séquence source.</span><span class="sxs-lookup"><span data-stu-id="1af66-131">In other words, it produces its groups as it moves through the source sequence.</span></span> <span data-ttu-id="1af66-132">Contrairement aux opérateurs `group` ou `orderby`, elle peut commencer à retourner des groupes à l’appelant avant que l’intégralité de la séquence ait été lue.</span><span class="sxs-lookup"><span data-stu-id="1af66-132">Unlike the `group` or `orderby` operators, it can begin returning groups to the caller before all of the sequence has been read.</span></span>

<span data-ttu-id="1af66-133">La cohérence de thread est obtenue en effectuant une copie de chaque groupe ou bloc pendant l’itération de la séquence source, comme expliqué dans les commentaires du code source.</span><span class="sxs-lookup"><span data-stu-id="1af66-133">Thread-safety is accomplished by making a copy of each group or chunk as the source sequence is iterated, as explained in the source code comments.</span></span> <span data-ttu-id="1af66-134">Si la séquence source comporte une longue séquence d’éléments contigus, le common language runtime peut lever une <xref:System.OutOfMemoryException>.</span><span class="sxs-lookup"><span data-stu-id="1af66-134">If the source sequence has a large sequence of contiguous items, the common language runtime may throw an <xref:System.OutOfMemoryException>.</span></span>

## <a name="example"></a><span data-ttu-id="1af66-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="1af66-135">Example</span></span>

<span data-ttu-id="1af66-136">L’exemple suivant montre la méthode d’extension et le code client qui l’utilise :</span><span class="sxs-lookup"><span data-stu-id="1af66-136">The following example shows both the extension method and the client code that uses it:</span></span>

[!code-csharp[cscsrefContiguousGroups#1](~/samples/snippets/csharp/concepts/linq/how-to-group-results-by-contiguous-keys_1.cs)]

<span data-ttu-id="1af66-137">Pour utiliser la méthode d’extension dans votre projet, copiez la classe statique `MyExtensions` dans un fichier de code source nouveau ou existant et, si nécessaire, ajoutez une directive `using` pour l’espace de noms dans lequel elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="1af66-137">To use the extension method in your project, copy the `MyExtensions` static class to a new or existing source code file and if it is required, add a `using` directive for the namespace where it is located.</span></span>

## <a name="see-also"></a><span data-ttu-id="1af66-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1af66-138">See also</span></span>

- [<span data-ttu-id="1af66-139">LINQ (Language Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="1af66-139">Language Integrated Query (LINQ)</span></span>](index.md)
