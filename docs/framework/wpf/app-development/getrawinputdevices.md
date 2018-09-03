---
title: GetRawInputDevices
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
ms.assetid: c4d37ecd-065a-4d1c-9e6c-26804ae968ca
ms.openlocfilehash: 1611183dc02e46ea6d5fbb53c26500be3ed93d0d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43483948"
---
# <a name="getrawinputdevices"></a>GetRawInputDevices
Permet à PresentationHost.exe de découvrir les périphériques d'entrée brute (périphériques d'interface utilisateur) qui intéressent l'application hôte.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRawInputDevices( [out] IEnumRAWINPUTDEVICE **ppEnum );  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppEnum`  
  
 [out] Un pointeur vers un [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) pour l’énumération des périphériques d’entrée brutes.  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 HRESULT :  
  
 S_OK - [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md) servira uniquement par PresentationHost.exe si S_OK est retourné.  
  
 E_NOTIMPL  
  
## <a name="remarks"></a>Notes  
 Les périphériques d'entrée brute correspondent à l'ensemble des périphériques d'entrée, notamment les claviers, les souris et, dans une moindre mesure, les périphériques classiques tels que les télécommandes.  
  
 Une fois la liste de périphériques d'entrée brute extraite, PresentationHost.exe s'inscrit auprès des périphériques pour recevoir les messages de notification WM_INPUT.  
  
## <a name="see-also"></a>Voir aussi  
 [http://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputfunctions/getrawinputdevicelist.asp](https://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputfunctions/getrawinputdevicelist.asp)  
 [FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md)
