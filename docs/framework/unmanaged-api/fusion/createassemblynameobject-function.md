---
title: CreateAssemblyNameObject, fonction
ms.date: 03/30/2017
api_name:
- CreateAssemblyNameObject
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateAssemblyNameObject
helpviewer_keywords:
- CreateAssemblyNameObject function [.NET Framework fusion]
ms.assetid: 55c8b41e-fbe4-4ae0-aa29-68fbb2311691
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cd8609bedcea28c1cb8559d378b5e171f3ad568e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61669889"
---
# <a name="createassemblynameobject-function"></a><span data-ttu-id="a4fc8-102">CreateAssemblyNameObject, fonction</span><span class="sxs-lookup"><span data-stu-id="a4fc8-102">CreateAssemblyNameObject Function</span></span>
<span data-ttu-id="a4fc8-103">Obtient un pointeur d’interface vers un [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) instance qui représente l’identité unique de l’assembly avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-103">Gets an interface pointer to an [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) instance that represents the unique identity of the assembly with the specified name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a4fc8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4fc8-104">Syntax</span></span>  
  
```  
HRESULT CreateAssemblyNameObject (  
    [out] LPASSEMBLYNAME  *ppAssemblyNameObj,  
    [in]  LPCWSTR         szAssemblyName,  
    [in]  DWORD           dwFlags,  
    [in]  LPVOID          pvReserved  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="a4fc8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4fc8-105">Parameters</span></span>  
 `ppAssemblyNameObj`  
 <span data-ttu-id="a4fc8-106">[out] Retourné `IAssemblyName`.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-106">[out] The returned `IAssemblyName`.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="a4fc8-107">[in] Le nom de l’assembly pour lequel créer le nouveau `IAssemblyName` instance.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-107">[in] The name of the assembly for which to create the new `IAssemblyName` instance.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="a4fc8-108">[in] Indicateurs à passer au constructeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-108">[in] Flags to pass to the object constructor.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="a4fc8-109">[in] Réservé pour une extensibilité future.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-109">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="a4fc8-110">`pvReserved` doit être une référence null.</span><span class="sxs-lookup"><span data-stu-id="a4fc8-110">`pvReserved` must be a null reference.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a4fc8-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4fc8-111">Requirements</span></span>  
 <span data-ttu-id="a4fc8-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4fc8-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4fc8-113">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="a4fc8-113">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="a4fc8-114">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a4fc8-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a4fc8-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a4fc8-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4fc8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4fc8-116">See also</span></span>

- [<span data-ttu-id="a4fc8-117">IAssemblyName, interface</span><span class="sxs-lookup"><span data-stu-id="a4fc8-117">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)
- [<span data-ttu-id="a4fc8-118">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="a4fc8-118">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
