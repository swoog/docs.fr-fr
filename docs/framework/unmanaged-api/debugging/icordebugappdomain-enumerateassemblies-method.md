---
title: ICorDebugAppDomain::EnumerateAssemblies, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.EnumerateAssemblies
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::EnumerateAssemblies
helpviewer_keywords:
- ICorDebugAppDomain::EnumerateAssemblies method [.NET Framework debugging]
- EnumerateAssemblies method [.NET Framework debugging]
ms.assetid: 7add64f9-19a8-46a9-be62-905d5e7d1bd8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6ce95daaee3c74ac57b107ab8bcb23d41e42cabb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61989535"
---
# <a name="icordebugappdomainenumerateassemblies-method"></a><span data-ttu-id="00e72-102">ICorDebugAppDomain::EnumerateAssemblies, méthode</span><span class="sxs-lookup"><span data-stu-id="00e72-102">ICorDebugAppDomain::EnumerateAssemblies Method</span></span>
<span data-ttu-id="00e72-103">Obtient un énumérateur pour les assemblys dans le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="00e72-103">Gets an enumerator for the assemblies in the application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00e72-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00e72-104">Syntax</span></span>  
  
```  
HRESULT EnumerateAssemblies (  
    [out] ICorDebugAssemblyEnum  **ppAssemblies  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="00e72-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00e72-105">Parameters</span></span>  
 `ppAssemblies`  
 <span data-ttu-id="00e72-106">[out] Pointeur vers l’adresse d’un objet ICorDebugAssemblyEnum qui est l’énumérateur pour les assemblys dans le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="00e72-106">[out] A pointer to the address of an ICorDebugAssemblyEnum object that is the enumerator for the assemblies in the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00e72-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00e72-107">Requirements</span></span>  
 <span data-ttu-id="00e72-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="00e72-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00e72-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="00e72-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="00e72-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="00e72-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="00e72-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00e72-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
