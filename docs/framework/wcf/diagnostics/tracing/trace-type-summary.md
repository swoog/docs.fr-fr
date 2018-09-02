---
title: Liste des types de suivis
ms.date: 03/30/2017
ms.assetid: e639410b-d1d1-479c-b78e-a4701d4e4085
ms.openlocfilehash: 73777df2b58b14947c416ce409bcb42d439499ec
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43403841"
---
# <a name="trace-type-summary"></a><span data-ttu-id="28dc1-102">Liste des types de suivis</span><span class="sxs-lookup"><span data-stu-id="28dc1-102">Trace Type Summary</span></span>
<span data-ttu-id="28dc1-103">[Niveaux de source](https://go.microsoft.com/fwlink/?LinkID=94943) définit différents niveaux de suivi : critique, erreur, avertissement, Information et Verbose, et fournit une description de la `ActivityTracing` indicateur qui active ou désactive la sortie de traçage des événements de transfert de limite et d’activité.</span><span class="sxs-lookup"><span data-stu-id="28dc1-103">[Source Levels](https://go.microsoft.com/fwlink/?LinkID=94943) defines various trace levels: Critical, Error, Warning, Information, and Verbose, as well as provides description of the `ActivityTracing` flag, which toggles the output of trace boundary and activity transfer events.</span></span>  
  
 <span data-ttu-id="28dc1-104">Vous pouvez également consulter [TraceEventType](https://go.microsoft.com/fwlink/?LinkId=95169) pour les types de suivis qui peuvent être émis à partir de <xref:System.Diagnostics>.</span><span class="sxs-lookup"><span data-stu-id="28dc1-104">You can also review [TraceEventType](https://go.microsoft.com/fwlink/?LinkId=95169) for the types of traces which can be emitted from <xref:System.Diagnostics>.</span></span>  
  
 <span data-ttu-id="28dc1-105">Le tableau suivant répertorie les plus importants.</span><span class="sxs-lookup"><span data-stu-id="28dc1-105">The following table lists the most important ones.</span></span>  
  
|<span data-ttu-id="28dc1-106">Type de suivi</span><span class="sxs-lookup"><span data-stu-id="28dc1-106">Trace Type</span></span>|<span data-ttu-id="28dc1-107">Description</span><span class="sxs-lookup"><span data-stu-id="28dc1-107">Description</span></span>|  
|----------------|-----------------|  
|<span data-ttu-id="28dc1-108">Critical</span><span class="sxs-lookup"><span data-stu-id="28dc1-108">Critical</span></span>|<span data-ttu-id="28dc1-109">Erreur irrécupérable ou panne d'application.</span><span class="sxs-lookup"><span data-stu-id="28dc1-109">Fatal error or application crash.</span></span>|  
|<span data-ttu-id="28dc1-110">Erreur</span><span class="sxs-lookup"><span data-stu-id="28dc1-110">Error</span></span>|<span data-ttu-id="28dc1-111">Erreur récupérable.</span><span class="sxs-lookup"><span data-stu-id="28dc1-111">Recoverable error.</span></span>|  
|<span data-ttu-id="28dc1-112">Warning</span><span class="sxs-lookup"><span data-stu-id="28dc1-112">Warning</span></span>|<span data-ttu-id="28dc1-113">Message d'informations.</span><span class="sxs-lookup"><span data-stu-id="28dc1-113">Informational message.</span></span>|  
|<span data-ttu-id="28dc1-114">Information</span><span class="sxs-lookup"><span data-stu-id="28dc1-114">Information</span></span>|<span data-ttu-id="28dc1-115">Problème non critique.</span><span class="sxs-lookup"><span data-stu-id="28dc1-115">Non-critical problem.</span></span>|  
|<span data-ttu-id="28dc1-116">Verbose</span><span class="sxs-lookup"><span data-stu-id="28dc1-116">Verbose</span></span>|<span data-ttu-id="28dc1-117">Suivi de débogage.</span><span class="sxs-lookup"><span data-stu-id="28dc1-117">Debugging trace.</span></span>|  
|<span data-ttu-id="28dc1-118">Start</span><span class="sxs-lookup"><span data-stu-id="28dc1-118">Start</span></span>|<span data-ttu-id="28dc1-119">Démarrage d'une unité logique de traitement.</span><span class="sxs-lookup"><span data-stu-id="28dc1-119">Starting of a logical unit of processing.</span></span>|  
|<span data-ttu-id="28dc1-120">Interrompre</span><span class="sxs-lookup"><span data-stu-id="28dc1-120">Suspend</span></span>|<span data-ttu-id="28dc1-121">Interruption d'une unité logique de traitement.</span><span class="sxs-lookup"><span data-stu-id="28dc1-121">Suspension of a logical unit of processing.</span></span>|  
|<span data-ttu-id="28dc1-122">Reprendre</span><span class="sxs-lookup"><span data-stu-id="28dc1-122">Resume</span></span>|<span data-ttu-id="28dc1-123">Reprise d'une unité logique de traitement.</span><span class="sxs-lookup"><span data-stu-id="28dc1-123">Resumption of a logical unit of processing.</span></span>|  
|<span data-ttu-id="28dc1-124">Arrêter</span><span class="sxs-lookup"><span data-stu-id="28dc1-124">Stop</span></span>|<span data-ttu-id="28dc1-125">Arrêt d'une unité logique de traitement.</span><span class="sxs-lookup"><span data-stu-id="28dc1-125">Stopping of a logical unit of processing.</span></span>|  
|<span data-ttu-id="28dc1-126">Transférer</span><span class="sxs-lookup"><span data-stu-id="28dc1-126">Transfer</span></span>|<span data-ttu-id="28dc1-127">Changement d'identité de corrélation.</span><span class="sxs-lookup"><span data-stu-id="28dc1-127">Changing of correlation identity.</span></span>|  
  
 <span data-ttu-id="28dc1-128">Une activité est définie comme une combinaison des types de suivi ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="28dc1-128">An activity is defined as a combination of the trace types above.</span></span>  
  
 <span data-ttu-id="28dc1-129">Le code suivant est une expression régulière qui définit une activité idéale dans une étendue locale (source de suivi).</span><span class="sxs-lookup"><span data-stu-id="28dc1-129">The following is a regular expression that defines an ideal activity in a local (trace source) scope,</span></span>  
  
 `R = Start (Critical | Error | Warning | Information | Verbose | Transfer | (Transfer Suspend Transfer Resume) )* Stop`  
  
 <span data-ttu-id="28dc1-130">Cela signifie qu'une activité doit remplir les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="28dc1-130">This means that an activity must satisfy the following conditions.</span></span>  
  
-   <span data-ttu-id="28dc1-131">Elle doit respectivement démarrer et s'arrêter avec les suivis Démarrer et Arrêter.</span><span class="sxs-lookup"><span data-stu-id="28dc1-131">It must start and stop respectively by a Start and Stop traces</span></span>  
  
-   <span data-ttu-id="28dc1-132">Elle doit contenir un suivi Transfert immédiatement avant un suivi Interrompre ou Reprendre.</span><span class="sxs-lookup"><span data-stu-id="28dc1-132">It must have a Transfer trace immediately preceding a Suspend or Resume trace</span></span>  
  
-   <span data-ttu-id="28dc1-133">Elle ne doit pas contenir de suivi entre les suivis Interrompre et Reprendre, s'ils existent.</span><span class="sxs-lookup"><span data-stu-id="28dc1-133">It must not have any traces between the Suspend and Resume traces if such traces exist</span></span>  
  
-   <span data-ttu-id="28dc1-134">Elle peut contenir n'importe quel type de suivi Critique/Avertissement/Informations/Commentaires/Transfert, en nombre illimité, tant que les conditions précédentes sont observées.</span><span class="sxs-lookup"><span data-stu-id="28dc1-134">It can have any and as many of critical/Error/Warning/Information/Verbose/Transfer traces as long as the previous conditions are observed</span></span>  
  
 <span data-ttu-id="28dc1-135">Le code suivant est une expression régulière qui définit une activité idéale dans la portée globale,</span><span class="sxs-lookup"><span data-stu-id="28dc1-135">The following is a regular expression that defines an ideal activity in the global scope,</span></span>  
  
```  
R+   
```  
  
 <span data-ttu-id="28dc1-136">R étant l'expression régulière d'une activité dans l'étendue locale.</span><span class="sxs-lookup"><span data-stu-id="28dc1-136">with R being the regular expression for an activity in the local scope.</span></span> <span data-ttu-id="28dc1-137">Cela se traduit par :</span><span class="sxs-lookup"><span data-stu-id="28dc1-137">This translates to,</span></span>  
  
```  
[R+ = Start ( Critical | Error | Warning | Information | Verbose | Transfer | (Transfer Suspend Transfer Resume) )* Stop]+  
```
