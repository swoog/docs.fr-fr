---
title: ISymUnmanagedDocument::GetDocumentType, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetDocumentType
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetDocumentType
helpviewer_keywords:
- ISymUnmanagedDocument::GetDocumentType method [.NET Framework debugging]
- GetDocumentType method [.NET Framework debugging]
ms.assetid: 2d381ab1-7e7c-4281-af2b-e54d879b3ef8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7694c9b736700466ac1299b9632440e133109288
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939891"
---
# <a name="isymunmanageddocumentgetdocumenttype-method"></a><span data-ttu-id="23ce5-102">ISymUnmanagedDocument::GetDocumentType, méthode</span><span class="sxs-lookup"><span data-stu-id="23ce5-102">ISymUnmanagedDocument::GetDocumentType Method</span></span>
<span data-ttu-id="23ce5-103">Obtient le type de document de ce document.</span><span class="sxs-lookup"><span data-stu-id="23ce5-103">Gets the document type of this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="23ce5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23ce5-104">Syntax</span></span>  
  
```  
HRESULT GetDocumentType(  
    [out, retval] GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="23ce5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23ce5-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="23ce5-106">[out] Pointeur vers une variable qui reçoit le type de document.</span><span class="sxs-lookup"><span data-stu-id="23ce5-106">[out] Pointer to a variable that receives the document type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="23ce5-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="23ce5-107">Return Value</span></span>  
 <span data-ttu-id="23ce5-108">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="23ce5-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23ce5-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23ce5-109">See also</span></span>

- [<span data-ttu-id="23ce5-110">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="23ce5-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
