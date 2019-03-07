---
title: ISymENCUnmanagedMethod::GetDocumentsForMethodCount, méthode
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetDocumentsForMethodCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount
helpviewer_keywords:
- GetDocumentsForMethodCount method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetDocumentsForMethodCount method [.NET Framework debugging]
ms.assetid: cc1a823a-3ff3-4a33-b641-96edc93d2b17
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 571db05b5ec33a0bee310afadf205ac236f7048c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471535"
---
# <a name="isymencunmanagedmethodgetdocumentsformethodcount-method"></a>ISymENCUnmanagedMethod::GetDocumentsForMethodCount, méthode
Obtient le nombre de documents que cette méthode a des lignes.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetDocumentsForMethodCount(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pRetVal`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les documents.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymENCUnmanagedMethod, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
