---
title: ISymUnmanagedWriter::DefineDocument, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineDocument
helpviewer_keywords:
- ISymUnmanagedWriter::DefineDocument method [.NET Framework debugging]
- DefineDocument method [.NET Framework debugging]
ms.assetid: c3bf15b0-3250-4bbe-b9b5-c5d695289b6f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 726ac0e23f739f451e1a0ab66c4c36aa6edbe569
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59132130"
---
# <a name="isymunmanagedwriterdefinedocument-method"></a>ISymUnmanagedWriter::DefineDocument, méthode
Définit un document source. GUID sont fournies pour les langages connus, les fournisseurs et les types de documents.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineDocument(  
    [in]  const WCHAR  *url,  
    [in]  const GUID   *language,  
    [in]  const GUID   *languageVendor,  
    [in]  const GUID   *documentType,  
    [out, retval] ISymUnmanagedDocumentWriter**  pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
 `url`  
 [in] Un pointeur vers un `WCHAR` qui définit l’uniform resource locator (URL) qui identifie le document.  
  
 `language`  
 [in] Pointeur vers un GUID qui définit le langage du document.  
  
 `languageVendor`  
 [in] Pointeur vers un GUID qui définit l’identité du fournisseur de langage du document.  
  
 `documentType`  
 [in] Pointeur vers un GUID qui définit le type du document.  
  
 `pRetVal`  
 [out] Un pointeur vers le texte retourné [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
