---
title: IMetaDataImport::IsValidToken, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.IsValidToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::IsValidToken
helpviewer_keywords:
- IMetaDataImport::IsValidToken method [.NET Framework metadata]
- IsValidToken method [.NET Framework metadata]
ms.assetid: aeb0fc63-9eff-4384-9284-cb9900572d74
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d752d6dbe8a6b7a23faae498f9118c8d89e92929
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447695"
---
# <a name="imetadataimportisvalidtoken-method"></a><span data-ttu-id="c4c51-102">IMetaDataImport::IsValidToken, méthode</span><span class="sxs-lookup"><span data-stu-id="c4c51-102">IMetaDataImport::IsValidToken Method</span></span>
<span data-ttu-id="c4c51-103">Obtient une valeur indiquant si le jeton spécifié contient une référence valide à un objet de code.</span><span class="sxs-lookup"><span data-stu-id="c4c51-103">Gets a value indicating whether the specified token holds a valid reference to a code object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4c51-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4c51-104">Syntax</span></span>  
  
```  
BOOL IsValidToken (  
   [in] mdToken     tk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c4c51-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4c51-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="c4c51-106">[in] Le jeton pour vérifier la validité de la référence.</span><span class="sxs-lookup"><span data-stu-id="c4c51-106">[in] The token to check the reference validity for.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c4c51-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c4c51-107">Return Value</span></span>  
 <span data-ttu-id="c4c51-108">`true` Si `tk` est un jeton de métadonnées valide dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="c4c51-108">`true` if `tk` is a valid metadata token within the current scope.</span></span> <span data-ttu-id="c4c51-109">Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="c4c51-109">Otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4c51-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4c51-110">Requirements</span></span>  
 <span data-ttu-id="c4c51-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c4c51-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4c51-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c4c51-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c4c51-113">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c4c51-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c4c51-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4c51-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4c51-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4c51-115">See Also</span></span>  
 [<span data-ttu-id="c4c51-116">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="c4c51-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="c4c51-117">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="c4c51-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
