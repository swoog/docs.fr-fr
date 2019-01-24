---
title: Énumération de CLRDataSourceType
ms.date: 01/16/2019
api.name:
- CLRDataSourceType Enumeration
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- CLRDataSourceType Enumeration
helpviewer.keywords:
- CLRDataSourceType Enumeration [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: c8b3f338659e2784db8deca3e1776e7926c30c32
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506082"
---
# <a name="clrdatasourcetype-enumeration"></a><span data-ttu-id="8c8ac-102">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="8c8ac-102">CLRDataSourceType Enumeration</span></span>

<span data-ttu-id="8c8ac-103">Fournit des valeurs qui sont utilisées par la structure CLRDATA_IL_ADDRESS_MAP.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-103">Provides values that are used by the CLRDATA_IL_ADDRESS_MAP structure.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="8c8ac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c8ac-104">Syntax</span></span>

```
typedef enum
{
    CLRDATA_SOURCE_TYPE_INVALID        = 0x00, // To indicate that nothing else applies
} CLRDataSourceType;
```

## <a name="members"></a><span data-ttu-id="8c8ac-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8c8ac-105">Members</span></span>

| <span data-ttu-id="8c8ac-106">Membre</span><span class="sxs-lookup"><span data-stu-id="8c8ac-106">Member</span></span>                        | <span data-ttu-id="8c8ac-107">Description</span><span class="sxs-lookup"><span data-stu-id="8c8ac-107">Description</span></span>                           |
| ----------------------------- | ------------------------------------- |
| `CLRDATA_SOURCE_TYPE_INVALID` | <span data-ttu-id="8c8ac-108">Pour indiquer que rien d’autre ne s’applique.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-108">To indicate that nothing else applies</span></span> |

## <a name="remarks"></a><span data-ttu-id="8c8ac-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8c8ac-109">Remarks</span></span>

<span data-ttu-id="8c8ac-110">Cette énumération réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-110">This enumeration lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="8c8ac-111">Pour l’utiliser, définir une énumération comme indiqué ci-dessus dans votre code.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-111">To use it, define an enumeration as defined above in your code.</span></span> <span data-ttu-id="8c8ac-112">Il s’agit également d’un alias à `CLRDATA_ENUM` comme indiqué dans [des Types de données courants](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8c8ac-112">This is also aliased to `CLRDATA_ENUM` as mentioned in [Common Data Types](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c8ac-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8c8ac-113">Requirements</span></span>

<span data-ttu-id="8c8ac-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8c8ac-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="8c8ac-115">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-115">**Header:** None</span></span>  
<span data-ttu-id="8c8ac-116">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="8c8ac-116">**Library:** None</span></span>  
<span data-ttu-id="8c8ac-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8c8ac-117">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c8ac-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c8ac-118">See also</span></span>

- [<span data-ttu-id="8c8ac-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="8c8ac-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="8c8ac-120">Énumérations de débogage</span><span class="sxs-lookup"><span data-stu-id="8c8ac-120">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
