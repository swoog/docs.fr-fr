---
title: ISymENCUnmanagedMethod::GetLineFromOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetLineFromOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetLineFromOffset
helpviewer_keywords:
- GetLineFromOffset method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetLineFromOffset method [.NET Framework debugging]
ms.assetid: cc09bad2-fb34-4d13-a521-6ec7b1a1d915
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 29990ad6a94f063577236bdbc84d02d4d2b4b2f9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426131"
---
# <a name="isymencunmanagedmethodgetlinefromoffset-method"></a>ISymENCUnmanagedMethod::GetLineFromOffset, méthode
Obtient les informations de ligne associées à un offset. Si le paramètre d’offset (`dwOffset`) n’est pas un point de séquence, cette méthode obtient les informations de ligne associées à l’offset précédent.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetLineFromOffset(  
     [in]  ULONG32   dwOffset,  
     [out] ULONG32*  pline,  
     [out] ULONG32*  pcolumn,  
     [out] ULONG32*  pendLine,  
     [out] ULONG32*  pendColumn,  
     [out] ULONG32*  pdwStartOffset);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `dwOffset`  
 [in] Un `ULONG32` qui contient le décalage.  
  
 `pline`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la ligne.  
  
 `pcolumn`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la colonne.  
  
 `pendLine`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la ligne de fin.  
  
 `pendColumn`  
 [out] Un pointeur vers un `ULONG32` qui reçoit la colonne de fin.  
  
 `pdwStartOffset`  
 [out] Un pointeur vers un `ULONG32` qui reçoit le point de séquence associé.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Spécifications  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi  
 [ISymENCUnmanagedMethod, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
