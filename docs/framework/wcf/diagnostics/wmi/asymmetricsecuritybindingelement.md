---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: 076313548828f1fbce9c68b48c0fa7db9cca095f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50185116"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="aecca-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="aecca-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="aecca-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="aecca-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aecca-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aecca-104">Syntax</span></span>  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="aecca-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aecca-105">Methods</span></span>  
 <span data-ttu-id="aecca-106">La classe AsymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="aecca-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="aecca-107">Properties</span><span class="sxs-lookup"><span data-stu-id="aecca-107">Properties</span></span>  
 <span data-ttu-id="aecca-108">La classe AsymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="aecca-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="aecca-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="aecca-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="aecca-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="aecca-110">Data type: string</span></span>  
  
 <span data-ttu-id="aecca-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="aecca-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="aecca-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="aecca-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="aecca-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="aecca-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="aecca-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="aecca-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="aecca-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="aecca-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="aecca-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="aecca-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aecca-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aecca-117">Requirements</span></span>  
  
|<span data-ttu-id="aecca-118">MOF</span><span class="sxs-lookup"><span data-stu-id="aecca-118">MOF</span></span>|<span data-ttu-id="aecca-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="aecca-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="aecca-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="aecca-120">Namespace</span></span>|<span data-ttu-id="aecca-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="aecca-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="aecca-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aecca-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
