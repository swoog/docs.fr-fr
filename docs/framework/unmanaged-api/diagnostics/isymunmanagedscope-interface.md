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
ms.openlocfilehash: 6305338a95d7710a5feda2dc4c89e5a92262514c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33428711"
---
# <a name="isymunmanagedscope-interface"></a><span data-ttu-id="ba2e2-102">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="ba2e2-102">ISymUnmanagedScope Interface</span></span>
<span data-ttu-id="ba2e2-103">Représente une portée lexicale dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-103">Represents a lexical scope within a method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="ba2e2-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ba2e2-104">Methods</span></span>  
  
|<span data-ttu-id="ba2e2-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-105">Method</span></span>|<span data-ttu-id="ba2e2-106">Description</span><span class="sxs-lookup"><span data-stu-id="ba2e2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="ba2e2-107">GetChildren, méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-107">GetChildren Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getchildren-method.md)|<span data-ttu-id="ba2e2-108">Obtient les enfants de cette étendue.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-108">Gets the children of this scope.</span></span>|  
|[<span data-ttu-id="ba2e2-109">GetEndOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-109">GetEndOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getendoffset-method.md)|<span data-ttu-id="ba2e2-110">Obtient l’offset de fin pour cette étendue.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-110">Gets the end offset for this scope.</span></span>|  
|[<span data-ttu-id="ba2e2-111">GetLocalCount, méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-111">GetLocalCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getlocalcount-method.md)|<span data-ttu-id="ba2e2-112">Obtient le nombre de variables locales définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-112">Gets a count of the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="ba2e2-113">GetLocals, méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-113">GetLocals Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getlocals-method.md)|<span data-ttu-id="ba2e2-114">Obtient les variables locales définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-114">Gets the local variables defined within this scope.</span></span>|  
|[<span data-ttu-id="ba2e2-115">GetMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-115">GetMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getmethod-method.md)|<span data-ttu-id="ba2e2-116">Obtient la méthode qui contient cette portée.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-116">Gets the method that contains this scope.</span></span>|  
|[<span data-ttu-id="ba2e2-117">GetNamespaces, méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-117">GetNamespaces Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getnamespaces-method.md)|<span data-ttu-id="ba2e2-118">Obtient les espaces de noms qui sont utilisés dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-118">Gets the namespaces that are being used within this scope.</span></span>|  
|[<span data-ttu-id="ba2e2-119">GetParent, méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-119">GetParent Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getparent-method.md)|<span data-ttu-id="ba2e2-120">Obtient la portée parent de cette étendue.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-120">Gets the parent scope of this scope.</span></span>|  
|[<span data-ttu-id="ba2e2-121">GetStartOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="ba2e2-121">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getstartoffset-method.md)|<span data-ttu-id="ba2e2-122">Obtient l’offset de début pour cette étendue.</span><span class="sxs-lookup"><span data-stu-id="ba2e2-122">Gets the start offset for this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ba2e2-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ba2e2-123">Requirements</span></span>  
 <span data-ttu-id="ba2e2-124">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ba2e2-124">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba2e2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba2e2-125">See Also</span></span>  
 [<span data-ttu-id="ba2e2-126">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="ba2e2-126">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [<span data-ttu-id="ba2e2-127">ISymUnmanagedScope2, interface</span><span class="sxs-lookup"><span data-stu-id="ba2e2-127">ISymUnmanagedScope2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)
