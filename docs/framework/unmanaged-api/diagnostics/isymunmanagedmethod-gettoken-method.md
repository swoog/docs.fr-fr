---
title: ISymUnmanagedMethod::GetToken, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetToken
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetToken
helpviewer_keywords:
- ISymUnmanagedMethod::GetToken method [.NET Framework debugging]
- GetToken method, ISymUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: 4effbe95-c36e-4a45-8b2a-ee21339415fb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5b0acee31017fd02ac3e51f9e585669b9c90ec48
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57467013"
---
# <a name="isymunmanagedmethodgettoken-method"></a>ISymUnmanagedMethod::GetToken, méthode
Retourne le jeton de métadonnées pour cette méthode.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetToken(  
   [out, retval]  mdMethodDef  *pToken);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pToken`  
 [out] Un pointeur vers un `mdMethodDef` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les métadonnées.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedMethod, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
