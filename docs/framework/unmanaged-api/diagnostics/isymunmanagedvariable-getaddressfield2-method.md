---
title: ISymUnmanagedVariable::GetAddressField2, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField2
helpviewer_keywords:
- GetAddressField2 method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressField2 method [.NET Framework debugging]
ms.assetid: 1f25b294-72b6-4882-a49b-6c9d364b6008
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2030a0da7a84695750d1dd9781adca9cd66f22ad
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59137694"
---
# <a name="isymunmanagedvariablegetaddressfield2-method"></a>ISymUnmanagedVariable::GetAddressField2, méthode
Obtient le deuxième champ d’adresse pour cette variable. Sa signification dépend du type d’adresse.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetAddressField2(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pRetVal`  
 [out] Un pointeur vers un `ULONG32` qui reçoit le deuxième champ d’adresse.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedVariable, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
- [GetAddressField1, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield1-method.md)
- [GetAddressField3, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield3-method.md)
- [GetAddressKind, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddresskind-method.md)
