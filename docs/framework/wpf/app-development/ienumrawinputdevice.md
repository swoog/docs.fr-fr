---
title: IEnumRAWINPUTDEVICE
ms.date: 03/30/2017
helpviewer_keywords:
- IEnumRAWINPUTDEVICE interface [WPF]
ms.assetid: 88c8b389-a48b-46b9-b895-8ed7b1e26fea
ms.openlocfilehash: e0e5a112b7444872dd74cb70bb044ae233334d2a
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "45999229"
---
# <a name="ienumrawinputdevice"></a>IEnumRAWINPUTDEVICE
Cette interface énumère les périphériques d'entrée brute ; elle est uniquement utilisée par PresentationHost.exe.  
  
> [!NOTE]
>  Cette API est conçue et pris en charge uniquement sur l'ordinateur client local  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|[IEnumRAWINPUTDEVIC:Next](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-next.md)|Énumère les éléments `celt` suivants (c'est-à-dire les structures RAWINPUTDEVICE) dans la liste de l'énumérateur, en les retournant dans `rgelt` avec le nombre réel d'éléments énumérés dans `pceltFetched`.|  
|[IEnumRAWINPUTDEVIC:Skip](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-skip.md)|Demande à l’énumérateur d’ignorer les `celt` éléments dans l’énumération afin que l’appel suivant à [IEnumRAWINPUTDEVIC:Next](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-next.md) ne retourne pas ces éléments.|  
|[IEnumRAWINPUTDEVIC:Reset](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-reset.md)|Réinitialise la séquence d'énumération au début.|  
|[IEnumRAWINPUTDEVIC:Clone](../../../../docs/framework/wpf/app-development/ienumrawinputdevic-clone.md)|Crée un autre énumérateur de périphériques d'entrée brute avec le même état que l'énumérateur actif pour itérer au sein de la même liste.|  
  
## <a name="see-also"></a>Voir aussi  
 [À propos des entrées brutes](https://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/aboutrawinput.asp)
