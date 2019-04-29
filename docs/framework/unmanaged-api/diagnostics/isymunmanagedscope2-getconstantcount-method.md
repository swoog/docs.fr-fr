---
title: ISymUnmanagedScope2::GetConstantCount, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2.GetConstantCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2::GetConstantCount
helpviewer_keywords:
- ISymUnmanagedScope2::GetConstantCount method [.NET Framework debugging]
- GetConstantCount method [.NET Framework debugging]
ms.assetid: 1e1f0be6-c4e8-4d6c-98cd-d5fa9f686e87
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2a063d25e180be466421c14ca65a5b4cea881fc8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61761614"
---
# <a name="isymunmanagedscope2getconstantcount-method"></a>ISymUnmanagedScope2::GetConstantCount, méthode
Obtient le nombre de constantes définies dans cette portée.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetConstantCount(  
    [out, retval] ULONG32 *pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pRetVal`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les constantes.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedScope2, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)
