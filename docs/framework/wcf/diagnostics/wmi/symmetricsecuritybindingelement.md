---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 7fc720f4f0be25a0cec25d979942af8472efa4ee
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33485054"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="e6df6-102">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="e6df6-102">SymmetricSecurityBindingElement</span></span>
<span data-ttu-id="e6df6-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="e6df6-103">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6df6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6df6-104">Syntax</span></span>  
  
```  
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="e6df6-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6df6-105">Methods</span></span>  
 <span data-ttu-id="e6df6-106">La classe SymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="e6df6-106">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="e6df6-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e6df6-107">Properties</span></span>  
 <span data-ttu-id="e6df6-108">La classe SymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6df6-108">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="e6df6-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="e6df6-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="e6df6-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="e6df6-110">Data type: string</span></span>  
  
 <span data-ttu-id="e6df6-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6df6-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e6df6-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="e6df6-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="e6df6-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="e6df6-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="e6df6-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="e6df6-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="e6df6-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="e6df6-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="e6df6-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="e6df6-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6df6-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e6df6-117">Requirements</span></span>  
  
|<span data-ttu-id="e6df6-118">MOF</span><span class="sxs-lookup"><span data-stu-id="e6df6-118">MOF</span></span>|<span data-ttu-id="e6df6-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="e6df6-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="e6df6-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e6df6-120">Namespace</span></span>|<span data-ttu-id="e6df6-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="e6df6-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="e6df6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6df6-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
