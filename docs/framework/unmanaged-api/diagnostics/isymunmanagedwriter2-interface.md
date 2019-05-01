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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61970194"
---
# <a name="isymunmanagedwriter2-interface"></a><span data-ttu-id="2ac74-102">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="2ac74-102">ISymUnmanagedWriter2 Interface</span></span>
<span data-ttu-id="2ac74-103">Représente un writer de symbole et fournit des méthodes pour définir des documents, les points de séquence, les portées lexicales et variables.</span><span class="sxs-lookup"><span data-stu-id="2ac74-103">Represents a symbol writer, and provides methods to define documents, sequence points, lexical scopes, and variables.</span></span> <span data-ttu-id="2ac74-104">Cette interface étend la [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="2ac74-104">This interface extends the [ISymUnmanagedWriter](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="2ac74-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2ac74-105">Methods</span></span>  
  
|<span data-ttu-id="2ac74-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="2ac74-106">Method</span></span>|<span data-ttu-id="2ac74-107">Description</span><span class="sxs-lookup"><span data-stu-id="2ac74-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="2ac74-108">DefineConstant2, méthode</span><span class="sxs-lookup"><span data-stu-id="2ac74-108">DefineConstant2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineconstant2-method.md)|<span data-ttu-id="2ac74-109">Définit un nom pour une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="2ac74-109">Defines a name for a constant value.</span></span>|  
|[<span data-ttu-id="2ac74-110">DefineGlobalVariable2, méthode</span><span class="sxs-lookup"><span data-stu-id="2ac74-110">DefineGlobalVariable2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineglobalvariable2-method.md)|<span data-ttu-id="2ac74-111">Définit une variable globale unique.</span><span class="sxs-lookup"><span data-stu-id="2ac74-111">Defines a single global variable.</span></span>|  
|[<span data-ttu-id="2ac74-112">DefineLocalVariable2, méthode</span><span class="sxs-lookup"><span data-stu-id="2ac74-112">DefineLocalVariable2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-definelocalvariable2-method.md)|<span data-ttu-id="2ac74-113">Définit une variable unique dans la portée lexicale actuelle.</span><span class="sxs-lookup"><span data-stu-id="2ac74-113">Defines a single variable in the current lexical scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2ac74-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ac74-114">Requirements</span></span>  
 <span data-ttu-id="2ac74-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2ac74-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ac74-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ac74-116">See also</span></span>

- [<span data-ttu-id="2ac74-117">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="2ac74-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="2ac74-118">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="2ac74-118">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="2ac74-119">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="2ac74-119">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
