---
title: INotifySink2::OnSyncCallOut, méthode
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallOut
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallOut
helpviewer_keywords:
- INotifySink2::OnSyncCallOut method [.NET Framework debugging]
- OnSyncCallOut method [.NET Framework debugging]
ms.assetid: 97f15656-8677-4079-8553-a1d8603355d6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4cf36b9e09f5e9eeb28930a6adc48426927a60e7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59145689"
---
# <a name="inotifysink2onsynccallout-method"></a><span data-ttu-id="6efbc-102">INotifySink2::OnSyncCallOut, méthode</span><span class="sxs-lookup"><span data-stu-id="6efbc-102">INotifySink2::OnSyncCallOut Method</span></span>
<span data-ttu-id="6efbc-103">Appelée lorsque l’appel est sortant.</span><span class="sxs-lookup"><span data-stu-id="6efbc-103">Gets invoked when a call is out.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6efbc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6efbc-104">Syntax</span></span>  
  
```  
HRESULT OnSyncCallOut  
(  
    [in]  CALL_ID  in_CallID,  
    [out, size_is(, *out_pBufferSize)] BYTE**  out_ppBuffer,  
    [out] DWORD*   out_pBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6efbc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6efbc-105">Parameters</span></span>  
 `in_CallID`  
 <span data-ttu-id="6efbc-106">[in] ID de l’appel sortant. Consultez [call_id, Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).</span><span class="sxs-lookup"><span data-stu-id="6efbc-106">[in] ID of the call that is out. See [CALL_ID Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).</span></span>  
  
 `out_ppBuffer`  
 <span data-ttu-id="6efbc-107">[out] Mémoire tampon d’appel.</span><span class="sxs-lookup"><span data-stu-id="6efbc-107">[out] Call buffer.</span></span>  
  
 `out_pBufferSize`  
 <span data-ttu-id="6efbc-108">[out] Taille de la mémoire tampon de l’appel, en octets.</span><span class="sxs-lookup"><span data-stu-id="6efbc-108">[out] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6efbc-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6efbc-109">Return Value</span></span>  
 <span data-ttu-id="6efbc-110">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="6efbc-110">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6efbc-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6efbc-111">Requirements</span></span>  
 <span data-ttu-id="6efbc-112">**En-tête :** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="6efbc-112">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6efbc-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6efbc-113">See also</span></span>

- [<span data-ttu-id="6efbc-114">INotifySink2, interface</span><span class="sxs-lookup"><span data-stu-id="6efbc-114">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)
- [<span data-ttu-id="6efbc-115">INotifySource2, interface</span><span class="sxs-lookup"><span data-stu-id="6efbc-115">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)
- [<span data-ttu-id="6efbc-116">INotifyConnection2, interface</span><span class="sxs-lookup"><span data-stu-id="6efbc-116">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
