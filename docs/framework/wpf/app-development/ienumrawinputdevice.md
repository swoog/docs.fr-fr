---
title: IEnumRAWINPUTDEVICE
ms.date: 03/30/2017
helpviewer_keywords:
- IEnumRAWINPUTDEVICE interface [WPF]
ms.assetid: 88c8b389-a48b-46b9-b895-8ed7b1e26fea
ms.openlocfilehash: 04caca0c580d26fde7fc9a3e3a11b7a8fed26d65
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59225519"
---
# <a name="ienumrawinputdevice"></a>IEnumRAWINPUTDEVICE
Cette interface énumère les périphériques d'entrée brute ; elle est uniquement utilisée par PresentationHost.exe.  
  
> [!NOTE]
>  Cette API est conçue et pris en charge uniquement sur l'ordinateur client local  
  
## <a name="members"></a>Membres  
  
|Membre|Description|  
|------------|-----------------|  
|[IEnumRAWINPUTDEVIC:Next](ienumrawinputdevic-next.md)|Énumère les éléments `celt` suivants (c'est-à-dire les structures RAWINPUTDEVICE) dans la liste de l'énumérateur, en les retournant dans `rgelt` avec le nombre réel d'éléments énumérés dans `pceltFetched`.|  
|[IEnumRAWINPUTDEVIC:Skip](ienumrawinputdevic-skip.md)|Demande à l’énumérateur d’ignorer les `celt` éléments dans l’énumération afin que l’appel suivant à [IEnumRAWINPUTDEVIC:Next](ienumrawinputdevic-next.md) ne retourne pas ces éléments.|  
|[IEnumRAWINPUTDEVIC:Reset](ienumrawinputdevic-reset.md)|Réinitialise la séquence d'énumération au début.|  
|[IEnumRAWINPUTDEVIC:Clone](ienumrawinputdevic-clone.md)|Crée un autre énumérateur de périphériques d'entrée brute avec le même état que l'énumérateur actif pour itérer au sein de la même liste.|  
  
## <a name="see-also"></a>Voir aussi

- [À propos des entrées brutes](/windows/desktop/inputdev/about-raw-input)
