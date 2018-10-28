---
title: AppDomainInfo
ms.date: 03/30/2017
ms.assetid: 6610b7d8-81eb-4bec-a543-9b72ad7b6f73
ms.openlocfilehash: 0b7f8aadbd9a9dfcdd33fc65be3a5a41ea95f5be
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50170222"
---
# <a name="appdomaininfo"></a><span data-ttu-id="1444e-102">AppDomainInfo</span><span class="sxs-lookup"><span data-stu-id="1444e-102">AppDomainInfo</span></span>
<span data-ttu-id="1444e-103">Informations du domaine d'application</span><span class="sxs-lookup"><span data-stu-id="1444e-103">Application domain information</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1444e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1444e-104">Syntax</span></span>  
  
```csharp
class AppDomainInfo  
{  
  sint32 AppDomainId;  
  boolean IsDefault;  
  boolean LogMalformedMessages;  
  boolean LogMessagesAtServiceLevel;  
  boolean LogMessagesAtTransportLevel;  
  TraceListener MessageLoggingTraceListeners[];  
  string Name;  
  string PerformanceCounters;  
  sint32 ProcessId;  
  string ServiceConfigPath;  
  string TraceLevel;  
  TraceListener wmiTraceListeners[];  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="1444e-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1444e-105">Methods</span></span>  
 <span data-ttu-id="1444e-106">La classe AppDomainInfo ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="1444e-106">The AppDomainInfo class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="1444e-107">Properties</span><span class="sxs-lookup"><span data-stu-id="1444e-107">Properties</span></span>  
 <span data-ttu-id="1444e-108">La classe AppDomainInfo a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="1444e-108">The AppDomainInfo class has the following properties:</span></span>  
  
### <a name="appdomainid"></a><span data-ttu-id="1444e-109">AppDomainId</span><span class="sxs-lookup"><span data-stu-id="1444e-109">AppDomainId</span></span>  
 <span data-ttu-id="1444e-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="1444e-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="1444e-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="1444e-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1444e-112">ID de l'appdomain.</span><span class="sxs-lookup"><span data-stu-id="1444e-112">The Id of the appdomain.</span></span>  
  
### <a name="isdefault"></a><span data-ttu-id="1444e-113">IsDefault</span><span class="sxs-lookup"><span data-stu-id="1444e-113">IsDefault</span></span>  
 <span data-ttu-id="1444e-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="1444e-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="1444e-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="1444e-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1444e-116">Indique si l'appdomain est l'appdomain par défaut.</span><span class="sxs-lookup"><span data-stu-id="1444e-116">Indicates whether the appdomain is the default appdomain.</span></span>  
  
### <a name="logmalformedmessages"></a><span data-ttu-id="1444e-117">LogMalformedMessages</span><span class="sxs-lookup"><span data-stu-id="1444e-117">LogMalformedMessages</span></span>  
 <span data-ttu-id="1444e-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="1444e-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="1444e-119">Type d'accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1444e-119">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="1444e-120">Valeur qui spécifie si les messages incorrects sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="1444e-120">A value that specifies whether malformed messages are logged.</span></span>  
  
### <a name="logmessagesatservicelevel"></a><span data-ttu-id="1444e-121">LogMessagesAtServiceLevel</span><span class="sxs-lookup"><span data-stu-id="1444e-121">LogMessagesAtServiceLevel</span></span>  
 <span data-ttu-id="1444e-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="1444e-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="1444e-123">Type d'accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1444e-123">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="1444e-124">Valeur qui spécifie si les messages sont suivis au niveau du service (avant les transformations associées au chiffrement et au transport).</span><span class="sxs-lookup"><span data-stu-id="1444e-124">A value that specifies whether messages are traced at the service level (before encryption and transport-related transforms).</span></span>  
  
### <a name="logmessagesattransportlevel"></a><span data-ttu-id="1444e-125">LogMessagesAtTransportLevel</span><span class="sxs-lookup"><span data-stu-id="1444e-125">LogMessagesAtTransportLevel</span></span>  
 <span data-ttu-id="1444e-126">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="1444e-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="1444e-127">Type d'accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1444e-127">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="1444e-128">Valeur qui spécifie si les messages sont suivis au niveau du transport.</span><span class="sxs-lookup"><span data-stu-id="1444e-128">A value that specifies whether messages are traced at the transport level.</span></span>  
  
### <a name="messageloggingtracelisteners"></a><span data-ttu-id="1444e-129">MessageLoggingTraceListeners</span><span class="sxs-lookup"><span data-stu-id="1444e-129">MessageLoggingTraceListeners</span></span>  
 <span data-ttu-id="1444e-130">Type de données : tableau TraceListener</span><span class="sxs-lookup"><span data-stu-id="1444e-130">Data type: TraceListener array</span></span>  
  
 <span data-ttu-id="1444e-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="1444e-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1444e-132">Écouteurs de suivi de la collection qui écoutent la source de suivi System.Wmi.MessageLogging.</span><span class="sxs-lookup"><span data-stu-id="1444e-132">The collection trace listeners that listen to the System.Wmi.MessageLogging trace source.</span></span>  
  
### <a name="name"></a><span data-ttu-id="1444e-133">Name</span><span class="sxs-lookup"><span data-stu-id="1444e-133">Name</span></span>  
 <span data-ttu-id="1444e-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="1444e-134">Data type: string</span></span>  
  
 <span data-ttu-id="1444e-135">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="1444e-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1444e-136">Nom de l'appdomain.</span><span class="sxs-lookup"><span data-stu-id="1444e-136">The name of the appdomain.</span></span>  
  
### <a name="performancecounters"></a><span data-ttu-id="1444e-137">PerformanceCounters</span><span class="sxs-lookup"><span data-stu-id="1444e-137">PerformanceCounters</span></span>  
 <span data-ttu-id="1444e-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="1444e-138">Data type: string</span></span>  
  
 <span data-ttu-id="1444e-139">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="1444e-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1444e-140">Portée de compteurs de performance actifs dans l'appdomain.</span><span class="sxs-lookup"><span data-stu-id="1444e-140">The scope of active performance counters in the appdomain.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="1444e-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="1444e-141">ProcessId</span></span>  
 <span data-ttu-id="1444e-142">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="1444e-142">Data type: sint32</span></span>  
  
 <span data-ttu-id="1444e-143">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="1444e-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1444e-144">ID de processus.</span><span class="sxs-lookup"><span data-stu-id="1444e-144">The process Id.</span></span>  
  
### <a name="serviceconfigpath"></a><span data-ttu-id="1444e-145">ServiceConfigPath</span><span class="sxs-lookup"><span data-stu-id="1444e-145">ServiceConfigPath</span></span>  
 <span data-ttu-id="1444e-146">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="1444e-146">Data type: string</span></span>  
  
 <span data-ttu-id="1444e-147">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="1444e-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1444e-148">Chemin d’accès à la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="1444e-148">The path to the configuration of the service.</span></span>  
  
### <a name="tracelevel"></a><span data-ttu-id="1444e-149">TraceLevel</span><span class="sxs-lookup"><span data-stu-id="1444e-149">TraceLevel</span></span>  
 <span data-ttu-id="1444e-150">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="1444e-150">Data type: string</span></span>  
  
 <span data-ttu-id="1444e-151">Type d'accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1444e-151">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="1444e-152">Niveau de suivi de la source de suivi System.Wmi.</span><span class="sxs-lookup"><span data-stu-id="1444e-152">The trace level of the System.Wmi trace source.</span></span>  
  
### <a name="servicemodeltracelisteners"></a><span data-ttu-id="1444e-153">ServiceModelTraceListeners</span><span class="sxs-lookup"><span data-stu-id="1444e-153">ServiceModelTraceListeners</span></span>  
 <span data-ttu-id="1444e-154">Type de données : tableau TraceListener</span><span class="sxs-lookup"><span data-stu-id="1444e-154">Data type: TraceListener array</span></span>  
  
 <span data-ttu-id="1444e-155">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="1444e-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1444e-156">Collection d’écouteurs de la source de suivi System.ServiceModel.</span><span class="sxs-lookup"><span data-stu-id="1444e-156">A collection of listeners from the System.ServiceModel trace source.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1444e-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1444e-157">Requirements</span></span>  
  
|<span data-ttu-id="1444e-158">MOF</span><span class="sxs-lookup"><span data-stu-id="1444e-158">MOF</span></span>|<span data-ttu-id="1444e-159">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="1444e-159">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="1444e-160">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1444e-160">Namespace</span></span>|<span data-ttu-id="1444e-161">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="1444e-161">Defined in root\ServiceModel</span></span>|
