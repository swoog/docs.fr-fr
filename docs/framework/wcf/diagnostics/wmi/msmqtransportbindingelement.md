---
title: MsmqTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 1c89f073-9ed3-4025-a8c5-13535a0f526b
ms.openlocfilehash: 33cd9c427ed5ad04eaf9e9889f60f091f335d1e7
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49374007"
---
# <a name="msmqtransportbindingelement"></a><span data-ttu-id="02174-102">MsmqTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="02174-102">MsmqTransportBindingElement</span></span>
<span data-ttu-id="02174-103">MsmqTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="02174-103">MsmqTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="02174-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02174-104">Syntax</span></span>  
  
```csharp
class MsmqTransportBindingElement : MsmqBindingElementBase  
{  
  sint32 MaxPoolSize;  
  string QueueTransferProtocol;  
  boolean UseActiveDirectory;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="02174-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="02174-105">Methods</span></span>  
 <span data-ttu-id="02174-106">La classe MsmqTransportBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="02174-106">The MsmqTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="02174-107">Properties</span><span class="sxs-lookup"><span data-stu-id="02174-107">Properties</span></span>  
 <span data-ttu-id="02174-108">La classe MsmqTransportBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="02174-108">The MsmqTransportBindingElement class has the following properties:</span></span>  
  
### <a name="maxpoolsize"></a><span data-ttu-id="02174-109">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="02174-109">MaxPoolSize</span></span>  
 <span data-ttu-id="02174-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="02174-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="02174-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="02174-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="02174-112">Taille maximale du pool contenant des objets de message MSMQ internes.</span><span class="sxs-lookup"><span data-stu-id="02174-112">The maximum size of the pool that contains internal MSMQ message objects.</span></span>  
  
### <a name="queuetransferprotocol"></a><span data-ttu-id="02174-113">QueueTransferProtocol</span><span class="sxs-lookup"><span data-stu-id="02174-113">QueueTransferProtocol</span></span>  
 <span data-ttu-id="02174-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="02174-114">Data type: string</span></span>  
  
 <span data-ttu-id="02174-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="02174-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="02174-116">Valeur d’énumération qui indique le transport de canal de communication mis en file d’attente que cette liaison utilise.</span><span class="sxs-lookup"><span data-stu-id="02174-116">An enumeration value that indicates the queued communication channel transport that this binding uses.</span></span>  
  
### <a name="useactivedirectory"></a><span data-ttu-id="02174-117">UseActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="02174-117">UseActiveDirectory</span></span>  
 <span data-ttu-id="02174-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="02174-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="02174-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="02174-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="02174-120">Retourne une valeur Boolean qui indique si les adresses de file d'attente doivent être converties à l'aide d'Active Directory.</span><span class="sxs-lookup"><span data-stu-id="02174-120">Returns a Boolean value that indicates whether queue addresses should be converted using Active Directory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="02174-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02174-121">Requirements</span></span>  
  
|<span data-ttu-id="02174-122">MOF</span><span class="sxs-lookup"><span data-stu-id="02174-122">MOF</span></span>|<span data-ttu-id="02174-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="02174-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="02174-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="02174-124">Namespace</span></span>|<span data-ttu-id="02174-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="02174-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="02174-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02174-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>
