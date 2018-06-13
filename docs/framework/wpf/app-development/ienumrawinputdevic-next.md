---
title: IEnumRAWINPUTDEVIC:Next
ms.date: 03/30/2017
helpviewer_keywords:
- Next method [WPF]
ms.assetid: 3698b44d-510e-4d18-b32b-85f17188ee26
ms.openlocfilehash: 3cf3231bd48290c5b6b0ce8eeb6534de564c0c85
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33546404"
---
# <a name="ienumrawinputdevicnext"></a><span data-ttu-id="6aad5-102">IEnumRAWINPUTDEVIC:Next</span><span class="sxs-lookup"><span data-stu-id="6aad5-102">IEnumRAWINPUTDEVIC:Next</span></span>
<span data-ttu-id="6aad5-103">Énumère les `celt` [RAWINPUTDEVICE](http://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp) structures dans la liste de l’énumérateur, en les retournant dans `rgelt` , ainsi que le nombre réel d’éléments énumérés dans `pceltFetched`.</span><span class="sxs-lookup"><span data-stu-id="6aad5-103">Enumerates the next `celt` [RAWINPUTDEVICE](http://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp) structures in the enumerator's list, returning them in `rgelt` along with the actual number of enumerated elements in `pceltFetched`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6aad5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aad5-104">Syntax</span></span>  
  
```  
HRESULT Next(  
      [in] ULONG celt,  
      [out, size_is(celt), length_is(*pceltFetched)] RAWINPUTDEVICE *rgelt,  
      [out] ULONG *pceltFetched);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6aad5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6aad5-105">Parameters</span></span>  
 `celt`  
  
 <span data-ttu-id="6aad5-106">[in] Nombre de [RAWINPUTDEVICE](http://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp) retournés dans des structures `rgelt`.</span><span class="sxs-lookup"><span data-stu-id="6aad5-106">[in] Number of [RAWINPUTDEVICE](http://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp) structures returned in `rgelt`.</span></span>  
  
 `rgelt`  
  
 <span data-ttu-id="6aad5-107">[out] Tableau de taille celt (ou supérieure) destiné à recevoir les structures RAWINPUTDEVICE énumérées.</span><span class="sxs-lookup"><span data-stu-id="6aad5-107">[out] Array of size celt (or larger) to receive enumerated RAWINPUTDEVICE structures.</span></span>  
  
 `pceltFetched`  
  
 <span data-ttu-id="6aad5-108">[out] Pointeur vers le nombre d'éléments réellement fournis dans `rgelt`.</span><span class="sxs-lookup"><span data-stu-id="6aad5-108">[out] Pointer to the number of elements actually supplied in `rgelt`.</span></span> <span data-ttu-id="6aad5-109">L'appelant peut passer `NULL` si `rgelt` a la valeur un.</span><span class="sxs-lookup"><span data-stu-id="6aad5-109">Caller can pass in `NULL` if `rgelt` is one.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6aad5-110">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6aad5-110">Property Value/Return Value</span></span>  
 <span data-ttu-id="6aad5-111">HRESULT : S_OK si le nombre d'éléments fournis est `celt` ; sinon, S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="6aad5-111">HRESULT: S_OK if the number of elements supplied is `celt`; S_FALSE otherwise.</span></span>
