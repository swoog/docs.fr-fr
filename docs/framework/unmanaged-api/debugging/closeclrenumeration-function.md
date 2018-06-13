---
title: Fonction CloseCLREnumeration
ms.date: 03/30/2017
api_name:
- CloseCLREnumeration
api_location:
- dbgshim.dll
api_type:
- COM
f1_keywords:
- CloseCLREnumeration
helpviewer_keywords:
- debugging API [Silverlight]
- Silverlight, debugging
- CloseCLR Enumeration function
ms.assetid: 5e3c3958-80bb-43b1-a96b-dd3e6dbd9cd7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 18903bd00b0a9d09365d03c155531a25dc013189
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33406086"
---
# <a name="closeclrenumeration-function"></a><span data-ttu-id="d3163-102">Fonction CloseCLREnumeration</span><span class="sxs-lookup"><span data-stu-id="d3163-102">CloseCLREnumeration Function</span></span>
<span data-ttu-id="d3163-103">Ferme tout valide common language runtime (CLR) événements continue-startup situés dans un tableau de handles retourné par le [fonction EnumerateCLRs](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md)et libère la mémoire pour les tableaux de chemin d’accès de handles et de chaînes.</span><span class="sxs-lookup"><span data-stu-id="d3163-103">Closes any valid common language runtime (CLR) continue-startup events located in an array of handles returned by the [EnumerateCLRs function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md), and frees the memory for the handle and string path arrays.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3163-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3163-104">Syntax</span></span>  
  
```  
HRESULT CloseCLREnumeration (  
    [in]  DWORD      pHandleArray,  
    [in]  LPWSTR**   pStringArray,  
    [in]  DWORD*     dwArrayLength  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d3163-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3163-105">Parameters</span></span>  
 `pHandleArray`  
 <span data-ttu-id="d3163-106">[in] Pointeur vers le tableau de handles d’événement retourné par la [fonction EnumerateCLRs](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md).</span><span class="sxs-lookup"><span data-stu-id="d3163-106">[in] Pointer to the array of event handles returned from the [EnumerateCLRs function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md).</span></span>  
  
 `pStringArray`  
 <span data-ttu-id="d3163-107">[in] Pointeur vers le tableau de chemins d’accès de la chaîne CLR retournée à partir de la [fonction EnumerateCLRs](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md).</span><span class="sxs-lookup"><span data-stu-id="d3163-107">[in] Pointer to the array of CLR string paths returned from the [EnumerateCLRs function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md).</span></span>  
  
 `dwArrayLength`  
 <span data-ttu-id="d3163-108">[in] Valeur DWORD contenant la taille (longueur) de `pHandleArray` ou de `pStringArray` (ils sont identiques).</span><span class="sxs-lookup"><span data-stu-id="d3163-108">[in] DWORD that contains the size (length) of either `pHandleArray` or `pStringArray` (they are the same).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d3163-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d3163-109">Return Value</span></span>  
 <span data-ttu-id="d3163-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3163-110">S_OK</span></span>  
 <span data-ttu-id="d3163-111">Handles ouverts par le [fonction EnumerateCLRs](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md) sont fermés, et de la mémoire allouée pour les tableaux de handles et de chaînes est libérée.</span><span class="sxs-lookup"><span data-stu-id="d3163-111">Handles opened by the [EnumerateCLRs function](../../../../docs/framework/unmanaged-api/debugging/enumerateclrs-function.md) are closed, and memory allocated for the handle and string arrays is freed.</span></span>  
  
 <span data-ttu-id="d3163-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d3163-112">E_INVALIDARG</span></span>  
 <span data-ttu-id="d3163-113">La longueur de `pHandleArray` ne correspond pas à la longueur passée dans `dwArrayLength`.</span><span class="sxs-lookup"><span data-stu-id="d3163-113">The length of `pHandleArray` does not match the length that is passed in `dwArrayLength`.</span></span>  
  
 <span data-ttu-id="d3163-114">E_FAIL (ou autres codes de retour E_)</span><span class="sxs-lookup"><span data-stu-id="d3163-114">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="d3163-115">La fonction ne peut pas libérer la mémoire pour `pHandleArray` et `pStringArray`.</span><span class="sxs-lookup"><span data-stu-id="d3163-115">The function is unable to free the memory for `pHandleArray` and `pStringArray`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3163-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d3163-116">Requirements</span></span>  
 <span data-ttu-id="d3163-117">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d3163-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3163-118">**En-tête :** dbgshim.h</span><span class="sxs-lookup"><span data-stu-id="d3163-118">**Header:** dbgshim.h</span></span>  
  
 <span data-ttu-id="d3163-119">**Bibliothèque :** dbgshim.dll</span><span class="sxs-lookup"><span data-stu-id="d3163-119">**Library:** dbgshim.dll</span></span>  
  
 <span data-ttu-id="d3163-120">**Versions du .NET framework :** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="d3163-120">**.NET Framework Versions:** 3.5 SP1</span></span>
