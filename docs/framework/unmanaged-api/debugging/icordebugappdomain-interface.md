---
title: ICorDebugAppDomain, interface
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain
api_location:
- corguids.lib
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain
helpviewer_keywords:
- ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: be7ae711-1217-4a44-be40-166e29641b77
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 40619aa40f9924d94c82541eb8d30790e774a675
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59141496"
---
# <a name="icordebugappdomain-interface"></a>ICorDebugAppDomain, interface

Fournit des méthodes pour le débogage de domaines d'application. Cette interface est une sous-classe de ICorDebugController.  
  
## <a name="methods"></a>Méthodes  
  
|Méthode|Description|  
|------------|-----------------|  
|[Attach, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-attach-method.md)|Attache le débogueur au domaine d’application.|  
|[EnumerateAssemblies, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-enumerateassemblies-method.md)|Obtient un énumérateur pour les assemblys dans le domaine d’application.|  
|[EnumerateBreakpoints, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-enumeratebreakpoints-method.md)|Obtient un énumérateur pour tous les points d’arrêt actifs dans le domaine d’application.|  
|[EnumerateSteppers, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-enumeratesteppers-method.md)|Obtient un énumérateur pour toutes les exécutions pas à pas active dans le domaine d’application.|  
|[GetID, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getid-method.md)|Obtient l’ID unique du domaine d’application.|  
|[GetModuleFromMetaDataInterface, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getmodulefrommetadatainterface-method.md)|Obtient l’objet ICorDebugModule avec l’interface de métadonnées fourni.|  
|[GetName, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getname-method.md)|Obtient le nom du domaine d’application.|  
|[GetObject, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getobject-method.md)|Obtient un pointeur d’interface vers le domaine d’application du common language runtime (CLR).|  
|[GetProcess, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-getprocess-method.md)|Obtient le processus contenant le domaine d’application.|  
|[IsAttached, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain-isattached-method.md)|Détermine si le débogueur est attaché au domaine d’application.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette interface ne prend pas en charge l'appel à distance, que ce soit entre ordinateurs ou entre processus.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
