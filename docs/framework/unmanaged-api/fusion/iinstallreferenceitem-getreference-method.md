---
title: IInstallReferenceItem::GetReference, méthode
ms.date: 03/30/2017
api_name:
- IInstallReferenceItem.GetReference
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IInstallReferenceItem::GetReference
helpviewer_keywords:
- IInstallReferenceItem::GetReference method [.NET Framework fusion]
- GetReference method [.NET Framework fusion]
ms.assetid: 8960332f-c98a-405a-ba92-7003de0c1187
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cd0a554535122b81f5812102c7951f56b294796a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59213361"
---
# <a name="iinstallreferenceitemgetreference-method"></a><span data-ttu-id="ebf9d-102">IInstallReferenceItem::GetReference, méthode</span><span class="sxs-lookup"><span data-stu-id="ebf9d-102">IInstallReferenceItem::GetReference Method</span></span>
<span data-ttu-id="ebf9d-103">Obtient un pointeur vers le [FUSION_INSTALL_REFERENCE](../../../../docs/framework/unmanaged-api/fusion/fusion-install-reference-structure.md) structure représentée par ce [IInstallReferenceItem](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-103">Gets a pointer to the [FUSION_INSTALL_REFERENCE](../../../../docs/framework/unmanaged-api/fusion/fusion-install-reference-structure.md) structure represented by this [IInstallReferenceItem](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ebf9d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf9d-104">Syntax</span></span>  
  
```  
HRESULT GetReference (  
    [out] LPFUSION_INSTALL_REFERENCE *ppRefData,  
    [in]  DWORD dwFlags,  
    [in]  LPVOID pvReserved  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ebf9d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebf9d-105">Parameters</span></span>  
 `ppRefData`  
 <span data-ttu-id="ebf9d-106">[out] Retourné `FUSION_INSTALL_REFERENCE` pointeur.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-106">[out] The returned `FUSION_INSTALL_REFERENCE` pointer.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="ebf9d-107">[in] Réservé pour une extensibilité future.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-107">[in] Reserved for future extensibility.</span></span> `dwFlags` <span data-ttu-id="ebf9d-108">doit être 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ebf9d-108">must be 0 (zero).</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="ebf9d-109">[in] Réservé pour une extensibilité future.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-109">[in] Reserved for future extensibility.</span></span> `pvReserved` <span data-ttu-id="ebf9d-110">doit être une référence null.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-110">must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ebf9d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf9d-111">Requirements</span></span>  
 <span data-ttu-id="ebf9d-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ebf9d-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ebf9d-113">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="ebf9d-113">**Header:** Fusion.h</span></span>  
  
 **<span data-ttu-id="ebf9d-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ebf9d-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ebf9d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf9d-115">See also</span></span>

- [<span data-ttu-id="ebf9d-116">IInstallReferenceItem, interface</span><span class="sxs-lookup"><span data-stu-id="ebf9d-116">IInstallReferenceItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iinstallreferenceitem-interface.md)
- [<span data-ttu-id="ebf9d-117">FUSION_INSTALL_REFERENCE, structure</span><span class="sxs-lookup"><span data-stu-id="ebf9d-117">FUSION_INSTALL_REFERENCE Structure</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-install-reference-structure.md)
