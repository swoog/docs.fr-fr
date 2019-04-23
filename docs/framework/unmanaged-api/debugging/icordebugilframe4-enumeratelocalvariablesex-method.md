---
title: ICorDebugILFrame4::EnumerateLocalVariablesEx, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugILFrame4.EnumerateLocalVariablesEx
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 6f60aae6-70ec-4c4c-963a-138df98c4668
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4f9d20eda8684a9a5ae43c6240d0f8a9722c4d97
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59076833"
---
# <a name="icordebugilframe4enumeratelocalvariablesex-method"></a>ICorDebugILFrame4::EnumerateLocalVariablesEx, méthode
[Pris en charge dans .NET Framework 4.5.2 et ultérieur]  
  
 Obtient un énumérateur pour la variable locale dans le frame, et peut inclure des variables ajoutées dans l'instrumentation ReJIT du profileur.  
  
## <a name="syntax"></a>Syntaxe  
  
```cpp
HRESULT EnumerateLocalVariablesEx(  
   [in] ILCodeKind flags,   
   [out] ICorDebugValueEnum **ppValueEnum  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `flags`  
 [in] Un [ILCodeKind](../../../../docs/framework/unmanaged-api/debugging/ilcodekind-enumeration.md) membre d’énumération qui spécifie si les variables ajoutées dans l’instrumentation ReJIT du profileur sont inclus dans le frame.  
  
 `ppValueEnum`  
 [out] Pointeur vers l’adresse d’un objet « ICorDebugValueEnum » qui est l’énumérateur pour les variables locales de ce frame.  
  
## <a name="remarks"></a>Notes  
 Cette méthode est similaire à la [EnumerateLocalVariables](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-enumeratelocalvariables-method.md) (méthode), à ceci près qu’elle peut accéder aux variables ajoutées dans l’instrumentation ReJIT du profileur. Paramètre `flags` à `ILCODE_ORIGINAL_IL` équivaut à appeler [ICorDebugILFrame::EnumerateLocalVariables](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-enumeratelocalvariables-method.md). La définition de `flags` à `ILCODE_REJIT_IL` autorise le débogueur à accéder aux variables locales ajoutées dans l'instrumentation ReJIT du profileur. Si le langage intermédiaire n'est pas instrumenté, l'énumération est vide et la méthode retourne `S_OK`.  
  
 L'énumérateur peut ne pas inclure toutes les variables locales dans la méthode en cours d'exécution, car il est possible que certaines d'entre elles ne soient pas actives.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugILFrame4, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe4-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [ReJIT : Guide pratique](https://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)
