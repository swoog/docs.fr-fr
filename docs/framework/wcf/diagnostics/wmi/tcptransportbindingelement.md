---
title: TcpTransportBindingElement
ms.date: 03/30/2017
ms.assetid: 33bbc1e5-44e4-4ee3-b7b5-801dc78956e4
ms.openlocfilehash: 0d5dc5c9b9bf2313d18c9fadb1a2adb87c1b11b1
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54610784"
---
# <a name="tcptransportbindingelement"></a><span data-ttu-id="3bbce-102">TcpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="3bbce-102">TcpTransportBindingElement</span></span>
<span data-ttu-id="3bbce-103">TcpTransportBindingElement</span><span class="sxs-lookup"><span data-stu-id="3bbce-103">TcpTransportBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3bbce-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bbce-104">Syntax</span></span>  
  
```csharp
class TcpTransportBindingElement : ConnectionOrientedTransportBindingElement  
{  
  TcpConnectionPoolSettings ConnectionPoolSettings;  
  sint32 ListenBacklog;  
  boolean PortSharingEnabled;  
  boolean TeredoEnabled;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3bbce-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3bbce-105">Methods</span></span>  
 <span data-ttu-id="3bbce-106">La classe TcpTransportBindingElement ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="3bbce-106">The TcpTransportBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3bbce-107">Properties</span><span class="sxs-lookup"><span data-stu-id="3bbce-107">Properties</span></span>  
 <span data-ttu-id="3bbce-108">La classe TcpTransportBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3bbce-108">The TcpTransportBindingElement class has the following properties:</span></span>  
  
### <a name="connectionpoolsettings"></a><span data-ttu-id="3bbce-109">ConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="3bbce-109">ConnectionPoolSettings</span></span>  
 <span data-ttu-id="3bbce-110">Type de données : TcpConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="3bbce-110">Data type: TcpConnectionPoolSettings</span></span>  
  
 <span data-ttu-id="3bbce-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3bbce-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3bbce-112">Paramètres de pool de connexions.</span><span class="sxs-lookup"><span data-stu-id="3bbce-112">The connection pool settings.</span></span>  
  
### <a name="listenbacklog"></a><span data-ttu-id="3bbce-113">ListenBacklog</span><span class="sxs-lookup"><span data-stu-id="3bbce-113">ListenBacklog</span></span>  
 <span data-ttu-id="3bbce-114">Type de données : sint32</span><span class="sxs-lookup"><span data-stu-id="3bbce-114">Data type: sint32</span></span>  
  
 <span data-ttu-id="3bbce-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3bbce-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3bbce-116">Nombre maximal de demandes de connexion en file d'attente pouvant être en attente.</span><span class="sxs-lookup"><span data-stu-id="3bbce-116">The maximum number of queued connection requests that can be pending.</span></span>  
  
### <a name="portsharingenabled"></a><span data-ttu-id="3bbce-117">PortSharingEnabled</span><span class="sxs-lookup"><span data-stu-id="3bbce-117">PortSharingEnabled</span></span>  
 <span data-ttu-id="3bbce-118">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3bbce-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="3bbce-119">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3bbce-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3bbce-120">Valeur booléenne qui spécifie si le partage de port TCP est activé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="3bbce-120">A boolean value that specifies whether TCP port sharing is enabled for this connection.</span></span>  
  
### <a name="teredoenabled"></a><span data-ttu-id="3bbce-121">TeredoEnabled</span><span class="sxs-lookup"><span data-stu-id="3bbce-121">TeredoEnabled</span></span>  
 <span data-ttu-id="3bbce-122">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="3bbce-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="3bbce-123">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="3bbce-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3bbce-124">Valeur booléenne qui spécifie si Teredo (technologie d'adressage de clients placés derrière des pare-feu) est activé.</span><span class="sxs-lookup"><span data-stu-id="3bbce-124">A boolean value that specifies whether Teredo (a technology for addressing clients that are behind firewalls) is enabled.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3bbce-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3bbce-125">Requirements</span></span>  
  
|<span data-ttu-id="3bbce-126">MOF</span><span class="sxs-lookup"><span data-stu-id="3bbce-126">MOF</span></span>|<span data-ttu-id="3bbce-127">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="3bbce-127">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3bbce-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3bbce-128">Namespace</span></span>|<span data-ttu-id="3bbce-129">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="3bbce-129">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3bbce-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bbce-130">See also</span></span>
- <xref:System.ServiceModel.Channels.TcpTransportBindingElement>
