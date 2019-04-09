---
title: IMetaDataEmit::DeleteFieldMarshal, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteFieldMarshal
helpviewer_keywords:
- IMetaDataEmit::DeleteFieldMarshal method [.NET Framework metadata]
- DeleteFieldMarshal method [.NET Framework metadata]
ms.assetid: 7c75aef9-c742-4b33-a14b-56ff94b0f725
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 78f2405bba9172b775b01e5417860c3f3d2dd4a4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59206926"
---
# <a name="imetadataemitdeletefieldmarshal-method"></a><span data-ttu-id="206e9-102">IMetaDataEmit::DeleteFieldMarshal, méthode</span><span class="sxs-lookup"><span data-stu-id="206e9-102">IMetaDataEmit::DeleteFieldMarshal Method</span></span>
<span data-ttu-id="206e9-103">Détruit la signature de métadonnées pour l’objet référencé par le jeton spécifié de marshaling de PInvoke.</span><span class="sxs-lookup"><span data-stu-id="206e9-103">Destroys the PInvoke marshaling metadata signature for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="206e9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="206e9-104">Syntax</span></span>  
  
```  
HRESULT DeleteFieldMarshal (  
    [in]  mdToken     tk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="206e9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="206e9-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="206e9-106">[in] Un `mdFieldDef` ou `mdParamDef` jeton qui représente le champ ou le paramètre pour lequel supprimer la signature de métadonnées de marshaling.</span><span class="sxs-lookup"><span data-stu-id="206e9-106">[in] An `mdFieldDef` or `mdParamDef` token that represents the field or parameter for which to delete the marshaling metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="206e9-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="206e9-107">Requirements</span></span>  
 <span data-ttu-id="206e9-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="206e9-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="206e9-109">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="206e9-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="206e9-110">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="206e9-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="206e9-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="206e9-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="206e9-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="206e9-112">See also</span></span>

- [<span data-ttu-id="206e9-113">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="206e9-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="206e9-114">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="206e9-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
