---
title: ICLRDataTarget::GetImageBase, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetImageBase
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetImageBase
helpviewer_keywords:
- ICLRDataTarget::GetImageBase method [.NET Framework debugging]
- GetImageBase method [.NET Framework debugging]
ms.assetid: 091c5f32-c160-49e3-a75f-4692e084c8e4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e823911280f52e16c745c9c77fe17b49bd35dc0b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59129829"
---
# <a name="iclrdatatargetgetimagebase-method"></a><span data-ttu-id="f9af8-102">ICLRDataTarget::GetImageBase, méthode</span><span class="sxs-lookup"><span data-stu-id="f9af8-102">ICLRDataTarget::GetImageBase Method</span></span>
<span data-ttu-id="f9af8-103">Obtient l’adresse mémoire de base de l’image spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f9af8-103">Gets the base memory address of the specified image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f9af8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9af8-104">Syntax</span></span>  
  
```  
HRESULT GetImageBase (  
    [in, string] LPCWSTR    imagePath,  
    [out] CLRDATA_ADDRESS   *baseAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f9af8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9af8-105">Parameters</span></span>  
 `imagePath`  
 <span data-ttu-id="f9af8-106">[in] Le nom de fichier de l’image, y compris son chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f9af8-106">[in] The file name of the image, including its path.</span></span>  
  
 `baseAddress`  
 <span data-ttu-id="f9af8-107">[out] Pointeur vers un CLRDATA_ADDRESS qui stocke l’adresse de base de l’image.</span><span class="sxs-lookup"><span data-stu-id="f9af8-107">[out] A pointer to a CLRDATA_ADDRESS that stores the base address of the image.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f9af8-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f9af8-108">Remarks</span></span>  
 <span data-ttu-id="f9af8-109">Le nom du fichier image peut ou ne peut pas avoir un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="f9af8-109">The image file name may or may not have a path.</span></span> <span data-ttu-id="f9af8-110">Si un chemin d’accès est spécifié, le filtrage s’effectue sur le chemin d’accès complet ; Sinon, la correspondance s’effectue uniquement sur le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="f9af8-110">If a path is specified, matching is done on the whole path; otherwise, matching is done only on the file name.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f9af8-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9af8-111">Requirements</span></span>  
 <span data-ttu-id="f9af8-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f9af8-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f9af8-113">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="f9af8-113">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="f9af8-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f9af8-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="f9af8-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f9af8-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f9af8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9af8-116">See also</span></span>

- [<span data-ttu-id="f9af8-117">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="f9af8-117">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
