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
ms.openlocfilehash: 4d3c3c0c5634653d14577de9a1334048d75216b9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405624"
---
# <a name="icordebugclassgetstaticfieldvalue-method"></a><span data-ttu-id="628dd-102">ICorDebugClass::GetStaticFieldValue, méthode</span><span class="sxs-lookup"><span data-stu-id="628dd-102">ICorDebugClass::GetStaticFieldValue Method</span></span>
<span data-ttu-id="628dd-103">Obtient la valeur du champ statique spécifié.</span><span class="sxs-lookup"><span data-stu-id="628dd-103">Gets the value of the specified static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="628dd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="628dd-104">Syntax</span></span>  
  
```  
HRESULT GetStaticFieldValue (  
    [in]  mdFieldDef         fieldDef,  
    [in]  ICorDebugFrame     *pFrame,  
    [out] ICorDebugValue     **ppValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="628dd-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="628dd-105">Parameters</span></span>  
 `fieldDef`  
 <span data-ttu-id="628dd-106">[in] Un champ `Def` jeton qui fait référence au champ à récupérer.</span><span class="sxs-lookup"><span data-stu-id="628dd-106">[in] A field `Def` token that references the field to be retrieved.</span></span>  
  
 `pFrame`  
 <span data-ttu-id="628dd-107">[in] Pointeur vers un objet ICorDebugFrame qui représente l’image à utiliser pour distinguer les threads, de contexte ou statiques de domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="628dd-107">[in] A pointer to an ICorDebugFrame object that represents the frame to be used to disambiguate among thread, context, or application domain statics.</span></span>  
  
 <span data-ttu-id="628dd-108">Si le champ statique est relatif à un thread, un contexte ou un domaine d’application, le frame déterminera la valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="628dd-108">If the static field is relative to a thread, a context, or an application domain, the frame will determine the proper value.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="628dd-109">[out] Pointeur vers l’adresse d’un objet ICorDebugValue qui représente la valeur du champ statique.</span><span class="sxs-lookup"><span data-stu-id="628dd-109">[out] A pointer to the address of an ICorDebugValue object that represents the value of the static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="628dd-110">Notes</span><span class="sxs-lookup"><span data-stu-id="628dd-110">Remarks</span></span>  
 <span data-ttu-id="628dd-111">Pour les types paramétrables, la valeur d’un champ statique est relatif à l’instanciation particulière.</span><span class="sxs-lookup"><span data-stu-id="628dd-111">For parameterized types, the value of a static field is relative to the particular instantiation.</span></span> <span data-ttu-id="628dd-112">Par conséquent, si le constructeur de classe accepte les paramètres de type <xref:System.Type>, appelez [ICorDebugType::GetStaticFieldValue](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getstaticfieldvalue-method.md) au lieu de `ICorDebugClass::GetStaticFieldValue`.</span><span class="sxs-lookup"><span data-stu-id="628dd-112">Therefore, if the class constructor takes parameters of type <xref:System.Type>, call [ICorDebugType::GetStaticFieldValue](../../../../docs/framework/unmanaged-api/debugging/icordebugtype-getstaticfieldvalue-method.md) instead of `ICorDebugClass::GetStaticFieldValue`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="628dd-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="628dd-113">Requirements</span></span>  
 <span data-ttu-id="628dd-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="628dd-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="628dd-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="628dd-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="628dd-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="628dd-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="628dd-117">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="628dd-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
