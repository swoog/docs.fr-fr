---
title: LocalServiceSecuritySettings
ms.date: 03/30/2017
ms.assetid: 490aa0e5-5242-4f8d-b505-5ec6287633b4
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 8f80af782c474ccf3a232ab353125fa223d4f5d1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33486895"
---
# <a name="localservicesecuritysettings"></a><span data-ttu-id="dff12-102">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="dff12-102">LocalServiceSecuritySettings</span></span>
<span data-ttu-id="dff12-103">LocalServiceSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="dff12-103">LocalServiceSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dff12-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dff12-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="dff12-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dff12-105">Methods</span></span>  
 <span data-ttu-id="dff12-106">La classe LocalServiceSecuritySettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="dff12-106">The LocalServiceSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="dff12-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dff12-107">Properties</span></span>  
 <span data-ttu-id="dff12-108">La classe LocalServiceSecuritySettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="dff12-108">The LocalServiceSecuritySettings class has the following properties:</span></span>  
  
### <a name="detectreplays"></a><span data-ttu-id="dff12-109">DetectReplays</span><span class="sxs-lookup"><span data-stu-id="dff12-109">DetectReplays</span></span>  
 <span data-ttu-id="dff12-110">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="dff12-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="dff12-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-112">Valeur booléenne qui spécifie si les attaques par relecture contre le canal sont détectées et traitées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="dff12-112">A Boolean value that specifies whether replay attacks against the channel are detected and dealt with automatically.</span></span>  
  
### <a name="inactivitytimeout"></a><span data-ttu-id="dff12-113">InactivityTimeout</span><span class="sxs-lookup"><span data-stu-id="dff12-113">InactivityTimeout</span></span>  
 <span data-ttu-id="dff12-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="dff12-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="dff12-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-116">Nombre maximal de sessions de sécurité en attente que le service prend en charge.</span><span class="sxs-lookup"><span data-stu-id="dff12-116">The maximum number of pending security sessions that the service supports.</span></span>  
  
### <a name="issuedcookielifetime"></a><span data-ttu-id="dff12-117">IssuedCookieLifetime</span><span class="sxs-lookup"><span data-stu-id="dff12-117">IssuedCookieLifetime</span></span>  
 <span data-ttu-id="dff12-118">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="dff12-118">Data type: datetime</span></span>  
  
 <span data-ttu-id="dff12-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-120">TimeSpan qui spécifie la durée de vie de tous les nouveaux cookies de sécurité.</span><span class="sxs-lookup"><span data-stu-id="dff12-120">A TimeSpan that specifies the lifetime issued to all new security cookies.</span></span>  
  
### <a name="maxcachedcookies"></a><span data-ttu-id="dff12-121">MaxCachedCookies</span><span class="sxs-lookup"><span data-stu-id="dff12-121">MaxCachedCookies</span></span>  
 <span data-ttu-id="dff12-122">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="dff12-122">Data type: sint32</span></span>  
  
 <span data-ttu-id="dff12-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-124">Nombre maximal de cookies qui peuvent être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="dff12-124">The maximum number of cookies that can be cached.</span></span>  
  
### <a name="maxclockskew"></a><span data-ttu-id="dff12-125">MaxClockSkew</span><span class="sxs-lookup"><span data-stu-id="dff12-125">MaxClockSkew</span></span>  
 <span data-ttu-id="dff12-126">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="dff12-126">Data type: datetime</span></span>  
  
 <span data-ttu-id="dff12-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-128">TimeSpan qui spécifie la différence de temps maximale entre les horloges système des deux parties communicantes.</span><span class="sxs-lookup"><span data-stu-id="dff12-128">A TimeSpan that specifies the maximum time difference between the system clocks of the two communicating parties.</span></span>  
  
### <a name="maxpendingsessions"></a><span data-ttu-id="dff12-129">MaxPendingSessions</span><span class="sxs-lookup"><span data-stu-id="dff12-129">MaxPendingSessions</span></span>  
 <span data-ttu-id="dff12-130">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="dff12-130">Data type: sint32</span></span>  
  
 <span data-ttu-id="dff12-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-132">Nombre maximal de connexions en attente sur le service.</span><span class="sxs-lookup"><span data-stu-id="dff12-132">The maximum number of pending connections on the service.</span></span>  
  
### <a name="maxstatefulnegotiations"></a><span data-ttu-id="dff12-133">MaxStatefulNegotiations</span><span class="sxs-lookup"><span data-stu-id="dff12-133">MaxStatefulNegotiations</span></span>  
 <span data-ttu-id="dff12-134">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="dff12-134">Data type: sint32</span></span>  
  
 <span data-ttu-id="dff12-135">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-136">Nombre de négociations de sécurité qui peuvent être actives simultanément.</span><span class="sxs-lookup"><span data-stu-id="dff12-136">The number of security negotiations that can be active concurrently.</span></span>  
  
### <a name="negotiationtimeout"></a><span data-ttu-id="dff12-137">NegotiationTimeout</span><span class="sxs-lookup"><span data-stu-id="dff12-137">NegotiationTimeout</span></span>  
 <span data-ttu-id="dff12-138">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="dff12-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="dff12-139">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-140">TimeSpan qui spécifie la durée maximale de la phase de négociation de sécurité entre le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="dff12-140">A TimeSpan that specifies the maximum duration for the security negotiation phase between server and client.</span></span>  
  
### <a name="reconnecttransportonfailure"></a><span data-ttu-id="dff12-141">ReconnectTransportOnFailure</span><span class="sxs-lookup"><span data-stu-id="dff12-141">ReconnectTransportOnFailure</span></span>  
 <span data-ttu-id="dff12-142">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="dff12-142">Data type: boolean</span></span>  
  
 <span data-ttu-id="dff12-143">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-144">Valeur booléenne qui spécifie si des connexions utilisant la messagerie WS-Reliable tentent une reconnexion après des incidents de transport.</span><span class="sxs-lookup"><span data-stu-id="dff12-144">A Boolean value that specifies whether connections using WS-Reliable messaging attempt to reconnect after transport failures.</span></span>  
  
### <a name="replaycachesize"></a><span data-ttu-id="dff12-145">ReplayCacheSize</span><span class="sxs-lookup"><span data-stu-id="dff12-145">ReplayCacheSize</span></span>  
 <span data-ttu-id="dff12-146">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="dff12-146">Data type: sint32</span></span>  
  
 <span data-ttu-id="dff12-147">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-148">Nombre de pointeurs en cache utilisés pour la détection de relecture.</span><span class="sxs-lookup"><span data-stu-id="dff12-148">The number of cached nonces used for replay detection.</span></span>  
  
### <a name="replaywindow"></a><span data-ttu-id="dff12-149">ReplayWindow</span><span class="sxs-lookup"><span data-stu-id="dff12-149">ReplayWindow</span></span>  
 <span data-ttu-id="dff12-150">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="dff12-150">Data type: datetime</span></span>  
  
 <span data-ttu-id="dff12-151">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-152">TimeSpan qui spécifie la durée de validité des pointeurs de messages individuels.</span><span class="sxs-lookup"><span data-stu-id="dff12-152">A TimeSpan that specifies the duration in which individual message nonces are valid.</span></span>  
  
### <a name="sessionkeyrenewalinterval"></a><span data-ttu-id="dff12-153">SessionKeyRenewalInterval</span><span class="sxs-lookup"><span data-stu-id="dff12-153">SessionKeyRenewalInterval</span></span>  
 <span data-ttu-id="dff12-154">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="dff12-154">Data type: datetime</span></span>  
  
 <span data-ttu-id="dff12-155">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-156">TimeSpan qui spécifie le délai d'attente au terme duquel l'initiateur renouvelle la clé de la session de sécurité.</span><span class="sxs-lookup"><span data-stu-id="dff12-156">A TimeSpan that specifies the duration after which the initiator renews the key for the security session.</span></span>  
  
### <a name="sessionkeyrolloverinterval"></a><span data-ttu-id="dff12-157">SessionKeyRolloverInterval</span><span class="sxs-lookup"><span data-stu-id="dff12-157">SessionKeyRolloverInterval</span></span>  
 <span data-ttu-id="dff12-158">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="dff12-158">Data type: datetime</span></span>  
  
 <span data-ttu-id="dff12-159">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-160">TimeSpan qui spécifie la période de validité d'une clé de session précédente sur les messages entrants pendant un renouvellement de clé.</span><span class="sxs-lookup"><span data-stu-id="dff12-160">A TimeSpan that specifies the time interval a previous session key is valid on incoming messages during a key renewal.</span></span>  
  
### <a name="timestampvalidityduration"></a><span data-ttu-id="dff12-161">TimestampValidityDuration</span><span class="sxs-lookup"><span data-stu-id="dff12-161">TimestampValidityDuration</span></span>  
 <span data-ttu-id="dff12-162">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="dff12-162">Data type: datetime</span></span>  
  
 <span data-ttu-id="dff12-163">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="dff12-163">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dff12-164">TimeSpan qui spécifie la durée de validité d'un horodatage.</span><span class="sxs-lookup"><span data-stu-id="dff12-164">A TimeSpan that specifies the duration in which a time stamp is valid.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dff12-165">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dff12-165">Requirements</span></span>  
  
|<span data-ttu-id="dff12-166">MOF</span><span class="sxs-lookup"><span data-stu-id="dff12-166">MOF</span></span>|<span data-ttu-id="dff12-167">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="dff12-167">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="dff12-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dff12-168">Namespace</span></span>|<span data-ttu-id="dff12-169">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="dff12-169">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dff12-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dff12-170">See Also</span></span>  
 <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
