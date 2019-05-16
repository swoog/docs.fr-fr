---
title: ICorDebugProcess4::ProcessStateChanged (méthode)
ms.date: 02/07/2019
api_name:
- ICorDebugProcess4::ProcessStateChanged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess4::ProcessStateChanged
helpviewer_keywords:
- ICorDebugProcess4::ProcessStateChanged method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 5e3a6714489e2051a09b5855ab9f911ef2f57450
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632286"
---
# <a name="icordebugprocess4processstatechanged-method"></a><span data-ttu-id="5f868-102">ICorDebugProcess4::ProcessStateChanged (méthode)</span><span class="sxs-lookup"><span data-stu-id="5f868-102">ICorDebugProcess4::ProcessStateChanged Method</span></span>

<span data-ttu-id="5f868-103">Notifie le pipeline ICorDebug que hors du débogueur de processus se poursuit l’exécution du programme débogué.</span><span class="sxs-lookup"><span data-stu-id="5f868-103">Notifies the ICorDebug pipeline that the out of process debugger is continuing the debugee's execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f868-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f868-104">Syntax</span></span>

```
HRESULT ProcessStateChanged(
    [in] CorDebugStateChange change
);
```

## <a name="parameters"></a><span data-ttu-id="5f868-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f868-105">Parameters</span></span>

 `eChange`\
<span data-ttu-id="5f868-106">[in] Un membre de la [cordebugstatechange, énumération](cordebugstatechange-enumeration.md) décrivant une modification dans l’état d’exécution du processus.</span><span class="sxs-lookup"><span data-stu-id="5f868-106">[in] A member of the [CorDebugStateChange enumeration](cordebugstatechange-enumeration.md) describing a change in the process's execution state.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f868-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5f868-107">Remarks</span></span>

<span data-ttu-id="5f868-108">La méthode fournie fait partie de la `ICorDebugProcess4` interface et correspond à l’emplacement de quatrième de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="5f868-108">The provided method is part of the `ICorDebugProcess4` interface and corresponds to the fourth slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f868-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f868-109">Requirements</span></span>

 <span data-ttu-id="5f868-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5f868-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

 <span data-ttu-id="5f868-111">**En-tête :** None</span><span class="sxs-lookup"><span data-stu-id="5f868-111">**Header:** None</span></span>

 <span data-ttu-id="5f868-112">**Bibliothèque :** None</span><span class="sxs-lookup"><span data-stu-id="5f868-112">**Library:** None</span></span>
 
 <span data-ttu-id="5f868-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5f868-113">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="5f868-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f868-114">See also</span></span>

- [<span data-ttu-id="5f868-115">ICorDebugProcess4 Interface</span><span class="sxs-lookup"><span data-stu-id="5f868-115">ICorDebugProcess4 Interface</span></span>](icordebugprocess4-interface.md)
- [<span data-ttu-id="5f868-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="5f868-116">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="5f868-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="5f868-117">Debugging</span></span>](index.md)
