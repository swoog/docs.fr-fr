---
title: 1148 - FlowchartSwitchCaseNotFound
ms.date: 03/30/2017
ms.assetid: 9ee7fcee-e040-4306-968e-ed840a1cb00c
ms.openlocfilehash: 7e96b5b7652d404e6fdbe2c04c6a4069ca78f20f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62009914"
---
# <a name="1148---flowchartswitchcasenotfound"></a><span data-ttu-id="420ae-102">1148 - FlowchartSwitchCaseNotFound</span><span class="sxs-lookup"><span data-stu-id="420ae-102">1148 - FlowchartSwitchCaseNotFound</span></span>
## <a name="properties"></a><span data-ttu-id="420ae-103">Properties</span><span class="sxs-lookup"><span data-stu-id="420ae-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="420ae-104">Id</span><span class="sxs-lookup"><span data-stu-id="420ae-104">ID</span></span>|<span data-ttu-id="420ae-105">1148</span><span class="sxs-lookup"><span data-stu-id="420ae-105">1148</span></span>|  
|<span data-ttu-id="420ae-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="420ae-106">Keywords</span></span>|<span data-ttu-id="420ae-107">WFActivities</span><span class="sxs-lookup"><span data-stu-id="420ae-107">WFActivities</span></span>|  
|<span data-ttu-id="420ae-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="420ae-108">Level</span></span>|<span data-ttu-id="420ae-109">Information</span><span class="sxs-lookup"><span data-stu-id="420ae-109">Information</span></span>|  
|<span data-ttu-id="420ae-110">Canal</span><span class="sxs-lookup"><span data-stu-id="420ae-110">Channel</span></span>|<span data-ttu-id="420ae-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="420ae-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="420ae-112">Description</span><span class="sxs-lookup"><span data-stu-id="420ae-112">Description</span></span>  
 <span data-ttu-id="420ae-113">Indique qu'une correspondance de cas ou un cas par défaut est introuvable dans un organigramme.</span><span class="sxs-lookup"><span data-stu-id="420ae-113">Indicates that neither a matching case or a default case in a Flowchart switch could be found.</span></span> <span data-ttu-id="420ae-114">L'exécution de Flowchart va se terminer.</span><span class="sxs-lookup"><span data-stu-id="420ae-114">Flowchart execution will end.</span></span>  
  
## <a name="message"></a><span data-ttu-id="420ae-115">Message</span><span class="sxs-lookup"><span data-stu-id="420ae-115">Message</span></span>  
 <span data-ttu-id="420ae-116">Flowchart « %1 »/FlowSwitch - impossible de trouver l'activité Case ou un cas par défaut correspondant au résultat de l'expression.</span><span class="sxs-lookup"><span data-stu-id="420ae-116">Flowchart '%1'/FlowSwitch - could find neither a Case activity nor a Default Case matching the Expression result.</span></span> <span data-ttu-id="420ae-117">L'exécution de Flowchart va se terminer.</span><span class="sxs-lookup"><span data-stu-id="420ae-117">Flowchart execution will end.</span></span>  
  
## <a name="details"></a><span data-ttu-id="420ae-118">Détails</span><span class="sxs-lookup"><span data-stu-id="420ae-118">Details</span></span>  
  
|<span data-ttu-id="420ae-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="420ae-119">Data Item Name</span></span>|<span data-ttu-id="420ae-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="420ae-120">Data Item Type</span></span>|<span data-ttu-id="420ae-121">Description</span><span class="sxs-lookup"><span data-stu-id="420ae-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="420ae-122">Organigramme</span><span class="sxs-lookup"><span data-stu-id="420ae-122">FlowChart</span></span>|<span data-ttu-id="420ae-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="420ae-123">xs:string</span></span>|<span data-ttu-id="420ae-124">Nom complet de l'organigramme.</span><span class="sxs-lookup"><span data-stu-id="420ae-124">The display name of the FlowChart.</span></span>|  
|<span data-ttu-id="420ae-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="420ae-125">AppDomain</span></span>|<span data-ttu-id="420ae-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="420ae-126">xs:string</span></span>|<span data-ttu-id="420ae-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="420ae-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
