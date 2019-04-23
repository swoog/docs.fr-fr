---
title: ICLRMetadataLocator::GetMetadata, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetadataLocator.GetMetadata
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRMetadataLocator::GetMetadata
helpviewer_keywords:
- GetMetadata method, ICLRMetadataLocator interface [.NET Framework debugging]
- ICLRMetadataLocator::GetMetadata method [.NET Framework debugging]
ms.assetid: 704a8893-ac56-43b4-90ea-715f38ccb40e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e677aefd5420f71867c1f11a2c9408c77d305c45
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59161378"
---
# <a name="iclrmetadatalocatorgetmetadata-method"></a><span data-ttu-id="d6a22-102">ICLRMetadataLocator::GetMetadata, méthode</span><span class="sxs-lookup"><span data-stu-id="d6a22-102">ICLRMetadataLocator::GetMetadata Method</span></span>
<span data-ttu-id="d6a22-103">Appelé par les services d’accès aux données du common language runtime (CLR) pour récupérer les métadonnées d’une image.</span><span class="sxs-lookup"><span data-stu-id="d6a22-103">Called by the common language runtime (CLR) data access services to retrieve the metadata of an image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6a22-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6a22-104">Syntax</span></span>  
  
```  
HRESULT GetMetadata(  
    [in]  LPCWSTR         imagePath,  
    [in]  ULONG32         imageTimestamp,  
    [in]  ULONG32         imageSize,  
    [in]  GUID*           mvid,  
    [in]  ULONG32         mdRva,  
    [in]  ULONG32         flags,  
    [in]  ULONG32         bufferSize,  
    [out, size_is(bufferSize), length_is(*dataSize)]  
          BYTE*           buffer,  
    [out] ULONG32*        dataSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d6a22-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6a22-105">Parameters</span></span>  
 `imagePath`  
 <span data-ttu-id="d6a22-106">[in] Chaîne qui spécifie le chemin d’accès du fichier image.</span><span class="sxs-lookup"><span data-stu-id="d6a22-106">[in] A string that specifies the path of the image file.</span></span>  
  
 `imageTimestamp`  
 <span data-ttu-id="d6a22-107">[in] L’horodatage du fichier image.</span><span class="sxs-lookup"><span data-stu-id="d6a22-107">[in] The time stamp of the image file.</span></span>  
  
 `imageSize`  
 <span data-ttu-id="d6a22-108">[in] La taille du fichier image.</span><span class="sxs-lookup"><span data-stu-id="d6a22-108">[in] The size of the image file.</span></span>  
  
 `mvid`  
 <span data-ttu-id="d6a22-109">[in] L’identificateur global unique de l’image.</span><span class="sxs-lookup"><span data-stu-id="d6a22-109">[in] The globally unique identifier of the image.</span></span>  
  
 `mdRva`  
 <span data-ttu-id="d6a22-110">[in] L’adresse virtuelle relative (RVA) des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d6a22-110">[in] The relative virtual address (RVA) of the metadata.</span></span> <span data-ttu-id="d6a22-111">L’adresse est par rapport à l’adresse de base d’image.</span><span class="sxs-lookup"><span data-stu-id="d6a22-111">The address is relative to the image base address.</span></span>  
  
 `flags`  
 <span data-ttu-id="d6a22-112">[in] Réservé pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d6a22-112">[in] Reserved for future use.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="d6a22-113">[in] La taille de la mémoire tampon dans lequel placer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d6a22-113">[in] The size of the buffer in which to place the metadata.</span></span>  
  
 `buffer`  
 <span data-ttu-id="d6a22-114">[out] La mémoire tampon dans lequel placer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d6a22-114">[out] The buffer in which to place the metadata.</span></span>  
  
 `dataSize`  
 <span data-ttu-id="d6a22-115">[out] La taille des métadonnées qui sont retournée.</span><span class="sxs-lookup"><span data-stu-id="d6a22-115">[out] The size of the metadata that is returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d6a22-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d6a22-116">Remarks</span></span>  
 <span data-ttu-id="d6a22-117">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="d6a22-117">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d6a22-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6a22-118">Requirements</span></span>  
 <span data-ttu-id="d6a22-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d6a22-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6a22-120">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="d6a22-120">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="d6a22-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d6a22-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d6a22-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d6a22-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6a22-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6a22-123">See also</span></span>

- [<span data-ttu-id="d6a22-124">ICLRMetadataLocator, interface</span><span class="sxs-lookup"><span data-stu-id="d6a22-124">ICLRMetadataLocator Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrmetadatalocator-interface.md)
