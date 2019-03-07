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
ms.openlocfilehash: 6e887fb5f4f9667bed7eef4a84899f82cada0fcd
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57489577"
---
# <a name="imetadataimportisvalidtoken-method"></a><span data-ttu-id="feeca-102">IMetaDataImport::IsValidToken, méthode</span><span class="sxs-lookup"><span data-stu-id="feeca-102">IMetaDataImport::IsValidToken Method</span></span>
<span data-ttu-id="feeca-103">Obtient une valeur indiquant si le jeton spécifié contient une référence valide à un objet de code.</span><span class="sxs-lookup"><span data-stu-id="feeca-103">Gets a value indicating whether the specified token holds a valid reference to a code object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="feeca-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="feeca-104">Syntax</span></span>  
  
```  
BOOL IsValidToken (  
   [in] mdToken     tk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="feeca-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="feeca-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="feeca-106">[in] Le jeton pour vérifier la validité de la référence.</span><span class="sxs-lookup"><span data-stu-id="feeca-106">[in] The token to check the reference validity for.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="feeca-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="feeca-107">Return Value</span></span>  
 <span data-ttu-id="feeca-108">`true` Si `tk` est un jeton de métadonnées valide dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="feeca-108">`true` if `tk` is a valid metadata token within the current scope.</span></span> <span data-ttu-id="feeca-109">Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="feeca-109">Otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="feeca-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="feeca-110">Requirements</span></span>  
 <span data-ttu-id="feeca-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="feeca-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="feeca-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="feeca-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="feeca-113">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="feeca-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="feeca-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="feeca-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="feeca-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="feeca-115">See also</span></span>
- [<span data-ttu-id="feeca-116">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="feeca-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="feeca-117">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="feeca-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
