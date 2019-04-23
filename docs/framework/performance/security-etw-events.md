---
title: Événements de sécurité ETW
ms.date: 03/30/2017
helpviewer_keywords:
- security events [.NET Framework]
- ETW, security events (CLR)
ms.assetid: 0ed69f73-5c01-4514-bd63-979c6e38d41d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 11a19dce496423883e5fed62375c6db8ed5efdb1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59134028"
---
# <a name="security-etw-events"></a><span data-ttu-id="1e3e4-102">Événements de sécurité ETW</span><span class="sxs-lookup"><span data-stu-id="1e3e4-102">Security ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="1e3e4-103">Les événements de sécurité sont déclenchés pendant la vérification de nom fort et la vérification Authenticode.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-103">Security events are raised during strong name verification and Authenticode verification.</span></span>  
  
 <span data-ttu-id="1e3e4-104">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="1e3e4-104">This category consists of the following events:</span></span>  
  
-   [<span data-ttu-id="1e3e4-105">Événements StrongNameVerificationStart_V1 et StrongNameVerificationStop_V1</span><span class="sxs-lookup"><span data-stu-id="1e3e4-105">StrongNameVerificationStart_V1 and StrongNameVerificationStop_V1 Events</span></span>](#strongnameverificationstart_v1_and_strongnameverificationstop_v1_events)  
  
-   [<span data-ttu-id="1e3e4-106">Événements AuthenticodeVerificationStart_V1 et AuthenticodeVerificationStop_V1</span><span class="sxs-lookup"><span data-stu-id="1e3e4-106">AuthenticodeVerificationStart_V1 and AuthenticodeVerificationStop_V1 Events</span></span>](#authenticodeverificationstart_v1_and_authenticodeverificationstop_v1_events)  
  
<a name="strongnameverificationstart_v1_and_strongnameverificationstop_v1_events"></a>   
## <a name="strongnameverificationstartv1-and-strongnameverificationstopv1-events"></a><span data-ttu-id="1e3e4-107">Événements StrongNameVerificationStart_V1 et StrongNameVerificationStop_V1</span><span class="sxs-lookup"><span data-stu-id="1e3e4-107">StrongNameVerificationStart_V1 and StrongNameVerificationStop_V1 Events</span></span>  
 <span data-ttu-id="1e3e4-108">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-108">The following table shows the keyword and level.</span></span> <span data-ttu-id="1e3e4-109">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="1e3e4-109">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="1e3e4-110">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="1e3e4-110">Keyword for raising the event</span></span>|<span data-ttu-id="1e3e4-111">Niveau</span><span class="sxs-lookup"><span data-stu-id="1e3e4-111">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="1e3e4-112">`SecurityKeyword` (0x400)</span><span class="sxs-lookup"><span data-stu-id="1e3e4-112">`SecurityKeyword` (0x400)</span></span>|<span data-ttu-id="1e3e4-113">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="1e3e4-113">Informational(4)</span></span>|  
  
 <span data-ttu-id="1e3e4-114">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-114">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="1e3e4-115">Événement</span><span class="sxs-lookup"><span data-stu-id="1e3e4-115">Event</span></span>|<span data-ttu-id="1e3e4-116">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="1e3e4-116">Event ID</span></span>|<span data-ttu-id="1e3e4-117">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="1e3e4-117">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`StrongNameVerificationStart_V1`|<span data-ttu-id="1e3e4-118">181</span><span class="sxs-lookup"><span data-stu-id="1e3e4-118">181</span></span>|<span data-ttu-id="1e3e4-119">Début de la vérification de nom fort.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-119">Start of strong name verification.</span></span>|  
|`StrongNameVerificationStop_V1`|<span data-ttu-id="1e3e4-120">182</span><span class="sxs-lookup"><span data-stu-id="1e3e4-120">182</span></span>|<span data-ttu-id="1e3e4-121">Fin de la vérification de nom fort.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-121">End of strong name verification.</span></span>|  
  
 <span data-ttu-id="1e3e4-122">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-122">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="1e3e4-123">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="1e3e4-123">Field name</span></span>|<span data-ttu-id="1e3e4-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="1e3e4-124">Data type</span></span>|<span data-ttu-id="1e3e4-125">Description</span><span class="sxs-lookup"><span data-stu-id="1e3e4-125">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="1e3e4-126">VerificationFlags</span><span class="sxs-lookup"><span data-stu-id="1e3e4-126">VerificationFlags</span></span>|<span data-ttu-id="1e3e4-127">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="1e3e4-127">win:UInt32</span></span>|<span data-ttu-id="1e3e4-128">Indicateurs de vérification.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-128">The verification flags.</span></span>|  
|<span data-ttu-id="1e3e4-129">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="1e3e4-129">ErrorCode</span></span>|<span data-ttu-id="1e3e4-130">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="1e3e4-130">win:UInt32</span></span>|<span data-ttu-id="1e3e4-131">Code d'erreur HResult.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-131">The HResult error code.</span></span>|  
|<span data-ttu-id="1e3e4-132">FullyQualifiedAssemblyName</span><span class="sxs-lookup"><span data-stu-id="1e3e4-132">FullyQualifiedAssemblyName</span></span>|<span data-ttu-id="1e3e4-133">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="1e3e4-133">win:UnicodeString</span></span>|<span data-ttu-id="1e3e4-134">Nom d'assembly qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-134">The fully qualified assembly name.</span></span>|  
|<span data-ttu-id="1e3e4-135">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="1e3e4-135">ClrInstanceID</span></span>|<span data-ttu-id="1e3e4-136">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="1e3e4-136">win:UInt16</span></span>|<span data-ttu-id="1e3e4-137">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-137">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="1e3e4-138">Retour au début</span><span class="sxs-lookup"><span data-stu-id="1e3e4-138">Back to top</span></span>](#top)  
  
<a name="authenticodeverificationstart_v1_and_authenticodeverificationstop_v1_events"></a>   
## <a name="authenticodeverificationstartv1-and-authenticodeverificationstopv1-events"></a><span data-ttu-id="1e3e4-139">Événements AuthenticodeVerificationStart_V1 et AuthenticodeVerificationStop_V1</span><span class="sxs-lookup"><span data-stu-id="1e3e4-139">AuthenticodeVerificationStart_V1 and AuthenticodeVerificationStop_V1 Events</span></span>  
 <span data-ttu-id="1e3e4-140">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-140">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="1e3e4-141">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="1e3e4-141">Keyword for raising the event</span></span>|<span data-ttu-id="1e3e4-142">Niveau</span><span class="sxs-lookup"><span data-stu-id="1e3e4-142">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="1e3e4-143">`SecurityKeyword` (0x400)</span><span class="sxs-lookup"><span data-stu-id="1e3e4-143">`SecurityKeyword` (0x400)</span></span>|<span data-ttu-id="1e3e4-144">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="1e3e4-144">Informational(4)</span></span>|  
  
 <span data-ttu-id="1e3e4-145">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-145">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="1e3e4-146">Événement</span><span class="sxs-lookup"><span data-stu-id="1e3e4-146">Event</span></span>|<span data-ttu-id="1e3e4-147">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="1e3e4-147">Event ID</span></span>|<span data-ttu-id="1e3e4-148">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="1e3e4-148">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AuthenticodeVerificationStart_V1`|<span data-ttu-id="1e3e4-149">183</span><span class="sxs-lookup"><span data-stu-id="1e3e4-149">183</span></span>|<span data-ttu-id="1e3e4-150">Début de la vérification Authenticode.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-150">Start of Authenticode verification.</span></span>|  
|`AuthenticodeVerificationStop_V1`|<span data-ttu-id="1e3e4-151">184</span><span class="sxs-lookup"><span data-stu-id="1e3e4-151">184</span></span>|<span data-ttu-id="1e3e4-152">Fin de la vérification Authenticode.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-152">End of Authenticode verification.</span></span>|  
  
 <span data-ttu-id="1e3e4-153">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-153">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="1e3e4-154">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="1e3e4-154">Field name</span></span>|<span data-ttu-id="1e3e4-155">Type de données</span><span class="sxs-lookup"><span data-stu-id="1e3e4-155">Data type</span></span>|<span data-ttu-id="1e3e4-156">Description</span><span class="sxs-lookup"><span data-stu-id="1e3e4-156">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="1e3e4-157">VerificationFlags</span><span class="sxs-lookup"><span data-stu-id="1e3e4-157">VerificationFlags</span></span>|<span data-ttu-id="1e3e4-158">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="1e3e4-158">win:UInt32</span></span>|<span data-ttu-id="1e3e4-159">Indicateurs de vérification.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-159">The verification flags.</span></span>|  
|<span data-ttu-id="1e3e4-160">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="1e3e4-160">ErrorCode</span></span>|<span data-ttu-id="1e3e4-161">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="1e3e4-161">win:UInt32</span></span>|<span data-ttu-id="1e3e4-162">Code d'erreur HResult.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-162">The HResult error code.</span></span>|  
|<span data-ttu-id="1e3e4-163">ModulePath</span><span class="sxs-lookup"><span data-stu-id="1e3e4-163">ModulePath</span></span>|<span data-ttu-id="1e3e4-164">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="1e3e4-164">win:UnicodeString</span></span>|<span data-ttu-id="1e3e4-165">Chemin d’accès du module.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-165">The module path.</span></span>|  
|<span data-ttu-id="1e3e4-166">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="1e3e4-166">ClrInstanceID</span></span>|<span data-ttu-id="1e3e4-167">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="1e3e4-167">win:UInt16</span></span>|<span data-ttu-id="1e3e4-168">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="1e3e4-168">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1e3e4-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e3e4-169">See also</span></span>

- [<span data-ttu-id="1e3e4-170">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="1e3e4-170">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
