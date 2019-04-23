---
title: ISymUnmanagedReader::GetVariables, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetVariables
helpviewer_keywords:
- ISymUnmanagedReader::GetVariables method [.NET Framework debugging]
- GetVariables method, ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: 16dc49cb-2c60-4ac8-9c35-020e9afba3f8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 846ff76fb1073394cc27597c9a2015148581cc70
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59165098"
---
# <a name="isymunmanagedreadergetvariables-method"></a>ISymUnmanagedReader::GetVariables, méthode
Retourne une variable non locale, en fonction de son parent et son nom.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetVariables (  
    [in]  mdToken  parent,  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is (cVars),  
        length_is (*pcVars)] ISymUnmanagedVariable *pVars[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `parent`  
 [in] Le parent de la variable.  
  
 `cVars`  
 [in] Taille du tableau `pVars`.  
  
 `pcVars`  
 [out] Un pointeur vers la variable qui reçoit le nombre de variables retournées dans `pVars`.  
  
 `pVars`  
 [out] Pointeur vers la variable qui reçoit les variables.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedReader, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
