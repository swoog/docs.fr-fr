---
title: Binding2
ms.date: 03/30/2017
ms.assetid: 09511c6c-5749-4bb0-874e-0f0be36bfe04
ms.openlocfilehash: 84e304f3dedcbd785d6238e6cb5eb142c288b995
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50198887"
---
# <a name="binding"></a><span data-ttu-id="45fad-102">Liaison</span><span class="sxs-lookup"><span data-stu-id="45fad-102">Binding</span></span>
<span data-ttu-id="45fad-103">WMI Binding</span><span class="sxs-lookup"><span data-stu-id="45fad-103">wmi Binding</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="45fad-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45fad-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="45fad-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45fad-105">Methods</span></span>  
 <span data-ttu-id="45fad-106">La classe Binding ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="45fad-106">The Binding class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="45fad-107">Properties</span><span class="sxs-lookup"><span data-stu-id="45fad-107">Properties</span></span>  
 <span data-ttu-id="45fad-108">La classe Binding a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="45fad-108">The Binding class has the following properties.</span></span>  
  
### <a name="bindingelements"></a><span data-ttu-id="45fad-109">BindingElement</span><span class="sxs-lookup"><span data-stu-id="45fad-109">BindingElements</span></span>  
 <span data-ttu-id="45fad-110">Type de données : tableau BindingElement</span><span class="sxs-lookup"><span data-stu-id="45fad-110">Data type: BindingElement array</span></span>  
  
 <span data-ttu-id="45fad-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="45fad-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="45fad-112">Collection d'éléments de liaison implémentés par la liaison.</span><span class="sxs-lookup"><span data-stu-id="45fad-112">The collection of binding elements implemented by the binding.</span></span>  
  
### <a name="closetimeout"></a><span data-ttu-id="45fad-113">CloseTimeout</span><span class="sxs-lookup"><span data-stu-id="45fad-113">CloseTimeout</span></span>  
 <span data-ttu-id="45fad-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="45fad-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="45fad-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="45fad-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="45fad-116">Intervalle de temps spécifié pour l'exécution d'une opération de fermeture.</span><span class="sxs-lookup"><span data-stu-id="45fad-116">The interval of time provided for a close operation to complete.</span></span>  
  
### <a name="name"></a><span data-ttu-id="45fad-117">Name</span><span class="sxs-lookup"><span data-stu-id="45fad-117">Name</span></span>  
 <span data-ttu-id="45fad-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="45fad-118">Data type: string</span></span>  
  
 <span data-ttu-id="45fad-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="45fad-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="45fad-120">Le nom de la liaison.</span><span class="sxs-lookup"><span data-stu-id="45fad-120">The name of the binding.</span></span>  
  
### <a name="namespace"></a><span data-ttu-id="45fad-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45fad-121">Namespace</span></span>  
 <span data-ttu-id="45fad-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="45fad-122">Data type: string</span></span>  
  
 <span data-ttu-id="45fad-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="45fad-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="45fad-124">Espace de noms XML de la liaison.</span><span class="sxs-lookup"><span data-stu-id="45fad-124">The XML namespace of the binding.</span></span>  
  
### <a name="opentimeout"></a><span data-ttu-id="45fad-125">OpenTimeout</span><span class="sxs-lookup"><span data-stu-id="45fad-125">OpenTimeout</span></span>  
 <span data-ttu-id="45fad-126">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="45fad-126">Data type: datetime</span></span>  
  
 <span data-ttu-id="45fad-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="45fad-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="45fad-128">Intervalle de temps spécifié pour l'exécution d'une opération d'ouverture.</span><span class="sxs-lookup"><span data-stu-id="45fad-128">The interval of time provided for an open operation to complete.</span></span>  
  
### <a name="receivetimeout"></a><span data-ttu-id="45fad-129">ReceiveTimeout</span><span class="sxs-lookup"><span data-stu-id="45fad-129">ReceiveTimeout</span></span>  
 <span data-ttu-id="45fad-130">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="45fad-130">Data type: datetime</span></span>  
  
 <span data-ttu-id="45fad-131">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="45fad-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="45fad-132">Intervalle de temps spécifié pour l'exécution d'une opération de réception.</span><span class="sxs-lookup"><span data-stu-id="45fad-132">The interval of time provided for a receive operation to complete.</span></span>  
  
### <a name="scheme"></a><span data-ttu-id="45fad-133">Scheme</span><span class="sxs-lookup"><span data-stu-id="45fad-133">Scheme</span></span>  
 <span data-ttu-id="45fad-134">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="45fad-134">Data type: string</span></span>  
  
 <span data-ttu-id="45fad-135">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="45fad-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="45fad-136">Modèle de transport URI utilisé par les fabrications et écouteurs de canal construits par la liaison.</span><span class="sxs-lookup"><span data-stu-id="45fad-136">The URI transport scheme that is used by the channel and listener factories that are built by the binding.</span></span>  
  
### <a name="sendtimeout"></a><span data-ttu-id="45fad-137">SendTimeout</span><span class="sxs-lookup"><span data-stu-id="45fad-137">SendTimeout</span></span>  
 <span data-ttu-id="45fad-138">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="45fad-138">Data type: datetime</span></span>  
  
 <span data-ttu-id="45fad-139">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="45fad-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="45fad-140">Intervalle de temps spécifié pour l'exécution d'une opération d'envoi.</span><span class="sxs-lookup"><span data-stu-id="45fad-140">The interval of time provided for a send operation to complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="45fad-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45fad-141">Requirements</span></span>  
  
|<span data-ttu-id="45fad-142">MOF</span><span class="sxs-lookup"><span data-stu-id="45fad-142">MOF</span></span>|<span data-ttu-id="45fad-143">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="45fad-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="45fad-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45fad-144">Namespace</span></span>|<span data-ttu-id="45fad-145">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="45fad-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="45fad-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45fad-146">See Also</span></span>  
 <xref:System.ServiceModel.Channels.Binding>
