---
title: IInstallReferenceEnum, interface
ms.date: 03/30/2017
api_name:
- IInstallReferenceEnum
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceEnum
helpviewer_keywords:
- IInstallReferenceEnum interface [.NET Framework fusion]
ms.assetid: 2863b33b-a541-462c-bbe8-702a2832898e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cac9f9db0b7527a80671c825a4435e8ea2d135b8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429658"
---
# <a name="iinstallreferenceenum-interface"></a><span data-ttu-id="58205-102">IInstallReferenceEnum, interface</span><span class="sxs-lookup"><span data-stu-id="58205-102">IInstallReferenceEnum Interface</span></span>
<span data-ttu-id="58205-103">Représente un énumérateur pour les assemblys référencés installés dans le global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="58205-103">Represents an enumerator for the referenced assemblies installed in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58205-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58205-104">Syntax</span></span>  
  
```  
interface IInstallReferenceEnum : IUnknown {  
    HRESULT GetNextInstallReferenceItem (  
        [out] IInstallReferenceItem **ppRefItem,  
        [in]  DWORD dwFlags,  
        [in]  LPVOID pvReserved  
    );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="58205-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="58205-105">Methods</span></span>  
  
|<span data-ttu-id="58205-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="58205-106">Method</span></span>|<span data-ttu-id="58205-107">Description</span><span class="sxs-lookup"><span data-stu-id="58205-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="58205-108">GetNextInstallReferenceItem, méthode</span><span class="sxs-lookup"><span data-stu-id="58205-108">GetNextInstallReferenceItem Method</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceenum-getnextinstallreferenceitem-method.md)|<span data-ttu-id="58205-109">Obtient un pointeur vers la prochaine `IInstallReferenceItem` contenus dans ce `IInstallReferenceEnum`.</span><span class="sxs-lookup"><span data-stu-id="58205-109">Gets a pointer to the next `IInstallReferenceItem` contained in this `IInstallReferenceEnum`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="58205-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="58205-110">Requirements</span></span>  
 <span data-ttu-id="58205-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="58205-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58205-112">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="58205-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="58205-113">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58205-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58205-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58205-114">See Also</span></span>  
 [<span data-ttu-id="58205-115">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="58205-115">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)  
 [<span data-ttu-id="58205-116">IInstallReferenceItem, interface</span><span class="sxs-lookup"><span data-stu-id="58205-116">IInstallReferenceItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)
