---
title: IDebugAutoAttach::AutoAttach, méthode
ms.date: 03/30/2017
api_name:
- IDebugAutoAttach.AutoAttach
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IDebugAutoAttach::AutoAttach
helpviewer_keywords:
- AutoAttach method [.NET Framework debugging]
- IDebugAutoAttach::AutoAttach method [.NET Framework debugging]
ms.assetid: 3cf3bd9c-7d88-4afa-a476-94cdc7609aa6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5064e66708044d82e3a097c8235b5b28a3412200
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61986490"
---
# <a name="idebugautoattachautoattach-method"></a><span data-ttu-id="65eb1-102">IDebugAutoAttach::AutoAttach, méthode</span><span class="sxs-lookup"><span data-stu-id="65eb1-102">IDebugAutoAttach::AutoAttach Method</span></span>
<span data-ttu-id="65eb1-103">Effectue automatique du débogueur appelé serveur attacher.</span><span class="sxs-lookup"><span data-stu-id="65eb1-103">Performs server-invoked debugger auto attach.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65eb1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65eb1-104">Syntax</span></span>  
  
```  
HRESULT AutoAttach  
(  
    [in]  REFGUID   guidPort,  
    [in]  DWORD     dwPid,  
    [in]  AUTOATTACH_PROGRAM_TYPE dwProgramType,  
    [in]  DWORD     dwProgramId,  
    [in]  LPCWSTR   pszSessionId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="65eb1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65eb1-105">Parameters</span></span>  
 `guidPort`  
 <span data-ttu-id="65eb1-106">[in] Toujours défini sur `GUID_NULL`.</span><span class="sxs-lookup"><span data-stu-id="65eb1-106">[in] Always set to `GUID_NULL`.</span></span>  
  
 `dwPid`  
 <span data-ttu-id="65eb1-107">[in] ID de processus, normalement récupéré avec la `GetCurrentProcessId` (fonction).</span><span class="sxs-lookup"><span data-stu-id="65eb1-107">[in] Process ID, normally retrieved with the `GetCurrentProcessId` function.</span></span>  
  
 `dwProgramType`  
 <span data-ttu-id="65eb1-108">[in] Type de programme : `AUTOATTACH_PROGRAM_WIN32`, `AUTOATTACH_PROGRAM_COMPLUS`, ou `AUTOATTACH_PROGRAM_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="65eb1-108">[in] Program type: `AUTOATTACH_PROGRAM_WIN32`, `AUTOATTACH_PROGRAM_COMPLUS`, or `AUTOATTACH_PROGRAM_UNKNOWN`.</span></span>  
  
 `dwProgramId`  
 <span data-ttu-id="65eb1-109">[in] ID de programme.</span><span class="sxs-lookup"><span data-stu-id="65eb1-109">[in] Program ID.</span></span>  
  
 `pszSessionId`  
 <span data-ttu-id="65eb1-110">[in] Chaîne passée par le verbe debug.</span><span class="sxs-lookup"><span data-stu-id="65eb1-110">[in] String passed by the debug verb.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="65eb1-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="65eb1-111">Return Value</span></span>  
 <span data-ttu-id="65eb1-112">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="65eb1-112">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65eb1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65eb1-113">Requirements</span></span>  
 <span data-ttu-id="65eb1-114">**En-tête :** DbgAutoAttach.h</span><span class="sxs-lookup"><span data-stu-id="65eb1-114">**Header:** DbgAutoAttach.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65eb1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65eb1-115">See also</span></span>

- [<span data-ttu-id="65eb1-116">IDebugAutoAttach, interface</span><span class="sxs-lookup"><span data-stu-id="65eb1-116">IDebugAutoAttach Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/idebugautoattach-interface.md)
