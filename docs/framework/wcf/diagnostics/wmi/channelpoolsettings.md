---
title: ChannelPoolSettings
ms.date: 03/30/2017
ms.assetid: d3f475bd-f780-4bbe-b291-339387322964
ms.openlocfilehash: 4a3e45140765f99f4a30b77fc9d02b167601b50b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54591475"
---
# <a name="channelpoolsettings"></a><span data-ttu-id="41637-102">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="41637-102">ChannelPoolSettings</span></span>
<span data-ttu-id="41637-103">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="41637-103">ChannelPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41637-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41637-104">Syntax</span></span>  
  
```csharp
class ChannelPoolSettings  
{  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundChannelsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="41637-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="41637-105">Methods</span></span>  
 <span data-ttu-id="41637-106">La classe ChannelPoolSettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="41637-106">The ChannelPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="41637-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="41637-107">Properties</span></span>  
 <span data-ttu-id="41637-108">La classe ChannelPoolSettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="41637-108">The ChannelPoolSettings class has the following properties:</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="41637-109">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="41637-109">IdleTimeout</span></span>  
 <span data-ttu-id="41637-110">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="41637-110">Data type: datetime</span></span>  
  
 <span data-ttu-id="41637-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="41637-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="41637-112">Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.</span><span class="sxs-lookup"><span data-stu-id="41637-112">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="leasetimeout"></a><span data-ttu-id="41637-113">LeaseTimeout</span><span class="sxs-lookup"><span data-stu-id="41637-113">LeaseTimeout</span></span>  
 <span data-ttu-id="41637-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="41637-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="41637-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="41637-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="41637-116">Période maximale d'exécution d'une opération de bail avant expiration du délai d'attente.</span><span class="sxs-lookup"><span data-stu-id="41637-116">The maximum time for a lease operation to complete before timing out.</span></span>  
  
### <a name="maxoutboundchannelsperendpoint"></a><span data-ttu-id="41637-117">MaxOutboundChannelsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="41637-117">MaxOutboundChannelsPerEndpoint</span></span>  
 <span data-ttu-id="41637-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="41637-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="41637-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="41637-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="41637-120">Nombre maximal de canaux sortants pour chaque point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="41637-120">The maximum number of outbound channels for each endpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41637-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="41637-121">Requirements</span></span>  
  
|<span data-ttu-id="41637-122">MOF</span><span class="sxs-lookup"><span data-stu-id="41637-122">MOF</span></span>|<span data-ttu-id="41637-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="41637-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="41637-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="41637-124">Namespace</span></span>|<span data-ttu-id="41637-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="41637-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="41637-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41637-126">See also</span></span>
- <xref:System.ServiceModel.Channels.ChannelPoolSettings>
