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
ms.openlocfilehash: c2df4b87016394d1998ef90abe2e3eeb911886ef
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59217496"
---
# <a name="geterrorinfo-function"></a><span data-ttu-id="c472b-103">GetErrorInfo (fonction)</span><span class="sxs-lookup"><span data-stu-id="c472b-103">GetErrorInfo function</span></span>
<span data-ttu-id="c472b-104">Récupère les informations d’erreur à partir de l’appel de fonction précédent.</span><span class="sxs-lookup"><span data-stu-id="c472b-104">Retrieves error information from the previous function call.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="c472b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c472b-105">Syntax</span></span>  
  
```  
IErrorInfo* GetErrorInfo(); 
```  

## <a name="return-value"></a><span data-ttu-id="c472b-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c472b-106">Return value</span></span>

<span data-ttu-id="c472b-107">Un pointeur vers un [IErrorInfo](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) objet si l’appel de fonction réussit, ou `null` en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="c472b-107">An pointer to an [IErrorInfo](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) object if the function call succeeds, or `null` if it fails.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c472b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c472b-108">Remarks</span></span>

<span data-ttu-id="c472b-109">Cette fonction encapsule un appel à la [IComThreadingInfo::GetErrorInfo](/windows/desktop/api/objidlbase/nf-objidlbase-icomthreadinginfo-getcurrentapartmenttype) (méthode).</span><span class="sxs-lookup"><span data-stu-id="c472b-109">This function wraps a call to the [IComThreadingInfo::GetErrorInfo](/windows/desktop/api/objidlbase/nf-objidlbase-icomthreadinginfo-getcurrentapartmenttype) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c472b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c472b-110">Requirements</span></span>  
 <span data-ttu-id="c472b-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c472b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c472b-112">**En-tête :** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="c472b-112">**Header:** WMINet_Utils.def</span></span>  
  
 **<span data-ttu-id="c472b-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c472b-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c472b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c472b-114">See also</span></span>

- [<span data-ttu-id="c472b-115">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="c472b-115">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
