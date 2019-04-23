---
title: ISymUnmanagedDocument::GetDocumentType, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetDocumentType
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetDocumentType
helpviewer_keywords:
- ISymUnmanagedDocument::GetDocumentType method [.NET Framework debugging]
- GetDocumentType method [.NET Framework debugging]
ms.assetid: 2d381ab1-7e7c-4281-af2b-e54d879b3ef8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7694c9b736700466ac1299b9632440e133109288
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59154074"
---
# <a name="isymunmanageddocumentgetdocumenttype-method"></a>ISymUnmanagedDocument::GetDocumentType, méthode
Obtient le type de document de ce document.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetDocumentType(  
    [out, retval] GUID*  pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pRetVal`  
 [out] Pointeur vers une variable qui reçoit le type de document.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit.  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedDocument, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
