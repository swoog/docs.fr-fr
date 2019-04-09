---
title: Méthode ICorDebugVariableSymbol::GetValue
ms.date: 03/30/2017
ms.assetid: 90abece1-392e-4ade-94a1-30c75b0f7074
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 186d9eec0aa6ad9e327b1dd4d0f19e251c79ecf9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59147275"
---
# <a name="icordebugvariablesymbolgetvalue-method"></a>Méthode ICorDebugVariableSymbol::GetValue
Obtient la valeur d'une variable sous forme d'un tableau d'octets.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetValue(  
   [in] ULONG32 offset,  
   [in] ULONG32 cbContext,  
   [in, size_is(cbContext)] BYTE context[],  
   [in] ULONG32 cbValue,  
   [out] ULONG32 *pcbValue,  
   [out, size_is(cbValue), length_is(*pcbValue)] BYTE pValue[]  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `offset`  
 [in] Offset de démarrage dans la variable au niveau duquel lire la valeur. Ce paramètre est utilisé lors de la lecture de champs membres d'un objet.  
  
 `cbContext`  
 [in] Taille en octets de l'argument `context`.  
  
 `context`  
 [in] Contexte de thread utilisé pour lire la valeur.  
  
 `cbValue`  
 [in] Taille en octets de la mémoire tampon `pValue`.  
  
 `pcbValue`  
 [out] Nombre d'octets réellement écrits dans la mémoire tampon `pValue`.  
  
 `pValue`  
 [out] Tableau d'octets contenant la valeur de la variable.  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugVariableSymbol, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md)
- [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
