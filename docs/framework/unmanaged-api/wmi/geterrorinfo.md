---
title: GetErrorInfo (fonction) (référence des API non managées)
description: La fonction GetErrorInfo récupère les informations d’erreur à partir de l’appel de fonction précédente.
ms.date: 11/06/2017
api_name:
- GetErrorInfo
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetErrorInfo
helpviewer_keywords:
- GetErrorInfo function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5f25777402fa31e72cbbf36f58a6c4cc65542979
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44039473"
---
# <a name="geterrorinfo-function"></a><span data-ttu-id="a8fa1-103">GetErrorInfo (fonction)</span><span class="sxs-lookup"><span data-stu-id="a8fa1-103">GetErrorInfo function</span></span>
<span data-ttu-id="a8fa1-104">Récupère les informations d’erreur à partir de l’appel de fonction précédent.</span><span class="sxs-lookup"><span data-stu-id="a8fa1-104">Retrieves error information from the previous function call.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="a8fa1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8fa1-105">Syntax</span></span>  
  
```  
IErrorInfo* GetErrorInfo(); 
```  

## <a name="return-value"></a><span data-ttu-id="a8fa1-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a8fa1-106">Return value</span></span>

<span data-ttu-id="a8fa1-107">Un pointeur vers un [IErrorInfo](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) objet si l’appel de fonction réussit, ou `null` en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="a8fa1-107">An pointer to an [IErrorInfo](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) object if the function call succeeds, or `null` if it fails.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8fa1-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a8fa1-108">Remarks</span></span>

<span data-ttu-id="a8fa1-109">Cette fonction encapsule un appel à la [IComThreadingInfo::GetErrorInfo](/windows/desktop/api/objidlbase/nf-objidlbase-icomthreadinginfo-getcurrentapartmenttype) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a8fa1-109">This function wraps a call to the [IComThreadingInfo::GetErrorInfo](/windows/desktop/api/objidlbase/nf-objidlbase-icomthreadinginfo-getcurrentapartmenttype) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8fa1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8fa1-110">Requirements</span></span>  
 <span data-ttu-id="a8fa1-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a8fa1-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8fa1-112">**En-tête :** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="a8fa1-112">**Header:** WMINet_Utils.def</span></span>  
  
 <span data-ttu-id="a8fa1-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a8fa1-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8fa1-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8fa1-114">See also</span></span>  
[<span data-ttu-id="a8fa1-115">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="a8fa1-115">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
