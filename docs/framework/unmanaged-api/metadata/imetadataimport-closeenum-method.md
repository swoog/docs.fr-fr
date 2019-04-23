---
title: IMetaDataImport::CloseEnum, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.CloseEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::CloseEnum
helpviewer_keywords:
- IMetaDataImport::CloseEnum method [.NET Framework metadata]
- CloseEnum method, IMetaDataImport interface [.NET Framework metadata]
ms.assetid: 727819d5-1dab-4ebb-ac25-950b4111dc72
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7846eeceeb4d59c4e9aae73c79172c89184396e0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59123853"
---
# <a name="imetadataimportcloseenum-method"></a><span data-ttu-id="55ac9-102">IMetaDataImport::CloseEnum, méthode</span><span class="sxs-lookup"><span data-stu-id="55ac9-102">IMetaDataImport::CloseEnum Method</span></span>
<span data-ttu-id="55ac9-103">Ferme l’énumérateur qui est identifié par le handle spécifié.</span><span class="sxs-lookup"><span data-stu-id="55ac9-103">Closes the enumerator that is identified by the specified handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55ac9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55ac9-104">Syntax</span></span>  
  
```  
void CloseEnum (  
   [in] HCORENUM hEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="55ac9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55ac9-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="55ac9-106">[in] Le handle pour l’énumérateur à fermer.</span><span class="sxs-lookup"><span data-stu-id="55ac9-106">[in] The handle for the enumerator to close.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="55ac9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="55ac9-107">Remarks</span></span>  
 <span data-ttu-id="55ac9-108">Le handle spécifié par `hEnum` est obtenue à partir d’une précédente `Enum` *nom* appeler (par exemple, [IMetaDataImport::EnumTypeDefs](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumtypedefs-method.md)).</span><span class="sxs-lookup"><span data-stu-id="55ac9-108">The handle specified by `hEnum` is obtained from a previous `Enum`*Name* call (for example, [IMetaDataImport::EnumTypeDefs](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumtypedefs-method.md)).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="55ac9-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55ac9-109">Requirements</span></span>  
 <span data-ttu-id="55ac9-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="55ac9-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="55ac9-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="55ac9-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="55ac9-112">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="55ac9-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="55ac9-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="55ac9-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55ac9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55ac9-114">See also</span></span>

- [<span data-ttu-id="55ac9-115">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="55ac9-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="55ac9-116">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="55ac9-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
