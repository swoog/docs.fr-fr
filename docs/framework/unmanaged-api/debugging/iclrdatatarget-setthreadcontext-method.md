---
title: ICLRDataTarget::SetThreadContext, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.SetThreadContext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::SetThreadContext
helpviewer_keywords:
- SetThreadContext method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::SetThreadContext method [.NET Framework debugging]
ms.assetid: 103c8502-81fe-40d7-9c1e-9008d8fb19e1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3f98ab65512a380ebd4dc0ecd50e36f94a6d6b5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698029"
---
# <a name="iclrdatatargetsetthreadcontext-method"></a><span data-ttu-id="b2326-102">ICLRDataTarget::SetThreadContext, méthode</span><span class="sxs-lookup"><span data-stu-id="b2326-102">ICLRDataTarget::SetThreadContext Method</span></span>
<span data-ttu-id="b2326-103">Définit le contexte actuel du thread spécifié dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="b2326-103">Sets the current context of the specified thread in the target process.</span></span> <span data-ttu-id="b2326-104">Cette méthode est appelée par les services d’accès de données common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="b2326-104">This method is called by the common language runtime (CLR) data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b2326-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2326-105">Syntax</span></span>  
  
```  
HRESULT SetThreadContext (  
    [in] ULONG32            threadID,  
    [in] ULONG32            contextSize,  
    [in, size_is(contextSize)]   
         BYTE               *context  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b2326-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2326-106">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="b2326-107">[in] L’identificateur de système d’exploitation d’un thread dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="b2326-107">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="b2326-108">[in] La taille du contexte.</span><span class="sxs-lookup"><span data-stu-id="b2326-108">[in] The size of the context.</span></span>  
  
 `context`  
 <span data-ttu-id="b2326-109">[in] Pointeur vers une mémoire tampon contenant le contexte.</span><span class="sxs-lookup"><span data-stu-id="b2326-109">[in] Pointer to a buffer containing the context.</span></span>  
  
 <span data-ttu-id="b2326-110">Les données dans le `context` tampon sera au format Win32 `CONTEXT` structure.</span><span class="sxs-lookup"><span data-stu-id="b2326-110">The data in the `context` buffer will be in the format of the Win32 `CONTEXT` structure.</span></span> <span data-ttu-id="b2326-111">Le contexte spécifie des données de Registre spécifiques au processeur, la définition de Win32 `CONTEXT` structure varie selon l’architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="b2326-111">The context specifies processor-specific register data, so the definition of the Win32 `CONTEXT` structure depends on the processor's architecture.</span></span> <span data-ttu-id="b2326-112">Consultez le fichier d’en-tête WinNT.h pour la définition de Win32 `CONTEXT` structure.</span><span class="sxs-lookup"><span data-stu-id="b2326-112">Refer to the WinNT.h header file for the definition of the Win32 `CONTEXT` structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b2326-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b2326-113">Remarks</span></span>  
 <span data-ttu-id="b2326-114">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="b2326-114">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b2326-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2326-115">Requirements</span></span>  
 <span data-ttu-id="b2326-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b2326-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b2326-117">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="b2326-117">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="b2326-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b2326-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b2326-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b2326-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2326-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2326-120">See also</span></span>

- [<span data-ttu-id="b2326-121">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="b2326-121">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
