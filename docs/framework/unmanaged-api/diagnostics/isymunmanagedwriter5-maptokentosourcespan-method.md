---
title: ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode
ms.date: 03/30/2017
ms.assetid: d0fbbf61-71c6-4fb1-8c9f-d619ca5d7d68
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 158ff204d57c3b08ced91d397ef71f24c5f44248
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499208"
---
# <a name="isymunmanagedwriter5maptokentosourcespan-method"></a>ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode
Cartes s’étendent sur le jeton de métadonnées donné à la ligne source donné dans le fichier source spécifié.  
  
 Doit être appelée entre les appels à [openmaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) et [closemaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```idl  
HRESULT MapTokenToSourceSpan(    [in] mdToken token,    [in] ISymUnmanagedDocumentWriter* document,    [in] ULONG32 line,    [in] ULONG32 column,    [in] ULONG32 endLine,    [in] ULONG32 endColumn);  
```  
  
#### <a name="parameters"></a>Paramètres  
  
|Paramètre|Description|  
|---------------|-----------------|  
|`token`||  
|`document`||  
|`line`||  
|`column`||  
|`endLine`||  
|`endColumn`||  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne `HRESULT`.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedWriter5, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
