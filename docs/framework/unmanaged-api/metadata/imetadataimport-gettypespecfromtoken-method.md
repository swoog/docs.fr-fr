---
title: IMetaDataImport::GetTypeSpecFromToken, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetTypeSpecFromToken
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetTypeSpecFromToken
helpviewer_keywords:
- GetTypeSpecFromToken method [.NET Framework metadata]
- IMetaDataImport::GetTypeSpecFromToken method [.NET Framework metadata]
ms.assetid: ee518bda-3296-482e-a7b7-e9d51dd1a181
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 362cbe9ff19e74bafc73fde857d231185179efbe
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079550"
---
# <a name="imetadataimportgettypespecfromtoken-method"></a><span data-ttu-id="2404e-102">IMetaDataImport::GetTypeSpecFromToken, méthode</span><span class="sxs-lookup"><span data-stu-id="2404e-102">IMetaDataImport::GetTypeSpecFromToken Method</span></span>
<span data-ttu-id="2404e-103">Obtient la signature de métadonnées binaires de la spécification de type représentée par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="2404e-103">Gets the binary metadata signature of the type specification represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2404e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2404e-104">Syntax</span></span>  
  
```  
HRESULT GetTypeSpecFromToken (   
   [in]  mdTypeSpec            typespec,   
   [out] PCCOR_SIGNATURE       *ppvSig,   
   [out] ULONG                 *pcbSig  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2404e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2404e-105">Parameters</span></span>  
 `typespec`  
 <span data-ttu-id="2404e-106">[in] Le jeton TypeSpec associé à la signature de métadonnées demandées.</span><span class="sxs-lookup"><span data-stu-id="2404e-106">[in] The TypeSpec token associated with the requested metadata signature.</span></span>  
  
 `ppvSig`  
 <span data-ttu-id="2404e-107">[out] Pointeur vers la signature de métadonnées binaires.</span><span class="sxs-lookup"><span data-stu-id="2404e-107">[out] A pointer to the binary metadata signature.</span></span>  
  
 `pcbSig`  
 <span data-ttu-id="2404e-108">[out] La taille, en octets, de la signature de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="2404e-108">[out] The size, in bytes, of the metadata signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2404e-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2404e-109">Return Value</span></span>  
 <span data-ttu-id="2404e-110">HRESULT qui indique la réussite ou l’échec.</span><span class="sxs-lookup"><span data-stu-id="2404e-110">An HRESULT that indicates success or failure.</span></span> <span data-ttu-id="2404e-111">Échecs peuvent être testés avec la macro FAILED.</span><span class="sxs-lookup"><span data-stu-id="2404e-111">Failures can be tested with the FAILED macro.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2404e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2404e-112">Requirements</span></span>  
 <span data-ttu-id="2404e-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2404e-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2404e-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="2404e-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="2404e-115">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2404e-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="2404e-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2404e-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2404e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2404e-117">See also</span></span>

- [<span data-ttu-id="2404e-118">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="2404e-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="2404e-119">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="2404e-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
