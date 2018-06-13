---
title: ICLRDataTarget::GetMachineType, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetMachineType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetMachineType
helpviewer_keywords:
- ICLRDataTarget::GetMachineType method [.NET Framework debugging]
- GetMachineType method [.NET Framework debugging]
ms.assetid: 5f1f9c61-3e3b-48b2-b111-a4395f7623a7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c515a8184e8c01b0e292057f3f66ffef28f2c5fb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402879"
---
# <a name="iclrdatatargetgetmachinetype-method"></a><span data-ttu-id="82687-102">ICLRDataTarget::GetMachineType, méthode</span><span class="sxs-lookup"><span data-stu-id="82687-102">ICLRDataTarget::GetMachineType Method</span></span>
<span data-ttu-id="82687-103">Obtient l’identificateur pour le type de jeu d’instructions qui utilise le processus cible.</span><span class="sxs-lookup"><span data-stu-id="82687-103">Gets the identifier for the kind of instruction set that the target process is using.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82687-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82687-104">Syntax</span></span>  
  
```  
HRESULT GetMachineType (  
    [out] ULONG32     *machineType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="82687-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82687-105">Parameters</span></span>  
 `machineType`  
 <span data-ttu-id="82687-106">[out] Un pointeur vers une valeur qui indique le jeu d’instructions que le processus cible est à l’aide.</span><span class="sxs-lookup"><span data-stu-id="82687-106">[out] A pointer to a value that indicates the instruction set that the target process is using.</span></span> <span data-ttu-id="82687-107">Retourné `machineType` est une des constantes IMAGE_FILE_MACHINE qui sont définies dans le fichier d’en-tête WinNT.h.</span><span class="sxs-lookup"><span data-stu-id="82687-107">The returned `machineType` is one of the IMAGE_FILE_MACHINE constants, which are defined in the WinNT.h header file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="82687-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="82687-108">Requirements</span></span>  
 <span data-ttu-id="82687-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="82687-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82687-110">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="82687-110">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="82687-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="82687-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="82687-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="82687-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="82687-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82687-113">See Also</span></span>  
 [<span data-ttu-id="82687-114">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="82687-114">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
