---
title: AsymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: 7bd3b6be-8f77-4927-93ae-6fa371893cca
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 09bfaa3ab4f2aceb3e80644953a87686fca9830c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33484360"
---
# <a name="asymmetricsecuritybindingelement"></a><span data-ttu-id="cd568-102">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="cd568-102">AsymmetricSecurityBindingElement</span></span>
<span data-ttu-id="cd568-103">AsymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="cd568-103">AsymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd568-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd568-104">Syntax</span></span>  
  
```  
class AsymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="cd568-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cd568-105">Methods</span></span>  
 <span data-ttu-id="cd568-106">La classe AsymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="cd568-106">The AsymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="cd568-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cd568-107">Properties</span></span>  
 <span data-ttu-id="cd568-108">La classe AsymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd568-108">The AsymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="cd568-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="cd568-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="cd568-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="cd568-110">Data type: string</span></span>  
  
 <span data-ttu-id="cd568-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd568-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="cd568-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="cd568-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="cd568-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="cd568-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="cd568-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="cd568-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="cd568-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="cd568-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="cd568-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="cd568-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd568-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cd568-117">Requirements</span></span>  
  
|<span data-ttu-id="cd568-118">MOF</span><span class="sxs-lookup"><span data-stu-id="cd568-118">MOF</span></span>|<span data-ttu-id="cd568-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="cd568-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="cd568-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cd568-120">Namespace</span></span>|<span data-ttu-id="cd568-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="cd568-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="cd568-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd568-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.AsymmetricSecurityBindingElement>
