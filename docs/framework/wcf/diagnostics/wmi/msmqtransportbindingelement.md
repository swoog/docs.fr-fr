---
title: MsmqTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 1c89f073-9ed3-4025-a8c5-13535a0f526b
ms.openlocfilehash: d37ee4527226d9347e24fc2ee8007a263c71f198
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564875"
---
# <a name="msmqtransportbindingelement"></a><span data-ttu-id="cf741-102">MsmqTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="cf741-102">MsmqTransportBindingElement</span></span>
<span data-ttu-id="cf741-103">MsmqTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="cf741-103">MsmqTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf741-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf741-104">Syntax</span></span>  
  
```csharp
class MsmqTransportBindingElement : MsmqBindingElementBase  
{  
  sint32 MaxPoolSize;  
  string QueueTransferProtocol;  
  boolean UseActiveDirectory;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="cf741-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cf741-105">Methods</span></span>  
 <span data-ttu-id="cf741-106">La classe MsmqTransportBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="cf741-106">The MsmqTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="cf741-107">Properties</span><span class="sxs-lookup"><span data-stu-id="cf741-107">Properties</span></span>  
 <span data-ttu-id="cf741-108">La classe MsmqTransportBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf741-108">The MsmqTransportBindingElement class has the following properties:</span></span>  
  
### <a name="maxpoolsize"></a><span data-ttu-id="cf741-109">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="cf741-109">MaxPoolSize</span></span>  
 <span data-ttu-id="cf741-110">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="cf741-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="cf741-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf741-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="cf741-112">Taille maximale du pool contenant des objets de message MSMQ internes.</span><span class="sxs-lookup"><span data-stu-id="cf741-112">The maximum size of the pool that contains internal MSMQ message objects.</span></span>  
  
### <a name="queuetransferprotocol"></a><span data-ttu-id="cf741-113">QueueTransferProtocol</span><span class="sxs-lookup"><span data-stu-id="cf741-113">QueueTransferProtocol</span></span>  
 <span data-ttu-id="cf741-114">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="cf741-114">Data type: string</span></span>  
  
 <span data-ttu-id="cf741-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf741-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="cf741-116">Valeur d’énumération qui indique le transport de canal de communication mis en file d’attente que cette liaison utilise.</span><span class="sxs-lookup"><span data-stu-id="cf741-116">An enumeration value that indicates the queued communication channel transport that this binding uses.</span></span>  
  
### <a name="useactivedirectory"></a><span data-ttu-id="cf741-117">UseActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="cf741-117">UseActiveDirectory</span></span>  
 <span data-ttu-id="cf741-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="cf741-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="cf741-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="cf741-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="cf741-120">Retourne une valeur Boolean qui indique si les adresses de file d'attente doivent être converties à l'aide d'Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf741-120">Returns a Boolean value that indicates whether queue addresses should be converted using Active Directory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cf741-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cf741-121">Requirements</span></span>  
  
|<span data-ttu-id="cf741-122">MOF</span><span class="sxs-lookup"><span data-stu-id="cf741-122">MOF</span></span>|<span data-ttu-id="cf741-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="cf741-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="cf741-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf741-124">Namespace</span></span>|<span data-ttu-id="cf741-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="cf741-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="cf741-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf741-126">See also</span></span>
- <xref:System.ServiceModel.Channels.MsmqTransportBindingElement>
