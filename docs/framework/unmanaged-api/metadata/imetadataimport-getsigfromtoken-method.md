---
title: IMetaDataImport::GetSigFromToken, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetSigFromToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetSigFromToken
helpviewer_keywords:
- IMetaDataImport::GetSigFromToken method [.NET Framework metadata]
- GetSigFromToken method [.NET Framework metadata]
ms.assetid: ab894dc4-f7b6-4afc-bfcb-582a4b7e53a2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 823a172c05d2ce76fef790966f54d7216f579fde
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59152982"
---
# <a name="imetadataimportgetsigfromtoken-method"></a><span data-ttu-id="5f81b-102">IMetaDataImport::GetSigFromToken, méthode</span><span class="sxs-lookup"><span data-stu-id="5f81b-102">IMetaDataImport::GetSigFromToken Method</span></span>
<span data-ttu-id="5f81b-103">Obtient la signature de métadonnées binaires associée au jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="5f81b-103">Gets the binary metadata signature associated with the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5f81b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f81b-104">Syntax</span></span>  
  
```  
HRESULT GetSigFromToken (   
   [in]   mdSignature        mdSig,   
   [out]  PCCOR_SIGNATURE    *ppvSig,   
   [out]  ULONG              *pcbSig   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5f81b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f81b-105">Parameters</span></span>  
 `mdSig`  
 <span data-ttu-id="5f81b-106">[in] Le jeton à retourner pour la signature de métadonnées binaires.</span><span class="sxs-lookup"><span data-stu-id="5f81b-106">[in] The token to return the binary metadata signature for.</span></span>  
  
 `ppvSig`  
 <span data-ttu-id="5f81b-107">[out] Pointeur vers la signature de métadonnées retournées.</span><span class="sxs-lookup"><span data-stu-id="5f81b-107">[out] A pointer to the returned metadata signature.</span></span>  
  
 `pcbSig`  
 <span data-ttu-id="5f81b-108">[out] La taille en octets de la signature de métadonnées binaires.</span><span class="sxs-lookup"><span data-stu-id="5f81b-108">[out] The size in bytes of the binary metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5f81b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f81b-109">Requirements</span></span>  
 <span data-ttu-id="5f81b-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5f81b-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5f81b-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="5f81b-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="5f81b-112">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="5f81b-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="5f81b-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f81b-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f81b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f81b-114">See also</span></span>

- [<span data-ttu-id="5f81b-115">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="5f81b-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="5f81b-116">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="5f81b-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
