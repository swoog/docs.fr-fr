---
title: LocalServiceSecuritySettings
ms.date: 03/30/2017
ms.assetid: 490aa0e5-5242-4f8d-b505-5ec6287633b4
author: BrucePerlerMS
ms.openlocfilehash: c79eb11fcc1973a3ef25a78afb8b141443d865c3
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47398863"
---
# <a name="localservicesecuritysettings"></a><span data-ttu-id="c055d-102">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="c055d-102">LocalServiceSecuritySettings</span></span>
<span data-ttu-id="c055d-103">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="c055d-103">LocalServiceSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c055d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c055d-104">Syntax</span></span>  
  
```  
class LocalServiceSecuritySettings  
{  
  boolean DetectReplays;  
  datetime InactivityTimeout;  
  datetime IssuedCookieLifetime;  
  sint32 MaxCachedCookies;  
  datetime MaxClockSkew;  
  sint32 MaxPendingSessions;  
  sint32 MaxStatefulNegotiations;  
  datetime NegotiationTimeout;  
  boolean ReconnectTransportOnFailure;  
  sint32 ReplayCacheSize;  
  datetime ReplayWindow;  
  datetime SessionKeyRenewalInterval;  
  datetime SessionKeyRolloverInterval;  
  datetime TimestampValidityDuration;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c055d-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c055d-105">Methods</span></span>  
 <span data-ttu-id="c055d-106">La classe LocalServiceSecuritySettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="c055d-106">The LocalServiceSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c055d-107">Properties</span><span class="sxs-lookup"><span data-stu-id="c055d-107">Properties</span></span>  
 <span data-ttu-id="c055d-108">La classe LocalServiceSecuritySettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="c055d-108">The LocalServiceSecuritySettings class has the following properties:</span></span>  
  
### <a name="detectreplays"></a><span data-ttu-id="c055d-109">DetectReplays</span><span class="sxs-lookup"><span data-stu-id="c055d-109">DetectReplays</span></span>  
 <span data-ttu-id="c055d-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="c055d-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="c055d-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-112">Valeur booléenne qui spécifie si les attaques par relecture contre le canal sont détectées et traitées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c055d-112">A Boolean value that specifies whether replay attacks against the channel are detected and dealt with automatically.</span></span>  
  
### <a name="inactivitytimeout"></a><span data-ttu-id="c055d-113">InactivityTimeout</span><span class="sxs-lookup"><span data-stu-id="c055d-113">InactivityTimeout</span></span>  
 <span data-ttu-id="c055d-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c055d-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="c055d-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-116">Nombre maximal de sessions de sécurité en attente que le service prend en charge.</span><span class="sxs-lookup"><span data-stu-id="c055d-116">The maximum number of pending security sessions that the service supports.</span></span>  
  
### <a name="issuedcookielifetime"></a><span data-ttu-id="c055d-117">IssuedCookieLifetime</span><span class="sxs-lookup"><span data-stu-id="c055d-117">IssuedCookieLifetime</span></span>  
 <span data-ttu-id="c055d-118">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c055d-118">Data type: datetime</span></span>  
  
 <span data-ttu-id="c055d-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-120">TimeSpan qui spécifie la durée de vie de tous les nouveaux cookies de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c055d-120">A TimeSpan that specifies the lifetime issued to all new security cookies.</span></span>  
  
### <a name="maxcachedcookies"></a><span data-ttu-id="c055d-121">MaxCachedCookies</span><span class="sxs-lookup"><span data-stu-id="c055d-121">MaxCachedCookies</span></span>  
 <span data-ttu-id="c055d-122">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c055d-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="c055d-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-124">Nombre maximal de cookies qui peuvent être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="c055d-124">The maximum number of cookies that can be cached.</span></span>  
  
### <a name="maxclockskew"></a><span data-ttu-id="c055d-125">MaxClockSkew</span><span class="sxs-lookup"><span data-stu-id="c055d-125">MaxClockSkew</span></span>  
 <span data-ttu-id="c055d-126">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c055d-126">Data type: datetime</span></span>  
  
 <span data-ttu-id="c055d-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-128">TimeSpan qui spécifie la différence de temps maximale entre les horloges système des deux parties communicantes.</span><span class="sxs-lookup"><span data-stu-id="c055d-128">A TimeSpan that specifies the maximum time difference between the system clocks of the two communicating parties.</span></span>  
  
### <a name="maxpendingsessions"></a><span data-ttu-id="c055d-129">MaxPendingSessions</span><span class="sxs-lookup"><span data-stu-id="c055d-129">MaxPendingSessions</span></span>  
 <span data-ttu-id="c055d-130">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c055d-130">Data type: sint32</span></span>  
  
 <span data-ttu-id="c055d-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-132">Nombre maximal de connexions en attente sur le service.</span><span class="sxs-lookup"><span data-stu-id="c055d-132">The maximum number of pending connections on the service.</span></span>  
  
### <a name="maxstatefulnegotiations"></a><span data-ttu-id="c055d-133">MaxStatefulNegotiations</span><span class="sxs-lookup"><span data-stu-id="c055d-133">MaxStatefulNegotiations</span></span>  
 <span data-ttu-id="c055d-134">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c055d-134">Data type: sint32</span></span>  
  
 <span data-ttu-id="c055d-135">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-136">Nombre de négociations de sécurité qui peuvent être actives simultanément.</span><span class="sxs-lookup"><span data-stu-id="c055d-136">The number of security negotiations that can be active concurrently.</span></span>  
  
### <a name="negotiationtimeout"></a><span data-ttu-id="c055d-137">NegotiationTimeout</span><span class="sxs-lookup"><span data-stu-id="c055d-137">NegotiationTimeout</span></span>  
 <span data-ttu-id="c055d-138">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c055d-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="c055d-139">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-140">TimeSpan qui spécifie la durée maximale de la phase de négociation de sécurité entre le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="c055d-140">A TimeSpan that specifies the maximum duration for the security negotiation phase between server and client.</span></span>  
  
### <a name="reconnecttransportonfailure"></a><span data-ttu-id="c055d-141">ReconnectTransportOnFailure</span><span class="sxs-lookup"><span data-stu-id="c055d-141">ReconnectTransportOnFailure</span></span>  
 <span data-ttu-id="c055d-142">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="c055d-142">Data type: boolean</span></span>  
  
 <span data-ttu-id="c055d-143">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-144">Valeur booléenne qui spécifie si des connexions utilisant la messagerie WS-Reliable tentent une reconnexion après des incidents de transport.</span><span class="sxs-lookup"><span data-stu-id="c055d-144">A Boolean value that specifies whether connections using WS-Reliable messaging attempt to reconnect after transport failures.</span></span>  
  
### <a name="replaycachesize"></a><span data-ttu-id="c055d-145">ReplayCacheSize</span><span class="sxs-lookup"><span data-stu-id="c055d-145">ReplayCacheSize</span></span>  
 <span data-ttu-id="c055d-146">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c055d-146">Data type: sint32</span></span>  
  
 <span data-ttu-id="c055d-147">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-148">Nombre de pointeurs en cache utilisés pour la détection de relecture.</span><span class="sxs-lookup"><span data-stu-id="c055d-148">The number of cached nonces used for replay detection.</span></span>  
  
### <a name="replaywindow"></a><span data-ttu-id="c055d-149">ReplayWindow</span><span class="sxs-lookup"><span data-stu-id="c055d-149">ReplayWindow</span></span>  
 <span data-ttu-id="c055d-150">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c055d-150">Data type: datetime</span></span>  
  
 <span data-ttu-id="c055d-151">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-152">TimeSpan qui spécifie la durée de validité des pointeurs de messages individuels.</span><span class="sxs-lookup"><span data-stu-id="c055d-152">A TimeSpan that specifies the duration in which individual message nonces are valid.</span></span>  
  
### <a name="sessionkeyrenewalinterval"></a><span data-ttu-id="c055d-153">SessionKeyRenewalInterval</span><span class="sxs-lookup"><span data-stu-id="c055d-153">SessionKeyRenewalInterval</span></span>  
 <span data-ttu-id="c055d-154">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c055d-154">Data type: datetime</span></span>  
  
 <span data-ttu-id="c055d-155">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-156">TimeSpan qui spécifie le délai d'attente au terme duquel l'initiateur renouvelle la clé de la session de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c055d-156">A TimeSpan that specifies the duration after which the initiator renews the key for the security session.</span></span>  
  
### <a name="sessionkeyrolloverinterval"></a><span data-ttu-id="c055d-157">SessionKeyRolloverInterval</span><span class="sxs-lookup"><span data-stu-id="c055d-157">SessionKeyRolloverInterval</span></span>  
 <span data-ttu-id="c055d-158">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c055d-158">Data type: datetime</span></span>  
  
 <span data-ttu-id="c055d-159">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-160">TimeSpan qui spécifie la période de validité d'une clé de session précédente sur les messages entrants pendant un renouvellement de clé.</span><span class="sxs-lookup"><span data-stu-id="c055d-160">A TimeSpan that specifies the time interval a previous session key is valid on incoming messages during a key renewal.</span></span>  
  
### <a name="timestampvalidityduration"></a><span data-ttu-id="c055d-161">TimestampValidityDuration</span><span class="sxs-lookup"><span data-stu-id="c055d-161">TimestampValidityDuration</span></span>  
 <span data-ttu-id="c055d-162">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="c055d-162">Data type: datetime</span></span>  
  
 <span data-ttu-id="c055d-163">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="c055d-163">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c055d-164">TimeSpan qui spécifie la durée de validité d'un horodatage.</span><span class="sxs-lookup"><span data-stu-id="c055d-164">A TimeSpan that specifies the duration in which a time stamp is valid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c055d-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c055d-165">Requirements</span></span>  
  
|<span data-ttu-id="c055d-166">MOF</span><span class="sxs-lookup"><span data-stu-id="c055d-166">MOF</span></span>|<span data-ttu-id="c055d-167">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="c055d-167">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c055d-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c055d-168">Namespace</span></span>|<span data-ttu-id="c055d-169">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c055d-169">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c055d-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c055d-170">See Also</span></span>  
 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
