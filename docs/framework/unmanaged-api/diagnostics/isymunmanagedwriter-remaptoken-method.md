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
ms.openlocfilehash: 979d14b4c404c3bf12c427bd5b8b1d4997805e7b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59160678"
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
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
