---
title: ISymUnmanagedReader::ReplaceSymbolStore, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.ReplaceSymbolStore
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::ReplaceSymbolStore
helpviewer_keywords:
- ReplaceSymbolStore method [.NET Framework debugging]
- ISymUnmanagedReader::ReplaceSymbolStore method [.NET Framework debugging]
ms.assetid: 43257761-8cb1-4eaf-8fb5-1f3980cb66cd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 03607cf96d73e96eef63fe62b86b50be02f34421
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33428200"
---
# <a name="isymunmanagedreaderreplacesymbolstore-method"></a>ISymUnmanagedReader::ReplaceSymbolStore, méthode
Remplace le magasin de symboles existant par un magasin de symboles delta. Cette méthode est similaire à la [UpdateSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-updatesymbolstore-method.md) (méthode), à ceci près que le delta donné opère un remplacement complet plutôt qu’une mise à jour.  
  
> [!NOTE]
>  Vous devez spécifier un seul de le `filename` ou `pIStream` paramètres, pas les deux. Si `filename` est spécifié, le magasin de symboles sera mise à jour avec les symboles dans ce fichier. Si `pIStream` est spécifié, le magasin sera mise à jour avec les données de la <xref:System.Runtime.InteropServices.ComTypes.IStream>.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT ReplaceSymbolStore (  
    [in] const WCHAR *filename,  
    [in] IStream *pIStream);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `filename`  
 [in] Le nom du fichier contenant le magasin de symboles.  
  
 `pIStream`  
 [in] Flux de fichier, utilisé comme alternative à le `filename` paramètre.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi  
 [ISymUnmanagedReader, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
