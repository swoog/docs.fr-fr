---
title: ISymUnmanagedWriter5, interface
ms.date: 03/30/2017
ms.assetid: 15b8526e-4f5d-475c-a1e3-d8b2d145c879
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 88a9fa2f720db403c45d4254b17dfaf4689cd0f7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706902"
---
# <a name="isymunmanagedwriter5-interface"></a>ISymUnmanagedWriter5, interface
Isymunmanagedwriter5, interface.  
  
## <a name="syntax"></a>Syntaxe  
  
```idl  
[object,uuid(DCF7780D-BDE9-45DF-ACFE-21731A32000C),pointer_default(unique)]interface ISymUnmanagedWriter5 : ISymUnmanagedWriter4  
```  
  
## <a name="methods"></a>Méthodes  
 Cette interface contient les méthodes suivantes :  
  
|Méthode|Description|  
|------------|-----------------|  
|[CloseMapTokensToSourceSpans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md)|Fermez la section de données personnalisé spécial pour l’étendue de jeton pour source des informations de mappage. Après sa fermeture, aucune information de mappage plus ne peut être ajoutée.|  
|[MapTokenToSourceSpan, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-maptokentosourcespan-method.md)|Cartes s’étendent sur le jeton de métadonnées donné à la ligne source donné dans le fichier source spécifié.<br /><br /> Doit être appelée entre les appels à [openmaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) et [closemaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).|  
|[OpenMapTokensToSourceSpans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md)|Ouvrez une section spéciale de données personnalisées pour émettre des informations de mappage de l’étendue de source de jeton dans. Ouverture de cette section quand une méthode est déjà ouverte, ou vice versa, est une erreur.|  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [Interfaces du magasin de symboles de diagnostics](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [ISymUnmanagedWriter4, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)
