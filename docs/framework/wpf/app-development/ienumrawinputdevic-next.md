---
title: IEnumRAWINPUTDEVIC:Next
ms.date: 03/30/2017
helpviewer_keywords:
- Next method [WPF]
ms.assetid: 3698b44d-510e-4d18-b32b-85f17188ee26
ms.openlocfilehash: 05867af48b64cd1898b13fa055859c8cc0367c8c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57494179"
---
# <a name="ienumrawinputdevicnext"></a>IEnumRAWINPUTDEVIC:Next
Énumère les prochaines `celt` [RAWINPUTDEVICE](/windows/desktop/api/winuser/ns-winuser-rawinputdevice) structures dans la liste de l’énumérateur, en les retournant dans `rgelt` , ainsi que le nombre réel d’éléments énumérés dans `pceltFetched`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Next(  
      [in] ULONG celt,  
      [out, size_is(celt), length_is(*pceltFetched)] RAWINPUTDEVICE *rgelt,  
      [out] ULONG *pceltFetched);  
```  
  
## <a name="parameters"></a>Paramètres  
 `celt`  
  
 [in] Nombre de [RAWINPUTDEVICE](/windows/desktop/api/winuser/ns-winuser-rawinputdevice) retournés dans des structures `rgelt`.  
  
 `rgelt`  
  
 [out] Tableau de taille celt (ou supérieure) destiné à recevoir les structures RAWINPUTDEVICE énumérées.  
  
 `pceltFetched`  
  
 [out] Pointeur vers le nombre d'éléments réellement fournis dans `rgelt`. L'appelant peut passer `NULL` si `rgelt` a la valeur un.  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 HRESULT : S_OK si le nombre d’éléments fournis est `celt`; Sinon, S_FALSE.
