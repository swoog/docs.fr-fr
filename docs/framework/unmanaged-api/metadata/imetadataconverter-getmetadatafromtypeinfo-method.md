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
ms.openlocfilehash: b87bc814179b35f594ec8fab812055ff0182c5c3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62044484"
---
# <a name="imetadataconvertergetmetadatafromtypeinfo-method"></a><span data-ttu-id="3cc95-102">IMetaDataConverter::GetMetaDataFromTypeInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="3cc95-102">IMetaDataConverter::GetMetaDataFromTypeInfo Method</span></span>
<span data-ttu-id="3cc95-103">Obtient un pointeur vers un [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance qui représente la signature de métadonnées de la bibliothèque de types référencée par le `ITypeInfo` instance.</span><span class="sxs-lookup"><span data-stu-id="3cc95-103">Gets a pointer to an [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance that represents the metadata signature of the type library referenced by the specified `ITypeInfo` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3cc95-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cc95-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataFromTypeInfo (  
    [in]  ITypeInfo         *pITI,  
    [out] IMetaDataImport   **ppMDI  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3cc95-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cc95-105">Parameters</span></span>  
 `pITI`  
 <span data-ttu-id="3cc95-106">[in] Un pointeur vers un `ITypeInfo` objet qui fait référence à la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="3cc95-106">[in] A pointer to an `ITypeInfo` object that refers to the type library.</span></span>  
  
 `ppMDI`  
 <span data-ttu-id="3cc95-107">[out] Un pointeur vers un emplacement qui reçoit l’adresse de la `IMetaDataImport` instance qui représente la signature de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="3cc95-107">[out] A pointer to a location that receives the address of the `IMetaDataImport` instance that represents the metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3cc95-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cc95-108">Requirements</span></span>  
 <span data-ttu-id="3cc95-109">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3cc95-109">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3cc95-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3cc95-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3cc95-111">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3cc95-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3cc95-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3cc95-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3cc95-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cc95-113">See also</span></span>

- [<span data-ttu-id="3cc95-114">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="3cc95-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="3cc95-115">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="3cc95-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
