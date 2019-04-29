---
title: ICLRDataTarget2, interface
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2
helpviewer_keywords:
- ICLRDataTarget2 interface [.NET Framework debugging]
ms.assetid: 94249397-861b-4294-a538-cf01466a66d3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d21bced214242866c47f40f392593f3f51cda02f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697938"
---
# <a name="iclrdatatarget2-interface"></a>ICLRDataTarget2, interface
Une sous-classe de [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) qui est utilisée par la couche de services d’accès aux données pour manipuler les régions de mémoire virtuelle dans le processus cible.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[AllocVirtual, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-allocvirtual-method.md)|Alloue de la mémoire dans l’espace d’adressage du processus cible.|  
|[FreeVirtual, méthode](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget2-freevirtual-method.md)|Libère la mémoire précédemment alloué dans l’espace d’adressage du processus cible.|  
  
## <a name="remarks"></a>Notes  
 Le client API (c'est-à-dire le débogueur) doit implémenter cette interface comme il convient pour le processus cible particulier. Par exemple, un processus actif aurait une implémentation différente de celle d'un vidage de la mémoire. La cible ne prend peut-être pas en charge la modification de ses régions de mémoire.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** ClrData.idl, ClrData.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICLRDataTarget, interface](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
