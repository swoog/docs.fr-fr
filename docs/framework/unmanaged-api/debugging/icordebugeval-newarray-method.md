---
title: ICorDebugEval::NewArray, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.NewArray
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::NewArray
helpviewer_keywords:
- NewArray method [.NET Framework debugging]
- ICorDebugEval::NewArray method [.NET Framework debugging]
ms.assetid: cc79a67d-5368-434d-a943-209db90491b9
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d1abe307e3b9fa607912f98e456a11176eb17c56
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61934756"
---
# <a name="icordebugevalnewarray-method"></a><span data-ttu-id="6373a-102">ICorDebugEval::NewArray, méthode</span><span class="sxs-lookup"><span data-stu-id="6373a-102">ICorDebugEval::NewArray Method</span></span>
<span data-ttu-id="6373a-103">Alloue un nouveau tableau du type d’élément spécifié et des dimensions.</span><span class="sxs-lookup"><span data-stu-id="6373a-103">Allocates a new array of the specified element type and dimensions.</span></span>  
  
 <span data-ttu-id="6373a-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="6373a-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="6373a-105">Utilisez [ICorDebugEval2::NewParameterizedArray](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedarray-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="6373a-105">Use [ICorDebugEval2::NewParameterizedArray](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedarray-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6373a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6373a-106">Syntax</span></span>  
  
```  
HRESULT NewArray (  
    [in] CorElementType     elementType,  
    [in] ICorDebugClass     *pElementClass,  
    [in] ULONG32            rank,  
    [in, size_is(rank)] ULONG32 dims[],  
    [in, size_is(rank)] ULONG32 lowBounds[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6373a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6373a-107">Parameters</span></span>  
 `elementType`  
 <span data-ttu-id="6373a-108">[in] Une valeur de l’énumération CorElementType qui spécifie le type d’élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="6373a-108">[in] A value of the CorElementType enumeration that specifies the element type of the array.</span></span>  
  
 `pElementClass`  
 <span data-ttu-id="6373a-109">[in] Pointeur vers un objet ICorDebugClass qui spécifie la classe de l’élément.</span><span class="sxs-lookup"><span data-stu-id="6373a-109">[in] A pointer to a ICorDebugClass object that specifies the class of the element.</span></span> <span data-ttu-id="6373a-110">Cette valeur peut être null si le type d’élément est un type primitif.</span><span class="sxs-lookup"><span data-stu-id="6373a-110">This value may be null if the element type is a primitive type.</span></span>  
  
 `rank`  
 <span data-ttu-id="6373a-111">[in] Le nombre de dimensions du tableau.</span><span class="sxs-lookup"><span data-stu-id="6373a-111">[in] The number of dimensions of the array.</span></span> <span data-ttu-id="6373a-112">Dans le .NET Framework 2.0, cette valeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="6373a-112">In the .NET Framework 2.0, this value must be 1.</span></span>  
  
 `dims`  
 <span data-ttu-id="6373a-113">[in] La taille, en octets, de chaque dimension du tableau.</span><span class="sxs-lookup"><span data-stu-id="6373a-113">[in] The size, in bytes, of each dimension of the array.</span></span>  
  
 `lowBounds`  
 <span data-ttu-id="6373a-114">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="6373a-114">[in] Optional.</span></span> <span data-ttu-id="6373a-115">La limite inférieure de chaque dimension du tableau.</span><span class="sxs-lookup"><span data-stu-id="6373a-115">The lower bound of each dimension of the array.</span></span> <span data-ttu-id="6373a-116">Si cette valeur est omise, une limite inférieure de zéro est prise en compte pour chaque dimension.</span><span class="sxs-lookup"><span data-stu-id="6373a-116">If this value is omitted, a lower bound of zero is assumed for each dimension.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6373a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6373a-117">Remarks</span></span>  
 <span data-ttu-id="6373a-118">Le tableau est toujours créé dans le domaine d’application dans lequel le thread est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="6373a-118">The array is always created in the application domain in which the thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6373a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6373a-119">Requirements</span></span>  
 <span data-ttu-id="6373a-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6373a-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6373a-121">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6373a-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6373a-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6373a-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6373a-123">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="6373a-123">**.NET Framework Versions:** 1.1, 1.0</span></span>
