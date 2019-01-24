---
title: StackOverflowType, énumération
ms.date: 03/30/2017
api_name:
- StackOverflowType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowType
helpviewer_keywords:
- StackOverflowType enumeration [.NET Framework hosting]
ms.assetid: dab648ad-972b-479c-b129-b4c1dcbd932e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 06c9119a2b842a0efcd4af752ba72dbfda03bf13
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54653857"
---
# <a name="stackoverflowtype-enumeration"></a><span data-ttu-id="3a931-102">StackOverflowType, énumération</span><span class="sxs-lookup"><span data-stu-id="3a931-102">StackOverflowType Enumeration</span></span>
<span data-ttu-id="3a931-103">Contient des valeurs qui indiquent la cause sous-jacente d’un événement de dépassement de capacité de pile.</span><span class="sxs-lookup"><span data-stu-id="3a931-103">Contains values that indicate the underlying cause of a stack overflow event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a931-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a931-104">Syntax</span></span>  
  
```  
typedef enum {  
    SO_Managed,  
    SO_ClrEngine,  
    SO_Other  
} StackOverflowType;  
```  
  
## <a name="members"></a><span data-ttu-id="3a931-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3a931-105">Members</span></span>  
  
|<span data-ttu-id="3a931-106">Membre</span><span class="sxs-lookup"><span data-stu-id="3a931-106">Member</span></span>|<span data-ttu-id="3a931-107">Description</span><span class="sxs-lookup"><span data-stu-id="3a931-107">Description</span></span>|  
|------------|-----------------|  
|`SO_ClrEngine`|<span data-ttu-id="3a931-108">Le dépassement de capacité de pile a été provoqué par le moteur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3a931-108">The stack overflow was caused by the execution engine.</span></span>|  
|`SO_Managed`|<span data-ttu-id="3a931-109">Le dépassement de capacité de pile a été provoqué par le code managé.</span><span class="sxs-lookup"><span data-stu-id="3a931-109">The stack overflow was caused by managed code.</span></span>|  
|`SO_Other`|<span data-ttu-id="3a931-110">Le dépassement de capacité de pile a été provoqué par le code non managé.</span><span class="sxs-lookup"><span data-stu-id="3a931-110">The stack overflow was caused by unmanaged code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3a931-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3a931-111">Remarks</span></span>  
 <span data-ttu-id="3a931-112">Ces informations sont passées à l’hôte via un appel à la [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="3a931-112">This information is passed to the host through a call to the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a931-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3a931-113">Requirements</span></span>  
 <span data-ttu-id="3a931-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3a931-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a931-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3a931-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3a931-116">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3a931-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3a931-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a931-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a931-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a931-118">See also</span></span>
- [<span data-ttu-id="3a931-119">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="3a931-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
