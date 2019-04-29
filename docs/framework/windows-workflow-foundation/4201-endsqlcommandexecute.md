---
title: 4201 - EndSqlCommandExecute
ms.date: 03/30/2017
ms.assetid: ae0dbc15-f98c-4096-a8d9-fbe4dc36f1cd
ms.openlocfilehash: 75c1cdd10aca6b177911bd9d2f51468016eb9e15
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774359"
---
# <a name="4201---endsqlcommandexecute"></a><span data-ttu-id="6a8ef-102">4201 - EndSqlCommandExecute</span><span class="sxs-lookup"><span data-stu-id="6a8ef-102">4201 - EndSqlCommandExecute</span></span>
## <a name="properties"></a><span data-ttu-id="6a8ef-103">Properties</span><span class="sxs-lookup"><span data-stu-id="6a8ef-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="6a8ef-104">Id</span><span class="sxs-lookup"><span data-stu-id="6a8ef-104">ID</span></span>|<span data-ttu-id="6a8ef-105">4201</span><span class="sxs-lookup"><span data-stu-id="6a8ef-105">4201</span></span>|  
|<span data-ttu-id="6a8ef-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="6a8ef-106">Keywords</span></span>|<span data-ttu-id="6a8ef-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="6a8ef-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="6a8ef-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="6a8ef-108">Level</span></span>|<span data-ttu-id="6a8ef-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="6a8ef-109">Verbose</span></span>|  
|<span data-ttu-id="6a8ef-110">Canal</span><span class="sxs-lookup"><span data-stu-id="6a8ef-110">Channel</span></span>|<span data-ttu-id="6a8ef-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="6a8ef-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="6a8ef-112">Description</span><span class="sxs-lookup"><span data-stu-id="6a8ef-112">Description</span></span>  
 <span data-ttu-id="6a8ef-113">Indique que l'exécution d'une commande SQL est terminée.</span><span class="sxs-lookup"><span data-stu-id="6a8ef-113">Indicates a SQL command has finished executing.</span></span>  
  
## <a name="message"></a><span data-ttu-id="6a8ef-114">Message</span><span class="sxs-lookup"><span data-stu-id="6a8ef-114">Message</span></span>  
 <span data-ttu-id="6a8ef-115">Fin de l'exécution de la commande SQL : %1</span><span class="sxs-lookup"><span data-stu-id="6a8ef-115">End SQL command execution: %1</span></span>  
  
## <a name="details"></a><span data-ttu-id="6a8ef-116">Détails</span><span class="sxs-lookup"><span data-stu-id="6a8ef-116">Details</span></span>  
  
|<span data-ttu-id="6a8ef-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="6a8ef-117">Data Item Name</span></span>|<span data-ttu-id="6a8ef-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="6a8ef-118">Data Item Type</span></span>|<span data-ttu-id="6a8ef-119">Description</span><span class="sxs-lookup"><span data-stu-id="6a8ef-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="6a8ef-120">SqlCommand</span><span class="sxs-lookup"><span data-stu-id="6a8ef-120">SqlCommand</span></span>|<span data-ttu-id="6a8ef-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="6a8ef-121">xs:string</span></span>|<span data-ttu-id="6a8ef-122">Commande SQL exécutée.</span><span class="sxs-lookup"><span data-stu-id="6a8ef-122">The SQL command that was executed.</span></span>|  
|<span data-ttu-id="6a8ef-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="6a8ef-123">AppDomain</span></span>|<span data-ttu-id="6a8ef-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="6a8ef-124">xs:string</span></span>|<span data-ttu-id="6a8ef-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="6a8ef-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
