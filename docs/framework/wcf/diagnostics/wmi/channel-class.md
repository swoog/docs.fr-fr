---
title: Channel, classe
ms.date: 03/30/2017
ms.assetid: d9fae2ca-209c-4341-a0f5-6b79d1a67776
ms.openlocfilehash: f60a3946617b0994db1ba9e9ddf43be863be81f9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59128841"
---
# <a name="channel-class"></a><span data-ttu-id="c8f48-102">Channel, classe</span><span class="sxs-lookup"><span data-stu-id="c8f48-102">Channel class</span></span>
<span data-ttu-id="c8f48-103">Canal</span><span class="sxs-lookup"><span data-stu-id="c8f48-103">Channel</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8f48-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8f48-104">Syntax</span></span>  
  
```csharp
class Channel  
{  
  string LocalAddress;  
  Endpoint ref;  
  string RemoteAddress;  
  string SessionId;  
  string Type;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c8f48-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c8f48-105">Methods</span></span>  
 <span data-ttu-id="c8f48-106">La classe Channel ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="c8f48-106">The Channel class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c8f48-107">Properties</span><span class="sxs-lookup"><span data-stu-id="c8f48-107">Properties</span></span>  
 <span data-ttu-id="c8f48-108">La classe Channel possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8f48-108">The Channel class has the following properties.</span></span>  
  
### <a name="localaddress"></a><span data-ttu-id="c8f48-109">LocalAddress</span><span class="sxs-lookup"><span data-stu-id="c8f48-109">LocalAddress</span></span>  
 <span data-ttu-id="c8f48-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c8f48-110">Data type: string</span></span>  
  
 <span data-ttu-id="c8f48-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8f48-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8f48-112">Point de terminaison local du canal.</span><span class="sxs-lookup"><span data-stu-id="c8f48-112">The local endpoint for the channel.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="c8f48-113">ref</span><span class="sxs-lookup"><span data-stu-id="c8f48-113">ref</span></span>  
 <span data-ttu-id="c8f48-114">Type de données : Point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c8f48-114">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="c8f48-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8f48-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8f48-116">Référence au point de terminaison auquel le canal se connecte.</span><span class="sxs-lookup"><span data-stu-id="c8f48-116">A reference to the endpoint the channel connects to.</span></span>  
  
### <a name="remoteaddress"></a><span data-ttu-id="c8f48-117">RemoteAddress</span><span class="sxs-lookup"><span data-stu-id="c8f48-117">RemoteAddress</span></span>  
 <span data-ttu-id="c8f48-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c8f48-118">Data type: string</span></span>  
  
 <span data-ttu-id="c8f48-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8f48-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8f48-120">Adresse distante associée au canal.</span><span class="sxs-lookup"><span data-stu-id="c8f48-120">The remote address associated with the channel.</span></span>  
  
### <a name="sessionid"></a><span data-ttu-id="c8f48-121">SessionId</span><span class="sxs-lookup"><span data-stu-id="c8f48-121">SessionId</span></span>  
 <span data-ttu-id="c8f48-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c8f48-122">Data type: string</span></span>  
  
 <span data-ttu-id="c8f48-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8f48-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8f48-124">Id de session actuel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="c8f48-124">The current session Id, if any.</span></span>  
  
### <a name="type"></a><span data-ttu-id="c8f48-125">Type</span><span class="sxs-lookup"><span data-stu-id="c8f48-125">Type</span></span>  
 <span data-ttu-id="c8f48-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c8f48-126">Data type: string</span></span>  
  
 <span data-ttu-id="c8f48-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8f48-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c8f48-128">Type du canal.</span><span class="sxs-lookup"><span data-stu-id="c8f48-128">The type of the channel.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c8f48-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8f48-129">Requirements</span></span>  
  
|<span data-ttu-id="c8f48-130">MOF</span><span class="sxs-lookup"><span data-stu-id="c8f48-130">MOF</span></span>|<span data-ttu-id="c8f48-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="c8f48-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c8f48-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8f48-132">Namespace</span></span>|<span data-ttu-id="c8f48-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c8f48-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c8f48-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8f48-134">See also</span></span>

- <xref:System.ServiceModel.Channels.ChannelBase>
