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
ms.openlocfilehash: 9e4e2cd49bdffd0a1293a5601cb44e4804e2b1ed
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33428952"
---
# <a name="isymunmanagedwriter3commit-method"></a><span data-ttu-id="f39e2-102">ISymUnmanagedWriter3::Commit, méthode</span><span class="sxs-lookup"><span data-stu-id="f39e2-102">ISymUnmanagedWriter3::Commit Method</span></span>
<span data-ttu-id="f39e2-103">Valide les modifications écrites jusqu'à présent dans le flux de données.</span><span class="sxs-lookup"><span data-stu-id="f39e2-103">Commits the changes written so far to the stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f39e2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f39e2-104">Syntax</span></span>  
  
```  
HRESULT Commit();  
```  
  
## <a name="return-value"></a><span data-ttu-id="f39e2-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f39e2-105">Return Value</span></span>  
 <span data-ttu-id="f39e2-106">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f39e2-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f39e2-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f39e2-107">Requirements</span></span>  
 <span data-ttu-id="f39e2-108">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f39e2-108">**Header:** CorSym.idl , CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f39e2-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f39e2-109">See Also</span></span>  
 [<span data-ttu-id="f39e2-110">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="f39e2-110">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
