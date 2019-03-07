---
title: ISymUnmanagedWriter::DefineDocument, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineDocument
helpviewer_keywords:
- ISymUnmanagedWriter::DefineDocument method [.NET Framework debugging]
- DefineDocument method [.NET Framework debugging]
ms.assetid: c3bf15b0-3250-4bbe-b9b5-c5d695289b6f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 41b27c8d545cce7051ca1507a6bd98b87a32468b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57499561"
---
# <a name="isymunmanagedwriterdefinedocument-method"></a><span data-ttu-id="4a4e2-102">ISymUnmanagedWriter::DefineDocument, méthode</span><span class="sxs-lookup"><span data-stu-id="4a4e2-102">ISymUnmanagedWriter::DefineDocument Method</span></span>
<span data-ttu-id="4a4e2-103">Définit un document source.</span><span class="sxs-lookup"><span data-stu-id="4a4e2-103">Defines a source document.</span></span> <span data-ttu-id="4a4e2-104">GUID sont fournies pour les langages connus, les fournisseurs et les types de documents.</span><span class="sxs-lookup"><span data-stu-id="4a4e2-104">GUIDs are provided for known languages, vendors, and document types.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a4e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a4e2-105">Syntax</span></span>  
  
```  
HRESULT DefineDocument(  
    [in]  const WCHAR  *url,  
    [in]  const GUID   *language,  
    [in]  const GUID   *languageVendor,  
    [in]  const GUID   *documentType,  
    [out, retval] ISymUnmanagedDocumentWriter**  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4a4e2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a4e2-106">Parameters</span></span>  
 `url`  
 <span data-ttu-id="4a4e2-107">[in] Un pointeur vers un `WCHAR` qui définit l’uniform resource locator (URL) qui identifie le document.</span><span class="sxs-lookup"><span data-stu-id="4a4e2-107">[in] A pointer to a `WCHAR` that defines the uniform resource locator (URL) that identifies the document.</span></span>  
  
 `language`  
 <span data-ttu-id="4a4e2-108">[in] Pointeur vers un GUID qui définit le langage du document.</span><span class="sxs-lookup"><span data-stu-id="4a4e2-108">[in] A pointer to a GUID that defines the document language.</span></span>  
  
 `languageVendor`  
 <span data-ttu-id="4a4e2-109">[in] Pointeur vers un GUID qui définit l’identité du fournisseur de langage du document.</span><span class="sxs-lookup"><span data-stu-id="4a4e2-109">[in] A pointer to a GUID that defines the identity of the vendor for the document language.</span></span>  
  
 `documentType`  
 <span data-ttu-id="4a4e2-110">[in] Pointeur vers un GUID qui définit le type du document.</span><span class="sxs-lookup"><span data-stu-id="4a4e2-110">[in] A pointer to a GUID that defines the type of the document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="4a4e2-111">[out] Un pointeur vers le texte retourné [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="4a4e2-111">[out] A pointer to the returned [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4a4e2-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4a4e2-112">Return Value</span></span>  
 <span data-ttu-id="4a4e2-113">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4a4e2-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a4e2-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4a4e2-114">Requirements</span></span>  
 <span data-ttu-id="4a4e2-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="4a4e2-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a4e2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a4e2-116">See also</span></span>
- [<span data-ttu-id="4a4e2-117">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="4a4e2-117">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
