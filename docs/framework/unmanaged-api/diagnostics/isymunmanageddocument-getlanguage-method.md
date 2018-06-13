---
title: ISymUnmanagedDocument::GetLanguage, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetLanguage
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetLanguage
helpviewer_keywords:
- ISymUnmanagedDocument::GetLanguage method [.NET Framework debugging]
- GetLanguage method [.NET Framework debugging]
ms.assetid: c6639418-e9f2-4a99-8ce2-ec9876e0bc79
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 98c981a10a07d035300349cc8687b3201ed70927
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424295"
---
# <a name="isymunmanageddocumentgetlanguage-method"></a><span data-ttu-id="4b82c-102">ISymUnmanagedDocument::GetLanguage, méthode</span><span class="sxs-lookup"><span data-stu-id="4b82c-102">ISymUnmanagedDocument::GetLanguage Method</span></span>
<span data-ttu-id="4b82c-103">Obtient l’identificateur de langue de ce document</span><span class="sxs-lookup"><span data-stu-id="4b82c-103">Gets the language identifier of this document</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b82c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b82c-104">Syntax</span></span>  
  
```  
HRESULT GetLanguage(  
    [out, retval]  GUID*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4b82c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b82c-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="4b82c-106">[out] Pointeur vers une variable qui reçoit l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="4b82c-106">[out] A pointer to a variable that receives the language identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4b82c-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4b82c-107">Return Value</span></span>  
 <span data-ttu-id="4b82c-108">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="4b82c-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b82c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b82c-109">See Also</span></span>  
 [<span data-ttu-id="4b82c-110">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="4b82c-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
