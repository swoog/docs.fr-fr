---
title: IMetaDataConverter::GetTypeLibFromMetaData, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataConverter.GetTypeLibFromMetaData
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter::GetTypeLibFromMetaData
helpviewer_keywords:
- GetTypeLibFromMetaData method [.NET Framework metadata]
- IMetaDataConverter::GetTypeLibFromMetaData method [.NET Framework metadata]
ms.assetid: 90eab7b3-1fae-4af4-8bce-f7bc0e188a99
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c0943971dc4858e2dce4d977f6f906b26f8ad51e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62044380"
---
# <a name="imetadataconvertergettypelibfrommetadata-method"></a><span data-ttu-id="c2b41-102">IMetaDataConverter::GetTypeLibFromMetaData, méthode</span><span class="sxs-lookup"><span data-stu-id="c2b41-102">IMetaDataConverter::GetTypeLibFromMetaData Method</span></span>
<span data-ttu-id="c2b41-103">Obtient un pointeur vers un `ITypeLib` instance qui représente la bibliothèque de types qui contient les noms de module et de bibliothèque spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c2b41-103">Gets a pointer to an `ITypeLib` instance that represents the type library that has the specified library and module names.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2b41-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2b41-104">Syntax</span></span>  
  
```  
HRESULT GetTypeLibFromMetaData (  
    [in]  BSTR     strModule,   
    [in]  BSTR     strTlbName,   
    [out] ITypeLib **ppITL  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c2b41-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2b41-105">Parameters</span></span>  
 `strModule`  
 <span data-ttu-id="c2b41-106">[in] Le nom du module de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="c2b41-106">[in] The name of the type library's module.</span></span>  
  
 `strTlbName`  
 <span data-ttu-id="c2b41-107">[in] Le nom de la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="c2b41-107">[in] The name of the type library.</span></span>  
  
 `ppITL`  
 <span data-ttu-id="c2b41-108">[out] Un pointeur vers un emplacement qui reçoit l’adresse de la `ITypeLib` instance qui représente la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="c2b41-108">[out] A pointer to a location that receives the address of the `ITypeLib` instance that represents the type library.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c2b41-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2b41-109">Requirements</span></span>  
 <span data-ttu-id="c2b41-110">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c2b41-110">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2b41-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c2b41-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c2b41-112">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c2b41-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c2b41-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2b41-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2b41-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2b41-114">See also</span></span>

- [<span data-ttu-id="c2b41-115">IMetaDataConverter, interface</span><span class="sxs-lookup"><span data-stu-id="c2b41-115">IMetaDataConverter Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-interface.md)
