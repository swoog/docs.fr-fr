---
title: IMetaDataTables::GetCodedTokenInfo, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables.GetCodedTokenInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetCodedTokenInfo
helpviewer_keywords:
- GetCodedTokenInfo method [.NET Framework metadata]
- IMetaDataTables::GetCodedTokenInfo method [.NET Framework metadata]
ms.assetid: 31214d3a-715e-49af-92b3-0fd11e4f218a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a7a36d14b67efb3934089dc16de41a3b80ea0c0e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447988"
---
# <a name="imetadatatablesgetcodedtokeninfo-method"></a><span data-ttu-id="81f72-102">IMetaDataTables::GetCodedTokenInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="81f72-102">IMetaDataTables::GetCodedTokenInfo Method</span></span>
<span data-ttu-id="81f72-103">Obtient un pointeur vers un tableau de jetons associé à l’index de ligne spécifié.</span><span class="sxs-lookup"><span data-stu-id="81f72-103">Gets a pointer to an array of tokens associated with the specified row index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81f72-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81f72-104">Syntax</span></span>  
  
```  
HRESULT GetCodedTokenInfo (   
    [in]  ULONG       ixCdTkn,  
    [out] ULONG       *pcTokens,  
    [out] ULONG       **ppTokens,  
    [out] const char  **ppName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="81f72-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81f72-105">Parameters</span></span>  
 `ixCdTkn`  
 <span data-ttu-id="81f72-106">[in] Le type de jeton codé à retourner.</span><span class="sxs-lookup"><span data-stu-id="81f72-106">[in] The kind of coded token to return.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="81f72-107">[out] Un pointeur vers la longueur de `ppTokens`.</span><span class="sxs-lookup"><span data-stu-id="81f72-107">[out] A pointer to the length of `ppTokens`.</span></span>  
  
 `ppTokens`  
 <span data-ttu-id="81f72-108">[out] Pointeur vers un pointeur vers un tableau qui contient la liste des jetons retournés.</span><span class="sxs-lookup"><span data-stu-id="81f72-108">[out] A pointer to a pointer to an array that contains the list of returned tokens.</span></span>  
  
 `ppName`  
 <span data-ttu-id="81f72-109">[out] Un pointeur vers un pointeur vers le nom du jeton à `ixCdTkn`.</span><span class="sxs-lookup"><span data-stu-id="81f72-109">[out] A pointer to a pointer to the name of the token at `ixCdTkn`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81f72-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="81f72-110">Requirements</span></span>  
 <span data-ttu-id="81f72-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="81f72-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81f72-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="81f72-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="81f72-113">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="81f72-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="81f72-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81f72-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81f72-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81f72-115">See Also</span></span>  
 [<span data-ttu-id="81f72-116">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="81f72-116">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="81f72-117">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="81f72-117">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
