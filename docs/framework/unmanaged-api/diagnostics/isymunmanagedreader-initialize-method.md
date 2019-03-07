---
title: ISymUnmanagedReader::Initialize, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.Initialize
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::Initialize
helpviewer_keywords:
- ISymUnmanagedReader::Initialize method [.NET Framework debugging]
- Initialize method, ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: 8f0dd2fe-7df7-464e-91f4-5518c586bb5f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1a5eb91d02ce55601f86dcadc744ef23ca430d9c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471691"
---
# <a name="isymunmanagedreaderinitialize-method"></a>ISymUnmanagedReader::Initialize, méthode
Initialise le lecteur de symboles avec l’interface d’importateur de métadonnées qui ce lecteur sera associé, ainsi que le nom de fichier du module.  
  
> [!NOTE]
>  Cette méthode peut être appelée qu’une seule fois et doit être appelée avant toute autre méthode de lecteur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Initialize (  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *filename,  
    [in]  const WCHAR  *searchPath,  
    [in]  IStream      *pIStream);  
```  
  
## <a name="parameters"></a>Paramètres  
 `importer`  
 [in] L’interface importateur de métadonnées avec laquelle ce lecteur sera associé.  
  
 `filename`  
 [in] Le nom de fichier du module. Vous pouvez utiliser le `pIStream` paramètre à la place.  
  
 `searchPath`  
 [in] Le chemin d’accès à rechercher. Ce paramètre est optionnel.  
  
 `pIStream`  
 [in] Le flux de fichier, utilisé comme alternative au paramètre de nom de fichier.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="remarks"></a>Notes  
 Vous devez spécifier un seul de le `filename` ou `pIStream` paramètres, pas les deux. Le paramètre `searchPath` est optionnel.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedReader, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
