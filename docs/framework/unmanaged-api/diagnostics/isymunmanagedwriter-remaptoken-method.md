---
title: ISymUnmanagedWriter::RemapToken, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.RemapToken
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::RemapToken
helpviewer_keywords:
- ISymUnmanagedWriter::RemapToken method [.NET Framework debugging]
- RemapToken method [.NET Framework debugging]
ms.assetid: bca92682-ee1e-467f-8fb0-d8d4617f82fe
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ec4a486b9dfb72c05a9e614fca22626dd84a83f7
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468456"
---
# <a name="isymunmanagedwriterremaptoken-method"></a>ISymUnmanagedWriter::RemapToken, méthode
Avertit le writer de symbole qu’un jeton de métadonnées a été remappé comme les métadonnées a été émises. Si le writer de symbole a stocké l’ancien jeton dans le magasin de symboles, il doit soit mettre à jour que le jeton stocké avec la nouvelle valeur, soit enregistrer le mappage pour le lecteur de symboles correspondant à remapper pendant la phase de lecture.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT RemapToken(  
    [in] mdToken  oldToken,  
    [in] mdToken  newToken);  
```  
  
## <a name="parameters"></a>Paramètres  
 `oldToken`  
 [in] Le jeton de métadonnées qui a été remappé.  
  
 `newToken`  
 [in] Le nouveau jeton de métadonnées auquel `oldToken` a été remappée.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
