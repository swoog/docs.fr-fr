---
title: ISOSDacInterface::GetMethodDescData (méthode)
ms.date: 01/16/2019
api.name:
- ISOSDacInterface::GetMethodDescData Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescData Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescData Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: e56f837c4d3362ec6e71030e4fb475df42b9fba4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54639946"
---
# <a name="isosdacinterfacegetmethoddescdata-method"></a><span data-ttu-id="bbca1-102">ISOSDacInterface::GetMethodDescData (méthode)</span><span class="sxs-lookup"><span data-stu-id="bbca1-102">ISOSDacInterface::GetMethodDescData Method</span></span>

<span data-ttu-id="bbca1-103">Obtient les données de la donnée [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bbca1-103">Gets the data for the given [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="bbca1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbca1-104">Syntax</span></span>

```
HRESULT GetMethodDescData(
    CLRDATA_ADDRESS            methodDesc,
    CLRDATA_ADDRESS            ip,
    void                       *data,
    ULONG                      cRevertedRejitVersions,
    void                      *rgRevertedRejitData,
    void                      *pcNeededRevertedRejitData
);
```

### <a name="parameters"></a><span data-ttu-id="bbca1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbca1-105">Parameters</span></span>

<span data-ttu-id="bbca1-106">`methodDesc` [in] L’adresse de la MethodDesc.</span><span class="sxs-lookup"><span data-stu-id="bbca1-106">`methodDesc` [in] The address of the MethodDesc.</span></span>

<span data-ttu-id="bbca1-107">`ip` [in] L’adresse IP de la méthode.</span><span class="sxs-lookup"><span data-stu-id="bbca1-107">`ip` [in] The IP address of the method.</span></span>

<span data-ttu-id="bbca1-108">`data` [out] Les données associées à la MethodDesc tel que retourné par l’API internes.</span><span class="sxs-lookup"><span data-stu-id="bbca1-108">`data` [out] The data associated with the MethodDesc as returned from the internal APIs.</span></span> <span data-ttu-id="bbca1-109">La structure doit au moins 168 octets.</span><span class="sxs-lookup"><span data-stu-id="bbca1-109">The structure needs at least 168 bytes.</span></span>

<span data-ttu-id="bbca1-110">`cRevertedRejitVersions` [out] Le nombre de versions de rejit rétablie.</span><span class="sxs-lookup"><span data-stu-id="bbca1-110">`cRevertedRejitVersions` [out] The number of reverted rejit versions.</span></span>

<span data-ttu-id="bbca1-111">`rgRevertedRejitData` [out] Les données associées aux versions rejit rétabli tel que retourné par l’API internes.</span><span class="sxs-lookup"><span data-stu-id="bbca1-111">`rgRevertedRejitData` [out] The data associated with the reverted rejit versions as returned from the internal APIs.</span></span> <span data-ttu-id="bbca1-112">La structure doit au moins 24 octets.</span><span class="sxs-lookup"><span data-stu-id="bbca1-112">The structure needs at least 24 bytes.</span></span>

<span data-ttu-id="bbca1-113">`pcNeededRevertedRejitData` [out] Le nombre d’octets requis pour stocker les données associées avec les versions ReJit rétablies.</span><span class="sxs-lookup"><span data-stu-id="bbca1-113">`pcNeededRevertedRejitData` [out] The number of bytes required to store the data associated with the reverted ReJit versions.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbca1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bbca1-114">Remarks</span></span>

<span data-ttu-id="bbca1-115">La méthode fournie fait partie de la `ISOSDacInterface` interface et correspond à l’emplacement de la table de la méthode virtuelle de 20.</span><span class="sxs-lookup"><span data-stu-id="bbca1-115">The provided method is part of the `ISOSDacInterface` interface and corresponds to the 20th slot of the virtual method table.</span></span> <span data-ttu-id="bbca1-116">Également le `CLRDATA_ADDRESS` sont des entiers non signés 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bbca1-116">Also the `CLRDATA_ADDRESS` are 64-bit unsigned integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbca1-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bbca1-117">Requirements</span></span>

<span data-ttu-id="bbca1-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bbca1-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="bbca1-119">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="bbca1-119">**Header:** None</span></span>  
<span data-ttu-id="bbca1-120">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="bbca1-120">**Library:** None</span></span>  
<span data-ttu-id="bbca1-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="bbca1-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="bbca1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbca1-122">See also</span></span>

- [<span data-ttu-id="bbca1-123">Débogage</span><span class="sxs-lookup"><span data-stu-id="bbca1-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="bbca1-124">Interface de ISOSDacInterface</span><span class="sxs-lookup"><span data-stu-id="bbca1-124">ISOSDacInterface Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-interface.md)
