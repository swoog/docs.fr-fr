---
title: IEnumRAWINPUTDEVIC:Clone
ms.date: 03/30/2017
helpviewer_keywords:
- Clone method [WPF]
ms.assetid: 2a6a1900-aa55-45fa-9382-241d569a2dc4
ms.openlocfilehash: a4c5e7db813089d1dd138416ac54dd4be467b87b
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57355017"
---
# <a name="ienumrawinputdevicclone"></a><span data-ttu-id="6e394-102">IEnumRAWINPUTDEVIC:Clone</span><span class="sxs-lookup"><span data-stu-id="6e394-102">IEnumRAWINPUTDEVIC:Clone</span></span>
<span data-ttu-id="6e394-103">Crée un autre énumérateur de périphériques d'entrée brute avec le même état que l'énumérateur actif pour itérer au sein de la même liste.</span><span class="sxs-lookup"><span data-stu-id="6e394-103">Creates another raw input device enumerator with the same state as the current enumerator to iterate over the same list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e394-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e394-104">Syntax</span></span>  
  
```  
HRESULT Clone( [out] IEnumRAWINPUTDEVICE **ppenum);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6e394-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6e394-105">Parameters</span></span>  
 `ppenum`  
  
 <span data-ttu-id="6e394-106">[out] Adresse de variable de sortie qui reçoit le [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="6e394-106">[out] Address of output variable that receives the [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) interface pointer.</span></span> <span data-ttu-id="6e394-107">Si la méthode échoue, la valeur de cette variable de sortie est indéfinie.</span><span class="sxs-lookup"><span data-stu-id="6e394-107">If the method is unsuccessful, the value of this output variable is undefined.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6e394-108">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6e394-108">Property Value/Return Value</span></span>  
 <span data-ttu-id="6e394-109">HRESULT : Cette méthode prend en charge les valeurs de retournés E_INVALIDARG et E_OUTOFMEMORY E_UNEXPECTED standard.</span><span class="sxs-lookup"><span data-stu-id="6e394-109">HRESULT: This method supports the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6e394-110">Notes</span><span class="sxs-lookup"><span data-stu-id="6e394-110">Remarks</span></span>  
 <span data-ttu-id="6e394-111">Cette méthode rend possible l’enregistrement d’un point dans la séquence d’énumération afin de retourner à ce point plus tard.</span><span class="sxs-lookup"><span data-stu-id="6e394-111">This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time.</span></span> <span data-ttu-id="6e394-112">L’appelant doit libérer ce nouvel énumérateur séparément à partir du premier énumérateur.</span><span class="sxs-lookup"><span data-stu-id="6e394-112">The caller must release this new enumerator separately from the first enumerator.</span></span>
