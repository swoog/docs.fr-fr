---
title: ISymUnmanagedWriter::CloseScope, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseScope
helpviewer_keywords:
- CloseScope method [.NET Framework debugging]
- ISymUnmanagedWriter::CloseScope method [.NET Framework debugging]
ms.assetid: 6dade525-7770-4cb4-bafd-4bb995ad0d87
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 250e58e4153edbee5c327ad46ecde73e94b83584
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468713"
---
# <a name="isymunmanagedwriterclosescope-method"></a>ISymUnmanagedWriter::CloseScope, méthode
Ferme la portée lexicale actuelle.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CloseScope(  
    [in] ULONG32 endOffset);  
```  
  
## <a name="parameters"></a>Paramètres  
 `endOffset`  
 [in] Le décalage à partir du début de la méthode du point à la fin de la dernière instruction dans la portée lexicale, en octets.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="remarks"></a>Notes  
 Une fois qu’une portée est fermée, plus aucune variable ne peut être définie qu’il contient.  
  
 [ISymUnmanagedWriter::OpenScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md) retourne un identificateur de portée opaque qui peut être utilisé avec [ISymUnmanagedWriter::SetScopeRange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md) pour définir ultérieurement une étendue de démarrage et de fin de décalage. Dans ce cas, les offsets passés à `ISymUnmanagedWriter::OpenScope` et `ISymUnmanagedWriter::CloseScope` sont ignorés. Les identificateurs de portée sont valides uniquement dans la méthode actuelle.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi
- [ISymUnmanagedWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
