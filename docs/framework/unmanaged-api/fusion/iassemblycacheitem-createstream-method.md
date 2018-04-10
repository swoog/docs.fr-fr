---
title: IAssemblyCacheItem::CreateStream, méthode
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: reference
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
caps.latest.revision: 7
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 726efe69f67627c48108b6b1ece9fe52f34a91c1
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="iassemblycacheitemcreatestream-method"></a><span data-ttu-id="6c65b-102">IAssemblyCacheItem::CreateStream, méthode</span><span class="sxs-lookup"><span data-stu-id="6c65b-102">IAssemblyCacheItem::CreateStream Method</span></span>
<span data-ttu-id="6c65b-103">Crée un flux de données avec le format et le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="6c65b-103">Creates a stream with the specified name and format.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c65b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c65b-104">Syntax</span></span>  
  
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
  
#### <a name="parameters"></a><span data-ttu-id="6c65b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c65b-105">Parameters</span></span>  
 `dwFlags`  
 <span data-ttu-id="6c65b-106">[in] Indicateurs définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="6c65b-106">[in] Flags defined in Fusion.idl.</span></span>  
  
 `pszStreamName`  
 <span data-ttu-id="6c65b-107">[in] Le nom du flux de données doit être créé.</span><span class="sxs-lookup"><span data-stu-id="6c65b-107">[in] The name of the stream to be created.</span></span>  
  
 `dwFormat`  
 <span data-ttu-id="6c65b-108">[in] Le format du fichier doit être diffusé en continu.</span><span class="sxs-lookup"><span data-stu-id="6c65b-108">[in] The format of the file to be streamed.</span></span>  
  
 `dwFormatFlags`  
 <span data-ttu-id="6c65b-109">[in] Indicateurs spécifiques au format définis dans Fusion.idl.</span><span class="sxs-lookup"><span data-stu-id="6c65b-109">[in] Format-specific flags defined in Fusion.idl.</span></span>  
  
 `ppIStream`  
 <span data-ttu-id="6c65b-110">[out] Un pointeur vers l’adresse de retourné [IStream](https://msdn.microsoft.com/library/aa380034.aspx) instance.</span><span class="sxs-lookup"><span data-stu-id="6c65b-110">[out] A pointer to the address of the returned [IStream](https://msdn.microsoft.com/library/aa380034.aspx) instance.</span></span>  
  
 `puliMaxSize`  
 <span data-ttu-id="6c65b-111">[in, facultatif] La taille maximale du flux référencé par `ppIStream`.</span><span class="sxs-lookup"><span data-stu-id="6c65b-111">[in, optional] The maximum size of the stream referenced by `ppIStream`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c65b-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6c65b-112">Requirements</span></span>  
 <span data-ttu-id="6c65b-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6c65b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c65b-114">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="6c65b-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="6c65b-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c65b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c65b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c65b-116">See Also</span></span>  
 [<span data-ttu-id="6c65b-117">IAssemblyCacheItem, interface</span><span class="sxs-lookup"><span data-stu-id="6c65b-117">IAssemblyCacheItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)
