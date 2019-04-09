---
title: ICorPublishAppDomain::GetName, méthode
ms.date: 03/30/2017
api_name:
- ICorPublishAppDomain.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishAppDomain::GetName
helpviewer_keywords:
- GetName method, ICorPublishAppDomain interface [.NET Framework debugging]
- ICorPublishAppDomain::GetName method [.NET Framework debugging]
ms.assetid: 6ef8ac9b-9803-4b65-8b13-25f3e0b1bc6b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5de74b52caee27a1a12cff4a7f9165a07e961ce7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59072783"
---
# <a name="icorpublishappdomaingetname-method"></a><span data-ttu-id="bcf3c-102">ICorPublishAppDomain::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="bcf3c-102">ICorPublishAppDomain::GetName Method</span></span>
<span data-ttu-id="bcf3c-103">Obtient le nom du domaine d’application qui est représenté par ce [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md).</span><span class="sxs-lookup"><span data-stu-id="bcf3c-103">Gets the name of the application domain that is represented by this [ICorPublishAppDomain](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bcf3c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcf3c-104">Syntax</span></span>  
  
```  
HRESULT GetName (  
    [in]  ULONG32   cchName,   
    [out] ULONG32   *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]   
        WCHAR       *szName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bcf3c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcf3c-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="bcf3c-106">[in] Taille du tableau `szName`.</span><span class="sxs-lookup"><span data-stu-id="bcf3c-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="bcf3c-107">[out] Un pointeur vers le nombre de caractères larges, y compris le caractère null, retourné dans le `szName` tableau.</span><span class="sxs-lookup"><span data-stu-id="bcf3c-107">[out] A pointer to the number of wide characters, including the null character, returned in the `szName` array.</span></span>  
  
 `szName`  
 <span data-ttu-id="bcf3c-108">[out] Tableau dans lequel stocker le nom.</span><span class="sxs-lookup"><span data-stu-id="bcf3c-108">[out] An array in which to store the name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bcf3c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bcf3c-109">Remarks</span></span>  
 <span data-ttu-id="bcf3c-110">Si `szName` n’est pas null, le `GetName` méthode copie jusqu'à `cchName` caractères (y compris le terminateur null) dans `szName`.</span><span class="sxs-lookup"><span data-stu-id="bcf3c-110">If `szName` is non-null, the `GetName` method copies up to `cchName` characters (including the null terminator) into `szName`.</span></span> <span data-ttu-id="bcf3c-111">Si une valeur non null est retournée dans `pcchName`, le nombre réel de caractères dans le nom (y compris le terminateur null) est stocké dans le `szName` tableau.</span><span class="sxs-lookup"><span data-stu-id="bcf3c-111">If a non-null is returned in `pcchName`, the actual number of characters in the name (including the null terminator) is stored in the `szName` array.</span></span>  
  
 <span data-ttu-id="bcf3c-112">Le `GetName` méthode retourne une valeur S_OK HRESULT, quel que soit le nombre de caractères ont été copié.</span><span class="sxs-lookup"><span data-stu-id="bcf3c-112">The `GetName` method returns an S_OK HRESULT regardless of how many characters were copied.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bcf3c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcf3c-113">Requirements</span></span>  
 <span data-ttu-id="bcf3c-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bcf3c-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcf3c-115">**En-tête :** CorPub.idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="bcf3c-115">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="bcf3c-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bcf3c-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="bcf3c-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="bcf3c-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bcf3c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcf3c-118">See also</span></span>

- [<span data-ttu-id="bcf3c-119">ICorPublishAppDomain, interface</span><span class="sxs-lookup"><span data-stu-id="bcf3c-119">ICorPublishAppDomain Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishappdomain-interface.md)
