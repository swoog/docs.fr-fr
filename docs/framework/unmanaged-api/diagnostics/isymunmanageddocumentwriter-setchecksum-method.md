---
title: ISymUnmanagedDocumentWriter::SetCheckSum, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocumentWriter.SetCheckSum
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocumentWriter::SetCheckSum
helpviewer_keywords:
- ISymUnmanagedDocumentWriter::SetCheckSum method [.NET Framework debugging]
- SetCheckSum method [.NET Framework debugging]
ms.assetid: c7e99879-421f-43ce-b193-34733cf30085
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ac3daccfade4f5ae10fe2ebbf83a7a11af34b89b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59196981"
---
# <a name="isymunmanageddocumentwritersetchecksum-method"></a>ISymUnmanagedDocumentWriter::SetCheckSum, méthode
Définit les informations de la somme de contrôle.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetCheckSum(  
    [in]  GUID     algorithmId,  
    [in]  ULONG32  checkSumSize,  
    [in, size_is(checkSumSize)]  BYTE checkSum[]);  
```  
  
## <a name="parameters"></a>Paramètres  
 `algorithmId`  
 [in] GUID qui représente l’identificateur d’algorithme.  
  
 `checkSumSize`  
 [in] Un `ULONG32` qui indique la taille, en octets, de la `checkSum` mémoire tampon.  
  
 `checkSum`  
 [in] La mémoire tampon qui stocke les informations de somme de contrôle.  
  
## <a name="return-value"></a>Valeur de retour  
 S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.  
  
## <a name="requirements"></a>Configuration requise  
 **En-tête :** CorSym.idl, CorSym.h  
  
## <a name="see-also"></a>Voir aussi

- [ISymUnmanagedDocumentWriter, interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)
