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
ms.openlocfilehash: 4cf0fbcbf6af53c6a7865e2a2cf7874ea44581e4
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57474616"
---
# <a name="isymunmanagedwriteropennamespace-method"></a><span data-ttu-id="b7dad-102">ISymUnmanagedWriter::OpenNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="b7dad-102">ISymUnmanagedWriter::OpenNamespace Method</span></span>
<span data-ttu-id="b7dad-103">Ouvre un nouvel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b7dad-103">Opens a new namespace.</span></span> <span data-ttu-id="b7dad-104">Appelez cette méthode avant de définir des méthodes ou des variables qui occupent un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b7dad-104">Call this method before defining methods or variables that occupy a namespace.</span></span> <span data-ttu-id="b7dad-105">Espaces de noms peuvent être imbriquées.</span><span class="sxs-lookup"><span data-stu-id="b7dad-105">Namespaces can be nested.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7dad-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7dad-106">Syntax</span></span>  
  
```  
HRESULT OpenNamespace(  
    [in] const WCHAR *name);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7dad-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7dad-107">Parameters</span></span>  
 `name`  
 <span data-ttu-id="b7dad-108">[in] Pointeur vers le nom du nouvel espace de noms.</span><span class="sxs-lookup"><span data-stu-id="b7dad-108">[in] A pointer to the name of the new namespace.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b7dad-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b7dad-109">Return Value</span></span>  
 <span data-ttu-id="b7dad-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b7dad-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7dad-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7dad-111">Requirements</span></span>  
 <span data-ttu-id="b7dad-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b7dad-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7dad-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7dad-113">See also</span></span>
- [<span data-ttu-id="b7dad-114">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="b7dad-114">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="b7dad-115">CloseNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="b7dad-115">CloseNamespace Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closenamespace-method.md)
