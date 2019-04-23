---
title: ISymUnmanagedWriter2, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2
helpviewer_keywords:
- ISymUnmanagedWriter2 interface [.NET Framework debugging]
ms.assetid: 8e78faa4-cf43-44fb-a91d-94d6df692a25
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 97df6d6ec9a446e89eef8a9f8a5e5e8ddc85c0f7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59127398"
---
# <a name="isymunmanagedwriter2-interface"></a><span data-ttu-id="fced7-102">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="fced7-102">ISymUnmanagedWriter2 Interface</span></span>
<span data-ttu-id="fced7-103">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="fced7-103">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="fced7-104">Cette interface étend la [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fced7-104">This interface extends the [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fced7-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fced7-105">Methods</span></span>  
  
|<span data-ttu-id="fced7-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="fced7-106">Method</span></span>|<span data-ttu-id="fced7-107">Description</span><span class="sxs-lookup"><span data-stu-id="fced7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fced7-108">DefineConstant2, méthode</span><span class="sxs-lookup"><span data-stu-id="fced7-108">DefineConstant2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineconstant2-method.md)|<span data-ttu-id="fced7-109">Définit un nom pour une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="fced7-109">Defines a name for a constant value.</span></span>|  
|[<span data-ttu-id="fced7-110">DefineGlobalVariable2, méthode</span><span class="sxs-lookup"><span data-stu-id="fced7-110">DefineGlobalVariable2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineglobalvariable2-method.md)|<span data-ttu-id="fced7-111">Définit une variable globale unique.</span><span class="sxs-lookup"><span data-stu-id="fced7-111">Defines a single global variable.</span></span>|  
|[<span data-ttu-id="fced7-112">DefineLocalVariable2, méthode</span><span class="sxs-lookup"><span data-stu-id="fced7-112">DefineLocalVariable2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-definelocalvariable2-method.md)|<span data-ttu-id="fced7-113">Définit une variable unique dans la portée lexicale actuelle.</span><span class="sxs-lookup"><span data-stu-id="fced7-113">Defines a single variable in the current lexical scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fced7-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fced7-114">Requirements</span></span>  
 <span data-ttu-id="fced7-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fced7-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fced7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fced7-116">See also</span></span>

- [<span data-ttu-id="fced7-117">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="fced7-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="fced7-118">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="fced7-118">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="fced7-119">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="fced7-119">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
