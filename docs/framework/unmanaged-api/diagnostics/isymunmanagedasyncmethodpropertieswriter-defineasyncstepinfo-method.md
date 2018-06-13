---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo, méthode
ms.date: 03/30/2017
ms.assetid: f738a6ed-7cd9-4106-a5cd-355481e5771c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3ebd4bb1d674a27785ccbe5460a65fed764638ea
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435875"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefineasyncstepinfo-method"></a><span data-ttu-id="2f486-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="2f486-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo Method</span></span>
<span data-ttu-id="2f486-103">Définissez un groupe d’async await des opérations dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="2f486-103">Define a group of async await operations in the current method.</span></span>  
  
 <span data-ttu-id="2f486-104">Chaque décalage yield correspond à l’instruction de retour d’une expression await, identifiant un rendement potentiel.</span><span class="sxs-lookup"><span data-stu-id="2f486-104">Each yield offset matches an await's return instruction, identifying a potential yield.</span></span> <span data-ttu-id="2f486-105">Chaque `breakpointMethod` / `breakpointOffset` paire nous indique où l’opération asynchrone reprendra, (qui peuvent être dans une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="2f486-105">Each `breakpointMethod`/`breakpointOffset` pair tells us where the asynchronous operation will resume,(which could be in a different method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f486-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f486-106">Syntax</span></span>  
  
```idl  
HRESULT DefineAsyncStepInfo(    [in] ULONG32 count,    [in, size_is(count)] ULONG32 yieldOffsets[],    [in, size_is(count)] ULONG32 breakpointOffset[],     [in, size_is(count)] mdToken breakpointMethod[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2f486-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f486-107">Parameters</span></span>  
  
|<span data-ttu-id="2f486-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="2f486-108">Parameter</span></span>|<span data-ttu-id="2f486-109">Description</span><span class="sxs-lookup"><span data-stu-id="2f486-109">Description</span></span>|  
|---------------|-----------------|  
|`count`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="2f486-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2f486-110">Return Value</span></span>  
 <span data-ttu-id="2f486-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="2f486-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2f486-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2f486-112">Requirements</span></span>  
 <span data-ttu-id="2f486-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2f486-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f486-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f486-114">See Also</span></span>  
 [<span data-ttu-id="2f486-115">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="2f486-115">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
