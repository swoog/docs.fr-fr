---
title: Point de terminaison
ms.date: 03/30/2017
ms.assetid: fe63370d-81a1-40f3-97c2-59cb357c78d2
ms.openlocfilehash: 4562481e8b0b18c0ea0d9df0af3427ffe6419821
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61963603"
---
# <a name="endpoint"></a><span data-ttu-id="57b6e-102">Point de terminaison</span><span class="sxs-lookup"><span data-stu-id="57b6e-102">Endpoint</span></span>
<span data-ttu-id="57b6e-103">Point de terminaison</span><span class="sxs-lookup"><span data-stu-id="57b6e-103">Endpoint</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57b6e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57b6e-104">Syntax</span></span>  
  
```csharp
class Endpoint  
{  
  string Address;  
  string AddressHeaders[];  
  string AddressIdentity;  
  sint32 AppDomainId;  
  Behavior Behaviors[];  
  Binding Binding;  
  string ContractName;  
  string CounterInstanceName;  
  string ListenUri;  
  string Name;  
  sint32 ProcessId;  
  Contract ref;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="57b6e-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="57b6e-105">Methods</span></span>  
 <span data-ttu-id="57b6e-106">La classe Endpoint définit la méthode suivante.</span><span class="sxs-lookup"><span data-stu-id="57b6e-106">The Endpoint class defines the following method.</span></span>  
  
|<span data-ttu-id="57b6e-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="57b6e-107">Method</span></span>|<span data-ttu-id="57b6e-108">Description</span><span class="sxs-lookup"><span data-stu-id="57b6e-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="57b6e-109">GetOperationCounterInstanceName</span><span class="sxs-lookup"><span data-stu-id="57b6e-109">GetOperationCounterInstanceName</span></span>](../../../../../docs/framework/wcf/diagnostics/wmi/getoperationcounterinstancename.md)|<span data-ttu-id="57b6e-110">Récupère le nom d'instance du compteur de performance d'opération</span><span class="sxs-lookup"><span data-stu-id="57b6e-110">Retrieves the operation performance counter instance name</span></span>|  
  
## <a name="properties"></a><span data-ttu-id="57b6e-111">Properties</span><span class="sxs-lookup"><span data-stu-id="57b6e-111">Properties</span></span>  
 <span data-ttu-id="57b6e-112">La classe Endpoint a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="57b6e-112">The Endpoint class has the following properties:</span></span>  
  
### <a name="address"></a><span data-ttu-id="57b6e-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="57b6e-113">Address</span></span>  
 <span data-ttu-id="57b6e-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="57b6e-114">Data type: string</span></span>  
  
 <span data-ttu-id="57b6e-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-116">URI qui contient l'adresse du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-116">A URI that contains the address of the endpoint.</span></span>  
  
### <a name="addressheaders"></a><span data-ttu-id="57b6e-117">AddressHeaders</span><span class="sxs-lookup"><span data-stu-id="57b6e-117">AddressHeaders</span></span>  
 <span data-ttu-id="57b6e-118">Type de données : tableau de chaînes</span><span class="sxs-lookup"><span data-stu-id="57b6e-118">Data type: string array</span></span>  
  
 <span data-ttu-id="57b6e-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-120">Collection d’en-têtes d’adresse jointe à ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-120">The collection of address headers attached to this endpoint.</span></span>  
  
### <a name="addressidentity"></a><span data-ttu-id="57b6e-121">AddressIdentity</span><span class="sxs-lookup"><span data-stu-id="57b6e-121">AddressIdentity</span></span>  
 <span data-ttu-id="57b6e-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="57b6e-122">Data type: string</span></span>  
  
 <span data-ttu-id="57b6e-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-124">Identité du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-124">The identity of the endpoint.</span></span>  
  
### <a name="appdomainid"></a><span data-ttu-id="57b6e-125">AppDomainId</span><span class="sxs-lookup"><span data-stu-id="57b6e-125">AppDomainId</span></span>  
 <span data-ttu-id="57b6e-126">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="57b6e-126">Data type: sint32</span></span>  
  
 <span data-ttu-id="57b6e-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-128">ID du domaine d'application qui héberge le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-128">The appdomain id of the appdomain that hosts the endpoint.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="57b6e-129">comportements</span><span class="sxs-lookup"><span data-stu-id="57b6e-129">Behaviors</span></span>  
 <span data-ttu-id="57b6e-130">Type de données : Tableau de comportements</span><span class="sxs-lookup"><span data-stu-id="57b6e-130">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="57b6e-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-132">Collection de comportements implémentée par ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-132">The collection of behaviors implemented by this endpoint.</span></span>  
  
### <a name="binding"></a><span data-ttu-id="57b6e-133">Liaison</span><span class="sxs-lookup"><span data-stu-id="57b6e-133">Binding</span></span>  
 <span data-ttu-id="57b6e-134">Type de données : Liaison</span><span class="sxs-lookup"><span data-stu-id="57b6e-134">Data type: Binding</span></span>  
  
 <span data-ttu-id="57b6e-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-136">Liaison utilisée par ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-136">The binding used by this endpoint.</span></span>  
  
### <a name="contractname"></a><span data-ttu-id="57b6e-137">ContractName</span><span class="sxs-lookup"><span data-stu-id="57b6e-137">ContractName</span></span>  
 <span data-ttu-id="57b6e-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="57b6e-138">Data type: string</span></span>  
  
 <span data-ttu-id="57b6e-139">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-140">Chaîne qui spécifie quel contrat est exposé par ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-140">A string that specifies which contract this endpoint is exposing.</span></span>  
  
### <a name="counterinstancename"></a><span data-ttu-id="57b6e-141">CounterInstanceName</span><span class="sxs-lookup"><span data-stu-id="57b6e-141">CounterInstanceName</span></span>  
 <span data-ttu-id="57b6e-142">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="57b6e-142">Data type: string</span></span>  
  
 <span data-ttu-id="57b6e-143">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-144">Nom de l'instance des compteurs de performance du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-144">The name of the instance of performance counters of the endpoint.</span></span>  
  
### <a name="listenuri"></a><span data-ttu-id="57b6e-145">ListenUri</span><span class="sxs-lookup"><span data-stu-id="57b6e-145">ListenUri</span></span>  
 <span data-ttu-id="57b6e-146">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="57b6e-146">Data type: string</span></span>  
  
 <span data-ttu-id="57b6e-147">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-148">URI sur lequel le point de terminaison écoute.</span><span class="sxs-lookup"><span data-stu-id="57b6e-148">The Uri the endpoint listens on.</span></span>  
  
### <a name="name"></a><span data-ttu-id="57b6e-149">Nom</span><span class="sxs-lookup"><span data-stu-id="57b6e-149">Name</span></span>  
 <span data-ttu-id="57b6e-150">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="57b6e-150">Data type: string</span></span>  
  
 <span data-ttu-id="57b6e-151">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-152">Nom unique de ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-152">The unique name of this endpoint.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="57b6e-153">ProcessId</span><span class="sxs-lookup"><span data-stu-id="57b6e-153">ProcessId</span></span>  
 <span data-ttu-id="57b6e-154">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="57b6e-154">Data type: sint32</span></span>  
  
 <span data-ttu-id="57b6e-155">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-156">ID du processus qui héberge le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-156">The process Id of the process that hosts the endpoint.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="57b6e-157">ref</span><span class="sxs-lookup"><span data-stu-id="57b6e-157">ref</span></span>  
 <span data-ttu-id="57b6e-158">Type de données : Contrat</span><span class="sxs-lookup"><span data-stu-id="57b6e-158">Data type: Contract</span></span>  
  
 <span data-ttu-id="57b6e-159">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="57b6e-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="57b6e-160">Le contrat exposé par ce point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="57b6e-160">The contract this endpoint is exposing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57b6e-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57b6e-161">Requirements</span></span>  
  
|<span data-ttu-id="57b6e-162">MOF</span><span class="sxs-lookup"><span data-stu-id="57b6e-162">MOF</span></span>|<span data-ttu-id="57b6e-163">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="57b6e-163">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="57b6e-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="57b6e-164">Namespace</span></span>|<span data-ttu-id="57b6e-165">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="57b6e-165">Defined in root\ServiceModel</span></span>|
