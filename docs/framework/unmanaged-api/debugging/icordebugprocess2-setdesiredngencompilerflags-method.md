---
title: ICorDebugProcess2::SetDesiredNGENCompilerFlags, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.SetDesiredNGENCompilerFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::SetDesiredNGENCompilerFlags
helpviewer_keywords:
- ICorDebugProcess2::SetDesiredNGENCompilerFlags method [.NET Framework debugging]
- SetDesiredNGENCompilerFlags method [.NET Framework debugging]
ms.assetid: 98320175-7c5e-4dbb-8683-86fa82e2641f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 94ba2b0cf7d88104eaadd434732edf3c1d4060e2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422699"
---
# <a name="icordebugprocess2setdesiredngencompilerflags-method"></a>ICorDebugProcess2::SetDesiredNGENCompilerFlags, méthode
Définit les indicateurs qui doivent être incorporés dans une image précompilée afin que le runtime charge cette image dans le processus actuel.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetDesiredNGENCompilerFlags (  
    [in] DWORD    pdwFlags  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pdwFlags`  
 [in] Une valeur de la [CorDebugJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/cordebugjitcompilerflags-enumeration.md) énumération qui spécifie les indicateurs de compilateur utilisés pour sélectionner l’image précompilée correcte.  
  
## <a name="remarks"></a>Notes  
 Le `SetDesiredNGENCompilerFlags` méthode spécifie les indicateurs qui doivent être incorporés dans une image précompilée afin que le runtime charge cette image dans ce processus. Les indicateurs définis par cette méthode servent uniquement à sélectionner l’image précompilée correcte. Si aucune image n’existe, le runtime charge à la place l’image MSIL (intermediate language) de Microsoft et le compilateur (JIT) juste-à-temps. Dans ce cas, le débogueur doit utiliseront le [ICorDebugModule2::SetJITCompilerFlags](../../../../docs/framework/unmanaged-api/debugging/icordebugmodule2-setjitcompilerflags-method.md) méthode pour définir les indicateurs voulus pour la compilation JIT.  
  
 Si une image est chargée, mais certains compilation JIT doit avoir lieu pour cette image (qui sera le cas si l’image contient des génériques), les indicateurs de compilateur spécifiés par la `SetDesiredNGENCompilerFlags` méthode s’applique à la compilation JIT supplémentaire.  
  
 Le `SetDesiredNGENCompilerFlags` méthode doit être appelée pendant la [ICorDebugManagedCallback::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) rappel. Tente d’appeler le `SetDesiredNGENCompilerFlags` méthode ensuite échoue. En outre, les tentatives de définir des indicateurs qui ne sont pas définis dans le `CorDebugJITCompilerFlags` énumération ou ne sont pas corrects pour le processus donné échoueront.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebug, interface](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)  
 [ICorDebugManagedCallback, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
