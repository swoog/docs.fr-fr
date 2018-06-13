---
title: IMetaDataTables2::GetMetaDataStreamInfo, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataTables2.GetMetaDataStreamInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables2::GetMetaDataStreamInfo
helpviewer_keywords:
- GetMetaDataStreamInfo method [.NET Framework metadata]
- IMetaDataTables2::GetMetaDataStreamInfo method [.NET Framework metadata]
ms.assetid: 8b280627-cc74-4789-95da-1fefc966de05
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 756b0ff726c31bf096a1c1b70004c3ff82fe9979
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450035"
---
# <a name="imetadatatables2getmetadatastreaminfo-method"></a><span data-ttu-id="a32f2-102">IMetaDataTables2::GetMetaDataStreamInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="a32f2-102">IMetaDataTables2::GetMetaDataStreamInfo Method</span></span>
<span data-ttu-id="a32f2-103">Obtient le nom, la taille et le contenu du flux de métadonnées à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="a32f2-103">Gets the name, size, and contents of the metadata stream at the specified index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a32f2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a32f2-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataStreamInfo (  
   [in]  ULONG        ix,  
   [out] const char   **ppchName,  
   [out] const void   **ppv,  
   [out] ULONG        *pcb  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a32f2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a32f2-105">Parameters</span></span>  
 `ix`  
 <span data-ttu-id="a32f2-106">[in] Index de flux de métadonnées demandé.</span><span class="sxs-lookup"><span data-stu-id="a32f2-106">[in] The index of the requested metadata stream.</span></span>  
  
 `ppchName`  
 <span data-ttu-id="a32f2-107">[out] Pointeur vers le nom du flux de données.</span><span class="sxs-lookup"><span data-stu-id="a32f2-107">[out] A pointer to the name of the stream.</span></span>  
  
 `ppv`  
 <span data-ttu-id="a32f2-108">[out] Un pointeur vers le flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a32f2-108">[out] A pointer to the metadata stream.</span></span>  
  
 `pcb`  
 <span data-ttu-id="a32f2-109">[out] La taille, en octets, de `ppv`.</span><span class="sxs-lookup"><span data-stu-id="a32f2-109">[out] The size, in bytes, of `ppv`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a32f2-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a32f2-110">Requirements</span></span>  
 <span data-ttu-id="a32f2-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a32f2-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a32f2-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a32f2-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a32f2-113">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a32f2-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a32f2-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a32f2-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a32f2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a32f2-115">See Also</span></span>  
 [<span data-ttu-id="a32f2-116">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="a32f2-116">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)  
 [<span data-ttu-id="a32f2-117">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="a32f2-117">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
