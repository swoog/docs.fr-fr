---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: e968f5f2d7ffdb193b30762d32a47be3778b98dc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54621355"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="65013-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="65013-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="65013-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="65013-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65013-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65013-104">Syntax</span></span>  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="65013-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="65013-105">Methods</span></span>  
 <span data-ttu-id="65013-106">La classe AsymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="65013-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="65013-107">Properties</span><span class="sxs-lookup"><span data-stu-id="65013-107">Properties</span></span>  
 <span data-ttu-id="65013-108">La classe AsymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="65013-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="65013-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="65013-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="65013-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="65013-110">Data type: string</span></span>  
  
 <span data-ttu-id="65013-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="65013-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="65013-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="65013-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="65013-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="65013-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="65013-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="65013-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="65013-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="65013-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="65013-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="65013-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65013-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65013-117">Requirements</span></span>  
  
|<span data-ttu-id="65013-118">MOF</span><span class="sxs-lookup"><span data-stu-id="65013-118">MOF</span></span>|<span data-ttu-id="65013-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="65013-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="65013-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="65013-120">Namespace</span></span>|<span data-ttu-id="65013-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="65013-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="65013-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65013-122">See also</span></span>
- <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
