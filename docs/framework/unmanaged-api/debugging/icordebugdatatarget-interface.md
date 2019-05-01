---
title: ICorDebugDataTarget, interface
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget
helpviewer_keywords:
- ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: df5f05be-bed7-4f3c-bc89-dbb435d79a0b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 480fc27bd41f7ca559ceee379b7f6f81c94da0ba
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61989194"
---
# <a name="icordebugdatatarget-interface"></a>ICorDebugDataTarget, interface
Fournit une interface de rappel qui permet d'accéder à un processus cible particulier.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[GetPlatform, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md)|Fournit des informations sur la plateforme, notamment l’architecture de processeur et de système d’exploitation, sur lequel s’exécute le processus cible.|  
|[ReadVirtual, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-readvirtual-method.md)|Obtient un bloc de mémoire contiguë en commençant à l’adresse spécifiée et le retourne dans la mémoire tampon fournie.|  
|[GetThreadContext, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getthreadcontext-method.md)|Demande le contexte actuel du thread pour le thread spécifié.|  
  
## <a name="remarks"></a>Notes  
 `ICorDebugDataTarget` et ses méthodes ont les caractéristiques suivantes :  
  
- Les services de débogage appellent des méthodes sur cette interface pour accéder à la mémoire et autres données dans le processus cible.  
  
- Le client de débogueur doit implémenter cette interface comme il convient pour la cible particulière (par exemple, un processus en cours ou une image mémoire).  
  
- Le `ICorDebugDataTarget` méthodes peuvent être appelées qu’à partir de méthodes implémentées dans d’autres `ICorDebug*` interfaces. Cela garantit que le client de débogueur a contrôler sur quel thread, il est appelé et à quel moment.  
  
- Le `ICorDebugDataTarget` implémentation doit toujours retourner des informations récentes sur la cible.  
  
 Le processus cible doit être arrêté et pas changé pendant que `ICorDebug*` interfaces (et par conséquent `ICorDebugDataTarget` méthodes) sont appelées. Si la cible est un processus en cours et les modifications de son état, le [ICLRDebugging::OpenVirtualProcess](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-openvirtualprocess-method.md) méthode doit être de nouveau appelée pour fournir une instance de ICorDebugProcess de remplacement.  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
