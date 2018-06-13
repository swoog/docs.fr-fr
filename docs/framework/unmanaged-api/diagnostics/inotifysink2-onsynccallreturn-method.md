---
title: INotifySink2::OnSyncCallReturn, méthode
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallReturn
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallReturn
helpviewer_keywords:
- OnSyncCallReturn method [.NET Framework debugging]
- INotifySink2::OnSyncCallReturn method [.NET Framework debugging]
ms.assetid: c1bda761-6292-4750-a14b-7d5db8f33456
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ebfa886e85cd72c4ea7d088ef345bc9968dec18f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426005"
---
# <a name="inotifysink2onsynccallreturn-method"></a><span data-ttu-id="cdf2f-102">INotifySink2::OnSyncCallReturn, méthode</span><span class="sxs-lookup"><span data-stu-id="cdf2f-102">INotifySink2::OnSyncCallReturn Method</span></span>
<span data-ttu-id="cdf2f-103">Appelée lorsqu’un appel est retourné.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-103">Gets invoked when a call returns.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cdf2f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdf2f-104">Syntax</span></span>  
  
```  
HRESULT OnSyncCallReturn  
(  
    [in]  CALL_ID   in_CallID,  
    [in, size_is(in_BufferSize)] BYTE*  in_pBuffer,  
    [in]  DWORD     in_BufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cdf2f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdf2f-105">Parameters</span></span>  
 `in_CallID`  
 <span data-ttu-id="cdf2f-106">[in] ID de l’appel retourné.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-106">[in] ID of the call being returned from.</span></span> <span data-ttu-id="cdf2f-107">Consultez [call_id, Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).</span><span class="sxs-lookup"><span data-stu-id="cdf2f-107">See [CALL_ID Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).</span></span>  
  
 `in_pBuffer`  
 <span data-ttu-id="cdf2f-108">[in] Mémoire tampon des appels.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-108">[in] Call buffer.</span></span>  
  
 `in_BufferSize`  
 <span data-ttu-id="cdf2f-109">[in] Taille de la mémoire tampon de l’appel, en octets.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-109">[in] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cdf2f-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cdf2f-110">Return Value</span></span>  
 <span data-ttu-id="cdf2f-111">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="cdf2f-111">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cdf2f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cdf2f-112">Requirements</span></span>  
 <span data-ttu-id="cdf2f-113">**En-tête :** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="cdf2f-113">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdf2f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdf2f-114">See Also</span></span>  
 [<span data-ttu-id="cdf2f-115">INotifySink2, interface</span><span class="sxs-lookup"><span data-stu-id="cdf2f-115">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)  
 [<span data-ttu-id="cdf2f-116">INotifySource2, interface</span><span class="sxs-lookup"><span data-stu-id="cdf2f-116">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)  
 [<span data-ttu-id="cdf2f-117">INotifyConnection2, interface</span><span class="sxs-lookup"><span data-stu-id="cdf2f-117">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
