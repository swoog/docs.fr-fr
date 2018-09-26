---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
author: BrucePerlerMS
ms.openlocfilehash: 180b64f6f37e5c765585e52b292319816618be28
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47198850"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="fa179-102">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="fa179-102">SymmetricSecurityBindingElement</span></span>
<span data-ttu-id="fa179-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="fa179-103">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fa179-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa179-104">Syntax</span></span>  
  
```  
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="fa179-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fa179-105">Methods</span></span>  
 <span data-ttu-id="fa179-106">La classe SymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="fa179-106">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="fa179-107">Properties</span><span class="sxs-lookup"><span data-stu-id="fa179-107">Properties</span></span>  
 <span data-ttu-id="fa179-108">La classe SymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="fa179-108">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="fa179-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="fa179-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="fa179-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="fa179-110">Data type: string</span></span>  
  
 <span data-ttu-id="fa179-111">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa179-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fa179-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="fa179-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="fa179-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="fa179-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="fa179-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="fa179-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="fa179-115">Type d'accès : lecture seule</span><span class="sxs-lookup"><span data-stu-id="fa179-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="fa179-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="fa179-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fa179-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa179-117">Requirements</span></span>  
  
|<span data-ttu-id="fa179-118">MOF</span><span class="sxs-lookup"><span data-stu-id="fa179-118">MOF</span></span>|<span data-ttu-id="fa179-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="fa179-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="fa179-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fa179-120">Namespace</span></span>|<span data-ttu-id="fa179-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="fa179-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="fa179-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa179-122">See Also</span></span>  
 <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
