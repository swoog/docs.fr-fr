---
title: ISymUnmanagedReader::GetUserEntryPoint, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetUserEntryPoint
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetUserEntryPoint
helpviewer_keywords:
- GetUserEntryPoint method [.NET Framework debugging]
- ISymUnmanagedReader::GetUserEntryPoint method [.NET Framework debugging]
ms.assetid: 3fd3a34c-d176-46e9-9996-fb1646cff9b0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7b4c334d82320066bf9459907660fe6b7e2acefd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425319"
---
# <a name="isymunmanagedreadergetuserentrypoint-method"></a>ISymUnmanagedReader::GetUserEntryPoint, méthode
Retourne la méthode qui a été spécifiée en tant que point d’entrée utilisateur pour le module, le cas échéant. Par exemple, cette méthode peut être méthode principale de l’utilisateur plutôt que des stubs générés par le compilateur avant la méthode principale.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetUserEntryPoint (  
    [out, retval]  mdMethodDef  *pToken);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pToken`  
 [out] Pointeur vers une variable qui reçoit le point d’entrée.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi  
 [ISymUnmanagedReader, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
