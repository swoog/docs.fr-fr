---
title: Contract1
ms.date: 03/30/2017
ms.assetid: aa00f6b3-7e1f-4213-841a-206463fca20b
ms.openlocfilehash: 10789f9a2940c239ae20c8fd1e9d48bca0e820ed
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59772997"
---
# <a name="contract"></a><span data-ttu-id="92582-102">Contrat</span><span class="sxs-lookup"><span data-stu-id="92582-102">Contract</span></span>
<span data-ttu-id="92582-103">Contrat</span><span class="sxs-lookup"><span data-stu-id="92582-103">Contract</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="92582-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92582-104">Syntax</span></span>  
  
```csharp
class Contract  
{  
  sint32 AppDomainId;  
  Behavior Behaviors[];  
  string Name;  
  string Namespace;  
  Operation Operations[];  
  sint32 ProcessId;  
  Contract ref;  
  string SessionMode;  
  string Type;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="92582-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92582-105">Methods</span></span>  
 <span data-ttu-id="92582-106">La classe Contract ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="92582-106">The Contract class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="92582-107">Properties</span><span class="sxs-lookup"><span data-stu-id="92582-107">Properties</span></span>  
 <span data-ttu-id="92582-108">La classe Contract a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="92582-108">The Contract class has the following properties:</span></span>  
  
### <a name="appdomainid"></a><span data-ttu-id="92582-109">AppDomainId</span><span class="sxs-lookup"><span data-stu-id="92582-109">AppDomainId</span></span>  
 <span data-ttu-id="92582-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="92582-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="92582-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-112">ID du domaine d'application qui héberge le contrat.</span><span class="sxs-lookup"><span data-stu-id="92582-112">The appdomain id of the appdomain that hosts the contract.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="92582-113">comportements</span><span class="sxs-lookup"><span data-stu-id="92582-113">Behaviors</span></span>  
 <span data-ttu-id="92582-114">Type de données : Tableau de comportements</span><span class="sxs-lookup"><span data-stu-id="92582-114">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="92582-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-116">Comportements associés à ce contrat.</span><span class="sxs-lookup"><span data-stu-id="92582-116">The behaviors associated with this contract.</span></span>  
  
### <a name="name"></a><span data-ttu-id="92582-117">Nom</span><span class="sxs-lookup"><span data-stu-id="92582-117">Name</span></span>  
 <span data-ttu-id="92582-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="92582-118">Data type: string</span></span>  
  
 <span data-ttu-id="92582-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-120">Nom du contrat dans WSDL.</span><span class="sxs-lookup"><span data-stu-id="92582-120">The name of the contract in WSDL.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="92582-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92582-121">Namespace</span></span>  
 <span data-ttu-id="92582-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="92582-122">Data type: string</span></span>  
  
 <span data-ttu-id="92582-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-124">Espace de noms de l'élément `portType` dans WSDL.</span><span class="sxs-lookup"><span data-stu-id="92582-124">The namespace of the `portType` element in WSDL.</span></span>  
  
### <a name="operations"></a><span data-ttu-id="92582-125">Opérations</span><span class="sxs-lookup"><span data-stu-id="92582-125">Operations</span></span>  
 <span data-ttu-id="92582-126">Type de données : Tableau d’opérations</span><span class="sxs-lookup"><span data-stu-id="92582-126">Data type: Operation array</span></span>  
  
 <span data-ttu-id="92582-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-128">Opérations de ce contrat.</span><span class="sxs-lookup"><span data-stu-id="92582-128">The operations of this contract.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="92582-129">ProcessId</span><span class="sxs-lookup"><span data-stu-id="92582-129">ProcessId</span></span>  
 <span data-ttu-id="92582-130">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="92582-130">Data type: sint32</span></span>  
  
 <span data-ttu-id="92582-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-132">ID du processus qui héberge le contrat.</span><span class="sxs-lookup"><span data-stu-id="92582-132">The process Id of the process that hosts the contract.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="92582-133">ref</span><span class="sxs-lookup"><span data-stu-id="92582-133">ref</span></span>  
 <span data-ttu-id="92582-134">Type de données : Contrat</span><span class="sxs-lookup"><span data-stu-id="92582-134">Data type: Contract</span></span>  
  
 <span data-ttu-id="92582-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-136">Type de rappel lorsque le contrat est un contrat duplex.</span><span class="sxs-lookup"><span data-stu-id="92582-136">The type of callback when the contract is a duplex contract.</span></span>  
  
### <a name="sessionmode"></a><span data-ttu-id="92582-137">SessionMode</span><span class="sxs-lookup"><span data-stu-id="92582-137">SessionMode</span></span>  
 <span data-ttu-id="92582-138">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="92582-138">Data type: string</span></span>  
  
 <span data-ttu-id="92582-139">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-140">Indique si le contrat nécessite que la liaison associée à ce contrat utilise les sessions de canal.</span><span class="sxs-lookup"><span data-stu-id="92582-140">Indicates whether the contract requires the binding associated with this contract to use channel sessions.</span></span>  
  
### <a name="type"></a><span data-ttu-id="92582-141">Type</span><span class="sxs-lookup"><span data-stu-id="92582-141">Type</span></span>  
 <span data-ttu-id="92582-142">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="92582-142">Data type: string</span></span>  
  
 <span data-ttu-id="92582-143">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="92582-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="92582-144">Type du contrat.</span><span class="sxs-lookup"><span data-stu-id="92582-144">The type of the contract.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="92582-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92582-145">Requirements</span></span>  
  
|<span data-ttu-id="92582-146">MOF</span><span class="sxs-lookup"><span data-stu-id="92582-146">MOF</span></span>|<span data-ttu-id="92582-147">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="92582-147">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="92582-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92582-148">Namespace</span></span>|<span data-ttu-id="92582-149">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="92582-149">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="92582-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92582-150">See also</span></span>

- <xref:System.ServiceModel.Description.ContractDescription>
