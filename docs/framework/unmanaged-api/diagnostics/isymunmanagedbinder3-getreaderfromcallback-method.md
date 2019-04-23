---
title: ISymUnmanagedBinder3::GetReaderFromCallback, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder3.GetReaderFromCallback
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder3::GetReaderFromCallback
helpviewer_keywords:
- GetReaderFromCallback method [.NET Framework debugging]
- ISymUnmanagedBinder3::GetReaderFromCallback method [.NET Framework debugging]
ms.assetid: 4ef83bd2-3d8e-499e-8a12-d9d6fd6ced30
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9487cf89d87b5f373302dc49a08c4fabb719e746
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59160756"
---
# <a name="isymunmanagedbinder3getreaderfromcallback-method"></a>ISymUnmanagedBinder3::GetReaderFromCallback, méthode
Permet à l’utilisateur d’implémenter ou de fournir via un rappel un `IID_IDiaReadExeAtRVACallback` ou `IID_IDiaReadExeAtOffsetCallback` pour obtenir les informations de répertoire de débogage de la mémoire.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetReaderFromCallback(  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *fileName,  
    [in]  const WCHAR  *searchPath,  
    [in]  ULONG32      searchPolicy,  
    [in]  IUnknown     *callback,  
    [out,retval] ISymUnmanagedReader  **pRetVal);  
```  
  
## <a name="parameters"></a>Paramètres  
 `importer`  
 [in] Pointeur vers l’interface d’importation de métadonnées.  
  
 `fileName`  
 [in] Pointeur vers le nom de fichier.  
  
 `searchPath`  
 [in] Pointeur vers le chemin de recherche.  
  
 `searchPolicy`  
 [in] Une valeur de la [CorSymSearchPolicyAttributes](../../../../docs/framework/unmanaged-api/diagnostics/corsymsearchpolicyattributes-enumeration.md) énumération qui spécifie la stratégie à utiliser lors d’une recherche pour un lecteur de symboles.  
  
 `callback`  
 [in] Pointeur vers la fonction de rappel.  
  
 `pRetVal`  
 [out] Un pointeur qui est défini à retourné [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedBinder3, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)
