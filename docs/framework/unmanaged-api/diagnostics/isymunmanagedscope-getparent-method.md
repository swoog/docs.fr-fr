---
title: ISymUnmanagedScope::GetParent, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetParent
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetParent
helpviewer_keywords:
- GetParent method [.NET Framework debugging]
- ISymUnmanagedScope::GetParent method [.NET Framework debugging]
ms.assetid: c7963c87-6ec5-49b3-a5cd-e0fe0c43f9b4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 634f30186c552f0e5330dd94f78c585da7d450c9
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57493828"
---
# <a name="isymunmanagedscopegetparent-method"></a>ISymUnmanagedScope::GetParent, méthode
Obtient la portée parente de cette étendue.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetParent(  
    [out, retval] ISymUnmanagedScope** pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pRetVal`  
 [out] Un pointeur vers le texte retourné [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedScope, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
- [GetChildren, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getchildren-method.md)
