---
title: ISymUnmanagedScope2, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2
helpviewer_keywords:
- ISymUnmanagedScope2 interface [.NET Framework debugging]
ms.assetid: 2ed6a387-ba45-483e-9a1e-b0c69f67998b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a33d8b489551dc69542e1b12bcf83602ec5a2008
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427246"
---
# <a name="isymunmanagedscope2-interface"></a><span data-ttu-id="65691-102">ISymUnmanagedScope2, interface</span><span class="sxs-lookup"><span data-stu-id="65691-102">ISymUnmanagedScope2 Interface</span></span>
<span data-ttu-id="65691-103">Représente une portée lexicale dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="65691-103">Represents a lexical scope within a method.</span></span> <span data-ttu-id="65691-104">Cette interface étend la [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface avec des méthodes qui obtiennent des informations sur les constantes définies dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="65691-104">This interface extends the [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface with methods that get information about constants defined within the scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="65691-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="65691-105">Methods</span></span>  
  
|<span data-ttu-id="65691-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="65691-106">Method</span></span>|<span data-ttu-id="65691-107">Description</span><span class="sxs-lookup"><span data-stu-id="65691-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="65691-108">GetConstantCount, méthode</span><span class="sxs-lookup"><span data-stu-id="65691-108">GetConstantCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-getconstantcount-method.md)|<span data-ttu-id="65691-109">Obtient le nombre de l’une des constantes définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="65691-109">Gets a count of the constants defined within this scope.</span></span>|  
|[<span data-ttu-id="65691-110">GetConstants, méthode</span><span class="sxs-lookup"><span data-stu-id="65691-110">GetConstants Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-getconstants-method.md)|<span data-ttu-id="65691-111">Obtient les variables constantes définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="65691-111">Gets the local constants defined within this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="65691-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="65691-112">Requirements</span></span>  
 <span data-ttu-id="65691-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="65691-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65691-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65691-114">See Also</span></span>  
 [<span data-ttu-id="65691-115">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="65691-115">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [<span data-ttu-id="65691-116">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="65691-116">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
