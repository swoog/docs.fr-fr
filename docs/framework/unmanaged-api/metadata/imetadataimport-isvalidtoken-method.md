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
ms.openlocfilehash: 5a9e5a2f7baa1c15ac54950bf1bfc0d448d08f58
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54567789"
---
# <a name="imetadataimportisvalidtoken-method"></a><span data-ttu-id="a1b01-102">IMetaDataImport::IsValidToken, méthode</span><span class="sxs-lookup"><span data-stu-id="a1b01-102">IMetaDataImport::IsValidToken Method</span></span>
<span data-ttu-id="a1b01-103">Obtient une valeur indiquant si le jeton spécifié contient une référence valide à un objet de code.</span><span class="sxs-lookup"><span data-stu-id="a1b01-103">Gets a value indicating whether the specified token holds a valid reference to a code object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a1b01-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1b01-104">Syntax</span></span>  
  
```  
BOOL IsValidToken (  
   [in] mdToken     tk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a1b01-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1b01-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="a1b01-106">[in] Le jeton pour vérifier la validité de la référence.</span><span class="sxs-lookup"><span data-stu-id="a1b01-106">[in] The token to check the reference validity for.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a1b01-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a1b01-107">Return Value</span></span>  
 <span data-ttu-id="a1b01-108">`true` Si `tk` est un jeton de métadonnées valide dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="a1b01-108">`true` if `tk` is a valid metadata token within the current scope.</span></span> <span data-ttu-id="a1b01-109">Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="a1b01-109">Otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a1b01-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a1b01-110">Requirements</span></span>  
 <span data-ttu-id="a1b01-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a1b01-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1b01-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a1b01-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a1b01-113">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a1b01-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a1b01-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a1b01-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1b01-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1b01-115">See also</span></span>
- [<span data-ttu-id="a1b01-116">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="a1b01-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="a1b01-117">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="a1b01-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
