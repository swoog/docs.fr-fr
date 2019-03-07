---
title: ISymUnmanagedENCUpdate::GetLocalVariableCount, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.GetLocalVariableCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariableCount
helpviewer_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariableCount method [.NET Framework debugging]
- GetLocalVariableCount method [.NET Framework debugging]
ms.assetid: 9777d8bb-4abc-4be8-aa7c-34f853eceb9c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5a8a56d9655a2754c110c08517229a39011d82c5
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57482455"
---
# <a name="isymunmanagedencupdategetlocalvariablecount-method"></a>ISymUnmanagedENCUpdate::GetLocalVariableCount, méthode
Obtient le nombre de variables locales.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetLocalVariableCount(  
    [in]  mdMethodDef  mdMethodToken,  
    [out] ULONG        *pcLocals);  
```  
  
## <a name="parameters"></a>Paramètres  
 `mdMethodToken`  
 [in] Le jeton de métadonnées de méthodes.  
  
 `pcLocals`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir le nombre de variables locales.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedENCUpdate, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
