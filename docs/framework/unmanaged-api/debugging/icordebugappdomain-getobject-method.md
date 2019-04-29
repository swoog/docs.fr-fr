---
title: ICorDebugAppDomain::GetObject, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetObject
api_location:
- corguids.lib
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetObject
helpviewer_keywords:
- ICorDebugAppDomain::GetObject method [.NET Framework debugging]
- GetObject method, ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: 78232e6f-ae18-4cfa-a6cd-e79471cf9d76
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0ca9792df69f859e20f1d9e40754d1cec138945d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785110"
---
# <a name="icordebugappdomaingetobject-method"></a><span data-ttu-id="6a703-102">ICorDebugAppDomain::GetObject, méthode</span><span class="sxs-lookup"><span data-stu-id="6a703-102">ICorDebugAppDomain::GetObject Method</span></span>
<span data-ttu-id="6a703-103">Obtient un pointeur d’interface vers le domaine d’application du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="6a703-103">Gets an interface pointer to the common language runtime (CLR) application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a703-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a703-104">Syntax</span></span>  
  
```  
HRESULT GetObject (  
    [out] ICorDebugValue   **ppObject  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6a703-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a703-105">Parameters</span></span>  
 `ppObject`  
 <span data-ttu-id="6a703-106">[out] Pointeur vers l’adresse d’un objet d’interface ICorDebugValue qui représente le domaine d’application CLR.</span><span class="sxs-lookup"><span data-stu-id="6a703-106">[out] A pointer to the address of an ICorDebugValue interface object that represents the CLR application domain.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6a703-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6a703-107">Return Value</span></span>  
 <span data-ttu-id="6a703-108">Si un géré <xref:System.AppDomain?displayProperty=nameWithType> objet n’a pas été construit pour ce domaine d’application, la méthode retourne `S_FALSE` et place `NULL` dans `*ppObject`.</span><span class="sxs-lookup"><span data-stu-id="6a703-108">If a managed <xref:System.AppDomain?displayProperty=nameWithType> object hasn't been constructed for this application domain, the method returns `S_FALSE` and places `NULL` in `*ppObject`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6a703-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6a703-109">Remarks</span></span>  
 <span data-ttu-id="6a703-110">Chaque domaine d’application dans un processus peut avoir un géré <xref:System.AppDomain?displayProperty=nameWithType> objet dans le runtime qui le représente.</span><span class="sxs-lookup"><span data-stu-id="6a703-110">Each application domain in a process may have a managed <xref:System.AppDomain?displayProperty=nameWithType> object in the runtime that represents it.</span></span> <span data-ttu-id="6a703-111">Cette fonction obtient un objet d’interface ICorDebugValue qui correspond à cet gérés <xref:System.AppDomain?displayProperty=nameWithType> objet.</span><span class="sxs-lookup"><span data-stu-id="6a703-111">This function gets an ICorDebugValue interface object that corresponds to this managed <xref:System.AppDomain?displayProperty=nameWithType> object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a703-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a703-112">Requirements</span></span>  
 <span data-ttu-id="6a703-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6a703-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a703-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6a703-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6a703-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6a703-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6a703-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a703-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>
