---
title: OneWayBindingElement
ms.date: 03/30/2017
ms.assetid: 5c7e17c3-39b9-4214-ae08-9e6141734305
ms.openlocfilehash: 34220a3651819978f5f597fdc67d54630ec5e059
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195812"
---
# <a name="onewaybindingelement"></a><span data-ttu-id="621dc-102">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="621dc-102">OneWayBindingElement</span></span>
<span data-ttu-id="621dc-103">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="621dc-103">OneWayBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="621dc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="621dc-104">Syntax</span></span>  
  
```csharp
class OneWayBindingElement : BindingElement  
{  
  ChannelPoolSettings ChannelPoolSettings;  
  sint32 MaxAcceptedChannels;  
  boolean PacketRoutable;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="621dc-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="621dc-105">Methods</span></span>  
 <span data-ttu-id="621dc-106">La classe OneWayBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="621dc-106">The OneWayBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="621dc-107">Properties</span><span class="sxs-lookup"><span data-stu-id="621dc-107">Properties</span></span>  
 <span data-ttu-id="621dc-108">La classe OneWayBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="621dc-108">The OneWayBindingElement class has the following properties:</span></span>  
  
### <a name="channelpoolsettings"></a><span data-ttu-id="621dc-109">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="621dc-109">ChannelPoolSettings</span></span>  
 <span data-ttu-id="621dc-110">Type de données : ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="621dc-110">Data type: ChannelPoolSettings</span></span>  
  
 <span data-ttu-id="621dc-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="621dc-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="621dc-112">Paramètres du pool de canaux.</span><span class="sxs-lookup"><span data-stu-id="621dc-112">The channel pool settings.</span></span>  
  
### <a name="maxacceptedchannels"></a><span data-ttu-id="621dc-113">MaxAcceptedChannels</span><span class="sxs-lookup"><span data-stu-id="621dc-113">MaxAcceptedChannels</span></span>  
 <span data-ttu-id="621dc-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="621dc-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="621dc-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="621dc-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="621dc-116">Nombre maximal de canaux acceptés.</span><span class="sxs-lookup"><span data-stu-id="621dc-116">The maximum number of accepted channels.</span></span>  
  
### <a name="packetroutable"></a><span data-ttu-id="621dc-117">PacketRoutable</span><span class="sxs-lookup"><span data-stu-id="621dc-117">PacketRoutable</span></span>  
 <span data-ttu-id="621dc-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="621dc-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="621dc-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="621dc-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="621dc-120">Valeur qui indique si le paquet peut être routé.</span><span class="sxs-lookup"><span data-stu-id="621dc-120">A value that indicates whether the packet is routable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="621dc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="621dc-121">Requirements</span></span>  
  
|<span data-ttu-id="621dc-122">MOF</span><span class="sxs-lookup"><span data-stu-id="621dc-122">MOF</span></span>|<span data-ttu-id="621dc-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="621dc-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="621dc-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="621dc-124">Namespace</span></span>|<span data-ttu-id="621dc-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="621dc-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="621dc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="621dc-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.OneWayBindingElement>
