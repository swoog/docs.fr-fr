---
title: IAssemblyCacheItem::CreateStream, méthode
ms.date: 03/30/2017
api_name:
- IAssemblyCacheItem.CreateStream
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyCacheItem::CreateStream
helpviewer_keywords:
- CreateStream method [.NET Framework fusion]
- IAsssemblyCacheItem::CreateStream method [.NET Framework fusion]
ms.assetid: 697ab0f4-470c-4baa-a415-4a975c42d0d5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3a0b3242e8ae29b9d21dc50d3ea0476967e9746f
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47171970"
---
# <a name="iassemblycacheitemcreatestream-method"></a><span data-ttu-id="775d9-102">IAssemblyCacheItem::CreateStream, méthode</span><span class="sxs-lookup"><span data-stu-id="775d9-102">IAssemblyCacheItem::CreateStream Method</span></span>
<span data-ttu-id="775d9-103">Crée un flux avec le format et le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="775d9-103">Creates a stream with the specified name and format.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="775d9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="775d9-104">Syntax</span></span>  
  
```  
HRESULT CreateStream (  
    [in]  DWORD dwFlags,  
    [in]  LPCWSTR pszStreamName,  
    [in]  DWORD dwFormat,  
    [in]  DWORD dwFormatFlags,  
    [out] IStream **ppIStream,  
    [in, optional] ULARGE_INTEGER *puliMaxSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="775d9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="775d9-105">Parameters</span></span>  
 `dwFlags`  
 <span data-ttu-id="775d9-106">[in] Indicateurs définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="775d9-106">[in] Flags defined in Fusion.idl.</span></span>  
  
 `pszStreamName`  
 <span data-ttu-id="775d9-107">[in] Le nom du flux doit être créé.</span><span class="sxs-lookup"><span data-stu-id="775d9-107">[in] The name of the stream to be created.</span></span>  
  
 `dwFormat`  
 <span data-ttu-id="775d9-108">[in] Le format du fichier à être diffusé en continu.</span><span class="sxs-lookup"><span data-stu-id="775d9-108">[in] The format of the file to be streamed.</span></span>  
  
 `dwFormatFlags`  
 <span data-ttu-id="775d9-109">[in] Indicateurs spécifiques au format définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="775d9-109">[in] Format-specific flags defined in Fusion.idl.</span></span>  
  
 `ppIStream`  
 <span data-ttu-id="775d9-110">[out] Un pointeur vers l’adresse de retourné [IStream](/windows/desktop/api/objidl/nn-objidl-istream) instance.</span><span class="sxs-lookup"><span data-stu-id="775d9-110">[out] A pointer to the address of the returned [IStream](/windows/desktop/api/objidl/nn-objidl-istream) instance.</span></span>  
  
 `puliMaxSize`  
 <span data-ttu-id="775d9-111">[in, optional] La taille maximale du flux référencé par `ppIStream`.</span><span class="sxs-lookup"><span data-stu-id="775d9-111">[in, optional] The maximum size of the stream referenced by `ppIStream`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="775d9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="775d9-112">Requirements</span></span>  
 <span data-ttu-id="775d9-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="775d9-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="775d9-114">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="775d9-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="775d9-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="775d9-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="775d9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="775d9-116">See Also</span></span>  
 [<span data-ttu-id="775d9-117">IAssemblyCacheItem, interface</span><span class="sxs-lookup"><span data-stu-id="775d9-117">IAssemblyCacheItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)
