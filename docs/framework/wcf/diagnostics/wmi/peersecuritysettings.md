---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
ms.openlocfilehash: 1c33e1ce710fea3b1698a6dab47a199e40388f5a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59217885"
---
# <a name="peersecuritysettings"></a><span data-ttu-id="21bd0-102">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="21bd0-102">PeerSecuritySettings</span></span>
<span data-ttu-id="21bd0-103">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="21bd0-103">PeerSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21bd0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21bd0-104">Syntax</span></span>  
  
```csharp
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="21bd0-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="21bd0-105">Methods</span></span>  
 <span data-ttu-id="21bd0-106">La classe PeerSecuritySettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="21bd0-106">The PeerSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="21bd0-107">Properties</span><span class="sxs-lookup"><span data-stu-id="21bd0-107">Properties</span></span>  
 <span data-ttu-id="21bd0-108">La classe PeerSecuritySettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="21bd0-108">The PeerSecuritySettings class has the following properties:</span></span>  
  
### <a name="mode"></a><span data-ttu-id="21bd0-109">Mode</span><span class="sxs-lookup"><span data-stu-id="21bd0-109">Mode</span></span>  
 <span data-ttu-id="21bd0-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="21bd0-110">Data type: string</span></span>  
  
 <span data-ttu-id="21bd0-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="21bd0-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="21bd0-112">Utilisation ou non d'une sécurité au niveau du message et au niveau du transport par un point de terminaison configuré avec la liaison.</span><span class="sxs-lookup"><span data-stu-id="21bd0-112">Whether message-level and transport-level security are used by an endpoint configured with the binding.</span></span>  
  
### <a name="transport"></a><span data-ttu-id="21bd0-113">Transport</span><span class="sxs-lookup"><span data-stu-id="21bd0-113">Transport</span></span>  
 <span data-ttu-id="21bd0-114">Type de données : PeerTransportSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="21bd0-114">Data type: PeerTransportSecuritySettings</span></span>  
  
 <span data-ttu-id="21bd0-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="21bd0-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="21bd0-116">Paramètres de sécurité du transport.</span><span class="sxs-lookup"><span data-stu-id="21bd0-116">Transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="21bd0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21bd0-117">Requirements</span></span>  
  
|<span data-ttu-id="21bd0-118">MOF</span><span class="sxs-lookup"><span data-stu-id="21bd0-118">MOF</span></span>|<span data-ttu-id="21bd0-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="21bd0-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="21bd0-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="21bd0-120">Namespace</span></span>|<span data-ttu-id="21bd0-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="21bd0-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="21bd0-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21bd0-122">See also</span></span>

- <xref:System.ServiceModel.PeerSecuritySettings>
