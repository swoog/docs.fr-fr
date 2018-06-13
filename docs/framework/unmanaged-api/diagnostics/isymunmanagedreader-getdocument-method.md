---
title: ISymUnmanagedReader::GetDocument, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetDocument
helpviewer_keywords:
- ISymUnmanagedReader::GetDocument method [.NET Framework debugging]
- GetDocument method [.NET Framework debugging]
ms.assetid: bb203853-6a6d-4027-b9e9-603a7f28b9d3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 45548fcd85e58086c2a43ac33e739c8ccb0e833f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33428079"
---
# <a name="isymunmanagedreadergetdocument-method"></a><span data-ttu-id="715b2-102">ISymUnmanagedReader::GetDocument, méthode</span><span class="sxs-lookup"><span data-stu-id="715b2-102">ISymUnmanagedReader::GetDocument Method</span></span>
<span data-ttu-id="715b2-103">Recherche d’un document.</span><span class="sxs-lookup"><span data-stu-id="715b2-103">Finds a document.</span></span> <span data-ttu-id="715b2-104">Le langage du document, le fournisseur et le type sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="715b2-104">The document language, vendor, and type are optional.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="715b2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="715b2-105">Syntax</span></span>  
  
```  
HRESULT GetDocument (  
    [in]  WCHAR  *url,  
    [in]  GUID   language,  
    [in]  GUID   languageVendor,  
    [in]  GUID   documentType,  
    [out, retval] ISymUnmanagedDocument** pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="715b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="715b2-106">Parameters</span></span>  
 `url`  
 <span data-ttu-id="715b2-107">[in] L’URL qui identifie le document.</span><span class="sxs-lookup"><span data-stu-id="715b2-107">[in] The URL that identifies the document.</span></span>  
  
 `language`  
 <span data-ttu-id="715b2-108">[in] Le langage du document.</span><span class="sxs-lookup"><span data-stu-id="715b2-108">[in] The document language.</span></span> <span data-ttu-id="715b2-109">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="715b2-109">This parameter is optional.</span></span>  
  
 `languageVendor`  
 <span data-ttu-id="715b2-110">[in] L’identité du fournisseur de langage du document.</span><span class="sxs-lookup"><span data-stu-id="715b2-110">[in] The identity of the vendor for the document language.</span></span> <span data-ttu-id="715b2-111">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="715b2-111">This parameter is optional.</span></span>  
  
 `documentType`  
 <span data-ttu-id="715b2-112">[in] Le type du document.</span><span class="sxs-lookup"><span data-stu-id="715b2-112">[in] The type of the document.</span></span> <span data-ttu-id="715b2-113">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="715b2-113">This parameter is optional.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="715b2-114">[out] Pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="715b2-114">[out] A pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="715b2-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="715b2-115">Return Value</span></span>  
 <span data-ttu-id="715b2-116">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="715b2-116">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="715b2-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="715b2-117">Requirements</span></span>  
 <span data-ttu-id="715b2-118">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="715b2-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="715b2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="715b2-119">See Also</span></span>  
 [<span data-ttu-id="715b2-120">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="715b2-120">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
