---
title: ISymUnmanagedWriter4::GetDebugInfoWithPadding, méthode
ms.date: 03/30/2017
ms.assetid: 881e20ca-8131-4bd0-ba41-c2d6391b0fe2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 191aa16c285b3a28beed65004d65525c9214ec93
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61650737"
---
# <a name="isymunmanagedwriter4getdebuginfowithpadding-method"></a>ISymUnmanagedWriter4::GetDebugInfoWithPadding, méthode
Fonctionne comme [GetDebugInfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) , à ceci près que la chaîne de chemin d’accès est remplie avec des zéros qui suivent le caractère null de fin pour rendre les données de chaîne de taille fixe de `MAX_PATH`. Marge intérieure est obtenu uniquement si la longueur de chaîne de chemin d’accès lui-même est inférieure à `MAX_PATH`.  
  
 Cela rend plus facile à écrire des outils que les fichiers PE de différence.  
  
## <a name="syntax"></a>Syntaxe  
  
```idl  
HRESULT GetDebugInfoWithPadding(    [in, out] IMAGE_DEBUG_DIRECTORY *pIDD,    [in] DWORD cData,    [out] DWORD *pcData,    [out, size_is(cData), length_is(*pcData)] BYTE data[]);  
```  
  
## <a name="parameters"></a>Paramètres  
  
|Paramètre|Description|  
|---------------|-----------------|  
|`pIDD`||  
|`cData`||  
|`pcData`||  
|`data`||  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne `HRESULT`.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedWriter4, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)
