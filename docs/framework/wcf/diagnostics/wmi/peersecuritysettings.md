---
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 58b372f26fee7dc180d75731fd4855db569c87c7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33484518"
---
# <a name="peersecuritysettings"></a><span data-ttu-id="f8654-102">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="f8654-102">PeerSecuritySettings</span></span>
<span data-ttu-id="f8654-103">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="f8654-103">PeerSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8654-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8654-104">Syntax</span></span>  
  
```  
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f8654-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f8654-105">Methods</span></span>  
 <span data-ttu-id="f8654-106">La classe PeerSecuritySettings ne définit pas de méthode.</span><span class="sxs-lookup"><span data-stu-id="f8654-106">The PeerSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f8654-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f8654-107">Properties</span></span>  
 <span data-ttu-id="f8654-108">La classe PeerSecuritySettings a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8654-108">The PeerSecuritySettings class has the following properties:</span></span>  
  
### <a name="mode"></a><span data-ttu-id="f8654-109">Mode</span><span class="sxs-lookup"><span data-stu-id="f8654-109">Mode</span></span>  
 <span data-ttu-id="f8654-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f8654-110">Data type: string</span></span>  
  
 <span data-ttu-id="f8654-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8654-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f8654-112">Utilisation ou non d’une sécurité au niveau du message et au niveau du transport par un point de terminaison configuré avec la liaison.</span><span class="sxs-lookup"><span data-stu-id="f8654-112">Whether message-level and transport-level security are used by an endpoint configured with the binding.</span></span>  
  
### <a name="transport"></a><span data-ttu-id="f8654-113">Transport</span><span class="sxs-lookup"><span data-stu-id="f8654-113">Transport</span></span>  
 <span data-ttu-id="f8654-114">Type de données : PeerTransportSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="f8654-114">Data type: PeerTransportSecuritySettings</span></span>  
  
 <span data-ttu-id="f8654-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="f8654-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f8654-116">Paramètres de sécurité du transport.</span><span class="sxs-lookup"><span data-stu-id="f8654-116">Transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8654-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8654-117">Requirements</span></span>  
  
|<span data-ttu-id="f8654-118">MOF</span><span class="sxs-lookup"><span data-stu-id="f8654-118">MOF</span></span>|<span data-ttu-id="f8654-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="f8654-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f8654-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f8654-120">Namespace</span></span>|<span data-ttu-id="f8654-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f8654-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f8654-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8654-122">See Also</span></span>  
 <xref:System.ServiceModel.PeerSecuritySettings>
