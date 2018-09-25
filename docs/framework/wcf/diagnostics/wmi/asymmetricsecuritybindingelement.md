---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
author: BrucePerlerMS
ms.openlocfilehash: 63af1c9a607cb9f81e2c0abf795ee2b3432cbf9c
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47075055"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="4ab8b-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="4ab8b-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="4ab8b-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="4ab8b-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ab8b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ab8b-104">Syntax</span></span>  
  
```  
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="4ab8b-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4ab8b-105">Methods</span></span>  
 <span data-ttu-id="4ab8b-106">La classe AsymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="4ab8b-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="4ab8b-107">Properties</span><span class="sxs-lookup"><span data-stu-id="4ab8b-107">Properties</span></span>  
 <span data-ttu-id="4ab8b-108">La classe AsymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ab8b-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="4ab8b-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="4ab8b-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="4ab8b-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="4ab8b-110">Data type: string</span></span>  
  
 <span data-ttu-id="4ab8b-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ab8b-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ab8b-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="4ab8b-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="4ab8b-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="4ab8b-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="4ab8b-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="4ab8b-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="4ab8b-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="4ab8b-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="4ab8b-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="4ab8b-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4ab8b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ab8b-117">Requirements</span></span>  
  
|<span data-ttu-id="4ab8b-118">MOF</span><span class="sxs-lookup"><span data-stu-id="4ab8b-118">MOF</span></span>|<span data-ttu-id="4ab8b-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="4ab8b-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="4ab8b-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4ab8b-120">Namespace</span></span>|<span data-ttu-id="4ab8b-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="4ab8b-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4ab8b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ab8b-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
