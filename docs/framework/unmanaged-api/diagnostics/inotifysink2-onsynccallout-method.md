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
ms.openlocfilehash: 0a38c35f0acd47c9183c043e1c436413a309b138
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426073"
---
# <a name="inotifysink2onsynccallout-method"></a><span data-ttu-id="083e6-102">INotifySink2::OnSyncCallOut, méthode</span><span class="sxs-lookup"><span data-stu-id="083e6-102">INotifySink2::OnSyncCallOut Method</span></span>
<span data-ttu-id="083e6-103">Appelée lorsqu’un appel est sortant.</span><span class="sxs-lookup"><span data-stu-id="083e6-103">Gets invoked when a call is out.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="083e6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="083e6-104">Syntax</span></span>  
  
```  
HRESULT OnSyncCallOut  
(  
    [in]  CALL_ID  in_CallID,  
    [out, size_is(, *out_pBufferSize)] BYTE**  out_ppBuffer,  
    [out] DWORD*   out_pBufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="083e6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="083e6-105">Parameters</span></span>  
 `in_CallID`  
 <span data-ttu-id="083e6-106">[in] ID de l’appel sortant. Consultez [call_id, Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).</span><span class="sxs-lookup"><span data-stu-id="083e6-106">[in] ID of the call that is out. See [CALL_ID Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).</span></span>  
  
 `out_ppBuffer`  
 <span data-ttu-id="083e6-107">[out] Mémoire tampon des appels.</span><span class="sxs-lookup"><span data-stu-id="083e6-107">[out] Call buffer.</span></span>  
  
 `out_pBufferSize`  
 <span data-ttu-id="083e6-108">[out] Taille de la mémoire tampon de l’appel, en octets.</span><span class="sxs-lookup"><span data-stu-id="083e6-108">[out] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="083e6-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="083e6-109">Return Value</span></span>  
 <span data-ttu-id="083e6-110">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="083e6-110">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="083e6-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="083e6-111">Requirements</span></span>  
 <span data-ttu-id="083e6-112">**En-tête :** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="083e6-112">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="083e6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="083e6-113">See Also</span></span>  
 [<span data-ttu-id="083e6-114">INotifySink2, interface</span><span class="sxs-lookup"><span data-stu-id="083e6-114">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)  
 [<span data-ttu-id="083e6-115">INotifySource2, interface</span><span class="sxs-lookup"><span data-stu-id="083e6-115">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)  
 [<span data-ttu-id="083e6-116">INotifyConnection2, interface</span><span class="sxs-lookup"><span data-stu-id="083e6-116">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
