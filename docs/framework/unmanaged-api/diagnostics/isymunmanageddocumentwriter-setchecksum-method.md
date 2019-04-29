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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939761"
---
# <a name="isymunmanageddocumentwritersetchecksum-method"></a><span data-ttu-id="2908d-102">ISymUnmanagedDocumentWriter::SetCheckSum, méthode</span><span class="sxs-lookup"><span data-stu-id="2908d-102">ISymUnmanagedDocumentWriter::SetCheckSum Method</span></span>
<span data-ttu-id="2908d-103">Définit les informations de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2908d-103">Sets checksum information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2908d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2908d-104">Syntax</span></span>  
  
```  
HRESULT SetCheckSum(  
    [in]  GUID     algorithmId,  
    [in]  ULONG32  checkSumSize,  
    [in, size_is(checkSumSize)]  BYTE checkSum[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2908d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2908d-105">Parameters</span></span>  
 `algorithmId`  
 <span data-ttu-id="2908d-106">[in] GUID qui représente l’identificateur d’algorithme.</span><span class="sxs-lookup"><span data-stu-id="2908d-106">[in] The GUID that represents the algorithm identifier.</span></span>  
  
 `checkSumSize`  
 <span data-ttu-id="2908d-107">[in] Un `ULONG32` qui indique la taille, en octets, de la `checkSum` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2908d-107">[in] A `ULONG32` that indicates the size, in bytes, of the `checkSum` buffer.</span></span>  
  
 `checkSum`  
 <span data-ttu-id="2908d-108">[in] La mémoire tampon qui stocke les informations de somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2908d-108">[in] The buffer that stores the checksum information.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2908d-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2908d-109">Return Value</span></span>  
 <span data-ttu-id="2908d-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2908d-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2908d-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2908d-111">Requirements</span></span>  
 <span data-ttu-id="2908d-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2908d-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2908d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2908d-113">See also</span></span>

- [<span data-ttu-id="2908d-114">ISymUnmanagedDocumentWriter, interface</span><span class="sxs-lookup"><span data-stu-id="2908d-114">ISymUnmanagedDocumentWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)
