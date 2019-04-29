---
title: IEnumRAWINPUTDEVIC:Clone
ms.date: 03/30/2017
helpviewer_keywords:
- Clone method [WPF]
ms.assetid: 2a6a1900-aa55-45fa-9382-241d569a2dc4
ms.openlocfilehash: abc8a6e4780c8fe50afcf1b04f7e14aeb6452704
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61949589"
---
# <a name="ienumrawinputdevicclone"></a><span data-ttu-id="b7829-102">IEnumRAWINPUTDEVIC:Clone</span><span class="sxs-lookup"><span data-stu-id="b7829-102">IEnumRAWINPUTDEVIC:Clone</span></span>
<span data-ttu-id="b7829-103">Crée un autre énumérateur de périphériques d'entrée brute avec le même état que l'énumérateur actif pour itérer au sein de la même liste.</span><span class="sxs-lookup"><span data-stu-id="b7829-103">Creates another raw input device enumerator with the same state as the current enumerator to iterate over the same list.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7829-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7829-104">Syntax</span></span>  
  
```  
HRESULT Clone( [out] IEnumRAWINPUTDEVICE **ppenum);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7829-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7829-105">Parameters</span></span>  
 `ppenum`  
  
 <span data-ttu-id="b7829-106">[out] Adresse de variable de sortie qui reçoit le [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="b7829-106">[out] Address of output variable that receives the [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) interface pointer.</span></span> <span data-ttu-id="b7829-107">Si la méthode échoue, la valeur de cette variable de sortie est indéfinie.</span><span class="sxs-lookup"><span data-stu-id="b7829-107">If the method is unsuccessful, the value of this output variable is undefined.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b7829-108">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b7829-108">Property Value/Return Value</span></span>  
 <span data-ttu-id="b7829-109">HRESULT : Cette méthode prend en charge les valeurs de retournés E_INVALIDARG et E_OUTOFMEMORY E_UNEXPECTED standard.</span><span class="sxs-lookup"><span data-stu-id="b7829-109">HRESULT: This method supports the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7829-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b7829-110">Remarks</span></span>  
 <span data-ttu-id="b7829-111">Cette méthode rend possible l’enregistrement d’un point dans la séquence d’énumération afin de retourner à ce point plus tard.</span><span class="sxs-lookup"><span data-stu-id="b7829-111">This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time.</span></span> <span data-ttu-id="b7829-112">L’appelant doit libérer ce nouvel énumérateur séparément à partir du premier énumérateur.</span><span class="sxs-lookup"><span data-stu-id="b7829-112">The caller must release this new enumerator separately from the first enumerator.</span></span>
