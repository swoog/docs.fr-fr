---
title: Channel, classe
ms.date: 03/30/2017
ms.assetid: d9fae2ca-209c-4341-a0f5-6b79d1a67776
ms.openlocfilehash: f60a3946617b0994db1ba9e9ddf43be863be81f9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61964079"
---
# <a name="channel-class"></a><span data-ttu-id="b2baf-102">Channel, classe</span><span class="sxs-lookup"><span data-stu-id="b2baf-102">Channel class</span></span>
<span data-ttu-id="b2baf-103">Canal</span><span class="sxs-lookup"><span data-stu-id="b2baf-103">Channel</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b2baf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2baf-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="b2baf-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b2baf-105">Methods</span></span>  
 <span data-ttu-id="b2baf-106">La classe Channel ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="b2baf-106">The Channel class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b2baf-107">Properties</span><span class="sxs-lookup"><span data-stu-id="b2baf-107">Properties</span></span>  
 <span data-ttu-id="b2baf-108">La classe Channel possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b2baf-108">The Channel class has the following properties.</span></span>  
  
### <a name="localaddress"></a><span data-ttu-id="b2baf-109">LocalAddress</span><span class="sxs-lookup"><span data-stu-id="b2baf-109">LocalAddress</span></span>  
 <span data-ttu-id="b2baf-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="b2baf-110">Data type: string</span></span>  
  
 <span data-ttu-id="b2baf-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2baf-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b2baf-112">Point de terminaison local du canal.</span><span class="sxs-lookup"><span data-stu-id="b2baf-112">The local endpoint for the channel.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="b2baf-113">ref</span><span class="sxs-lookup"><span data-stu-id="b2baf-113">ref</span></span>  
 <span data-ttu-id="b2baf-114">Type de données : Point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b2baf-114">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="b2baf-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2baf-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b2baf-116">Référence au point de terminaison auquel le canal se connecte.</span><span class="sxs-lookup"><span data-stu-id="b2baf-116">A reference to the endpoint the channel connects to.</span></span>  
  
### <a name="remoteaddress"></a><span data-ttu-id="b2baf-117">RemoteAddress</span><span class="sxs-lookup"><span data-stu-id="b2baf-117">RemoteAddress</span></span>  
 <span data-ttu-id="b2baf-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="b2baf-118">Data type: string</span></span>  
  
 <span data-ttu-id="b2baf-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2baf-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b2baf-120">Adresse distante associée au canal.</span><span class="sxs-lookup"><span data-stu-id="b2baf-120">The remote address associated with the channel.</span></span>  
  
### <a name="sessionid"></a><span data-ttu-id="b2baf-121">SessionId</span><span class="sxs-lookup"><span data-stu-id="b2baf-121">SessionId</span></span>  
 <span data-ttu-id="b2baf-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="b2baf-122">Data type: string</span></span>  
  
 <span data-ttu-id="b2baf-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2baf-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b2baf-124">Id de session actuel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b2baf-124">The current session Id, if any.</span></span>  
  
### <a name="type"></a><span data-ttu-id="b2baf-125">Type</span><span class="sxs-lookup"><span data-stu-id="b2baf-125">Type</span></span>  
 <span data-ttu-id="b2baf-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="b2baf-126">Data type: string</span></span>  
  
 <span data-ttu-id="b2baf-127">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2baf-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="b2baf-128">Type du canal.</span><span class="sxs-lookup"><span data-stu-id="b2baf-128">The type of the channel.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b2baf-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2baf-129">Requirements</span></span>  
  
|<span data-ttu-id="b2baf-130">MOF</span><span class="sxs-lookup"><span data-stu-id="b2baf-130">MOF</span></span>|<span data-ttu-id="b2baf-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="b2baf-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b2baf-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2baf-132">Namespace</span></span>|<span data-ttu-id="b2baf-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="b2baf-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b2baf-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2baf-134">See also</span></span>

- <xref:System.ServiceModel.Channels.ChannelBase>
