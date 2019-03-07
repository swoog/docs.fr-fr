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
ms.openlocfilehash: 16ccc56579a1ebe45ada61a9565cc8ade335333d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57469676"
---
# <a name="idebugautoattachautoattach-method"></a><span data-ttu-id="2117a-102">IDebugAutoAttach::AutoAttach, méthode</span><span class="sxs-lookup"><span data-stu-id="2117a-102">IDebugAutoAttach::AutoAttach Method</span></span>
<span data-ttu-id="2117a-103">Effectue automatique du débogueur appelé serveur attacher.</span><span class="sxs-lookup"><span data-stu-id="2117a-103">Performs server-invoked debugger auto attach.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2117a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2117a-104">Syntax</span></span>  
  
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
  
## <a name="parameters"></a><span data-ttu-id="2117a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2117a-105">Parameters</span></span>  
 `guidPort`  
 <span data-ttu-id="2117a-106">[in] Toujours défini sur `GUID_NULL`.</span><span class="sxs-lookup"><span data-stu-id="2117a-106">[in] Always set to `GUID_NULL`.</span></span>  
  
 `dwPid`  
 <span data-ttu-id="2117a-107">[in] ID de processus, normalement récupéré avec la `GetCurrentProcessId` (fonction).</span><span class="sxs-lookup"><span data-stu-id="2117a-107">[in] Process ID, normally retrieved with the `GetCurrentProcessId` function.</span></span>  
  
 `dwProgramType`  
 <span data-ttu-id="2117a-108">[in] Type de programme : `AUTOATTACH_PROGRAM_WIN32`, `AUTOATTACH_PROGRAM_COMPLUS`, ou `AUTOATTACH_PROGRAM_UNKNOWN`.</span><span class="sxs-lookup"><span data-stu-id="2117a-108">[in] Program type: `AUTOATTACH_PROGRAM_WIN32`, `AUTOATTACH_PROGRAM_COMPLUS`, or `AUTOATTACH_PROGRAM_UNKNOWN`.</span></span>  
  
 `dwProgramId`  
 <span data-ttu-id="2117a-109">[in] ID de programme.</span><span class="sxs-lookup"><span data-stu-id="2117a-109">[in] Program ID.</span></span>  
  
 `pszSessionId`  
 <span data-ttu-id="2117a-110">[in] Chaîne passée par le verbe debug.</span><span class="sxs-lookup"><span data-stu-id="2117a-110">[in] String passed by the debug verb.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2117a-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2117a-111">Return Value</span></span>  
 <span data-ttu-id="2117a-112">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="2117a-112">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2117a-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2117a-113">Requirements</span></span>  
 <span data-ttu-id="2117a-114">**En-tête :** DbgAutoAttach.h</span><span class="sxs-lookup"><span data-stu-id="2117a-114">**Header:** DbgAutoAttach.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2117a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2117a-115">See also</span></span>
- [<span data-ttu-id="2117a-116">IDebugAutoAttach, interface</span><span class="sxs-lookup"><span data-stu-id="2117a-116">IDebugAutoAttach Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/idebugautoattach-interface.md)
