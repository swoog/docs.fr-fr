---
title: CorThreadSafetyOptions, énumération
ms.date: 03/30/2017
api_name:
- CorThreadSafetyOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorThreadSafetyOptions
helpviewer_keywords:
- CorThreadSafetyOptions enumeration [.NET Framework metadata]
ms.assetid: dae07d9b-df51-488c-b17e-52d6e48217bd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d71d2a5b3007d4e877900443af426a9643b29125
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045225"
---
# <a name="corthreadsafetyoptions-enumeration"></a><span data-ttu-id="96fe8-102">CorThreadSafetyOptions, énumération</span><span class="sxs-lookup"><span data-stu-id="96fe8-102">CorThreadSafetyOptions Enumeration</span></span>

<span data-ttu-id="96fe8-103">Spécifie des indicateurs permettant de sélectionner des options pour la sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="96fe8-103">Specifies flags to select options for thread safety.</span></span>

## <a name="syntax"></a><span data-ttu-id="96fe8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96fe8-104">Syntax</span></span>

```cpp
typedef enum CorThreadSafetyOptions {
    MDThreadSafetyDefault       = 0x00000000,
    MDThreadSafetyOff           = 0x00000000,
    MDThreadSafetyOn            = 0x00000001,
} CorThreadSafetyOptions;
```

## <a name="members"></a><span data-ttu-id="96fe8-105">Membres</span><span class="sxs-lookup"><span data-stu-id="96fe8-105">Members</span></span>

|<span data-ttu-id="96fe8-106">Membre</span><span class="sxs-lookup"><span data-stu-id="96fe8-106">Member</span></span>|<span data-ttu-id="96fe8-107">Description</span><span class="sxs-lookup"><span data-stu-id="96fe8-107">Description</span></span>|
|------------|-----------------|
|`MDThreadSafetyDefault`|<span data-ttu-id="96fe8-108">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="96fe8-108">Default value.</span></span> <span data-ttu-id="96fe8-109">Comme pour `MDThreadSafetyOff`.</span><span class="sxs-lookup"><span data-stu-id="96fe8-109">Same as `MDThreadSafetyOff`.</span></span>|
|`MDThreadSafetyOff`|<span data-ttu-id="96fe8-110">Indique qu’un verrou de lecture/écriture ne peut pas être défini.</span><span class="sxs-lookup"><span data-stu-id="96fe8-110">Indicates that a reader/writer lock cannot be set.</span></span>|
|`MDThreadSafetyOn`|<span data-ttu-id="96fe8-111">Indique qu’un verrou en lecture/écriture peut être défini.</span><span class="sxs-lookup"><span data-stu-id="96fe8-111">Indicates that a reader/writer lock can be set.</span></span>|

## <a name="requirements"></a><span data-ttu-id="96fe8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96fe8-112">Requirements</span></span>

<span data-ttu-id="96fe8-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="96fe8-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="96fe8-114">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="96fe8-114">**Header:** CorHdr.h</span></span>

<span data-ttu-id="96fe8-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96fe8-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="96fe8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96fe8-116">See also</span></span>

- [<span data-ttu-id="96fe8-117">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="96fe8-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
