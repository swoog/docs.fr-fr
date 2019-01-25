---
title: ISymUnmanagedWriter5::CloseMapTokensToSourceSpans, méthode
ms.date: 03/30/2017
ms.assetid: f8a0c0a2-a11d-436c-aa85-bc110215cfd6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce4b41854d5d9324169b1873f431ef81c0a4c5be
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54677916"
---
# <a name="isymunmanagedwriter5closemaptokenstosourcespans-method"></a>ISymUnmanagedWriter5::CloseMapTokensToSourceSpans, méthode
Fermez la section de données personnalisé spécial pour l’étendue de jeton pour source des informations de mappage. Après sa fermeture, aucune information de mappage plus ne peut être ajoutée.  
  
## <a name="syntax"></a>Syntaxe  
  
```idl  
HRESULT CloseMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne `HRESULT`.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedWriter5, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
