---
title: GetDemultiplexedStub (fonction) (référence des API non managées)
description: La fonction GetDemultiplexedStub crée un récepteur de redirecteur d’objet pour aider un client lors de la réception des appels asynchrones de la gestion de Windows.
ms.date: 11/06/2017
api_name:
- GetDemultiplexedStub
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetDemultiplexedStub
helpviewer_keywords:
- GetDemultiplexedStub function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4311a77c9159428bf7beacc99d4479acb28b91b6
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44135807"
---
# <a name="getdemultiplexedstub-function"></a><span data-ttu-id="caab0-103">GetDemultiplexedStub (fonction)</span><span class="sxs-lookup"><span data-stu-id="caab0-103">GetDemultiplexedStub function</span></span>
<span data-ttu-id="caab0-104">Crée un récepteur de redirecteur d’objet pour aider un client lors de la réception des appels asynchrones WMI.</span><span class="sxs-lookup"><span data-stu-id="caab0-104">Creates an object forwarder sink to assist a client in receiving asynchronous calls from Windows Management.</span></span>
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="caab0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="caab0-105">Syntax</span></span>  
  
```  
HRESULT GetDemultiplexedStub (
   [in] IUnknown*    pObject, 
   [in] boolean      isLocal, 
   [out] IUnknown**  ppObject
); 
```  

## <a name="parameters"></a><span data-ttu-id="caab0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caab0-106">Parameters</span></span>

`pObject`  
<span data-ttu-id="caab0-107">[in] Un pointeur vers l’implémentation d’in-process du client de [IWbemObjectSink](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectsink).</span><span class="sxs-lookup"><span data-stu-id="caab0-107">[in] A pointer to the client's in-process implementation of [IWbemObjectSink](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectsink).</span></span>

`isLocal`  
<span data-ttu-id="caab0-108">[in] Un indicateur qui indique si l’événement est local (`true`) ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="caab0-108">[in] A flag that indicates whether the event is local (`true`); otherwise, `false`.</span></span>

`ppObject`  
<span data-ttu-id="caab0-109">[out] Un récepteur de redirecteur d’objet pour aider un client lors de la réception des appels asynchrones de la gestion de Windows.</span><span class="sxs-lookup"><span data-stu-id="caab0-109">[out] A object forwarder sink to assist a client in receiving asynchronous calls from Windows Management.</span></span>

## <a name="return-value"></a><span data-ttu-id="caab0-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="caab0-110">Return value</span></span>

<span data-ttu-id="caab0-111">Si la fonction réussit, la valeur de retour est `S_OK` (0).</span><span class="sxs-lookup"><span data-stu-id="caab0-111">If the function succeeds, the return value is `S_OK` (0).</span></span>

<span data-ttu-id="caab0-112">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="caab0-112">If the function fails, the return value is a non-zero error code.</span></span> <span data-ttu-id="caab0-113">Pour obtenir les informations d’erreur étendues, appelez le [GetErrorInfo](geterrorinfo.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="caab0-113">To get extended error information, call the [GetErrorInfo](geterrorinfo.md) function.</span></span>
    
## <a name="requirements"></a><span data-ttu-id="caab0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="caab0-114">Requirements</span></span>  
 <span data-ttu-id="caab0-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="caab0-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="caab0-116">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="caab0-116">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="caab0-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="caab0-117">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="caab0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caab0-118">See also</span></span>  
[<span data-ttu-id="caab0-119">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="caab0-119">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
