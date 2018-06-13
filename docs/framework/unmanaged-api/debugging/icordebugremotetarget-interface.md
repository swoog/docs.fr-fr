---
title: ICorDebugRemoteTarget, interface
ms.date: 03/30/2017
api_name:
- ICorDebugRemoteTarget
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemoteTarget
helpviewer_keywords:
- ICorDebugRemoteTarget interface [.NET Framework debugging]
ms.assetid: bd9936a6-cc24-4869-8761-0988664464e6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7a595438c53a88fcfb06960c8b7cb6ec8949cfa2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418429"
---
# <a name="icordebugremotetarget-interface"></a><span data-ttu-id="6a7c1-102">ICorDebugRemoteTarget, interface</span><span class="sxs-lookup"><span data-stu-id="6a7c1-102">ICorDebugRemoteTarget Interface</span></span>
<span data-ttu-id="6a7c1-103">Fournit des méthodes qui permettent aux développeurs de déboguer les applications Silverlight dans l’environnement du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="6a7c1-103">Provides methods that enable developers to debug Silverlight-based applications in the common language runtime (CLR) environment.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a7c1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a7c1-104">Syntax</span></span>  
  
```  
interface ICorDebugRemoteTarget  : IUnknown  
{  
    HRESULT GetHostName (  
        [in]  ULONG32                    cchHostName,  
        [out] ULONG32*                   pcchHostName,  
        [out, size_is(cchHostName),  
              length_is(*pcchHostName)]  
                  WCHAR szHostName[]  
        );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6a7c1-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6a7c1-105">Methods</span></span>  
  
|<span data-ttu-id="6a7c1-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="6a7c1-106">Method</span></span>|<span data-ttu-id="6a7c1-107">Description</span><span class="sxs-lookup"><span data-stu-id="6a7c1-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6a7c1-108">ICorDebugRemoteTarget::GetHostName, méthode</span><span class="sxs-lookup"><span data-stu-id="6a7c1-108">ICorDebugRemoteTarget::GetHostName Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-gethostname-method.md)|<span data-ttu-id="6a7c1-109">Retourne le nom d’hôte ou l’adresse IP d’un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="6a7c1-109">Returns the host name or the IP address of a remote machine.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6a7c1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6a7c1-110">Remarks</span></span>  
 <span data-ttu-id="6a7c1-111">Débogage en mode mixte (code managé et natif) n’est pas pris en charge sur Windows 95, Windows 98 ou Windows Millennium Edition ou sur les plateformes non-x86 (par exemple, ia64 et AMD64).</span><span class="sxs-lookup"><span data-stu-id="6a7c1-111">Mixed-mode (that is, managed and native code) debugging is not supported on Windows 95, Windows 98, or Windows ME, or on non-x86 platforms (such as IA-64 and AMD64).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a7c1-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6a7c1-112">Requirements</span></span>  
 <span data-ttu-id="6a7c1-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6a7c1-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a7c1-114">**En-tête :** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="6a7c1-114">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="6a7c1-115">**Bibliothèque :** : CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6a7c1-115">**Library:** : CorGuids.lib</span></span>  
  
 <span data-ttu-id="6a7c1-116">**Versions du .NET framework :** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="6a7c1-116">**.NET Framework Versions:** 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a7c1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a7c1-117">See Also</span></span>  
 [<span data-ttu-id="6a7c1-118">ICorDebugRemote, interface</span><span class="sxs-lookup"><span data-stu-id="6a7c1-118">ICorDebugRemote Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugremote-interface.md)  
 [<span data-ttu-id="6a7c1-119">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="6a7c1-119">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)  
 [<span data-ttu-id="6a7c1-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="6a7c1-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
