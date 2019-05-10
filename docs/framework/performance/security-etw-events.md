---
title: Événements de sécurité ETW
ms.date: 03/30/2017
helpviewer_keywords:
- security events [.NET Framework]
- ETW, security events (CLR)
ms.assetid: 0ed69f73-5c01-4514-bd63-979c6e38d41d
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f2ea19c88ff8b854b09ed372b35bf8c45d994585
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64583654"
---
# <a name="security-etw-events"></a><span data-ttu-id="852e5-102">Événements de sécurité ETW</span><span class="sxs-lookup"><span data-stu-id="852e5-102">Security ETW Events</span></span>
<a name="top"></a> <span data-ttu-id="852e5-103">Les événements de sécurité sont déclenchés pendant la vérification de nom fort et la vérification Authenticode.</span><span class="sxs-lookup"><span data-stu-id="852e5-103">Security events are raised during strong name verification and Authenticode verification.</span></span>  
  
 <span data-ttu-id="852e5-104">Cette catégorie comprend les événements suivants :</span><span class="sxs-lookup"><span data-stu-id="852e5-104">This category consists of the following events:</span></span>  
  
- [<span data-ttu-id="852e5-105">Événements StrongNameVerificationStart_V1 et StrongNameVerificationStop_V1</span><span class="sxs-lookup"><span data-stu-id="852e5-105">StrongNameVerificationStart_V1 and StrongNameVerificationStop_V1 Events</span></span>](#strongnameverificationstart_v1_and_strongnameverificationstop_v1_events)  
  
- [<span data-ttu-id="852e5-106">Événements AuthenticodeVerificationStart_V1 et AuthenticodeVerificationStop_V1</span><span class="sxs-lookup"><span data-stu-id="852e5-106">AuthenticodeVerificationStart_V1 and AuthenticodeVerificationStop_V1 Events</span></span>](#authenticodeverificationstart_v1_and_authenticodeverificationstop_v1_events)  
  
<a name="strongnameverificationstart_v1_and_strongnameverificationstop_v1_events"></a>   
## <a name="strongnameverificationstartv1-and-strongnameverificationstopv1-events"></a><span data-ttu-id="852e5-107">Événements StrongNameVerificationStart_V1 et StrongNameVerificationStop_V1</span><span class="sxs-lookup"><span data-stu-id="852e5-107">StrongNameVerificationStart_V1 and StrongNameVerificationStop_V1 Events</span></span>  
 <span data-ttu-id="852e5-108">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="852e5-108">The following table shows the keyword and level.</span></span> <span data-ttu-id="852e5-109">(Pour plus d'informations, consultez [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span><span class="sxs-lookup"><span data-stu-id="852e5-109">(For more information, see [CLR ETW Keywords and Levels](../../../docs/framework/performance/clr-etw-keywords-and-levels.md).)</span></span>  
  
|<span data-ttu-id="852e5-110">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="852e5-110">Keyword for raising the event</span></span>|<span data-ttu-id="852e5-111">Niveau</span><span class="sxs-lookup"><span data-stu-id="852e5-111">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="852e5-112">`SecurityKeyword` (0x400)</span><span class="sxs-lookup"><span data-stu-id="852e5-112">`SecurityKeyword` (0x400)</span></span>|<span data-ttu-id="852e5-113">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="852e5-113">Informational(4)</span></span>|  
  
 <span data-ttu-id="852e5-114">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="852e5-114">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="852e5-115">Événement</span><span class="sxs-lookup"><span data-stu-id="852e5-115">Event</span></span>|<span data-ttu-id="852e5-116">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="852e5-116">Event ID</span></span>|<span data-ttu-id="852e5-117">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="852e5-117">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`StrongNameVerificationStart_V1`|<span data-ttu-id="852e5-118">181</span><span class="sxs-lookup"><span data-stu-id="852e5-118">181</span></span>|<span data-ttu-id="852e5-119">Début de la vérification de nom fort.</span><span class="sxs-lookup"><span data-stu-id="852e5-119">Start of strong name verification.</span></span>|  
|`StrongNameVerificationStop_V1`|<span data-ttu-id="852e5-120">182</span><span class="sxs-lookup"><span data-stu-id="852e5-120">182</span></span>|<span data-ttu-id="852e5-121">Fin de la vérification de nom fort.</span><span class="sxs-lookup"><span data-stu-id="852e5-121">End of strong name verification.</span></span>|  
  
 <span data-ttu-id="852e5-122">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="852e5-122">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="852e5-123">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="852e5-123">Field name</span></span>|<span data-ttu-id="852e5-124">Type de données</span><span class="sxs-lookup"><span data-stu-id="852e5-124">Data type</span></span>|<span data-ttu-id="852e5-125">Description</span><span class="sxs-lookup"><span data-stu-id="852e5-125">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="852e5-126">VerificationFlags</span><span class="sxs-lookup"><span data-stu-id="852e5-126">VerificationFlags</span></span>|<span data-ttu-id="852e5-127">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="852e5-127">win:UInt32</span></span>|<span data-ttu-id="852e5-128">Indicateurs de vérification.</span><span class="sxs-lookup"><span data-stu-id="852e5-128">The verification flags.</span></span>|  
|<span data-ttu-id="852e5-129">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="852e5-129">ErrorCode</span></span>|<span data-ttu-id="852e5-130">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="852e5-130">win:UInt32</span></span>|<span data-ttu-id="852e5-131">Code d'erreur HResult.</span><span class="sxs-lookup"><span data-stu-id="852e5-131">The HResult error code.</span></span>|  
|<span data-ttu-id="852e5-132">FullyQualifiedAssemblyName</span><span class="sxs-lookup"><span data-stu-id="852e5-132">FullyQualifiedAssemblyName</span></span>|<span data-ttu-id="852e5-133">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="852e5-133">win:UnicodeString</span></span>|<span data-ttu-id="852e5-134">Nom d'assembly qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="852e5-134">The fully qualified assembly name.</span></span>|  
|<span data-ttu-id="852e5-135">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="852e5-135">ClrInstanceID</span></span>|<span data-ttu-id="852e5-136">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="852e5-136">win:UInt16</span></span>|<span data-ttu-id="852e5-137">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="852e5-137">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
 [<span data-ttu-id="852e5-138">Retour au début</span><span class="sxs-lookup"><span data-stu-id="852e5-138">Back to top</span></span>](#top)  
  
<a name="authenticodeverificationstart_v1_and_authenticodeverificationstop_v1_events"></a>   
## <a name="authenticodeverificationstartv1-and-authenticodeverificationstopv1-events"></a><span data-ttu-id="852e5-139">Événements AuthenticodeVerificationStart_V1 et AuthenticodeVerificationStop_V1</span><span class="sxs-lookup"><span data-stu-id="852e5-139">AuthenticodeVerificationStart_V1 and AuthenticodeVerificationStop_V1 Events</span></span>  
 <span data-ttu-id="852e5-140">Le tableau suivant montre les mots clés et les niveaux.</span><span class="sxs-lookup"><span data-stu-id="852e5-140">The following table shows the keyword and level.</span></span>  
  
|<span data-ttu-id="852e5-141">Mot clé pour déclencher l'événement</span><span class="sxs-lookup"><span data-stu-id="852e5-141">Keyword for raising the event</span></span>|<span data-ttu-id="852e5-142">Niveau</span><span class="sxs-lookup"><span data-stu-id="852e5-142">Level</span></span>|  
|-----------------------------------|-----------|  
|<span data-ttu-id="852e5-143">`SecurityKeyword` (0x400)</span><span class="sxs-lookup"><span data-stu-id="852e5-143">`SecurityKeyword` (0x400)</span></span>|<span data-ttu-id="852e5-144">Informatif(4)</span><span class="sxs-lookup"><span data-stu-id="852e5-144">Informational(4)</span></span>|  
  
 <span data-ttu-id="852e5-145">Le tableau ci-dessous montre les informations liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="852e5-145">The following table shows the event information.</span></span>  
  
|<span data-ttu-id="852e5-146">Événement</span><span class="sxs-lookup"><span data-stu-id="852e5-146">Event</span></span>|<span data-ttu-id="852e5-147">ID d'événement</span><span class="sxs-lookup"><span data-stu-id="852e5-147">Event ID</span></span>|<span data-ttu-id="852e5-148">Moment du déclenchement</span><span class="sxs-lookup"><span data-stu-id="852e5-148">Raised when</span></span>|  
|-----------|--------------|-----------------|  
|`AuthenticodeVerificationStart_V1`|<span data-ttu-id="852e5-149">183</span><span class="sxs-lookup"><span data-stu-id="852e5-149">183</span></span>|<span data-ttu-id="852e5-150">Début de la vérification Authenticode.</span><span class="sxs-lookup"><span data-stu-id="852e5-150">Start of Authenticode verification.</span></span>|  
|`AuthenticodeVerificationStop_V1`|<span data-ttu-id="852e5-151">184</span><span class="sxs-lookup"><span data-stu-id="852e5-151">184</span></span>|<span data-ttu-id="852e5-152">Fin de la vérification Authenticode.</span><span class="sxs-lookup"><span data-stu-id="852e5-152">End of Authenticode verification.</span></span>|  
  
 <span data-ttu-id="852e5-153">Le tableau ci-dessous montre les données liées aux événements.</span><span class="sxs-lookup"><span data-stu-id="852e5-153">The following table shows the event data.</span></span>  
  
|<span data-ttu-id="852e5-154">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="852e5-154">Field name</span></span>|<span data-ttu-id="852e5-155">Type de données</span><span class="sxs-lookup"><span data-stu-id="852e5-155">Data type</span></span>|<span data-ttu-id="852e5-156">Description</span><span class="sxs-lookup"><span data-stu-id="852e5-156">Description</span></span>|  
|----------------|---------------|-----------------|  
|<span data-ttu-id="852e5-157">VerificationFlags</span><span class="sxs-lookup"><span data-stu-id="852e5-157">VerificationFlags</span></span>|<span data-ttu-id="852e5-158">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="852e5-158">win:UInt32</span></span>|<span data-ttu-id="852e5-159">Indicateurs de vérification.</span><span class="sxs-lookup"><span data-stu-id="852e5-159">The verification flags.</span></span>|  
|<span data-ttu-id="852e5-160">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="852e5-160">ErrorCode</span></span>|<span data-ttu-id="852e5-161">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="852e5-161">win:UInt32</span></span>|<span data-ttu-id="852e5-162">Code d'erreur HResult.</span><span class="sxs-lookup"><span data-stu-id="852e5-162">The HResult error code.</span></span>|  
|<span data-ttu-id="852e5-163">ModulePath</span><span class="sxs-lookup"><span data-stu-id="852e5-163">ModulePath</span></span>|<span data-ttu-id="852e5-164">win:UnicodeString</span><span class="sxs-lookup"><span data-stu-id="852e5-164">win:UnicodeString</span></span>|<span data-ttu-id="852e5-165">Chemin d’accès du module.</span><span class="sxs-lookup"><span data-stu-id="852e5-165">The module path.</span></span>|  
|<span data-ttu-id="852e5-166">ClrInstanceID</span><span class="sxs-lookup"><span data-stu-id="852e5-166">ClrInstanceID</span></span>|<span data-ttu-id="852e5-167">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="852e5-167">win:UInt16</span></span>|<span data-ttu-id="852e5-168">ID unique de l'instance de CLR ou CoreCLR.</span><span class="sxs-lookup"><span data-stu-id="852e5-168">Unique ID for the instance of CLR or CoreCLR.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="852e5-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="852e5-169">See also</span></span>

- [<span data-ttu-id="852e5-170">Événements ETW du CLR</span><span class="sxs-lookup"><span data-stu-id="852e5-170">CLR ETW Events</span></span>](../../../docs/framework/performance/clr-etw-events.md)
