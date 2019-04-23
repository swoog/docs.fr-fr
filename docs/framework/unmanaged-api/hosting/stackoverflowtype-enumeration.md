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
ms.openlocfilehash: 8541ea7b614ff4a6ca666f0e2549a7f50e190192
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59135874"
---
# <a name="stackoverflowtype-enumeration"></a><span data-ttu-id="a0365-102">StackOverflowType, énumération</span><span class="sxs-lookup"><span data-stu-id="a0365-102">StackOverflowType Enumeration</span></span>
<span data-ttu-id="a0365-103">Contient des valeurs qui indiquent la cause sous-jacente d’un événement de dépassement de capacité de pile.</span><span class="sxs-lookup"><span data-stu-id="a0365-103">Contains values that indicate the underlying cause of a stack overflow event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0365-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0365-104">Syntax</span></span>  
  
```  
typedef enum {  
    SO_Managed,  
    SO_ClrEngine,  
    SO_Other  
} StackOverflowType;  
```  
  
## <a name="members"></a><span data-ttu-id="a0365-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a0365-105">Members</span></span>  
  
|<span data-ttu-id="a0365-106">Membre</span><span class="sxs-lookup"><span data-stu-id="a0365-106">Member</span></span>|<span data-ttu-id="a0365-107">Description</span><span class="sxs-lookup"><span data-stu-id="a0365-107">Description</span></span>|  
|------------|-----------------|  
|`SO_ClrEngine`|<span data-ttu-id="a0365-108">Le dépassement de capacité de pile a été provoqué par le moteur d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a0365-108">The stack overflow was caused by the execution engine.</span></span>|  
|`SO_Managed`|<span data-ttu-id="a0365-109">Le dépassement de capacité de pile a été provoqué par le code managé.</span><span class="sxs-lookup"><span data-stu-id="a0365-109">The stack overflow was caused by managed code.</span></span>|  
|`SO_Other`|<span data-ttu-id="a0365-110">Le dépassement de capacité de pile a été provoqué par le code non managé.</span><span class="sxs-lookup"><span data-stu-id="a0365-110">The stack overflow was caused by unmanaged code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a0365-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a0365-111">Remarks</span></span>  
 <span data-ttu-id="a0365-112">Ces informations sont passées à l’hôte via un appel à la [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a0365-112">This information is passed to the host through a call to the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0365-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0365-113">Requirements</span></span>  
 <span data-ttu-id="a0365-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a0365-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0365-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a0365-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a0365-116">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a0365-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a0365-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a0365-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0365-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0365-118">See also</span></span>

- [<span data-ttu-id="a0365-119">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="a0365-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
