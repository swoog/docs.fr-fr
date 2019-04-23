---
title: ISymUnmanagedWriter::OpenNamespace, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.OpenNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::OpenNamespace
helpviewer_keywords:
- ISymUnmanagedWriter::OpenNamespace method [.NET Framework debugging]
- OpenNamespace method [.NET Framework debugging]
ms.assetid: 426f4e4f-e60d-4ad1-b546-a10e3c55c283
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1585acce8bba0dff327c961f5e32ef6b46794401
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59126332"
---
# <a name="isymunmanagedwriteropennamespace-method"></a><span data-ttu-id="dfa9e-102">ISymUnmanagedWriter::OpenNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="dfa9e-102">ISymUnmanagedWriter::OpenNamespace Method</span></span>
<span data-ttu-id="dfa9e-103">Ouvre un nouvel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="dfa9e-103">Opens a new namespace.</span></span> <span data-ttu-id="dfa9e-104">Appelez cette méthode avant de définir des méthodes ou des variables qui occupent un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="dfa9e-104">Call this method before defining methods or variables that occupy a namespace.</span></span> <span data-ttu-id="dfa9e-105">Espaces de noms peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="dfa9e-105">Namespaces can be nested.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfa9e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfa9e-106">Syntax</span></span>  
  
```  
HRESULT OpenNamespace(  
    [in] const WCHAR *name);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dfa9e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfa9e-107">Parameters</span></span>  
 `name`  
 <span data-ttu-id="dfa9e-108">[in] Pointeur vers le nom du nouvel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="dfa9e-108">[in] A pointer to the name of the new namespace.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dfa9e-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dfa9e-109">Return Value</span></span>  
 <span data-ttu-id="dfa9e-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dfa9e-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dfa9e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfa9e-111">Requirements</span></span>  
 <span data-ttu-id="dfa9e-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="dfa9e-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfa9e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfa9e-113">See also</span></span>

- [<span data-ttu-id="dfa9e-114">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="dfa9e-114">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="dfa9e-115">CloseNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="dfa9e-115">CloseNamespace Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closenamespace-method.md)
