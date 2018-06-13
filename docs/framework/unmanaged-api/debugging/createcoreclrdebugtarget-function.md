---
title: Fonction CreateCoreClrDebugTarget
ms.date: 03/30/2017
api_name:
- CreateCorClrDebugTarget
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- CreateCoreClrDebugTarget
helpviewer_keywords:
- remote debugging API [Silverlight]
- Silverlight, remote debugging
- CreateCoreClrDebugTarget function
ms.assetid: 1cf4ca8e-d9bb-4633-9adf-5e24315bf87a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a957eb6907b55fe948d696a6a25076c3950f7381
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402973"
---
# <a name="createcoreclrdebugtarget-function"></a><span data-ttu-id="d8d41-102">Fonction CreateCoreClrDebugTarget</span><span class="sxs-lookup"><span data-stu-id="d8d41-102">CreateCoreClrDebugTarget Function</span></span>
<span data-ttu-id="d8d41-103">Crée une connexion à un proxy de débogueur qui s’exécute sur un ordinateur distant et retourne un [ICoreClrDebugTarget](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md) objet qui peut être utilisé pour interroger les processus en cours d’exécution et les runtimes chargés sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="d8d41-103">Creates a connection to a debugger proxy that is running on a remote machine, and returns an [ICoreClrDebugTarget](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md) object that can be used to query running processes and loaded runtimes on the remote machine.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8d41-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8d41-104">Syntax</span></span>  
  
```  
HRESULT CreateCoreClrDebugTarget (  
       [in]  DWORD    dwAddress,   
       [out] ICoreClrDebugTarget**     ppTarget  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d8d41-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8d41-105">Parameters</span></span>  
 `dwAddress`  
 <span data-ttu-id="d8d41-106">[in] Adresse IPv4 d'un ordinateur cible distant.</span><span class="sxs-lookup"><span data-stu-id="d8d41-106">[in] IPv4 address of a remote target machine.</span></span>  
  
 `ppTarget`  
 <span data-ttu-id="d8d41-107">[out] Pointeur vers un pointeur vers un [ICoreClrDebugTarget](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md) objet qui sera créé.</span><span class="sxs-lookup"><span data-stu-id="d8d41-107">[out] Pointer to a pointer to an [ICoreClrDebugTarget](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md) object that will be created.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d8d41-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d8d41-108">Return Value</span></span>  
 <span data-ttu-id="d8d41-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8d41-109">S_OK</span></span>  
 <span data-ttu-id="d8d41-110">Le nombre de CLR dans le processus a été correctement déterminé, et les tableaux de handles et de chemin d'accès correspondants ont été correctement remplis.</span><span class="sxs-lookup"><span data-stu-id="d8d41-110">The number of CLRs in the process was successfully determined, and the corresponding handle and path arrays were properly filled.</span></span>  
  
 <span data-ttu-id="d8d41-111">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d8d41-111">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="d8d41-112">Impossible d'allouer suffisamment de mémoire pour `ppTarget`.</span><span class="sxs-lookup"><span data-stu-id="d8d41-112">Unable to allocate enough memory for `ppTarget`.</span></span>  
  
 <span data-ttu-id="d8d41-113">E_FAIL (ou autres codes de retour E_)</span><span class="sxs-lookup"><span data-stu-id="d8d41-113">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="d8d41-114">Autres échecs.</span><span class="sxs-lookup"><span data-stu-id="d8d41-114">Other failures.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8d41-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8d41-115">Requirements</span></span>  
 <span data-ttu-id="d8d41-116">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d8d41-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8d41-117">**En-tête :** CoreClrRemoteDebuggingInterfaces.h</span><span class="sxs-lookup"><span data-stu-id="d8d41-117">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="d8d41-118">**Bibliothèque :** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="d8d41-118">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="d8d41-119">**Versions du .NET framework :** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="d8d41-119">**.NET Framework Versions:** 3.5 SP1</span></span>
