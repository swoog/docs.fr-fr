---
title: ICorDebugThread2::GetConnectionID, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread2.GetConnectionID
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2::GetConnectionID
helpviewer_keywords:
- ICorDebugThread2::GetConnectionID method [.NET Framework debugging]
- GetConnectionID method [.NET Framework debugging]
ms.assetid: 9c76b587-f941-4fa1-8b86-f3494fb10c8e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7d51e21eab4ac1edc81b58171e5382ada170a57f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946334"
---
# <a name="icordebugthread2getconnectionid-method"></a><span data-ttu-id="8d524-102">ICorDebugThread2::GetConnectionID, méthode</span><span class="sxs-lookup"><span data-stu-id="8d524-102">ICorDebugThread2::GetConnectionID Method</span></span>
<span data-ttu-id="8d524-103">Obtient l’identificateur de connexion pour cet objet ICorDebugThread2.</span><span class="sxs-lookup"><span data-stu-id="8d524-103">Gets the connection identifier for this ICorDebugThread2 object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d524-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d524-104">Syntax</span></span>  
  
```  
HRESULT GetConnectionID (  
    [out] CONNID *pdwConnectionId  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8d524-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d524-105">Parameters</span></span>  
 `pdwConnectionId`  
 <span data-ttu-id="8d524-106">[out] Un `CONNID` qui représente l’identificateur de connexion.</span><span class="sxs-lookup"><span data-stu-id="8d524-106">[out] A `CONNID` that represents the connection identifier.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8d524-107">Notes</span><span class="sxs-lookup"><span data-stu-id="8d524-107">Remarks</span></span>  
 <span data-ttu-id="8d524-108">Le `GetConnectionID` méthode retourne la valeur zéro dans le `pdwConnectionId` paramètre, si ce thread ne fait pas partie d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="8d524-108">The `GetConnectionID` method returns zero in the `pdwConnectionId` parameter, if this thread is not part of a connection.</span></span>  
  
 <span data-ttu-id="8d524-109">Si ce thread est connecté à une instance de Microsoft SQL Server 2005 Analysis Services (SSAS), le `CONNID` est mappé à un identificateur de processus serveur (SPID).</span><span class="sxs-lookup"><span data-stu-id="8d524-109">If this thread is connected to an instance of Microsoft SQL Server 2005 Analysis Services (SSAS), the `CONNID` maps to a server process identifier (SPID).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8d524-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d524-110">Requirements</span></span>  
 <span data-ttu-id="8d524-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8d524-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d524-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8d524-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8d524-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8d524-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8d524-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8d524-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
