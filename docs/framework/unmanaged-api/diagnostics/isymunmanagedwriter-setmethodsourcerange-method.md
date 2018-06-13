---
title: ISymUnmanagedWriter::SetMethodSourceRange, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetMethodSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetMethodSourceRange
helpviewer_keywords:
- SetMethodSourceRange method [.NET Framework debugging]
- ISymUnmanagedWriter::SetMethodSourceRange method [.NET Framework debugging]
ms.assetid: c698b86e-ace7-4b21-9549-f52d6a034959
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d057201c7d7bec3070027bb1d9de62735d583cf6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429000"
---
# <a name="isymunmanagedwritersetmethodsourcerange-method"></a>ISymUnmanagedWriter::SetMethodSourceRange, méthode
Spécifie les véritables début et la fin d’une méthode dans un fichier source. Utilisez cette méthode pour spécifier l’étendue d’une méthode indépendamment des points de séquence qui existent dans la méthode.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetMethodSourceRange(  
    [in] ISymUnmanagedDocumentWriter  *startDoc,  
    [in] ULONG32                      startLine,  
    [in] ULONG32                      startColumn,  
    [in] ISymUnmanagedDocumentWriter  *endDoc,  
    [in] ULONG32                      endLine,  
    [in] ULONG32                      endColumn);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `startDoc`  
 [in] Pointeur vers le document contenant la position de départ.  
  
 `startLine`  
 [in] Le numéro de ligne de départ.  
  
 `startColumn`  
 [in] La colonne de départ.  
  
 `endDoc`  
 [in] Pointeur vers le document contenant la position de fin.  
  
 `endLine`  
 [in] Le numéro de ligne de fin.  
  
 `endColumn`  
 [in] Le numéro de colonne de fin.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi  
 [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
