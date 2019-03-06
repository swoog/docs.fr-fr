---
title: ISymUnmanagedWriter3::Commit, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3.Commit
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3::Commit
helpviewer_keywords:
- Commit method, ISymUnmanagedWriter3 interface [.NET Framework debugging]
- ISymUnmanagedWriter3::Commit method [.NET Framework debugging]
ms.assetid: f6961922-46ec-4d2c-8369-85f880731f37
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 38d9c3eeb5cdb8b15ef5306a641910f2f4bcc9cf
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57372345"
---
# <a name="isymunmanagedwriter3commit-method"></a><span data-ttu-id="e3c97-102">ISymUnmanagedWriter3::Commit, méthode</span><span class="sxs-lookup"><span data-stu-id="e3c97-102">ISymUnmanagedWriter3::Commit Method</span></span>
<span data-ttu-id="e3c97-103">Valide les modifications écrites jusqu'à présent dans le flux.</span><span class="sxs-lookup"><span data-stu-id="e3c97-103">Commits the changes written so far to the stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3c97-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3c97-104">Syntax</span></span>  
  
```  
HRESULT Commit();  
```  
  
## <a name="return-value"></a><span data-ttu-id="e3c97-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e3c97-105">Return Value</span></span>  
 <span data-ttu-id="e3c97-106">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e3c97-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3c97-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e3c97-107">Requirements</span></span>  
 <span data-ttu-id="e3c97-108">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e3c97-108">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3c97-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3c97-109">See also</span></span>
- [<span data-ttu-id="e3c97-110">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="e3c97-110">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
