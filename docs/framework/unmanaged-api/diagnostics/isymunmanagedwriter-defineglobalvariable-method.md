---
title: ISymUnmanagedWriter::DefineGlobalVariable, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineGlobalVariable
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineGlobalVariable
helpviewer_keywords:
- ISymUnmanagedWriter::DefineGlobalVariable method [.NET Framework debugging]
- DefineGlobalVariable method [.NET Framework debugging]
ms.assetid: 843c904a-8176-4d8f-bd47-b4d4c29f4c5c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bba8d887bc516149135aae61c4f9bdb9a9e0c9d9
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57470534"
---
# <a name="isymunmanagedwriterdefineglobalvariable-method"></a>ISymUnmanagedWriter::DefineGlobalVariable, méthode
Définit une variable globale unique.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineGlobalVariable(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      cSig,  
    [in, size_is(cSig)] unsigned char signature[],  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a>Paramètres  
 `name`  
 [in] Un pointeur vers un `WCHAR` qui définit le nom de variable global.  
  
 `attributes`  
 [in] Attributs de la variable globale.  
  
 `cSig`  
 [in] Un `ULONG32` qui indique la taille, en caractères, de la `signature` mémoire tampon.  
  
 `signature`  
 [in] La signature de variable globale.  
  
 `addrKind`  
 [in] Le type d’adresse.  
  
 `addr1`  
 [in] La première adresse de la spécification de paramètre.  
  
 `addr2`  
 [in] La deuxième adresse de la spécification de paramètre.  
  
 `addr3`  
 [in] Troisième adresse de la spécification de paramètre.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [DefineLocalVariable, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-definelocalvariable-method.md)
- [DefineGlobalVariable2, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineglobalvariable2-method.md)
