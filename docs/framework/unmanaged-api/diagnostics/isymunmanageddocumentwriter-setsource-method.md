---
title: ISymUnmanagedDocumentWriter::SetSource, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocumentWriter.SetSource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocumentWriter::SetSource
helpviewer_keywords:
- ISymUnmanagedDocumentWriter::SetSource method [.NET Framework debugging]
- SetSource method [.NET Framework debugging]
ms.assetid: ea5b9d9f-ff06-4bd3-8de5-6435343aba59
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bcdda6f8cdd0fc0b333b81d58a8bff7c21aa1fef
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57486405"
---
# <a name="isymunmanageddocumentwritersetsource-method"></a>ISymUnmanagedDocumentWriter::SetSource, méthode
Définit la source incorporée d’un document qui est en cours d’écriture.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetSource(  
    [in]  ULONG32  sourceSize,  
    [in, size_is(sourceSize)] BYTE  source[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `sourceSize`  
 [in] Un `ULONG32` qui contient la taille de la `source` mémoire tampon.  
  
 `source`  
 [in] La mémoire tampon qui stocke la source incorporée.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedDocumentWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)
