---
title: ISymUnmanagedDocument::GetURL, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetURL
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetURL
helpviewer_keywords:
- GetURL method [.NET Framework debugging]
- ISymUnmanagedDocument::GetURL method [.NET Framework debugging]
ms.assetid: 60600178-c2b5-4cab-b3a5-f0f61acebaf1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5a447de2bb01e7bbf838ef5443e3ae7951bf8226
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431365"
---
# <a name="isymunmanageddocumentgeturl-method"></a>ISymUnmanagedDocument::GetURL, méthode
Retourne le localisateur de ressource uniforme (URL) pour ce document.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetURL(  
    [in]  ULONG32  cchUrl,  
    [out] ULONG32  *pcchUrl,  
    [out, size_is(cchUrl), length_is(*pcchUrl)] WCHAR szUrl[]);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `cchUrl`  
 [in] La taille, en caractères, de la `szURL` mémoire tampon.  
  
 `pcchUrl`  
 [out] Pointeur vers une variable qui reçoit la taille de l’URL, y compris le caractère null de fin.  
  
 `szUrl`  
 [out] La mémoire tampon contenant l’URL.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, un code d’erreur.  
  
## <a name="see-also"></a>Voir aussi  
 [ISymUnmanagedDocument, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
