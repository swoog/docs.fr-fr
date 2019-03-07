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
ms.openlocfilehash: 7fe5686f516f967ffd182788add643387cb8af9a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473966"
---
# <a name="isymunmanageddocumentgetlanguage-method"></a><span data-ttu-id="2f79b-102">ISymUnmanagedDocument::GetLanguage, méthode</span><span class="sxs-lookup"><span data-stu-id="2f79b-102">ISymUnmanagedDocument::GetLanguage Method</span></span>
<span data-ttu-id="2f79b-103">Obtient l’identificateur de langue de ce document</span><span class="sxs-lookup"><span data-stu-id="2f79b-103">Gets the language identifier of this document</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f79b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f79b-104">Syntax</span></span>  
  
```  
HRESULT GetLanguage(  
    [out, retval]  GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2f79b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f79b-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="2f79b-106">[out] Pointeur vers une variable qui reçoit l’identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="2f79b-106">[out] A pointer to a variable that receives the language identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2f79b-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2f79b-107">Return Value</span></span>  
 <span data-ttu-id="2f79b-108">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="2f79b-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f79b-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f79b-109">See also</span></span>
- [<span data-ttu-id="2f79b-110">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="2f79b-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
