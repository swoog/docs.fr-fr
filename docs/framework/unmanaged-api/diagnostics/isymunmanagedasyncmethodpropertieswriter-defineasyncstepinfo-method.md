---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo, méthode
ms.date: 03/30/2017
ms.assetid: f738a6ed-7cd9-4106-a5cd-355481e5771c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6bac541909e07aadff06006fba8c3cfcf4dc5465
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57486223"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefineasyncstepinfo-method"></a><span data-ttu-id="f4684-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="f4684-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo Method</span></span>
<span data-ttu-id="f4684-103">Définir un groupe d’async await des opérations dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="f4684-103">Define a group of async await operations in the current method.</span></span>  
  
 <span data-ttu-id="f4684-104">Chaque décalage yield correspond à l’instruction de retour d’une expression await, identifiant un rendement potentiel.</span><span class="sxs-lookup"><span data-stu-id="f4684-104">Each yield offset matches an await's return instruction, identifying a potential yield.</span></span> <span data-ttu-id="f4684-105">Chaque `breakpointMethod` / `breakpointOffset` paire nous indique où l’opération asynchrone reprendra qui pourrait être dans une méthode différente.</span><span class="sxs-lookup"><span data-stu-id="f4684-105">Each `breakpointMethod`/`breakpointOffset` pair tells us where the asynchronous operation will resume which could be in a different method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4684-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4684-106">Syntax</span></span>  
  
```idl  
HRESULT DefineAsyncStepInfo(    [in] ULONG32 count,    [in, size_is(count)] ULONG32 yieldOffsets[],    [in, size_is(count)] ULONG32 breakpointOffset[],     [in, size_is(count)] mdToken breakpointMethod[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f4684-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4684-107">Parameters</span></span>  
  
|<span data-ttu-id="f4684-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f4684-108">Parameter</span></span>|<span data-ttu-id="f4684-109">Description</span><span class="sxs-lookup"><span data-stu-id="f4684-109">Description</span></span>|  
|---------------|-----------------|  
|`count`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="f4684-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f4684-110">Return Value</span></span>  
 <span data-ttu-id="f4684-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="f4684-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4684-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f4684-112">Requirements</span></span>  
 <span data-ttu-id="f4684-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f4684-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4684-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4684-114">See also</span></span>
- [<span data-ttu-id="f4684-115">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="f4684-115">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
