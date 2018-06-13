---
title: 1126 - InvokedMethodThrewException
ms.date: 03/30/2017
ms.assetid: 0d3cff1a-97e6-4b6c-be18-108c6881bfc0
ms.openlocfilehash: 714a98a300426d80c3b494d701ae1bd53a49592f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33512292"
---
# <a name="1126---invokedmethodthrewexception"></a><span data-ttu-id="67149-102">1126 - InvokedMethodThrewException</span><span class="sxs-lookup"><span data-stu-id="67149-102">1126 - InvokedMethodThrewException</span></span>
## <a name="properties"></a><span data-ttu-id="67149-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67149-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="67149-104">ID</span><span class="sxs-lookup"><span data-stu-id="67149-104">ID</span></span>|<span data-ttu-id="67149-105">1126</span><span class="sxs-lookup"><span data-stu-id="67149-105">1126</span></span>|  
|<span data-ttu-id="67149-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="67149-106">Keywords</span></span>|<span data-ttu-id="67149-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="67149-107">WFRuntime</span></span>|  
|<span data-ttu-id="67149-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="67149-108">Level</span></span>|<span data-ttu-id="67149-109">Information</span><span class="sxs-lookup"><span data-stu-id="67149-109">Information</span></span>|  
|<span data-ttu-id="67149-110">Canal</span><span class="sxs-lookup"><span data-stu-id="67149-110">Channel</span></span>|<span data-ttu-id="67149-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="67149-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="67149-112">Description</span><span class="sxs-lookup"><span data-stu-id="67149-112">Description</span></span>  
 <span data-ttu-id="67149-113">Indique qu'une exception a été levée par la méthode appelée par l'activité InvokeMethod.</span><span class="sxs-lookup"><span data-stu-id="67149-113">Indicates an exception was thrown by the method called by the InvokeMethod activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="67149-114">Message</span><span class="sxs-lookup"><span data-stu-id="67149-114">Message</span></span>  
 <span data-ttu-id="67149-115">Une exception a été levée dans la méthode appelée par l'activité « %1 ».</span><span class="sxs-lookup"><span data-stu-id="67149-115">An exception was thrown in the method called by the activity '%1'.</span></span> <span data-ttu-id="67149-116">%2</span><span class="sxs-lookup"><span data-stu-id="67149-116">%2</span></span>  
  
## <a name="details"></a><span data-ttu-id="67149-117">Détails</span><span class="sxs-lookup"><span data-stu-id="67149-117">Details</span></span>  
  
|<span data-ttu-id="67149-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="67149-118">Data Item Name</span></span>|<span data-ttu-id="67149-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="67149-119">Data Item Type</span></span>|<span data-ttu-id="67149-120">Description</span><span class="sxs-lookup"><span data-stu-id="67149-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="67149-121">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="67149-121">InvokeMethod</span></span>|<span data-ttu-id="67149-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="67149-122">xs:string</span></span>|<span data-ttu-id="67149-123">Nom complet de l'activité InvokeMethod.</span><span class="sxs-lookup"><span data-stu-id="67149-123">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="67149-124">Exception</span><span class="sxs-lookup"><span data-stu-id="67149-124">Exception</span></span>|<span data-ttu-id="67149-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="67149-125">xs:string</span></span>|<span data-ttu-id="67149-126">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="67149-126">The exception details for the exception</span></span>|  
|<span data-ttu-id="67149-127">AppDomain</span><span class="sxs-lookup"><span data-stu-id="67149-127">AppDomain</span></span>|<span data-ttu-id="67149-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="67149-128">xs:string</span></span>|<span data-ttu-id="67149-129">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="67149-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
