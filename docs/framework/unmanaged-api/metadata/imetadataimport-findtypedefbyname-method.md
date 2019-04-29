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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777856"
---
# <a name="imetadataimportfindtypedefbyname-method"></a><span data-ttu-id="3a8ca-102">IMetaDataImport::FindTypeDefByName, méthode</span><span class="sxs-lookup"><span data-stu-id="3a8ca-102">IMetaDataImport::FindTypeDefByName Method</span></span>
<span data-ttu-id="3a8ca-103">Obtient un pointeur vers les métadonnées TypeDef jeton pour le <xref:System.Type> portant le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a8ca-103">Gets a pointer to the TypeDef metadata token for the <xref:System.Type> with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a8ca-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a8ca-104">Syntax</span></span>  
  
```  
HRESULT FindTypeDefByName  
   [in]  LPCWSTR       szTypeDef,  
   [in]  mdToken       tkEnclosingClass,  
   [out] mdTypeDef     *ptd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3a8ca-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a8ca-105">Parameters</span></span>  
 `szTypeDef`  
 <span data-ttu-id="3a8ca-106">[in] Le nom du type pour lequel obtenir le jeton TypeDef.</span><span class="sxs-lookup"><span data-stu-id="3a8ca-106">[in] The name of the type for which to get the TypeDef token.</span></span>  
  
 `tkEnclosingClass`  
 <span data-ttu-id="3a8ca-107">[in] Jeton TypeDef ou TypeRef qui représente la classe englobante.</span><span class="sxs-lookup"><span data-stu-id="3a8ca-107">[in] A TypeDef or TypeRef token representing the enclosing class.</span></span> <span data-ttu-id="3a8ca-108">Si le type à rechercher n’est pas une classe imbriquée, définissez cette valeur sur NULL.</span><span class="sxs-lookup"><span data-stu-id="3a8ca-108">If the type to find is not a nested class, set this value to NULL.</span></span>  
  
 `ptd`  
 <span data-ttu-id="3a8ca-109">[out] Pointeur vers le jeton TypeDef correspondant.</span><span class="sxs-lookup"><span data-stu-id="3a8ca-109">[out] A pointer to the matching TypeDef token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a8ca-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a8ca-110">Requirements</span></span>  
 <span data-ttu-id="3a8ca-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3a8ca-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a8ca-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3a8ca-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3a8ca-113">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3a8ca-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3a8ca-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a8ca-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a8ca-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a8ca-115">See also</span></span>

- [<span data-ttu-id="3a8ca-116">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="3a8ca-116">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="3a8ca-117">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="3a8ca-117">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
