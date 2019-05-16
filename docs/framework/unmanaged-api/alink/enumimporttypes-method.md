---
title: EnumImportTypes, méthode
ms.date: 03/30/2017
api_name:
- EnumImportTypes
- IALink.EnumImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EnumImportTypes
helpviewer_keywords:
- EnumImportTypes method
ms.assetid: 83a0e4e7-ec06-40cb-9b63-700b9695bb04
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0cd154ac90418dd0f6f476151686ff670c01c98c
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65632231"
---
# <a name="enumimporttypes-method"></a><span data-ttu-id="e31ec-102">EnumImportTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="e31ec-102">EnumImportTypes Method</span></span>

<span data-ttu-id="e31ec-103">Énumère chaque type dans chaque étendue.</span><span class="sxs-lookup"><span data-stu-id="e31ec-103">Enumerates each type in each scope.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31ec-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e31ec-104">Syntax</span></span>

```cpp
HRESULT EnumImportTypes(
    HALINKENUM   hEnum,
    DWORD        dwMax,
    mdTypeDef    aTypeDefs[],
    DWORD*       pdwCount
) PURE;
```

## <a name="parameters"></a><span data-ttu-id="e31ec-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e31ec-105">Parameters</span></span>

`hEnum`\
<span data-ttu-id="e31ec-106">Handle pour l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="e31ec-106">Handle for enumerator.</span></span>

`dwMax`\
<span data-ttu-id="e31ec-107">Nombre maximal de types à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e31ec-107">Maximum number of types to retrieve.</span></span>

`aTypeDefs`\
<span data-ttu-id="e31ec-108">Reçoit des jetons de type, ne pouvant excéder `dwMax`.</span><span class="sxs-lookup"><span data-stu-id="e31ec-108">Receives type tokens, not to exceed `dwMax`.</span></span>

`pdwCount`\
<span data-ttu-id="e31ec-109">Reçoit le nombre réel de type dans `aTypeDefs`.</span><span class="sxs-lookup"><span data-stu-id="e31ec-109">Receives actual number of type in `aTypeDefs`.</span></span>

## <a name="return-value"></a><span data-ttu-id="e31ec-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e31ec-110">Return Value</span></span>

<span data-ttu-id="e31ec-111">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="e31ec-111">Returns S_OK if the method succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31ec-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e31ec-112">Requirements</span></span>

<span data-ttu-id="e31ec-113">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="e31ec-113">Requires alink.h</span></span>

## <a name="see-also"></a><span data-ttu-id="e31ec-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e31ec-114">See also</span></span>

- [<span data-ttu-id="e31ec-115">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="e31ec-115">IALink Interface</span></span>](ialink-interface.md)
- [<span data-ttu-id="e31ec-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="e31ec-116">IALink2 Interface</span></span>](ialink2-interface.md)
- [<span data-ttu-id="e31ec-117">API ALink</span><span class="sxs-lookup"><span data-stu-id="e31ec-117">ALink API</span></span>](index.md)
