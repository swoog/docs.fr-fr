---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
ms.openlocfilehash: 7b979a6872da15c4130e580a3f7327802f42db18
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54701389"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="f758d-102">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="f758d-102">SymmetricSecurityBindingElement</span></span>
<span data-ttu-id="f758d-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="f758d-103">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f758d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f758d-104">Syntax</span></span>  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="f758d-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f758d-105">Methods</span></span>  
 <span data-ttu-id="f758d-106">La classe SymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="f758d-106">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="f758d-107">Properties</span><span class="sxs-lookup"><span data-stu-id="f758d-107">Properties</span></span>  
 <span data-ttu-id="f758d-108">La classe SymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="f758d-108">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="f758d-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="f758d-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="f758d-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="f758d-110">Data type: string</span></span>  
  
 <span data-ttu-id="f758d-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f758d-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f758d-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="f758d-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="f758d-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="f758d-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="f758d-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="f758d-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="f758d-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="f758d-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="f758d-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="f758d-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f758d-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f758d-117">Requirements</span></span>  
  
|<span data-ttu-id="f758d-118">MOF</span><span class="sxs-lookup"><span data-stu-id="f758d-118">MOF</span></span>|<span data-ttu-id="f758d-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="f758d-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="f758d-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f758d-120">Namespace</span></span>|<span data-ttu-id="f758d-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f758d-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f758d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f758d-122">See also</span></span>
- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
