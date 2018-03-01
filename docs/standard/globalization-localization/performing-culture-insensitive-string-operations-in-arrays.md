---
title: "Exécution d'opérations de chaînes indépendantes de la culture dans des tableaux"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- culture-insensitive string operations, in arrays
- arrays [.NET Framework], culture-insensitive string operations
- comparer parameter
ms.assetid: f12922e1-6234-4165-8896-63f0653ab478
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: d273fbaa792092f5ea56bfa59392794b6728ed67
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="performing-culture-insensitive-string-operations-in-arrays"></a><span data-ttu-id="7a1f8-102">Exécution d'opérations de chaînes indépendantes de la culture dans des tableaux</span><span class="sxs-lookup"><span data-stu-id="7a1f8-102">Performing Culture-Insensitive String Operations in Arrays</span></span>
<span data-ttu-id="7a1f8-103">Les surcharges des méthodes <xref:System.Array.Sort%2A?displayProperty=nameWithType> et <xref:System.Array.BinarySearch%2A?displayProperty=nameWithType> effectuent des tris dépendants de la culture par défaut à l’aide de la propriété <xref:System.Threading.Thread.CurrentCulture%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-103">Overloads of the <xref:System.Array.Sort%2A?displayProperty=nameWithType> and <xref:System.Array.BinarySearch%2A?displayProperty=nameWithType> methods perform culture-sensitive sorts by default using the <xref:System.Threading.Thread.CurrentCulture%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="7a1f8-104">Les résultats dépendants de la culture retournés par ces méthodes peuvent varier selon la culture en raison de différences dans les ordres de tri.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-104">Culture-sensitive results returned by these methods can vary by culture due to differences in sort orders.</span></span> <span data-ttu-id="7a1f8-105">Pour supprimer un comportement dépendant de la culture, utilisez l’une des surcharges de cette méthode qui accepte un paramètre `comparer`.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-105">To eliminate culture-sensitive behavior, use one of the overloads of this method that accepts a `comparer` parameter.</span></span> <span data-ttu-id="7a1f8-106">Le paramètre `comparer` spécifie l’implémentation <xref:System.Collections.IComparer> à utiliser lors de la comparaison d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-106">The `comparer` parameter specifies the <xref:System.Collections.IComparer> implementation to use when comparing elements in the array.</span></span> <span data-ttu-id="7a1f8-107">Pour le paramètre, spécifiez une classe de comparateur indifférent personnalisée qui utilise <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-107">For the parameter, specify a custom invariant comparer class that uses <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="7a1f8-108">Un exemple d’une classe de comparateur indifférent personnalisée est fourni dans la sous-rubrique « Utilisation de la classe SortedList » de la rubrique [Exécution d'opérations de chaînes indépendantes de la culture dans des collections](../../../docs/standard/globalization-localization/performing-culture-insensitive-string-operations-in-collections.md).</span><span class="sxs-lookup"><span data-stu-id="7a1f8-108">An example of a custom invariant comparer class is provided in the "Using the SortedList Class" subtopic of the [Performing Culture-Insensitive String Operations in Collections](../../../docs/standard/globalization-localization/performing-culture-insensitive-string-operations-in-collections.md) topic.</span></span>  
  
 <span data-ttu-id="7a1f8-109">**Remarque** La transmission de **CultureInfo.InvariantCulture** à une méthode de comparaison effectue une comparaison indépendante de la culture.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-109">**Note** Passing **CultureInfo.InvariantCulture** to a comparison method does perform a culture-insensitive comparison.</span></span> <span data-ttu-id="7a1f8-110">Toutefois, elle n’entraîne pas une comparaison non linguistique, par exemple, pour les chemins d’accès de fichier, les clés de Registre et les variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-110">However, it does not cause a non-linguistic comparison, for example, for file paths, registry keys, and environment variables.</span></span> <span data-ttu-id="7a1f8-111">Elle ne prend pas non plus en charge les décisions de sécurité basées sur le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-111">Neither does it support security decisions based on the comparison result.</span></span> <span data-ttu-id="7a1f8-112">Pour une comparaison non linguistique ou la prise en charge des décisions de sécurité basées sur le résultat, l’application doit utiliser une méthode de comparaison qui accepte une valeur <xref:System.StringComparison>.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-112">For a non-linguistic comparison or support for result-based security decisions, the application should use a comparison method that accepts a <xref:System.StringComparison> value.</span></span> <span data-ttu-id="7a1f8-113">L’application doit ensuite transmettre <xref:System.StringComparison.Ordinal>.</span><span class="sxs-lookup"><span data-stu-id="7a1f8-113">The application should then pass <xref:System.StringComparison.Ordinal>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a1f8-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a1f8-114">See Also</span></span>  
 <xref:System.Array.Sort%2A?displayProperty=nameWithType>  
 <xref:System.Array.BinarySearch%2A?displayProperty=nameWithType>  
 <xref:System.Collections.IComparer>  
 [<span data-ttu-id="7a1f8-115">Exécution d'opérations de chaînes indépendantes de la culture</span><span class="sxs-lookup"><span data-stu-id="7a1f8-115">Performing Culture-Insensitive String Operations</span></span>](../../../docs/standard/globalization-localization/performing-culture-insensitive-string-operations.md)
