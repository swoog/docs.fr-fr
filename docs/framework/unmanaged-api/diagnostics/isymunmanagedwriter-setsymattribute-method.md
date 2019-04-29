---
title: ISymUnmanagedWriter::SetSymAttribute, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetSymAttribute
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetSymAttribute
helpviewer_keywords:
- SetSymAttribute method [.NET Framework debugging]
- ISymUnmanagedWriter::SetSymAttribute method [.NET Framework debugging]
ms.assetid: 64d9b80e-b883-4539-89c7-03573185a1eb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8ffcc3a079e7e9a9d69622dc6666bb0e7641d4e3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61650769"
---
# <a name="isymunmanagedwritersetsymattribute-method"></a>ISymUnmanagedWriter::SetSymAttribute, méthode
Définit un attribut personnalisé en fonction de son nom. Ces attributs sont stockés dans le magasin de symboles, contrairement aux attributs personnalisés de métadonnées.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetSymAttribute(  
    [in] mdToken parent,  
    [in] const WCHAR *name,  
    [in] ULONG32 cData,  
    [in, size_is(cData)] unsigned char data[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `parent`  
 [in] Le jeton de métadonnées pour lequel l’attribut est défini.  
  
 `name`  
 [in] Un pointeur vers un `WCHAR` qui contient le nom d’attribut.  
  
 `cData`  
 [in] Un `ULONG32` qui indique la taille de la `data` tableau.  
  
 `data`  
 [in] La valeur d’attribut.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
