---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: 076313548828f1fbce9c68b48c0fa7db9cca095f
ms.sourcegitcommit: 296183dbe35077b5c5e5e74d5fbe7f399bc507ee
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2018
ms.locfileid: "50982788"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="efe88-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="efe88-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="efe88-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="efe88-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="efe88-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efe88-104">Syntax</span></span>  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="efe88-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="efe88-105">Methods</span></span>  
 <span data-ttu-id="efe88-106">La classe AsymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="efe88-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="efe88-107">Properties</span><span class="sxs-lookup"><span data-stu-id="efe88-107">Properties</span></span>  
 <span data-ttu-id="efe88-108">La classe AsymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="efe88-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="efe88-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="efe88-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="efe88-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="efe88-110">Data type: string</span></span>  
  
 <span data-ttu-id="efe88-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="efe88-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="efe88-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="efe88-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="efe88-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="efe88-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="efe88-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="efe88-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="efe88-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="efe88-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="efe88-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="efe88-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="efe88-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efe88-117">Requirements</span></span>  
  
|<span data-ttu-id="efe88-118">MOF</span><span class="sxs-lookup"><span data-stu-id="efe88-118">MOF</span></span>|<span data-ttu-id="efe88-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="efe88-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="efe88-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="efe88-120">Namespace</span></span>|<span data-ttu-id="efe88-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="efe88-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="efe88-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efe88-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
