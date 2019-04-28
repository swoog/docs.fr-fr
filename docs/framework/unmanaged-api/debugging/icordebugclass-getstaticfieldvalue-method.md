---
title: ICorDebugClass::GetStaticFieldValue, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugClass.GetStaticFieldValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass::GetStaticFieldValue
helpviewer_keywords:
- GetStaticFieldValue method, ICorDebugClass interface [.NET Framework debugging]
- ICorDebugClass::GetStaticFieldValue method [.NET Framework debugging]
ms.assetid: 56e718b4-fabd-418b-a5b3-3cc33c745683
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6b67f5ec233679461f61715d7562b47c2a195fb8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61750849"
---
# <a name="icordebugclassgetstaticfieldvalue-method"></a><span data-ttu-id="158c2-102">ICorDebugClass::GetStaticFieldValue, méthode</span><span class="sxs-lookup"><span data-stu-id="158c2-102">ICorDebugClass::GetStaticFieldValue Method</span></span>
<span data-ttu-id="158c2-103">Obtient la valeur du champ statique spécifié.</span><span class="sxs-lookup"><span data-stu-id="158c2-103">Gets the value of the specified static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="158c2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="158c2-104">Syntax</span></span>  
  
```  
HRESULT GetStaticFieldValue (  
    [in]  mdFieldDef         fieldDef,  
    [in]  ICorDebugFrame     *pFrame,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="158c2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="158c2-105">Parameters</span></span>  
 `fieldDef`  
 <span data-ttu-id="158c2-106">[in] Un champ `Def` jeton qui fait référence au champ à récupérer.</span><span class="sxs-lookup"><span data-stu-id="158c2-106">[in] A field `Def` token that references the field to be retrieved.</span></span>  
  
 `pFrame`  
 <span data-ttu-id="158c2-107">[in] Pointeur vers un objet ICorDebugFrame qui représente l’image à utiliser pour lever l’ambiguïté entre les threads, contexte ou statiques de domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="158c2-107">[in] A pointer to an ICorDebugFrame object that represents the frame to be used to disambiguate among thread, context, or application domain statics.</span></span>  
  
 <span data-ttu-id="158c2-108">Si le champ statique est relatif à un thread, un contexte ou un domaine d’application, le frame déterminera la valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="158c2-108">If the static field is relative to a thread, a context, or an application domain, the frame will determine the proper value.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="158c2-109">[out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente la valeur du champ statique.</span><span class="sxs-lookup"><span data-stu-id="158c2-109">[out] A pointer to the address of an ICorDebugValue object that represents the value of the static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="158c2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="158c2-110">Remarks</span></span>  
 <span data-ttu-id="158c2-111">Pour des types paramétrables, la valeur d’un champ statique est relatif à l’instanciation spécifique.</span><span class="sxs-lookup"><span data-stu-id="158c2-111">For parameterized types, the value of a static field is relative to the particular instantiation.</span></span> <span data-ttu-id="158c2-112">Par conséquent, si le constructeur de classe accepte des paramètres de type <xref:System.Type>, appelez [ICorDebugType::GetStaticFieldValue](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getstaticfieldvalue-method.md) au lieu de `ICorDebugClass::GetStaticFieldValue`.</span><span class="sxs-lookup"><span data-stu-id="158c2-112">Therefore, if the class constructor takes parameters of type <xref:System.Type>, call [ICorDebugType::GetStaticFieldValue](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getstaticfieldvalue-method.md) instead of `ICorDebugClass::GetStaticFieldValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="158c2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="158c2-113">Requirements</span></span>  
 <span data-ttu-id="158c2-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="158c2-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="158c2-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="158c2-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="158c2-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="158c2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="158c2-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="158c2-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
