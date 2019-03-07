---
title: ISymUnmanagedAsyncMethod::IsAsyncMethod, méthode
ms.date: 03/30/2017
ms.assetid: 670a7653-dac6-4171-98ee-d669e3adf4b2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 460d6781405b6042262d50e1aa79ee8c77f781a7
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57489720"
---
# <a name="isymunmanagedasyncmethodisasyncmethod-method"></a>ISymUnmanagedAsyncMethod::IsAsyncMethod, méthode
Vérifie si la méthode async informations ou pas.  
  
 Si cette méthode retourne `FALSE` , il est impossible d’appeler toutes les autres méthodes dans cette interface. Il s’agit de retour de tous les `E_UNEXPECTED` dans ce cas.  
  
## <a name="syntax"></a>Syntaxe  
  
```idl  
HRESULT IsAsyncMethod(    [out, retval] BOOL* pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
  
|Paramètre|Description|  
|---------------|-----------------|  
|`pRetVal`||  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne `HRESULT`.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedAsyncMethod, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
