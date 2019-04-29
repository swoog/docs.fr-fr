---
title: 4208 - RetryingSqlCommandDueToSqlError
ms.date: 03/30/2017
ms.assetid: a8e6483a-a6e4-4bbf-82ec-cd8b6e711aad
ms.openlocfilehash: a97336f12ccfe041b79328bcb48f4e7214a05b63
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774294"
---
# <a name="4208---retryingsqlcommandduetosqlerror"></a><span data-ttu-id="66e91-102">4208 - RetryingSqlCommandDueToSqlError</span><span class="sxs-lookup"><span data-stu-id="66e91-102">4208 - RetryingSqlCommandDueToSqlError</span></span>
## <a name="properties"></a><span data-ttu-id="66e91-103">Properties</span><span class="sxs-lookup"><span data-stu-id="66e91-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="66e91-104">Id</span><span class="sxs-lookup"><span data-stu-id="66e91-104">ID</span></span>|<span data-ttu-id="66e91-105">4208</span><span class="sxs-lookup"><span data-stu-id="66e91-105">4208</span></span>|  
|<span data-ttu-id="66e91-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="66e91-106">Keywords</span></span>|<span data-ttu-id="66e91-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="66e91-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="66e91-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="66e91-108">Level</span></span>|<span data-ttu-id="66e91-109">Information</span><span class="sxs-lookup"><span data-stu-id="66e91-109">Information</span></span>|  
|<span data-ttu-id="66e91-110">Canal</span><span class="sxs-lookup"><span data-stu-id="66e91-110">Channel</span></span>|<span data-ttu-id="66e91-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="66e91-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="66e91-112">Description</span><span class="sxs-lookup"><span data-stu-id="66e91-112">Description</span></span>  
 <span data-ttu-id="66e91-113">Indique que le fournisseur SQL effectue une nouvelle tentative de commande SQL en raison d'une erreur SQL.</span><span class="sxs-lookup"><span data-stu-id="66e91-113">Indicates the SQL provider is retrying a SQL command due to a SQL error.</span></span>  
  
## <a name="message"></a><span data-ttu-id="66e91-114">Message</span><span class="sxs-lookup"><span data-stu-id="66e91-114">Message</span></span>  
 <span data-ttu-id="66e91-115">Nouvelle tentative d'exécution d'une commande SQL en raison du numéro d'erreur SQL %1.</span><span class="sxs-lookup"><span data-stu-id="66e91-115">Retrying a SQL command due to SQL error number %1.</span></span>  
  
## <a name="details"></a><span data-ttu-id="66e91-116">Détails</span><span class="sxs-lookup"><span data-stu-id="66e91-116">Details</span></span>  
  
|<span data-ttu-id="66e91-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="66e91-117">Data Item Name</span></span>|<span data-ttu-id="66e91-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="66e91-118">Data Item Type</span></span>|<span data-ttu-id="66e91-119">Description</span><span class="sxs-lookup"><span data-stu-id="66e91-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="66e91-120">ErrorNumber</span><span class="sxs-lookup"><span data-stu-id="66e91-120">ErrorNumber</span></span>|<span data-ttu-id="66e91-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="66e91-121">xs:string</span></span>|<span data-ttu-id="66e91-122">Numéro d'erreur SQL.</span><span class="sxs-lookup"><span data-stu-id="66e91-122">The SQL error number.</span></span>|  
|<span data-ttu-id="66e91-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="66e91-123">AppDomain</span></span>|<span data-ttu-id="66e91-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="66e91-124">xs:string</span></span>|<span data-ttu-id="66e91-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="66e91-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
