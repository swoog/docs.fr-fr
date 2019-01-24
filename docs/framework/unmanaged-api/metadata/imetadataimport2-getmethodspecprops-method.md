---
title: IMetaDataImport2::GetMethodSpecProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetMethodSpecProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetMethodSpecProps
helpviewer_keywords:
- GetMethodSpecProps method [.NET Framework metadata]
- IMetaDataImport2::GetMethodSpecProps method [.NET Framework metadata]
ms.assetid: 9544b711-e669-4eaf-8630-ee862e5e4489
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 69af794d5405894d24f0d7545613a0e85ca3ec6a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54574012"
---
# <a name="imetadataimport2getmethodspecprops-method"></a><span data-ttu-id="a24f5-102">IMetaDataImport2::GetMethodSpecProps, méthode</span><span class="sxs-lookup"><span data-stu-id="a24f5-102">IMetaDataImport2::GetMethodSpecProps Method</span></span>
<span data-ttu-id="a24f5-103">Obtient le jeton de signature de métadonnées de la méthode référencée par le MethodSpec spécifié.</span><span class="sxs-lookup"><span data-stu-id="a24f5-103">Gets the metadata signature of the method referenced by the specified MethodSpec token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a24f5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a24f5-104">Syntax</span></span>  
  
```  
HRESULT GetMethodSpecProps (  
   [in]  mdMethodSpec     mi,  
   [out] mdToken          *tkParent,  
   [out] PCCOR_SIGNATURE  *ppvSigBlob,   
   [out] ULONG            *pcbSigBlob  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="a24f5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a24f5-105">Parameters</span></span>  
 `mi`  
 <span data-ttu-id="a24f5-106">[in] Jeton MethodSpec qui représente l’instanciation de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a24f5-106">[in] A MethodSpec token that represents the instantiation of the method.</span></span>  
  
 `tkParent`  
 <span data-ttu-id="a24f5-107">[out] Pointeur vers le jeton MethodDef ou MethodRef qui représente la définition de méthode.</span><span class="sxs-lookup"><span data-stu-id="a24f5-107">[out] A pointer to the MethodDef or MethodRef token that represents the method definition.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="a24f5-108">[out] Pointeur vers la signature de métadonnées binaires de la méthode.</span><span class="sxs-lookup"><span data-stu-id="a24f5-108">[out] A pointer to the binary metadata signature of the method.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="a24f5-109">[out] La taille, en octets, de `ppvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="a24f5-109">[out] The size, in bytes, of `ppvSigBlob`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a24f5-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a24f5-110">Requirements</span></span>  
 <span data-ttu-id="a24f5-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a24f5-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a24f5-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a24f5-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a24f5-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a24f5-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a24f5-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a24f5-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a24f5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a24f5-115">See also</span></span>
- [<span data-ttu-id="a24f5-116">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="a24f5-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [<span data-ttu-id="a24f5-117">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="a24f5-117">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
