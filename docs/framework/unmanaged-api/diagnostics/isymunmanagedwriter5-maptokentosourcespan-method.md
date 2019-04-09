---
title: ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode
ms.date: 03/30/2017
ms.assetid: d0fbbf61-71c6-4fb1-8c9f-d619ca5d7d68
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 08c219dd033b39fc07159875b184cdf70e3aa3ed
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59181517"
---
# <a name="isymunmanagedwriter5maptokentosourcespan-method"></a>ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode
Cartes s’étendent sur le jeton de métadonnées donné à la ligne source donné dans le fichier source spécifié.  
  
 Doit être appelée entre les appels à [openmaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) et [closemaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```idl  
HRESULT MapTokenToSourceSpan(    [in] mdToken token,    [in] ISymUnmanagedDocumentWriter* document,    [in] ULONG32 line,    [in] ULONG32 column,    [in] ULONG32 endLine,    [in] ULONG32 endColumn);  
```  
  
## <a name="parameters"></a>Paramètres  
  
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
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedWriter5, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
