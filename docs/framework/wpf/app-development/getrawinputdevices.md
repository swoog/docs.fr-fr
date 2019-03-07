---
title: GetRawInputDevices
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
ms.assetid: c4d37ecd-065a-4d1c-9e6c-26804ae968ca
ms.openlocfilehash: 763767514f5f157c676f2e5c86ff9b1e4e64f233
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57495245"
---
# <a name="getrawinputdevices"></a>GetRawInputDevices
Permet à PresentationHost.exe de découvrir les périphériques d'entrée brute (périphériques d'interface utilisateur) qui intéressent l'application hôte.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetRawInputDevices( [out] IEnumRAWINPUTDEVICE **ppEnum );  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppEnum`  
  
 [out] Un pointeur vers un [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) pour l’énumération des périphériques d’entrée brutes.  
  
## <a name="property-valuereturn-value"></a>Valeur de propriété/valeur de retour  
 HRESULT :  
  
 S_OK - [IEnumRAWINPUTDEVICE](ienumrawinputdevice.md) servira uniquement par PresentationHost.exe si S_OK est retourné.  
  
 E_NOTIMPL  
  
## <a name="remarks"></a>Notes  
 Les périphériques d'entrée brute correspondent à l'ensemble des périphériques d'entrée, notamment les claviers, les souris et, dans une moindre mesure, les périphériques classiques tels que les télécommandes.  
  
 Une fois la liste de périphériques d'entrée brute extraite, PresentationHost.exe s'inscrit auprès des périphériques pour recevoir les messages de notification WM_INPUT.  
  
## <a name="see-also"></a>Voir aussi
- [GetRawInputDeviceList](/windows/desktop/api/winuser/nf-winuser-getrawinputdevicelist)
- [FilterInputMessage](filterinputmessage.md)
