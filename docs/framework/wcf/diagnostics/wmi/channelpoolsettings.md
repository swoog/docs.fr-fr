---
title: ChannelPoolSettings
ms.date: 03/30/2017
ms.assetid: d3f475bd-f780-4bbe-b291-339387322964
ms.openlocfilehash: 8900af77d0d385bb68b4b85e1d15be57bb7a8d14
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59972860"
---
# <a name="channelpoolsettings"></a><span data-ttu-id="1ea5a-102">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="1ea5a-102">ChannelPoolSettings</span></span>
<span data-ttu-id="1ea5a-103">ChannelPoolSettings</span><span class="sxs-lookup"><span data-stu-id="1ea5a-103">ChannelPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ea5a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ea5a-104">Syntax</span></span>  
  
```csharp
class ChannelPoolSettings  
{  
  datetime IdleTimeout;  
  datetime LeaseTimeout;  
  sint32 MaxOutboundChannelsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="1ea5a-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1ea5a-105">Methods</span></span>  
 <span data-ttu-id="1ea5a-106">La classe ChannelPoolSettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="1ea5a-106">The ChannelPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="1ea5a-107">Properties</span><span class="sxs-lookup"><span data-stu-id="1ea5a-107">Properties</span></span>  
 <span data-ttu-id="1ea5a-108">La classe ChannelPoolSettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="1ea5a-108">The ChannelPoolSettings class has the following properties:</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="1ea5a-109">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="1ea5a-109">IdleTimeout</span></span>  
 <span data-ttu-id="1ea5a-110">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="1ea5a-110">Data type: datetime</span></span>  
  
 <span data-ttu-id="1ea5a-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea5a-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1ea5a-112">Période maximale d'inactivité de la connexion au terme de laquelle la connexion est coupée.</span><span class="sxs-lookup"><span data-stu-id="1ea5a-112">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="leasetimeout"></a><span data-ttu-id="1ea5a-113">LeaseTimeout</span><span class="sxs-lookup"><span data-stu-id="1ea5a-113">LeaseTimeout</span></span>  
 <span data-ttu-id="1ea5a-114">Type de données : datetime</span><span class="sxs-lookup"><span data-stu-id="1ea5a-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="1ea5a-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea5a-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1ea5a-116">Période maximale d'exécution d'une opération de bail avant expiration du délai d'attente.</span><span class="sxs-lookup"><span data-stu-id="1ea5a-116">The maximum time for a lease operation to complete before timing out.</span></span>  
  
### <a name="maxoutboundchannelsperendpoint"></a><span data-ttu-id="1ea5a-117">MaxOutboundChannelsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ea5a-117">MaxOutboundChannelsPerEndpoint</span></span>  
 <span data-ttu-id="1ea5a-118">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="1ea5a-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="1ea5a-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ea5a-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="1ea5a-120">Nombre maximal de canaux sortants pour chaque point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1ea5a-120">The maximum number of outbound channels for each endpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ea5a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ea5a-121">Requirements</span></span>  
  
|<span data-ttu-id="1ea5a-122">MOF</span><span class="sxs-lookup"><span data-stu-id="1ea5a-122">MOF</span></span>|<span data-ttu-id="1ea5a-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="1ea5a-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="1ea5a-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1ea5a-124">Namespace</span></span>|<span data-ttu-id="1ea5a-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="1ea5a-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1ea5a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ea5a-126">See also</span></span>

- <xref:System.ServiceModel.Channels.ChannelPoolSettings>
