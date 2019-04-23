---
title: GetRawInputDevices
ms.date: 03/30/2017
helpviewer_keywords:
- raw input [WPF]
ms.assetid: c4d37ecd-065a-4d1c-9e6c-26804ae968ca
ms.openlocfilehash: 3531ff9f42289a3ad3b029f090f2dd4987e5886c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59199402"
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
