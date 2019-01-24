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
ms.openlocfilehash: d7a3fcd34f8cab6fa3c2949a4ee3270189b3dc77
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730033"
---
# <a name="isymunmanageddocumentwritersetchecksum-method"></a><span data-ttu-id="f8a80-102">ISymUnmanagedDocumentWriter::SetCheckSum, méthode</span><span class="sxs-lookup"><span data-stu-id="f8a80-102">ISymUnmanagedDocumentWriter::SetCheckSum Method</span></span>
<span data-ttu-id="f8a80-103">Définit les informations de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f8a80-103">Sets checksum information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8a80-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8a80-104">Syntax</span></span>  
  
```  
HRESULT SetCheckSum(  
    [in]  GUID     algorithmId,  
    [in]  ULONG32  checkSumSize,  
    [in, size_is(checkSumSize)]  BYTE checkSum[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f8a80-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8a80-105">Parameters</span></span>  
 `algorithmId`  
 <span data-ttu-id="f8a80-106">[in] GUID qui représente l’identificateur d’algorithme.</span><span class="sxs-lookup"><span data-stu-id="f8a80-106">[in] The GUID that represents the algorithm identifier.</span></span>  
  
 `checkSumSize`  
 <span data-ttu-id="f8a80-107">[in] Un `ULONG32` qui indique la taille, en octets, de la `checkSum` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f8a80-107">[in] A `ULONG32` that indicates the size, in bytes, of the `checkSum` buffer.</span></span>  
  
 `checkSum`  
 <span data-ttu-id="f8a80-108">[in] La mémoire tampon qui stocke les informations de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f8a80-108">[in] The buffer that stores the checksum information.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f8a80-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f8a80-109">Return Value</span></span>  
 <span data-ttu-id="f8a80-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f8a80-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f8a80-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8a80-111">Requirements</span></span>  
 <span data-ttu-id="f8a80-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f8a80-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8a80-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8a80-113">See also</span></span>
- [<span data-ttu-id="f8a80-114">ISymUnmanagedDocumentWriter, interface</span><span class="sxs-lookup"><span data-stu-id="f8a80-114">ISymUnmanagedDocumentWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)
