---
title: ISymUnmanagedScope::GetEndOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetEndOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetEndOffset
helpviewer_keywords:
- ISymUnmanagedScope::GetEndOffset method [.NET Framework debugging]
- GetEndOffset method, ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 1d0b15c9-8059-435f-9fce-346a08b9bd36
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 47db4313354b00514084ec1110710cbd174a3788
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57492619"
---
# <a name="isymunmanagedscopegetendoffset-method"></a>ISymUnmanagedScope::GetEndOffset, méthode
Obtient l’offset de fin pour cette étendue.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pRetVal`  
 [out] Un pointeur vers un `ULONG32` qui reçoit l’offset de fin.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedScope, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
- [GetStartOffset, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getstartoffset-method.md)
