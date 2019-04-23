---
title: ICorDebugEval::NewObjectNoConstructor, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.NewObjectNoConstructor
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::NewObjectNoConstructor
helpviewer_keywords:
- NewObjectNoConstructor method [.NET Framework debugging]
- ICorDebugEval::NewObjectNoConstructor method [.NET Framework debugging]
ms.assetid: 80d509ca-b5e3-4c46-9c14-800db73d9bf7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6846b866fd47674ca6b5fd187b580fd28e080fd0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59162304"
---
# <a name="icordebugevalnewobjectnoconstructor-method"></a><span data-ttu-id="78875-102">ICorDebugEval::NewObjectNoConstructor, méthode</span><span class="sxs-lookup"><span data-stu-id="78875-102">ICorDebugEval::NewObjectNoConstructor Method</span></span>
<span data-ttu-id="78875-103">Alloue une nouvelle instance d’objet du type spécifié, sans tenter d’appeler une méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="78875-103">Allocates a new object instance of the specified type, without attempting to call a constructor method.</span></span>  
  
 <span data-ttu-id="78875-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="78875-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="78875-105">Utilisez [ICorDebugEval2::NewParameterizedObjectNoConstructor](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobjectnoconstructor-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="78875-105">Use [ICorDebugEval2::NewParameterizedObjectNoConstructor](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobjectnoconstructor-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="78875-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78875-106">Syntax</span></span>  
  
```  
HRESULT NewObjectNoConstructor (  
    [in] ICorDebugClass     *pClass  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="78875-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78875-107">Parameters</span></span>  
 `pClass`  
 <span data-ttu-id="78875-108">[in] Pointeur vers un objet ICorDebugClass qui représente le type d’objet à instancier.</span><span class="sxs-lookup"><span data-stu-id="78875-108">[in] Pointer to an ICorDebugClass object that represents the type of object to be instantiated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="78875-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78875-109">Requirements</span></span>  
 <span data-ttu-id="78875-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="78875-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="78875-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="78875-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="78875-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="78875-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="78875-113">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="78875-113">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="78875-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78875-114">See also</span></span>

- [<span data-ttu-id="78875-115">NewParameterizedObjectNoConstructor, méthode</span><span class="sxs-lookup"><span data-stu-id="78875-115">NewParameterizedObjectNoConstructor Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobjectnoconstructor-method.md)
