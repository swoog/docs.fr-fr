---
title: ICLRDataTarget::Request, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.Request
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::Request
helpviewer_keywords:
- ICLRDataTarget::Request method [.NET Framework debugging]
- Request method [.NET Framework debugging]
ms.assetid: 4723bd1c-eddb-4ed2-897a-010024a47e01
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e9005dd8fde0d7258bd1dd48b561e4925e87733b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59102689"
---
# <a name="iclrdatatargetrequest-method"></a><span data-ttu-id="0bfd0-102">ICLRDataTarget::Request, méthode</span><span class="sxs-lookup"><span data-stu-id="0bfd0-102">ICLRDataTarget::Request Method</span></span>
<span data-ttu-id="0bfd0-103">Appelé par les services d’accès aux données du common language runtime (CLR) pour demander une opération, tel que défini par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-103">Called by the common language runtime (CLR) data access services to request an operation, as defined by the implementation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0bfd0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bfd0-104">Syntax</span></span>  
  
```  
HRESULT Request (  
    [in] ULONG32            reqCode,  
    [in] ULONG32            inBufferSize,  
    [in, size_is(inBufferSize)]   
        BYTE                *inBuffer,  
    [in] ULONG32            outBufferSize,  
    [out, size_is(outBufferSize)]   
        BYTE                *outBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0bfd0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bfd0-105">Parameters</span></span>  
 `reqCode`  
 <span data-ttu-id="0bfd0-106">[in] Défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-106">[in] User-defined.</span></span>  
  
 `inBufferSize`  
 <span data-ttu-id="0bfd0-107">[in] La taille de la mémoire tampon d’entrée, qui est utilisé pour la demande entrante.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-107">[in] The size of the input buffer, which is used for the incoming request.</span></span>  
  
 `inBuffer`  
 <span data-ttu-id="0bfd0-108">[in] Une mémoire tampon contenant la demande.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-108">[in] A buffer containing the request.</span></span>  
  
 `outBufferSize`  
 <span data-ttu-id="0bfd0-109">[in] La taille de la mémoire tampon de sortie, qui est utilisé pour la réponse.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-109">[in] The size of the output buffer, which is used for the response.</span></span>  
  
 `outBuffer`  
 <span data-ttu-id="0bfd0-110">[out] Une mémoire tampon contenant la réponse.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-110">[out] A Buffer containing the response.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0bfd0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0bfd0-111">Remarks</span></span>  
 <span data-ttu-id="0bfd0-112">Le `Request` méthode facilite l’ajout d’opérations personnalisées non spécifiées.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-112">The `Request` method facilitates the addition of unspecified custom operations.</span></span> <span data-ttu-id="0bfd0-113">Autrement dit, cette méthode fournit une extensibilité sans nécessiter une révision de la définition d’interface.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-113">That is, this method provides extensibility without requiring revision of the interface definition.</span></span>  
  
 <span data-ttu-id="0bfd0-114">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="0bfd0-114">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0bfd0-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bfd0-115">Requirements</span></span>  
 <span data-ttu-id="0bfd0-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0bfd0-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0bfd0-117">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="0bfd0-117">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="0bfd0-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0bfd0-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0bfd0-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0bfd0-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0bfd0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bfd0-120">See also</span></span>

- [<span data-ttu-id="0bfd0-121">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="0bfd0-121">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
