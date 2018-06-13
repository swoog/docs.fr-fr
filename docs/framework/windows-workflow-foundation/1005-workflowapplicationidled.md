---
title: 1005 - WorkflowApplicationIdled
ms.date: 03/30/2017
ms.assetid: 74d77dfa-f20d-4fe9-a6ae-e6d1b5fe4182
ms.openlocfilehash: 6bbd12e8025b6a127dbfec8e5d3690825c188c4d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33509292"
---
# <a name="1005---workflowapplicationidled"></a><span data-ttu-id="50fd7-102">1005 - WorkflowApplicationIdled</span><span class="sxs-lookup"><span data-stu-id="50fd7-102">1005 - WorkflowApplicationIdled</span></span>
## <a name="properties"></a><span data-ttu-id="50fd7-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50fd7-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="50fd7-104">ID</span><span class="sxs-lookup"><span data-stu-id="50fd7-104">ID</span></span>|<span data-ttu-id="50fd7-105">1005</span><span class="sxs-lookup"><span data-stu-id="50fd7-105">1005</span></span>|  
|<span data-ttu-id="50fd7-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="50fd7-106">Keywords</span></span>|<span data-ttu-id="50fd7-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="50fd7-107">WFRuntime</span></span>|  
|<span data-ttu-id="50fd7-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="50fd7-108">Level</span></span>|<span data-ttu-id="50fd7-109">Information</span><span class="sxs-lookup"><span data-stu-id="50fd7-109">Information</span></span>|  
|<span data-ttu-id="50fd7-110">Canal</span><span class="sxs-lookup"><span data-stu-id="50fd7-110">Channel</span></span>|<span data-ttu-id="50fd7-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="50fd7-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="50fd7-112">Description</span><span class="sxs-lookup"><span data-stu-id="50fd7-112">Description</span></span>  
 <span data-ttu-id="50fd7-113">Indique qu'une application de workflow a été inactive.</span><span class="sxs-lookup"><span data-stu-id="50fd7-113">Indicates a workflow application has idled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="50fd7-114">Message</span><span class="sxs-lookup"><span data-stu-id="50fd7-114">Message</span></span>  
 <span data-ttu-id="50fd7-115">ID WorkflowApplication : « %1 » est devenu inactif.</span><span class="sxs-lookup"><span data-stu-id="50fd7-115">WorkflowApplication Id: '%1' went idle.</span></span>  
  
## <a name="details"></a><span data-ttu-id="50fd7-116">Détails</span><span class="sxs-lookup"><span data-stu-id="50fd7-116">Details</span></span>  
  
|<span data-ttu-id="50fd7-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="50fd7-117">Data Item Name</span></span>|<span data-ttu-id="50fd7-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="50fd7-118">Data Item Type</span></span>|<span data-ttu-id="50fd7-119">Description</span><span class="sxs-lookup"><span data-stu-id="50fd7-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="50fd7-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="50fd7-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="50fd7-121">ID d'application de flux de travail</span><span class="sxs-lookup"><span data-stu-id="50fd7-121">The workflow application id</span></span>|  
|<span data-ttu-id="50fd7-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="50fd7-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="50fd7-123">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="50fd7-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
