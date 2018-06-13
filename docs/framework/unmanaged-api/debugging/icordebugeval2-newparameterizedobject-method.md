---
title: ICorDebugEval2::NewParameterizedObject, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEval2.NewParameterizedObject
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval2::NewParameterizedObject
helpviewer_keywords:
- NewParameterizedObject method [.NET Framework debugging]
- ICorDebugEval2::NewParameterizedObject method [.NET Framework debugging]
ms.assetid: 3d705463-e640-4249-8036-4e8206d03cfe
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f20c24984aadd05139d1a427b75bc65438539ff1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412803"
---
# <a name="icordebugeval2newparameterizedobject-method"></a><span data-ttu-id="f1955-102">ICorDebugEval2::NewParameterizedObject, méthode</span><span class="sxs-lookup"><span data-stu-id="f1955-102">ICorDebugEval2::NewParameterizedObject Method</span></span>
<span data-ttu-id="f1955-103">Instancie un nouvel objet de type paramétré et appelle la méthode de constructeur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1955-103">Instantiates a new parameterized type object and calls the object's constructor method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1955-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1955-104">Syntax</span></span>  
  
```  
HRESULT NewParameterizedObject (  
    [in] ICorDebugFunction     *pConstructor,  
    [in] ULONG32               nTypeArgs,  
    [in, size_is(nTypeArgs)] ICorDebugType *ppTypeArgs[],  
    [in] ULONG32               nArgs,  
    [in, size_is(nArgs)] ICorDebugValue *ppArgs[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f1955-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1955-105">Parameters</span></span>  
 `pConstructor`  
 <span data-ttu-id="f1955-106">[in] Pointeur vers un objet ICorDebugFunction qui représente le constructeur de l’objet à instancier.</span><span class="sxs-lookup"><span data-stu-id="f1955-106">[in] A pointer to an ICorDebugFunction object that represents the constructor of the object to be instantiated.</span></span>  
  
 `nTypeArgs`  
 <span data-ttu-id="f1955-107">[in] Le nombre d’arguments de type passés.</span><span class="sxs-lookup"><span data-stu-id="f1955-107">[in] The number of type arguments passed.</span></span>  
  
 `ppTypeArgs`  
 <span data-ttu-id="f1955-108">[in] Tableau de pointeurs, chacun pointant vers un objet ICorDebugType qui représente un argument de type pour l’objet qui est en cours d’instanciation.</span><span class="sxs-lookup"><span data-stu-id="f1955-108">[in] An array of pointers, each of which points to an ICorDebugType object that represents a type argument for the object that is being instantiated.</span></span>  
  
 `nArgs`  
 <span data-ttu-id="f1955-109">[in] Le nombre d’arguments passés au constructeur.</span><span class="sxs-lookup"><span data-stu-id="f1955-109">[in] The number of arguments passed to the constructor.</span></span>  
  
 `ppArgs`  
 <span data-ttu-id="f1955-110">[in] Tableau de pointeurs, chacun pointant vers un objet ICorDebugValue qui représente une valeur d’argument est passée au constructeur.</span><span class="sxs-lookup"><span data-stu-id="f1955-110">[in] An array of pointers, each of which points to an ICorDebugValue object that represents an argument value that is passed to the constructor.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f1955-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f1955-111">Remarks</span></span>  
 <span data-ttu-id="f1955-112">Constructeur de l’objet peut prendre <xref:System.Type> paramètres.</span><span class="sxs-lookup"><span data-stu-id="f1955-112">The object's constructor may take <xref:System.Type> parameters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1955-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f1955-113">Requirements</span></span>  
 <span data-ttu-id="f1955-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f1955-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1955-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f1955-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f1955-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f1955-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f1955-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1955-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
