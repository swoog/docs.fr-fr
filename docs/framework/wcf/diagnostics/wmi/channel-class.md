---
title: Channel, classe
ms.date: 03/30/2017
ms.assetid: d9fae2ca-209c-4341-a0f5-6b79d1a67776
ms.openlocfilehash: 108d5f8e3cd092863dbd48e2bb9d180798b091a4
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50047369"
---
# <a name="channel-class"></a><span data-ttu-id="5e56c-102">Channel, classe</span><span class="sxs-lookup"><span data-stu-id="5e56c-102">Channel class</span></span>
<span data-ttu-id="5e56c-103">Canal</span><span class="sxs-lookup"><span data-stu-id="5e56c-103">Channel</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e56c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e56c-104">Syntax</span></span>  
  
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
  
## <a name="methods"></a><span data-ttu-id="5e56c-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5e56c-105">Methods</span></span>  
 <span data-ttu-id="5e56c-106">La classe Channel ne définit aucune méthode.</span><span class="sxs-lookup"><span data-stu-id="5e56c-106">The Channel class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="5e56c-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5e56c-107">Properties</span></span>  
 <span data-ttu-id="5e56c-108">La classe Channel possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e56c-108">The Channel class has the following properties.</span></span>  
  
### <a name="localaddress"></a><span data-ttu-id="5e56c-109">LocalAddress</span><span class="sxs-lookup"><span data-stu-id="5e56c-109">LocalAddress</span></span>  
 <span data-ttu-id="5e56c-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5e56c-110">Data type: string</span></span>  
  
 <span data-ttu-id="5e56c-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e56c-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5e56c-112">Point de terminaison local du canal.</span><span class="sxs-lookup"><span data-stu-id="5e56c-112">The local endpoint for the channel.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="5e56c-113">ref</span><span class="sxs-lookup"><span data-stu-id="5e56c-113">ref</span></span>  
 <span data-ttu-id="5e56c-114">Type de données : point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5e56c-114">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="5e56c-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e56c-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5e56c-116">Référence au point de terminaison auquel le canal se connecte.</span><span class="sxs-lookup"><span data-stu-id="5e56c-116">A reference to the endpoint the channel connects to.</span></span>  
  
### <a name="remoteaddress"></a><span data-ttu-id="5e56c-117">RemoteAddress</span><span class="sxs-lookup"><span data-stu-id="5e56c-117">RemoteAddress</span></span>  
 <span data-ttu-id="5e56c-118">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5e56c-118">Data type: string</span></span>  
  
 <span data-ttu-id="5e56c-119">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e56c-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5e56c-120">Adresse distante associée au canal.</span><span class="sxs-lookup"><span data-stu-id="5e56c-120">The remote address associated with the channel.</span></span>  
  
### <a name="sessionid"></a><span data-ttu-id="5e56c-121">SessionId</span><span class="sxs-lookup"><span data-stu-id="5e56c-121">SessionId</span></span>  
 <span data-ttu-id="5e56c-122">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5e56c-122">Data type: string</span></span>  
  
 <span data-ttu-id="5e56c-123">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e56c-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5e56c-124">Id de session actuel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="5e56c-124">The current session Id, if any.</span></span>  
  
### <a name="type"></a><span data-ttu-id="5e56c-125">Type</span><span class="sxs-lookup"><span data-stu-id="5e56c-125">Type</span></span>  
 <span data-ttu-id="5e56c-126">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="5e56c-126">Data type: string</span></span>  
  
 <span data-ttu-id="5e56c-127">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="5e56c-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="5e56c-128">Type du canal.</span><span class="sxs-lookup"><span data-stu-id="5e56c-128">The type of the channel.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5e56c-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5e56c-129">Requirements</span></span>  
  
|<span data-ttu-id="5e56c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5e56c-130">MOF</span></span>|<span data-ttu-id="5e56c-131">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="5e56c-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="5e56c-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5e56c-132">Namespace</span></span>|<span data-ttu-id="5e56c-133">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="5e56c-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="5e56c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e56c-134">See Also</span></span>  
 <xref:System.ServiceModel.Channels.ChannelBase>
