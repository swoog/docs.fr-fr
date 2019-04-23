---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
ms.openlocfilehash: 0f86fc1b410753b5ec100f0a7d43de9badd1401b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59978066"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="051a3-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="051a3-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="051a3-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="051a3-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="051a3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="051a3-104">Syntax</span></span>  
  
```csharp
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="051a3-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="051a3-105">Methods</span></span>  
 <span data-ttu-id="051a3-106">La classe AsymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="051a3-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="051a3-107">Properties</span><span class="sxs-lookup"><span data-stu-id="051a3-107">Properties</span></span>  
 <span data-ttu-id="051a3-108">La classe AsymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="051a3-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="051a3-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="051a3-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="051a3-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="051a3-110">Data type: string</span></span>  
  
 <span data-ttu-id="051a3-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="051a3-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="051a3-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="051a3-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="051a3-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="051a3-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="051a3-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="051a3-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="051a3-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="051a3-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="051a3-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="051a3-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="051a3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="051a3-117">Requirements</span></span>  
  
|<span data-ttu-id="051a3-118">MOF</span><span class="sxs-lookup"><span data-stu-id="051a3-118">MOF</span></span>|<span data-ttu-id="051a3-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="051a3-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="051a3-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="051a3-120">Namespace</span></span>|<span data-ttu-id="051a3-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="051a3-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="051a3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="051a3-122">See also</span></span>

- <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
