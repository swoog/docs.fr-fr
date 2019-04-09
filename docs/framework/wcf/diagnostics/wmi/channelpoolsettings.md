---
title: ChannelPoolSettings
ms.date: 03/30/2017
ms.assetid: d3f475bd-f780-4bbe-b291-339387322964
ms.openlocfilehash: 8900af77d0d385bb68b4b85e1d15be57bb7a8d14
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59131909"
---
# <a name="channelpoolsettings"></a><span data-ttu-id="800bf-102">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="800bf-102">ChannelPoolSettings</span></span>
<span data-ttu-id="800bf-103">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="800bf-103">ChannelPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="800bf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="800bf-104">Syntax</span></span>  
  
```csharp
class ChannelPoolSettings  
{  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundChannelsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="800bf-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="800bf-105">Methods</span></span>  
 <span data-ttu-id="800bf-106">La classe ChannelPoolSettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="800bf-106">The ChannelPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="800bf-107">Properties</span><span class="sxs-lookup"><span data-stu-id="800bf-107">Properties</span></span>  
 <span data-ttu-id="800bf-108">La classe ChannelPoolSettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="800bf-108">The ChannelPoolSettings class has the following properties:</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="800bf-109">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="800bf-109">IdleTimeout</span></span>  
 <span data-ttu-id="800bf-110">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="800bf-110">Data type: datetime</span></span>  
  
 <span data-ttu-id="800bf-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="800bf-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="800bf-112">Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.</span><span class="sxs-lookup"><span data-stu-id="800bf-112">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="leasetimeout"></a><span data-ttu-id="800bf-113">LeaseTimeout</span><span class="sxs-lookup"><span data-stu-id="800bf-113">LeaseTimeout</span></span>  
 <span data-ttu-id="800bf-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="800bf-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="800bf-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="800bf-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="800bf-116">Période maximale d'exécution d'une opération de bail avant expiration du délai d'attente.</span><span class="sxs-lookup"><span data-stu-id="800bf-116">The maximum time for a lease operation to complete before timing out.</span></span>  
  
### <a name="maxoutboundchannelsperendpoint"></a><span data-ttu-id="800bf-117">MaxOutboundChannelsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="800bf-117">MaxOutboundChannelsPerEndpoint</span></span>  
 <span data-ttu-id="800bf-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="800bf-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="800bf-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="800bf-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="800bf-120">Nombre maximal de canaux sortants pour chaque point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="800bf-120">The maximum number of outbound channels for each endpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="800bf-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="800bf-121">Requirements</span></span>  
  
|<span data-ttu-id="800bf-122">MOF</span><span class="sxs-lookup"><span data-stu-id="800bf-122">MOF</span></span>|<span data-ttu-id="800bf-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="800bf-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="800bf-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="800bf-124">Namespace</span></span>|<span data-ttu-id="800bf-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="800bf-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="800bf-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="800bf-126">See also</span></span>

- <xref:System.ServiceModel.Channels.ChannelPoolSettings>
