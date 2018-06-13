---
title: GetCurrentApartmentType (fonction) (référence des API non managées)
description: La fonction GetCurrentApartmentType récupère le type de cloisonnement dans lequel l’appelant s’exécute.
ms.date: 11/06/2017
api_name:
- GetCurrentApartmentType
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetCurrentApartmentType
helpviewer_keywords:
- GetCurrentApartmentType function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ca7b5fa5bf6d845d542d3e80c0571e59f3d4c1e0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33461722"
---
# <a name="getcurrentapartmenttype-function"></a><span data-ttu-id="dbafa-103">GetCurrentApartmentType (fonction)</span><span class="sxs-lookup"><span data-stu-id="dbafa-103">GetCurrentApartmentType function</span></span>
<span data-ttu-id="dbafa-104">Récupère le type de cloisonnement dans lequel l’appelant s’exécute.</span><span class="sxs-lookup"><span data-stu-id="dbafa-104">Retrieves the type of apartment in which the caller is executing.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="dbafa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbafa-105">Syntax</span></span>  
  
```  
HRESULT GetCurrentApartmentType (
   [in] int                   vFunc, 
   [in] IComThreadingInfo*    ptr, 
   [out] APTTYPE*             aptType
); 
```  

## <a name="parameters"></a><span data-ttu-id="dbafa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbafa-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="dbafa-107">[in] Ce paramètre est inutilisé.</span><span class="sxs-lookup"><span data-stu-id="dbafa-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="dbafa-108">[in] Un pointeur vers un [IComThreadingInfo](https://msdn.microsoft.com/library/windows/desktop/ms694502(v=vs.85).aspx) instance.</span><span class="sxs-lookup"><span data-stu-id="dbafa-108">[in] A pointer to an [IComThreadingInfo](https://msdn.microsoft.com/library/windows/desktop/ms694502(v=vs.85).aspx) instance.</span></span>

`aptType`  
<span data-ttu-id="dbafa-109">[out] Un pointeur vers un [APTTYPE](https://msdn.microsoft.com/library/windows/desktop/ms693793(v=vs.85).aspx) valeur d’énumération qui indique le cloisonnement de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="dbafa-109">[out] A pointer to an [APTTYPE](https://msdn.microsoft.com/library/windows/desktop/ms693793(v=vs.85).aspx) enumeration value that indicates the caller's apartment.</span></span>

## <a name="return-value"></a><span data-ttu-id="dbafa-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dbafa-110">Return value</span></span>


|<span data-ttu-id="dbafa-111">Constante</span><span class="sxs-lookup"><span data-stu-id="dbafa-111">Constant</span></span>  |<span data-ttu-id="dbafa-112">Value</span><span class="sxs-lookup"><span data-stu-id="dbafa-112">Value</span></span>  |<span data-ttu-id="dbafa-113">Description</span><span class="sxs-lookup"><span data-stu-id="dbafa-113">Description</span></span>  |
|---------|---------|---------|
| `S_OK` | <span data-ttu-id="dbafa-114">0</span><span class="sxs-lookup"><span data-stu-id="dbafa-114">0</span></span> | <span data-ttu-id="dbafa-115">La fonction s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="dbafa-115">The function completed successfully.</span></span> |
| `E_FAIL` | <span data-ttu-id="dbafa-116">0x80000008</span><span class="sxs-lookup"><span data-stu-id="dbafa-116">0x80000008</span></span> | <span data-ttu-id="dbafa-117">L’appelant ne s’exécute pas dans un thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="dbafa-117">The caller is not executing in an apartment.</span></span> |
  
## <a name="remarks"></a><span data-ttu-id="dbafa-118">Notes</span><span class="sxs-lookup"><span data-stu-id="dbafa-118">Remarks</span></span>

<span data-ttu-id="dbafa-119">Cette fonction encapsule un appel à la [IComThreadingInfo::GetCurrentApartmentType](https://msdn.microsoft.com/library/windows/desktop/ms683752(v=vs.85).aspx) (méthode).</span><span class="sxs-lookup"><span data-stu-id="dbafa-119">This function wraps a call to the [IComThreadingInfo::GetCurrentApartmentType](https://msdn.microsoft.com/library/windows/desktop/ms683752(v=vs.85).aspx) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbafa-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dbafa-120">Requirements</span></span>  
 <span data-ttu-id="dbafa-121">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dbafa-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dbafa-122">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="dbafa-122">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="dbafa-123">**Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="dbafa-123">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbafa-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbafa-124">See also</span></span>  
[<span data-ttu-id="dbafa-125">WMI et les compteurs de Performance (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="dbafa-125">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
