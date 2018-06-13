---
title: IEnumRAWINPUTDEVIC:Skip
ms.date: 03/30/2017
helpviewer_keywords:
- Skip method [WPF]
ms.assetid: c967b0f8-1c6a-459c-8c16-d4f08918ab65
ms.openlocfilehash: b03d141f1d2bfc18428c2f8651a340b789cfb995
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33548553"
---
# <a name="ienumrawinputdevicskip"></a><span data-ttu-id="aa9a9-102">IEnumRAWINPUTDEVIC:Skip</span><span class="sxs-lookup"><span data-stu-id="aa9a9-102">IEnumRAWINPUTDEVIC:Skip</span></span>
<span data-ttu-id="aa9a9-103">Fait en sorte que l’énumérateur d’ignorer la prochaine `celt` éléments dans l’énumération afin que le prochain appel à [IEnumRAWINPUTDEVIC:Next](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-next.md) ne retourne pas ces éléments.</span><span class="sxs-lookup"><span data-stu-id="aa9a9-103">Instructs the enumerator to skip the next `celt` elements in the enumeration so that the next call to [IEnumRAWINPUTDEVIC:Next](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-next.md) will not return those elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa9a9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa9a9-104">Syntax</span></span>  
  
```  
HRESULT Skip( [in] ULONG celt);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aa9a9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa9a9-105">Parameters</span></span>  
 `celt`  
  
 <span data-ttu-id="aa9a9-106">[in] Nombre d’éléments à ignorer.</span><span class="sxs-lookup"><span data-stu-id="aa9a9-106">[in] Number of elements to be skipped.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="aa9a9-107">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="aa9a9-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="aa9a9-108">HRESULT : S_OK si le nombre d'éléments fournis est `celt` ; sinon, S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="aa9a9-108">HRESULT: S_OK if the number of elements supplied is `celt`; S_FALSE otherwise.</span></span>
