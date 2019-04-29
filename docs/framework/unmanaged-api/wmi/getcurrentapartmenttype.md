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
ms.openlocfilehash: 9ead1c1a91b910e7cfbb09f17ba823fc7a77ce0f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61609007"
---
# <a name="getcurrentapartmenttype-function"></a><span data-ttu-id="d9ef1-103">GetCurrentApartmentType (fonction)</span><span class="sxs-lookup"><span data-stu-id="d9ef1-103">GetCurrentApartmentType function</span></span>
<span data-ttu-id="d9ef1-104">Récupère le type de cloisonnement dans lequel l’appelant s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d9ef1-104">Retrieves the type of apartment in which the caller is executing.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="d9ef1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9ef1-105">Syntax</span></span>  
  
```  
HRESULT GetCurrentApartmentType (
   [in] int                   vFunc, 
   [in] IComThreadingInfo*    ptr, 
   [out] APTTYPE*             aptType
); 
```  

## <a name="parameters"></a><span data-ttu-id="d9ef1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9ef1-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="d9ef1-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="d9ef1-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="d9ef1-108">[in] Un pointeur vers un [IComThreadingInfo](/windows/desktop/api/objidlbase/nn-objidlbase-icomthreadinginfo) instance.</span><span class="sxs-lookup"><span data-stu-id="d9ef1-108">[in] A pointer to an [IComThreadingInfo](/windows/desktop/api/objidlbase/nn-objidlbase-icomthreadinginfo) instance.</span></span>

`aptType`  
<span data-ttu-id="d9ef1-109">[out] Un pointeur vers un [APTTYPE](/windows/desktop/api/objidlbase/ne-objidlbase-_apttype) valeur d’énumération qui indique le cloisonnement de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d9ef1-109">[out] A pointer to an [APTTYPE](/windows/desktop/api/objidlbase/ne-objidlbase-_apttype) enumeration value that indicates the caller's apartment.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9ef1-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d9ef1-110">Return value</span></span>

|<span data-ttu-id="d9ef1-111">Constante</span><span class="sxs-lookup"><span data-stu-id="d9ef1-111">Constant</span></span>  |<span data-ttu-id="d9ef1-112">Value</span><span class="sxs-lookup"><span data-stu-id="d9ef1-112">Value</span></span>  |<span data-ttu-id="d9ef1-113">Description</span><span class="sxs-lookup"><span data-stu-id="d9ef1-113">Description</span></span>  |
|---------|---------|---------|
| `S_OK` | <span data-ttu-id="d9ef1-114">0</span><span class="sxs-lookup"><span data-stu-id="d9ef1-114">0</span></span> | <span data-ttu-id="d9ef1-115">La fonction s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="d9ef1-115">The function completed successfully.</span></span> |
| `E_FAIL` | <span data-ttu-id="d9ef1-116">0x80000008</span><span class="sxs-lookup"><span data-stu-id="d9ef1-116">0x80000008</span></span> | <span data-ttu-id="d9ef1-117">L’appelant s’exécute pas dans un thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="d9ef1-117">The caller is not executing in an apartment.</span></span> |
  
## <a name="remarks"></a><span data-ttu-id="d9ef1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="d9ef1-118">Remarks</span></span>

<span data-ttu-id="d9ef1-119">Cette fonction encapsule un appel à la [IComThreadingInfo::GetCurrentApartmentType](/windows/desktop/api/objidlbase/nf-objidlbase-icomthreadinginfo-getcurrentapartmenttype) (méthode).</span><span class="sxs-lookup"><span data-stu-id="d9ef1-119">This function wraps a call to the [IComThreadingInfo::GetCurrentApartmentType](/windows/desktop/api/objidlbase/nf-objidlbase-icomthreadinginfo-getcurrentapartmenttype) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9ef1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9ef1-120">Requirements</span></span>  
 <span data-ttu-id="d9ef1-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d9ef1-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9ef1-122">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="d9ef1-122">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="d9ef1-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d9ef1-123">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9ef1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9ef1-124">See also</span></span>

- [<span data-ttu-id="d9ef1-125">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="d9ef1-125">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
