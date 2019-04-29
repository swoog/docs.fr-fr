---
title: ICorDebugProcess4, interface
ms.date: 02/07/2019
api_name:
- ICorDebugProcess4
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess4
helpviewer_keywords:
- ICorDebugProcess4 interface [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 1bdc958f2516bcd7c2eb74312fbf478e6d49535a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61948800"
---
# <a name="icordebugprocess4-interface"></a><span data-ttu-id="9ae99-102">ICorDebugProcess4, interface</span><span class="sxs-lookup"><span data-stu-id="9ae99-102">ICorDebugProcess4 Interface</span></span>

<span data-ttu-id="9ae99-103">Prend en charge hors de contrôle de l’exécution de processus.</span><span class="sxs-lookup"><span data-stu-id="9ae99-103">Provides support for out of process execution control.</span></span>

## <a name="methods"></a><span data-ttu-id="9ae99-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9ae99-104">Methods</span></span>

| <span data-ttu-id="9ae99-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="9ae99-105">Method</span></span>                                                                 | <span data-ttu-id="9ae99-106">Description</span><span class="sxs-lookup"><span data-stu-id="9ae99-106">Description</span></span>                                                                                             |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="9ae99-107">ProcessStateChanged</span><span class="sxs-lookup"><span data-stu-id="9ae99-107">ProcessStateChanged</span></span>](icordebugprocess4-processstatechanged-method.md) | <span data-ttu-id="9ae99-108">Notifie le pipeline ICorDebug que hors du débogueur de processus se poursuit l’exécution du programme débogué.</span><span class="sxs-lookup"><span data-stu-id="9ae99-108">Notifies the ICorDebug pipeline that the out of process debugger is continuing the debugee's execution.</span></span> |

## <a name="remarks"></a><span data-ttu-id="9ae99-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9ae99-109">Remarks</span></span>

<span data-ttu-id="9ae99-110">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="9ae99-110">This interface lives inside the runtime and isn't exposed through any headers or library files.</span></span> <span data-ttu-id="9ae99-111">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `E930C679-78AF-4953-8AB7-B0AABF0F9F80` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="9ae99-111">However, it's a COM interface that derives from `IUnknown` with GUID `E930C679-78AF-4953-8AB7-B0AABF0F9F80` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae99-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ae99-112">Requirements</span></span>

<span data-ttu-id="9ae99-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9ae99-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="9ae99-114">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="9ae99-114">**Header:** None</span></span>

<span data-ttu-id="9ae99-115">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="9ae99-115">**Library:** None</span></span>

<span data-ttu-id="9ae99-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ae99-116">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="9ae99-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ae99-117">See also</span></span>

- [<span data-ttu-id="9ae99-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="9ae99-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="9ae99-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="9ae99-119">Debugging</span></span>](index.md)
