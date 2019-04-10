---
title: ICorPublishProcess::GetDisplayName, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishProcess.GetDisplayName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::GetDisplayName
helpviewer_keywords:
- ICorPublishProcess::GetDisplayName method [.NET Framework debugging]
- GetDisplayName method, ICorPublishProcess interface [.NET Framework debugging]
ms.assetid: 7c0af9e9-a73f-41aa-a685-b21c439e059d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a6e7aa845f104ef734f039d46e1eeaba5fd01c73
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59221767"
---
# <a name="icorpublishprocessgetdisplayname-method"></a><span data-ttu-id="68d05-102">ICorPublishProcess::GetDisplayName, méthode</span><span class="sxs-lookup"><span data-stu-id="68d05-102">ICorPublishProcess::GetDisplayName Method</span></span>
<span data-ttu-id="68d05-103">Obtient le chemin d’accès complet du fichier exécutable pour le processus référencé par ce [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md).</span><span class="sxs-lookup"><span data-stu-id="68d05-103">Gets the full path of the executable for the process referenced by this [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68d05-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68d05-104">Syntax</span></span>  
  
```  
HRESULT GetDisplayName (  
    [in]  ULONG32                    cchName,   
    [out] ULONG32                    *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]   
        WCHAR                        *szName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="68d05-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68d05-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="68d05-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="68d05-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="68d05-107">[out] Le nombre de caractères étendus retournés dans le `szName` tableau.</span><span class="sxs-lookup"><span data-stu-id="68d05-107">[out] The number of wide characters returned in the `szName` array.</span></span>  
  
 `szName`  
 <span data-ttu-id="68d05-108">[out] Un tableau pour stocker le nom, y compris le chemin d’accès complet du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="68d05-108">[out] An array to store the name, including the full path, of the executable.</span></span> <span data-ttu-id="68d05-109">Le nom est nul.</span><span class="sxs-lookup"><span data-stu-id="68d05-109">The name is null-terminated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="68d05-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68d05-110">Requirements</span></span>  
 <span data-ttu-id="68d05-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="68d05-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68d05-112">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="68d05-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="68d05-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="68d05-113">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="68d05-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="68d05-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="68d05-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68d05-115">See also</span></span>

- [<span data-ttu-id="68d05-116">ICorPublishProcess, interface</span><span class="sxs-lookup"><span data-stu-id="68d05-116">ICorPublishProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
