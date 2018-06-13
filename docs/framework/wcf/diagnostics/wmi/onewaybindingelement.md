---
title: OneWayBindingElement
ms.date: 03/30/2017
ms.assetid: 5c7e17c3-39b9-4214-ae08-9e6141734305
ms.openlocfilehash: ee7cfed20234175ba54dd25dbbbab4615c1ed7af
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485741"
---
# <a name="onewaybindingelement"></a><span data-ttu-id="68bc5-102">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="68bc5-102">OneWayBindingElement</span></span>
<span data-ttu-id="68bc5-103">OneWayBindingElement</span><span class="sxs-lookup"><span data-stu-id="68bc5-103">OneWayBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68bc5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68bc5-104">Syntax</span></span>  
  
```  
class OneWayBindingElement : BindingElement  
{  
  ChannelPoolSettings ChannelPoolSettings;  
  sint32 MaxAcceptedChannels;  
  boolean PacketRoutable;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="68bc5-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="68bc5-105">Methods</span></span>  
 <span data-ttu-id="68bc5-106">La classe OneWayBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="68bc5-106">The OneWayBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="68bc5-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="68bc5-107">Properties</span></span>  
 <span data-ttu-id="68bc5-108">La classe OneWayBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="68bc5-108">The OneWayBindingElement class has the following properties:</span></span>  
  
### <a name="channelpoolsettings"></a><span data-ttu-id="68bc5-109">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="68bc5-109">ChannelPoolSettings</span></span>  
 <span data-ttu-id="68bc5-110">Type de données : ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="68bc5-110">Data type: ChannelPoolSettings</span></span>  
  
 <span data-ttu-id="68bc5-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="68bc5-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="68bc5-112">Paramètres du pool de canaux.</span><span class="sxs-lookup"><span data-stu-id="68bc5-112">The channel pool settings.</span></span>  
  
### <a name="maxacceptedchannels"></a><span data-ttu-id="68bc5-113">MaxAcceptedChannels</span><span class="sxs-lookup"><span data-stu-id="68bc5-113">MaxAcceptedChannels</span></span>  
 <span data-ttu-id="68bc5-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="68bc5-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="68bc5-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="68bc5-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="68bc5-116">Nombre maximal de canaux acceptés.</span><span class="sxs-lookup"><span data-stu-id="68bc5-116">The maximum number of accepted channels.</span></span>  
  
### <a name="packetroutable"></a><span data-ttu-id="68bc5-117">PacketRoutable</span><span class="sxs-lookup"><span data-stu-id="68bc5-117">PacketRoutable</span></span>  
 <span data-ttu-id="68bc5-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="68bc5-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="68bc5-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="68bc5-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="68bc5-120">Valeur qui indique si le paquet peut être routé.</span><span class="sxs-lookup"><span data-stu-id="68bc5-120">A value that indicates whether the packet is routable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="68bc5-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="68bc5-121">Requirements</span></span>  
  
|<span data-ttu-id="68bc5-122">MOF</span><span class="sxs-lookup"><span data-stu-id="68bc5-122">MOF</span></span>|<span data-ttu-id="68bc5-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="68bc5-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="68bc5-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68bc5-124">Namespace</span></span>|<span data-ttu-id="68bc5-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="68bc5-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="68bc5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68bc5-126">See Also</span></span>  
 <xref:System.ServiceModel.Channels.OneWayBindingElement>
