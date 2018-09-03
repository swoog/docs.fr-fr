---
title: IEnumRAWINPUTDEVIC:Next
ms.date: 03/30/2017
helpviewer_keywords:
- Next method [WPF]
ms.assetid: 3698b44d-510e-4d18-b32b-85f17188ee26
ms.openlocfilehash: 329a2cd96346e199ee834856dd6dbfac6175b722
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43481176"
---
# <a name="ienumrawinputdevicnext"></a>IEnumRAWINPUTDEVIC:Next
Énumère les prochaines `celt` [RAWINPUTDEVICE](https://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp) structures dans la liste de l’énumérateur, en les retournant dans `rgelt` , ainsi que le nombre réel d’éléments énumérés dans `pceltFetched`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Next(  
      [in] ULONG celt,  
      [out, size_is(celt), length_is(*pceltFetched)] RAWINPUTDEVICE *rgelt,  
      [out] ULONG *pceltFetched);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `celt`  
  
 [in] Nombre de [RAWINPUTDEVICE](https://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp) retournés dans des structures `rgelt`.  
  
 `rgelt`  
  
 [out] Tableau de taille celt (ou supérieure) destiné à recevoir les structures RAWINPUTDEVICE énumérées.  
  
 `pceltFetched`  
  
 [out] Pointeur vers le nombre d'éléments réellement fournis dans `rgelt`. L'appelant peut passer `NULL` si `rgelt` a la valeur un.  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 HRESULT : S_OK si le nombre d'éléments fournis est `celt` ; sinon, S_FALSE.
