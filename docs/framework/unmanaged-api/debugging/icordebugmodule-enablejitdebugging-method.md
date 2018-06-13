---
title: ICorDebugModule::EnableJITDebugging, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.EnableJITDebugging
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::EnableJITDebugging
helpviewer_keywords:
- ICorDebugModule::EnableJITDebugging method [.NET Framework debugging]
- EnableJITDebugging method [.NET Framework debugging]
ms.assetid: 0a65e2a4-5bb6-496c-ae6f-40474426b5a6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 71722293bfb80a7e57393916560f922d970ea2ab
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33415640"
---
# <a name="icordebugmoduleenablejitdebugging-method"></a>ICorDebugModule::EnableJITDebugging, méthode
Contrôle si le compilateur (JIT) juste-à-temps conserve les informations de débogage pour les méthodes de ce module.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnableJITDebugging(  
    [in] BOOL bTrackJITInfo,  
    [in] BOOL bAllowJitOpts  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `bTrackJITInfo`  
 [in] Définissez cette valeur sur `true` pour permettre au compilateur JIT de conserver les informations de mappage entre la version de langage intermédiaire (MSIL) de Microsoft et de la version de compilation JIT de chaque méthode dans ce module.  
  
 `bAllowJitOpts`  
 [in] Définissez cette valeur sur `true` pour permettre au compilateur JIT de générer du code avec certaines optimisations spécifiques au JIT pour le débogage.  
  
## <a name="remarks"></a>Notes  
 Débogage JIT est activé par défaut pour tous les modules qui sont chargés lorsque le débogueur est actif. Par programmation l’activation ou désactivation des paramètres substitue les paramètres globaux.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
