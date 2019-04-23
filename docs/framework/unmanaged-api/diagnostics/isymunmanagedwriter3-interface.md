---
title: ISymUnmanagedWriter3, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3
helpviewer_keywords:
- ISymUnmanagedWriter3 interface [.NET Framework debugging]
ms.assetid: a034c21e-e371-4360-b470-29e88288948f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e26d79a5b597b8585f2fffd7f3945f00832ca134
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59138449"
---
# <a name="isymunmanagedwriter3-interface"></a><span data-ttu-id="a0529-102">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="a0529-102">ISymUnmanagedWriter3 Interface</span></span>
<span data-ttu-id="a0529-103">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="a0529-103">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="a0529-104">Cette interface étend la [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="a0529-104">This interface extends the [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a0529-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0529-105">Methods</span></span>  
  
|<span data-ttu-id="a0529-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0529-106">Method</span></span>|<span data-ttu-id="a0529-107">Description</span><span class="sxs-lookup"><span data-stu-id="a0529-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a0529-108">Commit, méthode</span><span class="sxs-lookup"><span data-stu-id="a0529-108">Commit Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-commit-method.md)|<span data-ttu-id="a0529-109">Valide les modifications écrites jusqu'à présent dans le flux.</span><span class="sxs-lookup"><span data-stu-id="a0529-109">Commits the changes written so far to the stream.</span></span>|  
|[<span data-ttu-id="a0529-110">OpenMethod2, méthode</span><span class="sxs-lookup"><span data-stu-id="a0529-110">OpenMethod2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-openmethod2-method.md)|<span data-ttu-id="a0529-111">Ouvre une méthode et fournit son décalage de la section réel dans l’image.</span><span class="sxs-lookup"><span data-stu-id="a0529-111">Opens a method and provides its real section offset in the image.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a0529-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0529-112">Requirements</span></span>  
 <span data-ttu-id="a0529-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="a0529-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0529-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0529-114">See also</span></span>

- [<span data-ttu-id="a0529-115">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="a0529-115">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="a0529-116">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="a0529-116">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="a0529-117">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="a0529-117">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)
