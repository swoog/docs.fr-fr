---
title: Binding2
ms.date: 03/30/2017
ms.assetid: 09511c6c-5749-4bb0-874e-0f0be36bfe04
ms.openlocfilehash: a040cc6e12833d2c737eb14c591300e5873ddce7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59106513"
---
# <a name="binding"></a><span data-ttu-id="113b1-102">Liaison</span><span class="sxs-lookup"><span data-stu-id="113b1-102">Binding</span></span>
<span data-ttu-id="113b1-103">WMI Binding</span><span class="sxs-lookup"><span data-stu-id="113b1-103">wmi Binding</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="113b1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="113b1-104">Syntax</span></span>  
  
```csharp
class Binding  
{  
  BindingElement BindingElements[];  
  datetime CloseTimeout;  
  string Name;  
  string Namespace;  
  datetime OpenTimeout;  
  datetime ReceiveTimeout;  
  string Scheme;  
  datetime SendTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="113b1-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="113b1-105">Methods</span></span>  
 <span data-ttu-id="113b1-106">La classe Binding ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="113b1-106">The Binding class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="113b1-107">Properties</span><span class="sxs-lookup"><span data-stu-id="113b1-107">Properties</span></span>  
 <span data-ttu-id="113b1-108">La classe Binding a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="113b1-108">The Binding class has the following properties.</span></span>  
  
### <a name="bindingelements"></a><span data-ttu-id="113b1-109">BindingElement</span><span class="sxs-lookup"><span data-stu-id="113b1-109">BindingElements</span></span>  
 <span data-ttu-id="113b1-110">Type de données : Tableau BindingElement</span><span class="sxs-lookup"><span data-stu-id="113b1-110">Data type: BindingElement array</span></span>  
  
 <span data-ttu-id="113b1-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="113b1-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="113b1-112">Collection d'éléments de liaison implémentés par la liaison.</span><span class="sxs-lookup"><span data-stu-id="113b1-112">The collection of binding elements implemented by the binding.</span></span>  
  
### <a name="closetimeout"></a><span data-ttu-id="113b1-113">CloseTimeout</span><span class="sxs-lookup"><span data-stu-id="113b1-113">CloseTimeout</span></span>  
 <span data-ttu-id="113b1-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="113b1-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="113b1-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="113b1-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="113b1-116">Intervalle de temps spécifié pour l'exécution d'une opération de fermeture.</span><span class="sxs-lookup"><span data-stu-id="113b1-116">The interval of time provided for a close operation to complete.</span></span>  
  
### <a name="name"></a><span data-ttu-id="113b1-117">Nom</span><span class="sxs-lookup"><span data-stu-id="113b1-117">Name</span></span>  
 <span data-ttu-id="113b1-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="113b1-118">Data type: string</span></span>  
  
 <span data-ttu-id="113b1-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="113b1-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="113b1-120">Le nom de la liaison.</span><span class="sxs-lookup"><span data-stu-id="113b1-120">The name of the binding.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="113b1-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="113b1-121">Namespace</span></span>  
 <span data-ttu-id="113b1-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="113b1-122">Data type: string</span></span>  
  
 <span data-ttu-id="113b1-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="113b1-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="113b1-124">Espace de noms XML de la liaison.</span><span class="sxs-lookup"><span data-stu-id="113b1-124">The XML namespace of the binding.</span></span>  
  
### <a name="opentimeout"></a><span data-ttu-id="113b1-125">OpenTimeout</span><span class="sxs-lookup"><span data-stu-id="113b1-125">OpenTimeout</span></span>  
 <span data-ttu-id="113b1-126">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="113b1-126">Data type: datetime</span></span>  
  
 <span data-ttu-id="113b1-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="113b1-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="113b1-128">Intervalle de temps spécifié pour l'exécution d'une opération d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="113b1-128">The interval of time provided for an open operation to complete.</span></span>  
  
### <a name="receivetimeout"></a><span data-ttu-id="113b1-129">ReceiveTimeout</span><span class="sxs-lookup"><span data-stu-id="113b1-129">ReceiveTimeout</span></span>  
 <span data-ttu-id="113b1-130">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="113b1-130">Data type: datetime</span></span>  
  
 <span data-ttu-id="113b1-131">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="113b1-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="113b1-132">Intervalle de temps spécifié pour l'exécution d'une opération de réception.</span><span class="sxs-lookup"><span data-stu-id="113b1-132">The interval of time provided for a receive operation to complete.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="113b1-133">Scheme</span><span class="sxs-lookup"><span data-stu-id="113b1-133">Scheme</span></span>  
 <span data-ttu-id="113b1-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="113b1-134">Data type: string</span></span>  
  
 <span data-ttu-id="113b1-135">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="113b1-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="113b1-136">Modèle de transport URI utilisé par les fabrications et écouteurs de canal construits par la liaison.</span><span class="sxs-lookup"><span data-stu-id="113b1-136">The URI transport scheme that is used by the channel and listener factories that are built by the binding.</span></span>  
  
### <a name="sendtimeout"></a><span data-ttu-id="113b1-137">SendTimeout</span><span class="sxs-lookup"><span data-stu-id="113b1-137">SendTimeout</span></span>  
 <span data-ttu-id="113b1-138">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="113b1-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="113b1-139">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="113b1-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="113b1-140">Intervalle de temps spécifié pour l'exécution d'une opération d'envoi.</span><span class="sxs-lookup"><span data-stu-id="113b1-140">The interval of time provided for a send operation to complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="113b1-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="113b1-141">Requirements</span></span>  
  
|<span data-ttu-id="113b1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="113b1-142">MOF</span></span>|<span data-ttu-id="113b1-143">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="113b1-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="113b1-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="113b1-144">Namespace</span></span>|<span data-ttu-id="113b1-145">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="113b1-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="113b1-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="113b1-146">See also</span></span>

- <xref:System.ServiceModel.Channels.Binding>
