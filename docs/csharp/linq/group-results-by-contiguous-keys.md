---
title: Regrouper des résultats par clés contiguës
description: Comment regrouper des résultats par clés contiguës.
ms.date: 12/1/2016
ms.assetid: cbda9c08-151b-4c9e-82f7-c3d7f3dac66b
ms.openlocfilehash: a8d6ac133932a12154d5b23454065144c7652067
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33281435"
---
# <a name="group-results-by-contiguous-keys"></a><span data-ttu-id="29c1b-103">Regrouper des résultats par clés contiguës</span><span class="sxs-lookup"><span data-stu-id="29c1b-103">Group results by contiguous keys</span></span>

<span data-ttu-id="29c1b-104">L’exemple suivant montre comment regrouper des éléments dans des blocs représentant des sous-séquences de clés contiguës.</span><span class="sxs-lookup"><span data-stu-id="29c1b-104">The following example shows how to group elements into chunks that represent subsequences of contiguous keys.</span></span> <span data-ttu-id="29c1b-105">Par exemple, supposons que vous disposiez de la séquence de paires clé-valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="29c1b-105">For example, assume that you are given the following sequence of key-value pairs:</span></span>  
  
|<span data-ttu-id="29c1b-106">Touche</span><span class="sxs-lookup"><span data-stu-id="29c1b-106">Key</span></span>|<span data-ttu-id="29c1b-107">Value</span><span class="sxs-lookup"><span data-stu-id="29c1b-107">Value</span></span>|  
|---------|-----------|  
|<span data-ttu-id="29c1b-108">A</span><span class="sxs-lookup"><span data-stu-id="29c1b-108">A</span></span>|<span data-ttu-id="29c1b-109">Nous</span><span class="sxs-lookup"><span data-stu-id="29c1b-109">We</span></span>|  
|<span data-ttu-id="29c1b-110">A</span><span class="sxs-lookup"><span data-stu-id="29c1b-110">A</span></span>|<span data-ttu-id="29c1b-111">pensons</span><span class="sxs-lookup"><span data-stu-id="29c1b-111">think</span></span>|  
|<span data-ttu-id="29c1b-112">A</span><span class="sxs-lookup"><span data-stu-id="29c1b-112">A</span></span>|<span data-ttu-id="29c1b-113">que</span><span class="sxs-lookup"><span data-stu-id="29c1b-113">that</span></span>|  
|<span data-ttu-id="29c1b-114">B</span><span class="sxs-lookup"><span data-stu-id="29c1b-114">B</span></span>|<span data-ttu-id="29c1b-115">Linq</span><span class="sxs-lookup"><span data-stu-id="29c1b-115">Linq</span></span>|  
|<span data-ttu-id="29c1b-116">C</span><span class="sxs-lookup"><span data-stu-id="29c1b-116">C</span></span>|<span data-ttu-id="29c1b-117">est</span><span class="sxs-lookup"><span data-stu-id="29c1b-117">is</span></span>|  
|<span data-ttu-id="29c1b-118">A</span><span class="sxs-lookup"><span data-stu-id="29c1b-118">A</span></span>|<span data-ttu-id="29c1b-119">vraiment</span><span class="sxs-lookup"><span data-stu-id="29c1b-119">really</span></span>|  
|<span data-ttu-id="29c1b-120">B</span><span class="sxs-lookup"><span data-stu-id="29c1b-120">B</span></span>|<span data-ttu-id="29c1b-121">chouette</span><span class="sxs-lookup"><span data-stu-id="29c1b-121">cool</span></span>|  
|<span data-ttu-id="29c1b-122">B</span><span class="sxs-lookup"><span data-stu-id="29c1b-122">B</span></span>|<span data-ttu-id="29c1b-123">!</span><span class="sxs-lookup"><span data-stu-id="29c1b-123">!</span></span>|  
  
 <span data-ttu-id="29c1b-124">Les groupes suivants seront créés dans cet ordre :</span><span class="sxs-lookup"><span data-stu-id="29c1b-124">The following groups will be created in this order:</span></span>  
  
1.  <span data-ttu-id="29c1b-125">Nous, pensons, que</span><span class="sxs-lookup"><span data-stu-id="29c1b-125">We, think, that</span></span>  
  
2.  <span data-ttu-id="29c1b-126">Linq</span><span class="sxs-lookup"><span data-stu-id="29c1b-126">Linq</span></span>  
  
3.  <span data-ttu-id="29c1b-127">est</span><span class="sxs-lookup"><span data-stu-id="29c1b-127">is</span></span>  
  
4.  <span data-ttu-id="29c1b-128">vraiment</span><span class="sxs-lookup"><span data-stu-id="29c1b-128">really</span></span>  
  
5.  <span data-ttu-id="29c1b-129">chouette, !</span><span class="sxs-lookup"><span data-stu-id="29c1b-129">cool, !</span></span>  
  
 <span data-ttu-id="29c1b-130">La solution est implémentée comme une méthode d’extension thread-safe qui retourne ses résultats en continu.</span><span class="sxs-lookup"><span data-stu-id="29c1b-130">The solution is implemented as an extension method that is thread-safe and that returns its results in a streaming manner.</span></span> <span data-ttu-id="29c1b-131">En d’autres termes, elle produit ses groupes à mesure qu’elle se déplace dans la séquence source.</span><span class="sxs-lookup"><span data-stu-id="29c1b-131">In other words, it produces its groups as it moves through the source sequence.</span></span> <span data-ttu-id="29c1b-132">Contrairement aux opérateurs `group` ou `orderby`, elle peut commencer à retourner des groupes à l’appelant avant que l’intégralité de la séquence ait été lue.</span><span class="sxs-lookup"><span data-stu-id="29c1b-132">Unlike the `group` or `orderby` operators, it can begin returning groups to the caller before all of the sequence has been read.</span></span>  
  
 <span data-ttu-id="29c1b-133">La cohérence de thread est obtenue en effectuant une copie de chaque groupe ou bloc pendant l’itération de la séquence source, comme expliqué dans les commentaires du code source.</span><span class="sxs-lookup"><span data-stu-id="29c1b-133">Thread-safety is accomplished by making a copy of each group or chunk as the source sequence is iterated, as explained in the source code comments.</span></span> <span data-ttu-id="29c1b-134">Si la séquence source comporte une longue séquence d’éléments contigus, le common language runtime peut lever une <xref:System.OutOfMemoryException>.</span><span class="sxs-lookup"><span data-stu-id="29c1b-134">If the source sequence has a large sequence of contiguous items, the common language runtime may throw an <xref:System.OutOfMemoryException>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29c1b-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="29c1b-135">Example</span></span>  
 <span data-ttu-id="29c1b-136">L’exemple suivant montre la méthode d’extension et le code client qui l’utilise.</span><span class="sxs-lookup"><span data-stu-id="29c1b-136">The following example shows both the extension method and the client code that uses it.</span></span>  
  
 [!code-csharp[cscsrefContiguousGroups#1](../../../samples/snippets/csharp/concepts/linq/how-to-group-results-by-contiguous-keys_1.cs)]  
  
 <span data-ttu-id="29c1b-137">Pour utiliser la méthode d’extension dans votre projet, copiez la classe statique `MyExtensions` dans un fichier de code source nouveau ou existant et, si nécessaire, ajoutez une directive `using` pour l’espace de noms dans lequel elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="29c1b-137">To use the extension method in your project, copy the `MyExtensions` static class to a new or existing source code file and if it is required, add a `using` directive for the namespace where it is located.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29c1b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29c1b-138">See also</span></span>  
 [<span data-ttu-id="29c1b-139">Expressions de requête LINQ</span><span class="sxs-lookup"><span data-stu-id="29c1b-139">LINQ Query Expressions</span></span>](index.md)  
 
