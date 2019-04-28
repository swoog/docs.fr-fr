---
title: 1005 - WorkflowApplicationIdled
ms.date: 03/30/2017
ms.assetid: 74d77dfa-f20d-4fe9-a6ae-e6d1b5fe4182
ms.openlocfilehash: 6bbd12e8025b6a127dbfec8e5d3690825c188c4d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008601"
---
# <a name="1005---workflowapplicationidled"></a><span data-ttu-id="06ce8-102">1005 - WorkflowApplicationIdled</span><span class="sxs-lookup"><span data-stu-id="06ce8-102">1005 - WorkflowApplicationIdled</span></span>
## <a name="properties"></a><span data-ttu-id="06ce8-103">Properties</span><span class="sxs-lookup"><span data-stu-id="06ce8-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="06ce8-104">Id</span><span class="sxs-lookup"><span data-stu-id="06ce8-104">ID</span></span>|<span data-ttu-id="06ce8-105">1005</span><span class="sxs-lookup"><span data-stu-id="06ce8-105">1005</span></span>|  
|<span data-ttu-id="06ce8-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="06ce8-106">Keywords</span></span>|<span data-ttu-id="06ce8-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="06ce8-107">WFRuntime</span></span>|  
|<span data-ttu-id="06ce8-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="06ce8-108">Level</span></span>|<span data-ttu-id="06ce8-109">Information</span><span class="sxs-lookup"><span data-stu-id="06ce8-109">Information</span></span>|  
|<span data-ttu-id="06ce8-110">Canal</span><span class="sxs-lookup"><span data-stu-id="06ce8-110">Channel</span></span>|<span data-ttu-id="06ce8-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="06ce8-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="06ce8-112">Description</span><span class="sxs-lookup"><span data-stu-id="06ce8-112">Description</span></span>  
 <span data-ttu-id="06ce8-113">Indique qu'une application de workflow a été inactive.</span><span class="sxs-lookup"><span data-stu-id="06ce8-113">Indicates a workflow application has idled.</span></span>  
  
## <a name="message"></a><span data-ttu-id="06ce8-114">Message</span><span class="sxs-lookup"><span data-stu-id="06ce8-114">Message</span></span>  
 <span data-ttu-id="06ce8-115">ID WorkflowApplication : « %1 » est devenu inactif.</span><span class="sxs-lookup"><span data-stu-id="06ce8-115">WorkflowApplication Id: '%1' went idle.</span></span>  
  
## <a name="details"></a><span data-ttu-id="06ce8-116">Détails</span><span class="sxs-lookup"><span data-stu-id="06ce8-116">Details</span></span>  
  
|<span data-ttu-id="06ce8-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="06ce8-117">Data Item Name</span></span>|<span data-ttu-id="06ce8-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="06ce8-118">Data Item Type</span></span>|<span data-ttu-id="06ce8-119">Description</span><span class="sxs-lookup"><span data-stu-id="06ce8-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="06ce8-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="06ce8-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="06ce8-121">ID d'application de flux de travail</span><span class="sxs-lookup"><span data-stu-id="06ce8-121">The workflow application id</span></span>|  
|<span data-ttu-id="06ce8-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="06ce8-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="06ce8-123">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="06ce8-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
