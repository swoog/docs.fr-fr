---
title: IMetaDataImport::FindTypeDefByName, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.FindTypeDefByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::FindTypeDefByName
helpviewer_keywords:
- FindTypeDefByName method [.NET Framework metadata]
- IMetaDataImport::FindTypeDefByName method [.NET Framework metadata]
ms.assetid: f4c2cd88-ac28-4bad-9ab1-2cf9d2de41e6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5cd6b74ce2871cfafc0dc2260be3f758f6a28704
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59168686"
---
# <a name="imetadataimportfindtypedefbyname-method"></a><span data-ttu-id="2080e-102">IMetaDataImport::FindTypeDefByName, méthode</span><span class="sxs-lookup"><span data-stu-id="2080e-102">IMetaDataImport::FindTypeDefByName Method</span></span>
<span data-ttu-id="2080e-103">Obtient un pointeur vers les métadonnées TypeDef jeton pour le <xref:System.Type> portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="2080e-103">Gets a pointer to the TypeDef metadata token for the <xref:System.Type> with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2080e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2080e-104">Syntax</span></span>  
  
```  
HRESULT FindTypeDefByName  
   [in]  LPCWSTR       szTypeDef,  
   [in]  mdToken       tkEnclosingClass,  
   [out] mdTypeDef     *ptd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2080e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2080e-105">Parameters</span></span>  
 `szTypeDef`  
 <span data-ttu-id="2080e-106">[in] Le nom du type pour lequel obtenir le jeton TypeDef.</span><span class="sxs-lookup"><span data-stu-id="2080e-106">[in] The name of the type for which to get the TypeDef token.</span></span>  
  
 `tkEnclosingClass`  
 <span data-ttu-id="2080e-107">[in] Jeton TypeDef ou TypeRef qui représente la classe englobante.</span><span class="sxs-lookup"><span data-stu-id="2080e-107">[in] A TypeDef or TypeRef token representing the enclosing class.</span></span> <span data-ttu-id="2080e-108">Si le type à rechercher n’est pas une classe imbriquée, définissez cette valeur sur NULL.</span><span class="sxs-lookup"><span data-stu-id="2080e-108">If the type to find is not a nested class, set this value to NULL.</span></span>  
  
 `ptd`  
 <span data-ttu-id="2080e-109">[out] Pointeur vers le jeton TypeDef correspondant.</span><span class="sxs-lookup"><span data-stu-id="2080e-109">[out] A pointer to the matching TypeDef token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2080e-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2080e-110">Requirements</span></span>  
 <span data-ttu-id="2080e-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2080e-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2080e-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="2080e-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2080e-113">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2080e-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2080e-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2080e-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2080e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2080e-115">See also</span></span>

- [<span data-ttu-id="2080e-116">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="2080e-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="2080e-117">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="2080e-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
