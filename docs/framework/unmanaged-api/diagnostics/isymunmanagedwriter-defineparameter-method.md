---
title: ISymUnmanagedWriter::DefineParameter, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineParameter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineParameter
helpviewer_keywords:
- DefineParameter method [.NET Framework debugging]
- ISymUnmanagedWriter::DefineParameter method [.NET Framework debugging]
ms.assetid: a8e3dd32-6a44-4371-9a74-f417b11998c8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b552ef39c7f73aaa5cfeae4a313e329b267abf98
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54643388"
---
# <a name="isymunmanagedwriterdefineparameter-method"></a>ISymUnmanagedWriter::DefineParameter, méthode
Définit un paramètre unique dans la méthode actuelle. Le type de paramètre provient de la position du paramètre (séquence) au sein de la signature de la méthode.  
  
 Si les paramètres sont définis dans les métadonnées pour une méthode donnée, vous n’êtes pas obligé de les définir à nouveau à l’aide de cette méthode. Les lecteurs de symbole doivent vérifier les métadonnées normales pour les paramètres avant de vérifier le magasin de symboles.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT DefineParameter(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      sequence,  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `name`  
 [in] Le nom du paramètre.  
  
 `attributes`  
 [in] Les attributs de paramètre.  
  
 `sequence`  
 [in] La signature de paramètre.  
  
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
