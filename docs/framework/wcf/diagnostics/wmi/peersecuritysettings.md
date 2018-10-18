---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
author: BrucePerlerMS
ms.openlocfilehash: 18caaf2750fa3a263c09176e975204258330752c
ms.sourcegitcommit: e42d09e5966dd9fd02847d3e7eeb4ec0877069f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "49371626"
---
# <a name="peersecuritysettings"></a><span data-ttu-id="94144-102">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="94144-102">PeerSecuritySettings</span></span>
<span data-ttu-id="94144-103">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="94144-103">PeerSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94144-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94144-104">Syntax</span></span>  
  
```csharp
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="94144-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="94144-105">Methods</span></span>  
 <span data-ttu-id="94144-106">La classe PeerSecuritySettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="94144-106">The PeerSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="94144-107">Properties</span><span class="sxs-lookup"><span data-stu-id="94144-107">Properties</span></span>  
 <span data-ttu-id="94144-108">La classe PeerSecuritySettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="94144-108">The PeerSecuritySettings class has the following properties:</span></span>  
  
### <a name="mode"></a><span data-ttu-id="94144-109">Mode</span><span class="sxs-lookup"><span data-stu-id="94144-109">Mode</span></span>  
 <span data-ttu-id="94144-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="94144-110">Data type: string</span></span>  
  
 <span data-ttu-id="94144-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="94144-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="94144-112">Utilisation ou non d’une sécurité au niveau du message et au niveau du transport par un point de terminaison configuré avec la liaison.</span><span class="sxs-lookup"><span data-stu-id="94144-112">Whether message-level and transport-level security are used by an endpoint configured with the binding.</span></span>  
  
### <a name="transport"></a><span data-ttu-id="94144-113">Transport</span><span class="sxs-lookup"><span data-stu-id="94144-113">Transport</span></span>  
 <span data-ttu-id="94144-114">Type de données : PeerTransportSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="94144-114">Data type: PeerTransportSecuritySettings</span></span>  
  
 <span data-ttu-id="94144-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="94144-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="94144-116">Paramètres de sécurité du transport.</span><span class="sxs-lookup"><span data-stu-id="94144-116">Transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94144-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94144-117">Requirements</span></span>  
  
|<span data-ttu-id="94144-118">MOF</span><span class="sxs-lookup"><span data-stu-id="94144-118">MOF</span></span>|<span data-ttu-id="94144-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="94144-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="94144-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="94144-120">Namespace</span></span>|<span data-ttu-id="94144-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="94144-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="94144-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94144-122">See Also</span></span>  
 <xref:System.ServiceModel.PeerSecuritySettings>
