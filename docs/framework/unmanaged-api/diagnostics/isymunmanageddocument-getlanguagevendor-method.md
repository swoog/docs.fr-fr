---
title: ISymUnmanagedDocument::GetLanguageVendor, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetLanguageVendor
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetLanguageVendor
helpviewer_keywords:
- GetLanguageVendor method [.NET Framework debugging]
- ISymUnmanagedDocument::GetLanguageVendor method [.NET Framework debugging]
ms.assetid: 1d4b702e-4922-441d-8b44-03804284f70b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cd01dcbd45ecae84ccccffb510c20f580ae8c598
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59080807"
---
# <a name="isymunmanageddocumentgetlanguagevendor-method"></a><span data-ttu-id="0c55b-102">ISymUnmanagedDocument::GetLanguageVendor, méthode</span><span class="sxs-lookup"><span data-stu-id="0c55b-102">ISymUnmanagedDocument::GetLanguageVendor Method</span></span>
<span data-ttu-id="0c55b-103">Obtient le fournisseur de langage de ce document.</span><span class="sxs-lookup"><span data-stu-id="0c55b-103">Gets the language vendor of this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c55b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c55b-104">Syntax</span></span>  
  
```  
HRESULT GetLanguageVendor(  
    [out, retval]  GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0c55b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c55b-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="0c55b-106">[out] Pointeur vers une variable qui reçoit le fournisseur de langage.</span><span class="sxs-lookup"><span data-stu-id="0c55b-106">[out] A pointer to a variable that receives the language vendor.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0c55b-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0c55b-107">Return Value</span></span>  
 <span data-ttu-id="0c55b-108">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="0c55b-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c55b-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c55b-109">See also</span></span>

- [<span data-ttu-id="0c55b-110">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="0c55b-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
