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
ms.openlocfilehash: f531b96211a1dd6072d62937b9f93fc17f105d4d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59149043"
---
# <a name="isymunmanagedwriter3commit-method"></a><span data-ttu-id="77931-102">ISymUnmanagedWriter3::Commit, méthode</span><span class="sxs-lookup"><span data-stu-id="77931-102">ISymUnmanagedWriter3::Commit Method</span></span>
<span data-ttu-id="77931-103">Valide les modifications écrites jusqu'à présent dans le flux.</span><span class="sxs-lookup"><span data-stu-id="77931-103">Commits the changes written so far to the stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77931-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77931-104">Syntax</span></span>  
  
```  
HRESULT Commit();  
```  
  
## <a name="return-value"></a><span data-ttu-id="77931-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="77931-105">Return Value</span></span>  
 <span data-ttu-id="77931-106">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="77931-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77931-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77931-107">Requirements</span></span>  
 <span data-ttu-id="77931-108">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="77931-108">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="77931-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77931-109">See also</span></span>

- [<span data-ttu-id="77931-110">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="77931-110">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
