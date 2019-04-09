---
title: ISymUnmanagedWriter::CloseNamespace, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseNamespace
helpviewer_keywords:
- ISymUnmanagedWriter::CloseNamespace method [.NET Framework debugging]
- CloseNamespace method [.NET Framework debugging]
ms.assetid: 7f74d9c5-1377-4958-b842-6306d611cbd5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 66f8804c911e053758442670afb3c3f27d0f7453
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59130050"
---
# <a name="isymunmanagedwriterclosenamespace-method"></a><span data-ttu-id="477cc-102">ISymUnmanagedWriter::CloseNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="477cc-102">ISymUnmanagedWriter::CloseNamespace Method</span></span>
<span data-ttu-id="477cc-103">Espace de noms le plus récemment ouvert par se ferme.</span><span class="sxs-lookup"><span data-stu-id="477cc-103">Closes the most recently opened namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="477cc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="477cc-104">Syntax</span></span>  
  
```  
HRESULT CloseNamespace();  
```  
  
## <a name="return-value"></a><span data-ttu-id="477cc-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="477cc-105">Return Value</span></span>  
 <span data-ttu-id="477cc-106">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="477cc-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="477cc-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="477cc-107">Requirements</span></span>  
 <span data-ttu-id="477cc-108">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="477cc-108">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="477cc-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="477cc-109">See also</span></span>

- [<span data-ttu-id="477cc-110">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="477cc-110">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="477cc-111">OpenNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="477cc-111">OpenNamespace Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-opennamespace-method.md)
