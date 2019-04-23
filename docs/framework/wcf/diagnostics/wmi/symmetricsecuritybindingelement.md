---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
ms.openlocfilehash: f6effd533a205d0e8fd1421119e325f06b340dd1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59770410"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="0fcf8-102">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="0fcf8-102">SymmetricSecurityBindingElement</span></span>
<span data-ttu-id="0fcf8-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="0fcf8-103">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fcf8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fcf8-104">Syntax</span></span>  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="0fcf8-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0fcf8-105">Methods</span></span>  
 <span data-ttu-id="0fcf8-106">La classe SymmetricSecurityBindingElement ne définit pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="0fcf8-106">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="0fcf8-107">Properties</span><span class="sxs-lookup"><span data-stu-id="0fcf8-107">Properties</span></span>  
 <span data-ttu-id="0fcf8-108">La classe SymmetricSecurityBindingElement a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="0fcf8-108">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="0fcf8-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="0fcf8-109">MessageProtectionOrder</span></span>  
 <span data-ttu-id="0fcf8-110">Type de données : chaîne</span><span class="sxs-lookup"><span data-stu-id="0fcf8-110">Data type: string</span></span>  
  
 <span data-ttu-id="0fcf8-111">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="0fcf8-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0fcf8-112">Ordre de chiffrement et de signature des messages de cette liaison.</span><span class="sxs-lookup"><span data-stu-id="0fcf8-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="0fcf8-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="0fcf8-113">RequireSignatureConfirmation</span></span>  
 <span data-ttu-id="0fcf8-114">Type de données : booléen</span><span class="sxs-lookup"><span data-stu-id="0fcf8-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="0fcf8-115">Type d’accès : Propriétés en lecture seule</span><span class="sxs-lookup"><span data-stu-id="0fcf8-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0fcf8-116">Si la liaison requiert la confirmation de signature.</span><span class="sxs-lookup"><span data-stu-id="0fcf8-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fcf8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0fcf8-117">Requirements</span></span>  
  
|<span data-ttu-id="0fcf8-118">MOF</span><span class="sxs-lookup"><span data-stu-id="0fcf8-118">MOF</span></span>|<span data-ttu-id="0fcf8-119">Déclaré dans Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="0fcf8-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="0fcf8-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0fcf8-120">Namespace</span></span>|<span data-ttu-id="0fcf8-121">Défini dans root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="0fcf8-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0fcf8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fcf8-122">See also</span></span>

- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
