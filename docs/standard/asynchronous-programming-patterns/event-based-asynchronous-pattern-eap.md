---
title: Modèle asynchrone basé sur les événements (EAP)
ms.date: 07/23/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- asynchronous calls
- asynchronous programming, design patterns
- asynchronous programming
ms.assetid: c6baed9f-2a25-4728-9a9a-53b7b14840cf
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7811113244d8c5f7d79a55ebb01f04e99e9bd2a6
ms.sourcegitcommit: e8dc507cfdaad504fc9d4c83d28d24569dcef91c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/03/2018
ms.locfileid: "33567804"
---
# <a name="event-based-asynchronous-pattern-eap"></a><span data-ttu-id="03e24-102">Modèle asynchrone basé sur les événements (EAP)</span><span class="sxs-lookup"><span data-stu-id="03e24-102">Event-based Asynchronous Pattern (EAP)</span></span>

<span data-ttu-id="03e24-103">Il existe plusieurs façons d’exposer des fonctionnalités asynchrones à du code client.</span><span class="sxs-lookup"><span data-stu-id="03e24-103">There are a number of ways to expose asynchronous features to client code.</span></span> <span data-ttu-id="03e24-104">Le modèle asynchrone basé sur les événements recommande une méthode pour obtenir des classes un comportement asynchrone.</span><span class="sxs-lookup"><span data-stu-id="03e24-104">The Event-based Asynchronous Pattern prescribes one way for classes to present asynchronous behavior.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="03e24-105">À compter du .NET Framework 4, la bibliothèque parallèle de tâches propose un nouveau modèle pour la programmation asynchrone et parallèle.</span><span class="sxs-lookup"><span data-stu-id="03e24-105">Starting with the .NET Framework 4, the Task Parallel Library provides a new model for asynchronous and parallel programming.</span></span> <span data-ttu-id="03e24-106">Pour plus d’informations, consultez [Bibliothèque parallèle de tâches](../parallel-programming/task-parallel-library-tpl.md) et [Modèle asynchrone basé sur les tâches (TAP, Task-based Asynchronous Pattern)](task-based-asynchronous-pattern-tap.md).</span><span class="sxs-lookup"><span data-stu-id="03e24-106">For more information, see [Task Parallel Library (TPL)](../parallel-programming/task-parallel-library-tpl.md) and [Task-based Asynchronous Pattern (TAP)](task-based-asynchronous-pattern-tap.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="03e24-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="03e24-107">In This Section</span></span>

 [<span data-ttu-id="03e24-108">Vue d’ensemble du modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="03e24-108">Event-based Asynchronous Pattern Overview</span></span>](event-based-asynchronous-pattern-overview.md)  
 <span data-ttu-id="03e24-109">Explique comment le modèle asynchrone basé sur les événements permet de profiter des avantages des applications multithread tout en masquant de nombreux problèmes complexes inhérents à la conception multithread.</span><span class="sxs-lookup"><span data-stu-id="03e24-109">Describes how the Event-based Asynchronous Pattern makes available the advantages of multithreaded applications while hiding many of the complex issues inherent in multithreaded design.</span></span>  
  
 [<span data-ttu-id="03e24-110">Implémentation du modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="03e24-110">Implementing the Event-based Asynchronous Pattern</span></span>](implementing-the-event-based-asynchronous-pattern.md)  
 <span data-ttu-id="03e24-111">Décrit la façon standardisée de placer dans un package une classe qui possède des fonctionnalités asynchrones.</span><span class="sxs-lookup"><span data-stu-id="03e24-111">Describes the standardized way to package a class that has asynchronous features.</span></span>  
  
 [<span data-ttu-id="03e24-112">Meilleures pratiques pour implémenter le modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="03e24-112">Best Practices for Implementing the Event-based Asynchronous Pattern</span></span>](best-practices-for-implementing-the-event-based-asynchronous-pattern.md)  
 <span data-ttu-id="03e24-113">Décrit les exigences liées à l’exposition de fonctionnalités asynchrones conformément au modèle asynchrone basé sur les événements.</span><span class="sxs-lookup"><span data-stu-id="03e24-113">Describes the requirements for exposing asynchronous features according to the Event-based Asynchronous Pattern.</span></span>  
  
 [<span data-ttu-id="03e24-114">Choix du moment auquel implémenter le modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="03e24-114">Deciding When to Implement the Event-based Asynchronous Pattern</span></span>](deciding-when-to-implement-the-event-based-asynchronous-pattern.md)  
 <span data-ttu-id="03e24-115">Explique comment savoir quand vous devez implémenter le modèle asynchrone basé sur les événements au lieu du modèle <xref:System.IAsyncResult> représenté par le [ modèle de programmation asynchrone (APM)](asynchronous-programming-model-apm.md).</span><span class="sxs-lookup"><span data-stu-id="03e24-115">Describes how to determine when you should choose to implement the Event-based Asynchronous Pattern instead of the <xref:System.IAsyncResult> pattern represented by the [Asynchronous Programming Model (APM)](asynchronous-programming-model-apm.md)</span></span>
  
 [<span data-ttu-id="03e24-116">Guide pratique pour implémenter un composant qui prend en charge le modèle asynchrone basé sur des événements</span><span class="sxs-lookup"><span data-stu-id="03e24-116">How to: Implement a Component That Supports the Event-based Asynchronous Pattern</span></span>](component-that-supports-the-event-based-asynchronous-pattern.md)  
 <span data-ttu-id="03e24-117">Décrit comment créer un composant qui implémente le modèle asynchrone basé sur les événements.</span><span class="sxs-lookup"><span data-stu-id="03e24-117">Describes how to create a component that implements the Event-based Asynchronous Pattern.</span></span> <span data-ttu-id="03e24-118">Il est implémenté à l'aide de classes d'assistance à partir de l'espace de noms <xref:System.ComponentModel?displayProperty=nameWithType>, ce qui garantit le bon fonctionnement du composant avec n'importe quel modèle d'application.</span><span class="sxs-lookup"><span data-stu-id="03e24-118">It is implemented using helper classes from the <xref:System.ComponentModel?displayProperty=nameWithType> namespace, which ensures that the component works correctly under any application model.</span></span>  

 [<span data-ttu-id="03e24-119">Guide pratique pour implémenter un client du modèle asynchrone basé sur des événements</span><span class="sxs-lookup"><span data-stu-id="03e24-119">How to: Implement a Client of the Event-based Asynchronous Pattern</span></span>](how-to-implement-a-client-of-the-event-based-asynchronous-pattern.md)  
 <span data-ttu-id="03e24-120">Décrit comment créer un client qui utilise un composant implémentant le modèle asynchrone basé sur les événements.</span><span class="sxs-lookup"><span data-stu-id="03e24-120">Describes how to create a client that uses a component that implements the Event-based Asynchronous Pattern.</span></span>
  
 [<span data-ttu-id="03e24-121">Guide pratique : utiliser des composants qui prennent en charge le modèle asynchrone basé sur les événements</span><span class="sxs-lookup"><span data-stu-id="03e24-121">How to: Use Components That Support the Event-based Asynchronous Pattern</span></span>](how-to-use-components-that-support-the-event-based-asynchronous-pattern.md)  
 <span data-ttu-id="03e24-122">Explique comment créer un composant qui prend en charge le modèle asynchrone basé sur les événements.</span><span class="sxs-lookup"><span data-stu-id="03e24-122">Describes how to use a component that supports the Event-based Asynchronous Pattern.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="03e24-123">Référence</span><span class="sxs-lookup"><span data-stu-id="03e24-123">Reference</span></span>

 <xref:System.ComponentModel.AsyncOperation>  
 <span data-ttu-id="03e24-124">Décrit la classe <xref:System.ComponentModel.AsyncOperation> et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="03e24-124">Describes the <xref:System.ComponentModel.AsyncOperation> class and has links to all its members.</span></span>  
  
 <xref:System.ComponentModel.AsyncOperationManager>  
 <span data-ttu-id="03e24-125">Décrit la classe <xref:System.ComponentModel.AsyncOperationManager> et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="03e24-125">Describes the <xref:System.ComponentModel.AsyncOperationManager> class and has links to all its members.</span></span>  
  
 <xref:System.ComponentModel.BackgroundWorker>  
 <span data-ttu-id="03e24-126">Décrit le composant <xref:System.ComponentModel.BackgroundWorker> et propose des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="03e24-126">Describes the <xref:System.ComponentModel.BackgroundWorker> component and has links to all its members.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="03e24-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03e24-127">Related Sections</span></span>

 [<span data-ttu-id="03e24-128">La bibliothèque parallèle de tâches</span><span class="sxs-lookup"><span data-stu-id="03e24-128">Task Parallel Library (TPL)</span></span>](../parallel-programming/task-parallel-library-tpl.md)  
 <span data-ttu-id="03e24-129">Décrit un modèle de programmation pour les opérations asynchrones et parallèles.</span><span class="sxs-lookup"><span data-stu-id="03e24-129">Describes a programming model for asynchronous and parallel operations.</span></span>  
  
 [<span data-ttu-id="03e24-130">Thread</span><span class="sxs-lookup"><span data-stu-id="03e24-130">Threading</span></span>](../../../docs/standard/threading/index.md)  
 <span data-ttu-id="03e24-131">Décrit les fonctionnalités de multithreading dans .NET.</span><span class="sxs-lookup"><span data-stu-id="03e24-131">Describes multithreading features in .NET.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03e24-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03e24-132">See also</span></span>

 [<span data-ttu-id="03e24-133">Bonnes pratiques de threading géré</span><span class="sxs-lookup"><span data-stu-id="03e24-133">Managed Threading Best Practices</span></span>](../threading/managed-threading-best-practices.md)  
 [<span data-ttu-id="03e24-134">Événements</span><span class="sxs-lookup"><span data-stu-id="03e24-134">Events</span></span>](../events/index.md)  
 [<span data-ttu-id="03e24-135">Modèles de conception de la programmation asynchrone</span><span class="sxs-lookup"><span data-stu-id="03e24-135">Asynchronous Programming Design Patterns</span></span>](index.md)
