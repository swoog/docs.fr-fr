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
ms.openlocfilehash: 0f70187ba9bd71225162e6e10184e4992b5600f5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59228846"
---
# <a name="imetadatatables2getmetadatastreaminfo-method"></a><span data-ttu-id="f4700-102">IMetaDataTables2::GetMetaDataStreamInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="f4700-102">IMetaDataTables2::GetMetaDataStreamInfo Method</span></span>
<span data-ttu-id="f4700-103">Obtient le nom, la taille et le contenu du flux de métadonnées à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4700-103">Gets the name, size, and contents of the metadata stream at the specified index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4700-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4700-104">Syntax</span></span>  
  
```  
HRESULT GetMetaDataStreamInfo (  
   [in]  ULONG        ix,  
   [out] const char   **ppchName,  
   [out] const void   **ppv,  
   [out] ULONG        *pcb  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f4700-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4700-105">Parameters</span></span>  
 `ix`  
 <span data-ttu-id="f4700-106">[in] L’index du flux de métadonnées demandées.</span><span class="sxs-lookup"><span data-stu-id="f4700-106">[in] The index of the requested metadata stream.</span></span>  
  
 `ppchName`  
 <span data-ttu-id="f4700-107">[out] Un pointeur vers le nom du flux.</span><span class="sxs-lookup"><span data-stu-id="f4700-107">[out] A pointer to the name of the stream.</span></span>  
  
 `ppv`  
 <span data-ttu-id="f4700-108">[out] Un pointeur vers le flux de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="f4700-108">[out] A pointer to the metadata stream.</span></span>  
  
 `pcb`  
 <span data-ttu-id="f4700-109">[out] La taille, en octets, de `ppv`.</span><span class="sxs-lookup"><span data-stu-id="f4700-109">[out] The size, in bytes, of `ppv`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4700-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4700-110">Requirements</span></span>  
 <span data-ttu-id="f4700-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f4700-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4700-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f4700-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f4700-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f4700-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="f4700-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f4700-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f4700-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4700-115">See also</span></span>

- [<span data-ttu-id="f4700-116">IMetaDataTables2, interface</span><span class="sxs-lookup"><span data-stu-id="f4700-116">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
- [<span data-ttu-id="f4700-117">IMetaDataTables, interface</span><span class="sxs-lookup"><span data-stu-id="f4700-117">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)
