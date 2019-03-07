---
title: ISymUnmanagedReader2::GetMethodsInDocument, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2.GetMethodsInDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument
helpviewer_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument method [.NET Framework debugging]
- GetMethodsInDocument method [.NET Framework debugging]
ms.assetid: c7ae84d6-81e8-4cb7-a1f9-d48b6cde5d79
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 26e6efff403f7fa10e1d96ffb3bf0f4b9ab3a96d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57465853"
---
# <a name="isymunmanagedreader2getmethodsindocument-method"></a>ISymUnmanagedReader2::GetMethodsInDocument, méthode
Obtient toutes les méthodes ayant des informations de ligne dans le document fourni.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetMethodsInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [in]  ULONG32 cMethod,  
    [out] ULONG32* pcMethod,  
    [out, size_is(cMethod),  
        length_is(*pcMethod)] ISymUnmanagedMethod* pRetVal[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `document`  
 [in] Pointeur vers le document.  
  
 `cMethod`  
 [in] Un `ULONG32` qui indique la taille de la `pRetVal` tableau.  
  
 `pcMethod`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les méthodes.  
  
 `pRetVal`  
 [out] Pointeur vers la mémoire tampon qui reçoit les méthodes.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedReader2, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)
