---
title: IEnumRAWINPUTDEVIC:Skip
ms.date: 03/30/2017
helpviewer_keywords:
- Skip method [WPF]
ms.assetid: c967b0f8-1c6a-459c-8c16-d4f08918ab65
ms.openlocfilehash: f7d7df77c54d4551025aa5a344c96083c263f455
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57467166"
---
# <a name="ienumrawinputdevicskip"></a><span data-ttu-id="d6784-102">IEnumRAWINPUTDEVIC:Skip</span><span class="sxs-lookup"><span data-stu-id="d6784-102">IEnumRAWINPUTDEVIC:Skip</span></span>
<span data-ttu-id="d6784-103">Demande à l’énumérateur d’ignorer les `celt` éléments dans l’énumération afin que l’appel suivant à [IEnumRAWINPUTDEVIC:Next](ienumrawinputdevic-next.md) ne retourne pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="d6784-103">Instructs the enumerator to skip the next `celt` elements in the enumeration so that the next call to [IEnumRAWINPUTDEVIC:Next](ienumrawinputdevic-next.md) will not return those elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d6784-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6784-104">Syntax</span></span>  
  
```  
HRESULT Skip( [in] ULONG celt);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d6784-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6784-105">Parameters</span></span>  
 `celt`  
  
 <span data-ttu-id="d6784-106">[in] Nombre d’éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="d6784-106">[in] Number of elements to be skipped.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d6784-107">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d6784-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="d6784-108">HRESULT : S_OK si le nombre d’éléments fournis est `celt`; Sinon, S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="d6784-108">HRESULT: S_OK if the number of elements supplied is `celt`; S_FALSE otherwise.</span></span>
