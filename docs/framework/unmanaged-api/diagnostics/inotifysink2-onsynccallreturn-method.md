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
ms.openlocfilehash: 0adc6ec1db3f12d1850bb6ff9a01d5b6cc5f90c7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940346"
---
# <a name="inotifysink2onsynccallreturn-method"></a><span data-ttu-id="efd53-102">INotifySink2::OnSyncCallReturn, méthode</span><span class="sxs-lookup"><span data-stu-id="efd53-102">INotifySink2::OnSyncCallReturn Method</span></span>
<span data-ttu-id="efd53-103">Appelée lorsqu’un appel est retourné.</span><span class="sxs-lookup"><span data-stu-id="efd53-103">Gets invoked when a call returns.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="efd53-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efd53-104">Syntax</span></span>  
  
```  
HRESULT OnSyncCallReturn  
(  
    [in]  CALL_ID   in_CallID,  
    [in, size_is(in_BufferSize)] BYTE*  in_pBuffer,  
    [in]  DWORD     in_BufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="efd53-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efd53-105">Parameters</span></span>  
 `in_CallID`  
 <span data-ttu-id="efd53-106">[in] ID de l’appel retourné.</span><span class="sxs-lookup"><span data-stu-id="efd53-106">[in] ID of the call being returned from.</span></span> <span data-ttu-id="efd53-107">Consultez [call_id, Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).</span><span class="sxs-lookup"><span data-stu-id="efd53-107">See [CALL_ID Structure](../../../../docs/framework/unmanaged-api/diagnostics/call-id-structure.md).</span></span>  
  
 `in_pBuffer`  
 <span data-ttu-id="efd53-108">[in] Mémoire tampon d’appel.</span><span class="sxs-lookup"><span data-stu-id="efd53-108">[in] Call buffer.</span></span>  
  
 `in_BufferSize`  
 <span data-ttu-id="efd53-109">[in] Taille de la mémoire tampon de l’appel, en octets.</span><span class="sxs-lookup"><span data-stu-id="efd53-109">[in] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="efd53-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="efd53-110">Return Value</span></span>  
 <span data-ttu-id="efd53-111">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="efd53-111">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="efd53-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efd53-112">Requirements</span></span>  
 <span data-ttu-id="efd53-113">**En-tête :** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="efd53-113">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efd53-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efd53-114">See also</span></span>

- [<span data-ttu-id="efd53-115">INotifySink2, interface</span><span class="sxs-lookup"><span data-stu-id="efd53-115">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)
- [<span data-ttu-id="efd53-116">INotifySource2, interface</span><span class="sxs-lookup"><span data-stu-id="efd53-116">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)
- [<span data-ttu-id="efd53-117">INotifyConnection2, interface</span><span class="sxs-lookup"><span data-stu-id="efd53-117">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
