---
title: ICorDebugClass::GetToken, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugClass.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass::GetToken
helpviewer_keywords:
- GetToken method, ICorDebugClass interface [.NET Framework debugging]
- ICorDebugClass::GetToken method [.NET Framework debugging]
ms.assetid: ee5c848a-eac4-4462-b07a-07ccd76a75df
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c4f33bb15a351be5fe8318dcc3339d429dec039e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59183701"
---
# <a name="icordebugclassgettoken-method"></a><span data-ttu-id="96474-102">ICorDebugClass::GetToken, méthode</span><span class="sxs-lookup"><span data-stu-id="96474-102">ICorDebugClass::GetToken Method</span></span>
<span data-ttu-id="96474-103">Obtient le `TypeDef` jeton de métadonnées qui fait référence à la définition de cette classe.</span><span class="sxs-lookup"><span data-stu-id="96474-103">Gets the `TypeDef` metadata token that references the definition of this class.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96474-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96474-104">Syntax</span></span>  
  
```  
HRESULT GetToken (  
    [out] mdTypeDef          *pTypeDef  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="96474-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96474-105">Parameters</span></span>  
 `pTypeDef`  
 <span data-ttu-id="96474-106">[out] Un pointeur vers un `mdTypeDef` jeton qui fait référence à la définition de cette classe.</span><span class="sxs-lookup"><span data-stu-id="96474-106">[out] A pointer to an `mdTypeDef` token that references the definition of this class.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96474-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96474-107">Requirements</span></span>  
 <span data-ttu-id="96474-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="96474-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96474-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="96474-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="96474-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="96474-110">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="96474-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="96474-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="96474-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96474-112">See also</span></span>

- [<span data-ttu-id="96474-113">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="96474-113">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
