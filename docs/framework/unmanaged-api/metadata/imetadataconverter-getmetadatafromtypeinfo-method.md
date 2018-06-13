---
title: IMetaDataConverter::GetMetaDataFromTypeInfo, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataConverter.GetMetaDataFromTypeInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter::GetMetaDataFromTypeInfo
helpviewer_keywords:
- GetMetaDataFromTypeInfo method [.NET Framework metadata]
- IMetaDataConverter::GetMetaDataFromTypeInfo method [.NET Framework metadata]
ms.assetid: d44484bb-23a3-49c3-9e46-69d0d9ab4f0f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a4bbe3bf259c6d06964f105113ecb30da4e7d8ef
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446962"
---
# <a name="imetadataconvertergetmetadatafromtypeinfo-method"></a><span data-ttu-id="9b8e3-102">IMetaDataConverter::GetMetaDataFromTypeInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="9b8e3-102">IMetaDataConverter::GetMetaDataFromTypeInfo Method</span></span>
<span data-ttu-id="9b8e3-103">Obtient un pointeur vers un [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance qui représente la signature de métadonnées de la bibliothèque de types référencée par le `ITypeInfo` instance.</span><span class="sxs-lookup"><span data-stu-id="9b8e3-103">Gets a pointer to an [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance that represents the metadata signature of the type library referenced by the specified `ITypeInfo` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b8e3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b8e3-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataFromTypeInfo (  
    [in]  ITypeInfo         *pITI,  
    [out] IMetaDataImport   **ppMDI  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9b8e3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b8e3-105">Parameters</span></span>  
 `pITI`  
 <span data-ttu-id="9b8e3-106">[in] Un pointeur vers un `ITypeInfo` objet qui fait référence à la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="9b8e3-106">[in] A pointer to an `ITypeInfo` object that refers to the type library.</span></span>  
  
 `ppMDI`  
 <span data-ttu-id="9b8e3-107">[out] Un pointeur vers un emplacement qui reçoit l’adresse de le `IMetaDataImport` instance qui représente la signature de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="9b8e3-107">[out] A pointer to a location that receives the address of the `IMetaDataImport` instance that represents the metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b8e3-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9b8e3-108">Requirements</span></span>  
 <span data-ttu-id="9b8e3-109">**Plateforme :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9b8e3-109">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9b8e3-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9b8e3-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9b8e3-111">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9b8e3-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9b8e3-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9b8e3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b8e3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b8e3-113">See Also</span></span>  
 [<span data-ttu-id="9b8e3-114">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="9b8e3-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="9b8e3-115">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="9b8e3-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
