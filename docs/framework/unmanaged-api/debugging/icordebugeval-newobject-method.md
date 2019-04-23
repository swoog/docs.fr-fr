---
title: ICorDebugEval::NewObject, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval.NewObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::NewObject
helpviewer_keywords:
- NewObject method [.NET Framework debugging]
- ICorDebugEval::NewObject method [.NET Framework debugging]
ms.assetid: ce3025e8-defa-4c5e-8298-f49d71fa5736
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9c2d6a66eca080b480b508afea36c33b3e0aeec0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59178228"
---
# <a name="icordebugevalnewobject-method"></a><span data-ttu-id="0a00d-102">ICorDebugEval::NewObject, méthode</span><span class="sxs-lookup"><span data-stu-id="0a00d-102">ICorDebugEval::NewObject Method</span></span>
<span data-ttu-id="0a00d-103">Alloue une nouvelle instance d’objet et appelle la méthode de constructeur spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a00d-103">Allocates a new object instance and calls the specified constructor method.</span></span>  
  
 <span data-ttu-id="0a00d-104">Cette méthode est obsolète dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="0a00d-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="0a00d-105">Utilisez [ICorDebugEval2::NewParameterizedObject](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobject-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="0a00d-105">Use [ICorDebugEval2::NewParameterizedObject](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobject-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a00d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a00d-106">Syntax</span></span>  
  
```  
HRESULT NewObject (  
    [in] ICorDebugFunction  *pConstructor,  
    [in] ULONG32            nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0a00d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a00d-107">Parameters</span></span>  
 `pConstructor`  
 <span data-ttu-id="0a00d-108">[in] Le constructeur à appeler.</span><span class="sxs-lookup"><span data-stu-id="0a00d-108">[in] The constructor to be called.</span></span>  
  
 `nArgs`  
 <span data-ttu-id="0a00d-109">[in] Taille du tableau `ppArgs`.</span><span class="sxs-lookup"><span data-stu-id="0a00d-109">[in] The size of the `ppArgs` array.</span></span>  
  
 `ppArgs`  
 <span data-ttu-id="0a00d-110">[in] Tableau d’objets ICorDebugValue, chacun d’eux représente un argument à passer au constructeur.</span><span class="sxs-lookup"><span data-stu-id="0a00d-110">[in] An array of ICorDebugValue objects, each of which represents an argument to be passed to the constructor.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a00d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a00d-111">Requirements</span></span>  
 <span data-ttu-id="0a00d-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a00d-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a00d-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0a00d-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0a00d-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0a00d-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0a00d-115">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="0a00d-115">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a00d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a00d-116">See also</span></span>

- [<span data-ttu-id="0a00d-117">NewParameterizedObject, méthode</span><span class="sxs-lookup"><span data-stu-id="0a00d-117">NewParameterizedObject Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugeval2-newparameterizedobject-method.md)
