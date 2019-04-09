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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59126332"
---
# <a name="isymunmanagedwriteropennamespace-method"></a><span data-ttu-id="95203-102">ISymUnmanagedWriter::OpenNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="95203-102">ISymUnmanagedWriter::OpenNamespace Method</span></span>
<span data-ttu-id="95203-103">Ouvre un nouvel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="95203-103">Opens a new namespace.</span></span> <span data-ttu-id="95203-104">Appelez cette méthode avant de définir des méthodes ou des variables qui occupent un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="95203-104">Call this method before defining methods or variables that occupy a namespace.</span></span> <span data-ttu-id="95203-105">Espaces de noms peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="95203-105">Namespaces can be nested.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95203-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95203-106">Syntax</span></span>  
  
```  
HRESULT OpenNamespace(  
    [in] const WCHAR *name);  
```  
  
## <a name="parameters"></a><span data-ttu-id="95203-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95203-107">Parameters</span></span>  
 `name`  
 <span data-ttu-id="95203-108">[in] Pointeur vers le nom du nouvel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="95203-108">[in] A pointer to the name of the new namespace.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="95203-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="95203-109">Return Value</span></span>  
 <span data-ttu-id="95203-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="95203-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="95203-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95203-111">Requirements</span></span>  
 <span data-ttu-id="95203-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="95203-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95203-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95203-113">See also</span></span>

- [<span data-ttu-id="95203-114">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="95203-114">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="95203-115">CloseNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="95203-115">CloseNamespace Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closenamespace-method.md)
