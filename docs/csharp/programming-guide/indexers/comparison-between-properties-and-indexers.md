---
title: Comparaison entre propriétés et indexeurs (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- properties [C#], vs. indexers
- indexers [C#], vs. properties
ms.assetid: 3358a89f-44a0-4a4d-bf8c-07237a90af39
ms.openlocfilehash: a8b347be33ea6acbdf8a78a7af45fd3d0c27f8fb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33330370"
---
# <a name="comparison-between-properties-and-indexers-c-programming-guide"></a><span data-ttu-id="33fac-102">Comparaison entre propriétés et indexeurs (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="33fac-102">Comparison Between Properties and Indexers (C# Programming Guide)</span></span>
<span data-ttu-id="33fac-103">Les indexeurs sont semblables aux propriétés.</span><span class="sxs-lookup"><span data-stu-id="33fac-103">Indexers are like properties.</span></span> <span data-ttu-id="33fac-104">À l’exception des différences répertoriées dans le tableau suivant, toutes les règles définies pour les accesseurs des propriétés s’appliquent également aux accesseurs des indexeurs.</span><span class="sxs-lookup"><span data-stu-id="33fac-104">Except for the differences shown in the following table, all the rules that are defined for property accessors apply to indexer accessors also.</span></span>  
  
|<span data-ttu-id="33fac-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="33fac-105">Property</span></span>|<span data-ttu-id="33fac-106">Indexeur</span><span class="sxs-lookup"><span data-stu-id="33fac-106">Indexer</span></span>|  
|--------------|-------------|  
|<span data-ttu-id="33fac-107">Permet aux méthodes d’être appelées comme si elles étaient des membres de données publics.</span><span class="sxs-lookup"><span data-stu-id="33fac-107">Allows methods to be called as if they were public data members.</span></span>|<span data-ttu-id="33fac-108">Permet aux éléments d’une collection interne d’un objet d’être accessibles à l’aide de la notation de tableau sur l’objet lui-même.</span><span class="sxs-lookup"><span data-stu-id="33fac-108">Allows elements of an internal collection of an object to be accessed by using array notation on the object itself.</span></span>|  
|<span data-ttu-id="33fac-109">Accessible par le biais d’un nom simple.</span><span class="sxs-lookup"><span data-stu-id="33fac-109">Accessed through a simple name.</span></span>|<span data-ttu-id="33fac-110">Accessible par le biais d’un index.</span><span class="sxs-lookup"><span data-stu-id="33fac-110">Accessed through an index.</span></span>|  
|<span data-ttu-id="33fac-111">Peut être un membre statique ou un membre d’instance.</span><span class="sxs-lookup"><span data-stu-id="33fac-111">Can be a static or an instance member.</span></span>|<span data-ttu-id="33fac-112">Doit être un membre d’instance.</span><span class="sxs-lookup"><span data-stu-id="33fac-112">Must be an instance member.</span></span>|  
|<span data-ttu-id="33fac-113">Un accesseur [get](../../../csharp/language-reference/keywords/get.md) d’une propriété n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="33fac-113">A [get](../../../csharp/language-reference/keywords/get.md) accessor of a property has no parameters.</span></span>|<span data-ttu-id="33fac-114">Un accesseur `get` d’un indexeur possède la même liste de paramètres formels que l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="33fac-114">A `get` accessor of an indexer has the same formal parameter list as the indexer.</span></span>|  
|<span data-ttu-id="33fac-115">Un accesseur [set](../../../csharp/language-reference/keywords/set.md) d’une propriété contient le paramètre `value` implicite.</span><span class="sxs-lookup"><span data-stu-id="33fac-115">A [set](../../../csharp/language-reference/keywords/set.md) accessor of a property contains the implicit `value` parameter.</span></span>|<span data-ttu-id="33fac-116">Un accesseur `set` d’un indexeur possède la même liste de paramètres formels que l’indexeur, outre le paramètre [value](../../../csharp/language-reference/keywords/value.md).</span><span class="sxs-lookup"><span data-stu-id="33fac-116">A `set` accessor of an indexer has the same formal parameter list as the indexer, and also to the [value](../../../csharp/language-reference/keywords/value.md) parameter.</span></span>|  
|<span data-ttu-id="33fac-117">Prend en charge la syntaxe abrégée avec les [propriétés implémentées automatiquement](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md).</span><span class="sxs-lookup"><span data-stu-id="33fac-117">Supports shortened syntax with [Auto-Implemented Properties](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md).</span></span>|<span data-ttu-id="33fac-118">Ne prend pas en charge la syntaxe abrégée.</span><span class="sxs-lookup"><span data-stu-id="33fac-118">Does not support shortened syntax.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="33fac-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33fac-119">See Also</span></span>  
 [<span data-ttu-id="33fac-120">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="33fac-120">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="33fac-121">Indexeurs</span><span class="sxs-lookup"><span data-stu-id="33fac-121">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)  
 [<span data-ttu-id="33fac-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33fac-122">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)
