---
title: ISymUnmanagedScope, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope
helpviewer_keywords:
- ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 3db7a220-cfe9-4810-8ca8-a094bb8e0f5b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 809368ea19528a7ce00d4fcada06ef5724eb79a6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59228157"
---
# <a name="isymunmanagedscope-interface"></a><span data-ttu-id="d0a76-102">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="d0a76-102">ISymUnmanagedScope Interface</span></span>
<span data-ttu-id="d0a76-103">Représente une portée lexicale dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="d0a76-103">Represents a lexical scope within a method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d0a76-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d0a76-104">Methods</span></span>  
  
|<span data-ttu-id="d0a76-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-105">Method</span></span>|<span data-ttu-id="d0a76-106">Description</span><span class="sxs-lookup"><span data-stu-id="d0a76-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d0a76-107">GetChildren, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-107">GetChildren Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getchildren-method.md)|<span data-ttu-id="d0a76-108">Obtient les enfants de cette étendue.</span><span class="sxs-lookup"><span data-stu-id="d0a76-108">Gets the children of this scope.</span></span>|  
|[<span data-ttu-id="d0a76-109">GetEndOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-109">GetEndOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getendoffset-method.md)|<span data-ttu-id="d0a76-110">Obtient l’offset de fin pour cette étendue.</span><span class="sxs-lookup"><span data-stu-id="d0a76-110">Gets the end offset for this scope.</span></span>|  
|[<span data-ttu-id="d0a76-111">GetLocalCount, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-111">GetLocalCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getlocalcount-method.md)|<span data-ttu-id="d0a76-112">Obtient le nombre des variables locales définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="d0a76-112">Gets a count of the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="d0a76-113">GetLocals, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-113">GetLocals Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getlocals-method.md)|<span data-ttu-id="d0a76-114">Obtient les variables locales définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="d0a76-114">Gets the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="d0a76-115">GetMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-115">GetMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getmethod-method.md)|<span data-ttu-id="d0a76-116">Obtient la méthode qui contient cette étendue.</span><span class="sxs-lookup"><span data-stu-id="d0a76-116">Gets the method that contains this scope.</span></span>|  
|[<span data-ttu-id="d0a76-117">GetNamespaces, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-117">GetNamespaces Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getnamespaces-method.md)|<span data-ttu-id="d0a76-118">Obtient les espaces de noms qui sont utilisés dans cette étendue.</span><span class="sxs-lookup"><span data-stu-id="d0a76-118">Gets the namespaces that are being used within this scope.</span></span>|  
|[<span data-ttu-id="d0a76-119">GetParent, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-119">GetParent Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getparent-method.md)|<span data-ttu-id="d0a76-120">Obtient la portée parente de cette étendue.</span><span class="sxs-lookup"><span data-stu-id="d0a76-120">Gets the parent scope of this scope.</span></span>|  
|[<span data-ttu-id="d0a76-121">GetStartOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="d0a76-121">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getstartoffset-method.md)|<span data-ttu-id="d0a76-122">Obtient l’offset de début pour cette étendue.</span><span class="sxs-lookup"><span data-stu-id="d0a76-122">Gets the start offset for this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d0a76-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0a76-123">Requirements</span></span>  
 <span data-ttu-id="d0a76-124">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d0a76-124">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0a76-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0a76-125">See also</span></span>

- [<span data-ttu-id="d0a76-126">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="d0a76-126">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="d0a76-127">ISymUnmanagedScope2, interface</span><span class="sxs-lookup"><span data-stu-id="d0a76-127">ISymUnmanagedScope2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)
