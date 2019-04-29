---
title: ISymUnmanagedDocumentWriter::SetSource, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocumentWriter.SetSource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocumentWriter::SetSource
helpviewer_keywords:
- ISymUnmanagedDocumentWriter::SetSource method [.NET Framework debugging]
- SetSource method [.NET Framework debugging]
ms.assetid: ea5b9d9f-ff06-4bd3-8de5-6435343aba59
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 64982308c6eb7e9df4b94b4e123857c65939f044
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939748"
---
# <a name="isymunmanageddocumentwritersetsource-method"></a><span data-ttu-id="65292-102">ISymUnmanagedDocumentWriter::SetSource, méthode</span><span class="sxs-lookup"><span data-stu-id="65292-102">ISymUnmanagedDocumentWriter::SetSource Method</span></span>
<span data-ttu-id="65292-103">Définit la source incorporée d’un document qui est en cours d’écriture.</span><span class="sxs-lookup"><span data-stu-id="65292-103">Sets embedded source for a document that is being written.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65292-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65292-104">Syntax</span></span>  
  
```  
HRESULT SetSource(  
    [in]  ULONG32  sourceSize,  
    [in, size_is(sourceSize)] BYTE  source[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="65292-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65292-105">Parameters</span></span>  
 `sourceSize`  
 <span data-ttu-id="65292-106">[in] Un `ULONG32` qui contient la taille de la `source` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="65292-106">[in] A `ULONG32` that contains the size of the `source` buffer.</span></span>  
  
 `source`  
 <span data-ttu-id="65292-107">[in] La mémoire tampon qui stocke la source incorporée.</span><span class="sxs-lookup"><span data-stu-id="65292-107">[in] The buffer that stores the embedded source.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="65292-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="65292-108">Return Value</span></span>  
 <span data-ttu-id="65292-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="65292-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65292-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65292-110">Requirements</span></span>  
 <span data-ttu-id="65292-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="65292-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65292-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65292-112">See also</span></span>

- [<span data-ttu-id="65292-113">ISymUnmanagedDocumentWriter, interface</span><span class="sxs-lookup"><span data-stu-id="65292-113">ISymUnmanagedDocumentWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)
