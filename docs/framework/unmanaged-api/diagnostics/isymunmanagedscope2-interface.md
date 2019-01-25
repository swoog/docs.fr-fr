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
ms.openlocfilehash: beb48835039f142ea1d9e18871f77ada1b6f4f3e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706311"
---
# <a name="isymunmanagedscope2-interface"></a><span data-ttu-id="83370-102">ISymUnmanagedScope2, interface</span><span class="sxs-lookup"><span data-stu-id="83370-102">ISymUnmanagedScope2 Interface</span></span>
<span data-ttu-id="83370-103">Représente une portée lexicale dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="83370-103">Represents a lexical scope within a method.</span></span> <span data-ttu-id="83370-104">Cette interface étend la [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface avec des méthodes qui obtiennent des informations sur les constantes définies dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="83370-104">This interface extends the [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface with methods that get information about constants defined within the scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="83370-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="83370-105">Methods</span></span>  
  
|<span data-ttu-id="83370-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="83370-106">Method</span></span>|<span data-ttu-id="83370-107">Description</span><span class="sxs-lookup"><span data-stu-id="83370-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="83370-108">GetConstantCount, méthode</span><span class="sxs-lookup"><span data-stu-id="83370-108">GetConstantCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-getconstantcount-method.md)|<span data-ttu-id="83370-109">Obtient le nombre de constantes définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="83370-109">Gets a count of the constants defined within this scope.</span></span>|  
|[<span data-ttu-id="83370-110">GetConstants, méthode</span><span class="sxs-lookup"><span data-stu-id="83370-110">GetConstants Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-getconstants-method.md)|<span data-ttu-id="83370-111">Obtient les variables constantes définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="83370-111">Gets the local constants defined within this scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="83370-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="83370-112">Requirements</span></span>  
 <span data-ttu-id="83370-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="83370-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83370-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83370-114">See also</span></span>
- [<span data-ttu-id="83370-115">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="83370-115">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="83370-116">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="83370-116">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
