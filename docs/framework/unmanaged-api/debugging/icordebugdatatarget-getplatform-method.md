---
title: ICorDebugDataTarget::GetPlatform, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget.GetPlatform Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget::GetPlatform
helpviewer_keywords:
- GetPlatform method [.NET Framework debugging]
- ICorDebugDataTarget::GetPlatform method [.NET Framework debugging]
ms.assetid: 9ee96c9d-7a3d-4129-a6cc-7675c7f2dda4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 17ae761b2d48552aded8191ddbea26552d8da277
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugdatatargetgetplatform-method"></a>ICorDebugDataTarget::GetPlatform, méthode
Fournit des informations sur la plateforme, notamment l’architecture de processeur et de système d’exploitation, sur lequel s’exécute le processus cible.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetPlatform([out] CorDebugPlatform * pTargetPlatform);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pTargetPlatform`  
 [out] Un pointeur vers un [CorDebugPlatformEnum](../../../../docs/framework/unmanaged-api/debugging/cordebugplatform-enumeration.md) énumération qui décrit la plateforme cible.  
  
## <a name="remarks"></a>Notes  
 Le `CorDebugPlatformEnum` valeur de retour d’énumération est utilisée par le [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) interface pour déterminer les détails du processus cible tels que sa taille du pointeur disposition de l’espace adresse, jeu de Registre, format de l’instruction, mise en page du contexte, et conventions d’appel.  
  
 Le `pTargetPlatform` valeur peut faire référence à une plateforme émulée pour la cible au lieu de spécifier le matériel en cours d’utilisation. Par exemple, un processus qui s’exécute dans l’environnement Windows on Windows (WOW) sur une édition 64 bits du système d’exploitation Windows doit utiliser le `CORDB_PLATFORM_WINDOWS_X86` valeur de la [CorDebugPlatformEnum](../../../../docs/framework/unmanaged-api/debugging/cordebugplatform-enumeration.md) énumération.  
  
 Cette méthode doit réussir. En cas d’échec, la plateforme cible est inutilisable. La méthode peut échouer pour les raisons suivantes :  
  
-   La plateforme émulée pour la cible est inutilisable.  
  
-   Le matériel sur la plateforme cible est inutilisable.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugDataTarget, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-interface.md)  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [Débogage](../../../../docs/framework/unmanaged-api/debugging/index.md)
