---
title: IXCLRDataModule::Request (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::Request Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::Request Method
helpviewer.keywords:
- IXCLRDataModule::Request Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 0226a11b142515296d976e3d645cb2475d634420
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416414"
---
# <a name="ixclrdatamodulerequest-method"></a><span data-ttu-id="8b97e-102">IXCLRDataModule::Request (méthode)</span><span class="sxs-lookup"><span data-stu-id="8b97e-102">IXCLRDataModule::Request Method</span></span>

<span data-ttu-id="8b97e-103">Demandes pour remplir la mémoire tampon spécifiée avec les données du module.</span><span class="sxs-lookup"><span data-stu-id="8b97e-103">Requests to populate the buffer given with the module's data.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="8b97e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b97e-104">Syntax</span></span>
```
HRESULT Request([in] ULONG32 reqCode,
    [in] ULONG32 inBufferSize,
    [in, size_is(inBufferSize)] BYTE* inBuffer,
    [in] ULONG32 outBufferSize,
    [out, size_is(outBufferSize)] BYTE* outBuffer);
```

### <a name="parameters"></a><span data-ttu-id="8b97e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b97e-105">Parameters</span></span>

<span data-ttu-id="8b97e-106">`reqCode` [in] Type à envoyer de demande.</span><span class="sxs-lookup"><span data-stu-id="8b97e-106">`reqCode` [in] Request type to be sent.</span></span>

<span data-ttu-id="8b97e-107">`inBufferSize` [in] taille de la mémoire tampon d’entrée à transmettre.</span><span class="sxs-lookup"><span data-stu-id="8b97e-107">`inBufferSize` [in] size of the input buffer to be passed in.</span></span>

<span data-ttu-id="8b97e-108">`inBuffer` [in, size_is(inBufferSize)] Pointeur de mémoire tampon pour les données brutes à envoyer dans la demande.</span><span class="sxs-lookup"><span data-stu-id="8b97e-108">`inBuffer` [in, size_is(inBufferSize)] Buffer pointer for the raw data to be sent in the request.</span></span>

<span data-ttu-id="8b97e-109">`outBufferSize` [in] Taille de la mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="8b97e-109">`outBufferSize` [in] Size of the output buffer.</span></span>

<span data-ttu-id="8b97e-110">`outBuffer` [out, size_is(outBufferSize)] Pointeur de mémoire tampon utilisée pour stocker la réponse de la demande.</span><span class="sxs-lookup"><span data-stu-id="8b97e-110">`outBuffer` [out, size_is(outBufferSize)] Buffer pointer to used to store the request response.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b97e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8b97e-111">Remarks</span></span>

<span data-ttu-id="8b97e-112">La méthode fournie fait partie de la `IXCLRDataModule` interface et correspond à l’emplacement 36e de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="8b97e-112">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 36th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b97e-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8b97e-113">Requirements</span></span>

<span data-ttu-id="8b97e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8b97e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="8b97e-115">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="8b97e-115">**Header:** None</span></span>   
<span data-ttu-id="8b97e-116">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="8b97e-116">**Library:** None</span></span>  
<span data-ttu-id="8b97e-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8b97e-117">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="8b97e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b97e-118">See Also</span></span>
- [<span data-ttu-id="8b97e-119">Débogage</span><span class="sxs-lookup"><span data-stu-id="8b97e-119">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="8b97e-120">Interface de IXCLRDataModule</span><span class="sxs-lookup"><span data-stu-id="8b97e-120">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
