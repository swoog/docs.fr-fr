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
ms.openlocfilehash: c35212e7d261a5b385823fdaa345f6fbd638571c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079342"
---
# <a name="imetadataimport2getmethodspecprops-method"></a><span data-ttu-id="ddbd7-102">IMetaDataImport2::GetMethodSpecProps, méthode</span><span class="sxs-lookup"><span data-stu-id="ddbd7-102">IMetaDataImport2::GetMethodSpecProps Method</span></span>
<span data-ttu-id="ddbd7-103">Obtient le jeton de signature de métadonnées de la méthode référencée par le MethodSpec spécifié.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-103">Gets the metadata signature of the method referenced by the specified MethodSpec token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ddbd7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddbd7-104">Syntax</span></span>  
  
```  
HRESULT GetMethodSpecProps (  
   [in]  mdMethodSpec     mi,  
   [out] mdToken          *tkParent,  
   [out] PCCOR_SIGNATURE  *ppvSigBlob,   
   [out] ULONG            *pcbSigBlob  
);   
```  
  
## <a name="parameters"></a><span data-ttu-id="ddbd7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddbd7-105">Parameters</span></span>  
 `mi`  
 <span data-ttu-id="ddbd7-106">[in] Jeton MethodSpec qui représente l’instanciation de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-106">[in] A MethodSpec token that represents the instantiation of the method.</span></span>  
  
 `tkParent`  
 <span data-ttu-id="ddbd7-107">[out] Pointeur vers le jeton MethodDef ou MethodRef qui représente la définition de méthode.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-107">[out] A pointer to the MethodDef or MethodRef token that represents the method definition.</span></span>  
  
 `ppvSigBlob`  
 <span data-ttu-id="ddbd7-108">[out] Pointeur vers la signature de métadonnées binaires de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-108">[out] A pointer to the binary metadata signature of the method.</span></span>  
  
 `pcbSigBlob`  
 <span data-ttu-id="ddbd7-109">[out] La taille, en octets, de `ppvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="ddbd7-109">[out] The size, in bytes, of `ppvSigBlob`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ddbd7-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ddbd7-110">Requirements</span></span>  
 <span data-ttu-id="ddbd7-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ddbd7-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ddbd7-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ddbd7-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ddbd7-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ddbd7-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="ddbd7-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ddbd7-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ddbd7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddbd7-115">See also</span></span>

- [<span data-ttu-id="ddbd7-116">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="ddbd7-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [<span data-ttu-id="ddbd7-117">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="ddbd7-117">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
