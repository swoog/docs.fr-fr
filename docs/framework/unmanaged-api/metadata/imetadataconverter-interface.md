---
title: IMetaDataConverter, interface
ms.date: 03/30/2017
api_name:
- IMetaDataConverter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataConverter
helpviewer_keywords:
- IMetaDataConverter interface [.NET Framework metadata]
ms.assetid: 9caea662-0167-4267-b14a-2fa42c3be4ea
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fc1f813cac237642fdaab653cd47552ab7472ab0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54732924"
---
# <a name="imetadataconverter-interface"></a><span data-ttu-id="6f32c-102">IMetaDataConverter, interface</span><span class="sxs-lookup"><span data-stu-id="6f32c-102">IMetaDataConverter Interface</span></span>
<span data-ttu-id="6f32c-103">Fournit des méthodes pour mapper des bibliothèques de types à leurs signatures de métadonnées et effectuer la conversion entre les deux.</span><span class="sxs-lookup"><span data-stu-id="6f32c-103">Provides methods to map type libraries to their metadata signatures, and to convert from one to the other.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6f32c-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f32c-104">Methods</span></span>  
  
|<span data-ttu-id="6f32c-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="6f32c-105">Method</span></span>|<span data-ttu-id="6f32c-106">Description</span><span class="sxs-lookup"><span data-stu-id="6f32c-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6f32c-107">GetMetaDataFromTypeInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="6f32c-107">GetMetaDataFromTypeInfo Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-getmetadatafromtypeinfo-method.md)|<span data-ttu-id="6f32c-108">Obtient un pointeur vers un [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance qui représente la signature de métadonnées pour la bibliothèque de types référencée par le `ITypeInfo` instance.</span><span class="sxs-lookup"><span data-stu-id="6f32c-108">Gets a pointer to an [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md) instance that represents the metadata signature for the type library referenced by the specified `ITypeInfo` instance.</span></span>|  
|[<span data-ttu-id="6f32c-109">GetMetaDataFromTypeLib, méthode</span><span class="sxs-lookup"><span data-stu-id="6f32c-109">GetMetaDataFromTypeLib Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-getmetadatafromtypelib-method.md)|<span data-ttu-id="6f32c-110">Obtient un pointeur vers un `IMetaDataImport` instance qui représente la signature de métadonnées pour la bibliothèque de types représentée par le `ITypeLib` instance.</span><span class="sxs-lookup"><span data-stu-id="6f32c-110">Gets a pointer to an `IMetaDataImport` instance that represents the metadata signature for the type library represented by the specified `ITypeLib` instance.</span></span>|  
|[<span data-ttu-id="6f32c-111">GetTypeLibFromMetaData, méthode</span><span class="sxs-lookup"><span data-stu-id="6f32c-111">GetTypeLibFromMetaData Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataconverter-gettypelibfrommetadata-method.md)|<span data-ttu-id="6f32c-112">Obtient un pointeur vers un `ITypeLib` instance qui représente la bibliothèque de types qui contient les noms de module et de bibliothèque spécifiés.</span><span class="sxs-lookup"><span data-stu-id="6f32c-112">Gets a pointer to an `ITypeLib` instance that represents the type library that has the specified module and library names.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6f32c-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6f32c-113">Requirements</span></span>  
 <span data-ttu-id="6f32c-114">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6f32c-114">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6f32c-115">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="6f32c-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6f32c-116">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6f32c-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6f32c-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f32c-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f32c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f32c-118">See also</span></span>
- [<span data-ttu-id="6f32c-119">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="6f32c-119">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [<span data-ttu-id="6f32c-120">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="6f32c-120">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
