---
title: PeerTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 40bf6be2-8087-4cb3-a66c-408d53eb9269
ms.openlocfilehash: 437ccc0446e3cc05596ab12b7908177b7f78e431
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54670652"
---
# <a name="peertransportbindingelement"></a><span data-ttu-id="c5cbb-102">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="c5cbb-102">PeerTransportBindingElement</span></span>
<span data-ttu-id="c5cbb-103">PeerTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="c5cbb-103">PeerTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c5cbb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5cbb-104">Syntax</span></span>  
  
```csharp
class PeerTransportBindingElement : TransportBindingElement  
{  
  string ListenIPAddress;  
  sint32 Port;  
  PeerSecuritySettings Security;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c5cbb-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c5cbb-105">Methods</span></span>  
 <span data-ttu-id="c5cbb-106">La classe PeerTransportBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="c5cbb-106">The PeerTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="c5cbb-107">Properties</span><span class="sxs-lookup"><span data-stu-id="c5cbb-107">Properties</span></span>  
 <span data-ttu-id="c5cbb-108">La classe PeerTransportBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="c5cbb-108">The PeerTransportBindingElement class has the following properties:</span></span>  
  
### <a name="listenipaddress"></a><span data-ttu-id="c5cbb-109">ListenIPAddress</span><span class="sxs-lookup"><span data-stu-id="c5cbb-109">ListenIPAddress</span></span>  
 <span data-ttu-id="c5cbb-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="c5cbb-110">Data type: string</span></span>  
  
 <span data-ttu-id="c5cbb-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5cbb-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c5cbb-112">Adresse IP sur laquelle le nœud homologue écoute les messages.</span><span class="sxs-lookup"><span data-stu-id="c5cbb-112">The IP address on which the peer node listens for messages.</span></span>  
  
### <a name="port"></a><span data-ttu-id="c5cbb-113">Port</span><span class="sxs-lookup"><span data-stu-id="c5cbb-113">Port</span></span>  
 <span data-ttu-id="c5cbb-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="c5cbb-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="c5cbb-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5cbb-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c5cbb-116">Port d’interface de réseau sur lequel la liaison traite les messages de canaux homologues.</span><span class="sxs-lookup"><span data-stu-id="c5cbb-116">The network interface port on which this binding processes peer channel messages.</span></span>  
  
### <a name="security"></a><span data-ttu-id="c5cbb-117">Sécurité</span><span class="sxs-lookup"><span data-stu-id="c5cbb-117">Security</span></span>  
 <span data-ttu-id="c5cbb-118">Type de données : PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="c5cbb-118">Data type: PeerSecuritySettings</span></span>  
  
 <span data-ttu-id="c5cbb-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c5cbb-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="c5cbb-120">Paramètres de sécurité de transport de l'homologue.</span><span class="sxs-lookup"><span data-stu-id="c5cbb-120">Peer transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c5cbb-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c5cbb-121">Requirements</span></span>  
  
|<span data-ttu-id="c5cbb-122">MOF</span><span class="sxs-lookup"><span data-stu-id="c5cbb-122">MOF</span></span>|<span data-ttu-id="c5cbb-123">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="c5cbb-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="c5cbb-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c5cbb-124">Namespace</span></span>|<span data-ttu-id="c5cbb-125">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c5cbb-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="c5cbb-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5cbb-126">See also</span></span>
- <xref:System.ServiceModel.Channels.PeerTransportBindingElement>
