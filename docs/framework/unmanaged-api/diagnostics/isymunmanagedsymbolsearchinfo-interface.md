---
title: ISymUnmanagedSymbolSearchInfo, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo
helpviewer_keywords:
- ISymUnmanagedSymbolSearchInfo interface [.NET Framework debugging]
ms.assetid: 30817373-0a21-49c1-a0c4-8e8daeecb8db
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d573264bb7a3cac02dd41afacaa2bc4a6f9e6dcd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61944569"
---
# <a name="isymunmanagedsymbolsearchinfo-interface"></a><span data-ttu-id="b75c6-102">ISymUnmanagedSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="b75c6-102">ISymUnmanagedSymbolSearchInfo Interface</span></span>
<span data-ttu-id="b75c6-103">Fournit des méthodes permettant d’obtenir des informations sur le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="b75c6-103">Provides methods that get information about the search path.</span></span> <span data-ttu-id="b75c6-104">Obtenez cette interface en appelant `QueryInterface` sur un objet qui implémente le [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="b75c6-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b75c6-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b75c6-105">Methods</span></span>  
  
|<span data-ttu-id="b75c6-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="b75c6-106">Method</span></span>|<span data-ttu-id="b75c6-107">Description</span><span class="sxs-lookup"><span data-stu-id="b75c6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b75c6-108">GetHRESULT, méthode</span><span class="sxs-lookup"><span data-stu-id="b75c6-108">GetHRESULT Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-gethresult-method.md)|<span data-ttu-id="b75c6-109">Obtient le HRESULT.</span><span class="sxs-lookup"><span data-stu-id="b75c6-109">Gets the HRESULT.</span></span>|  
|[<span data-ttu-id="b75c6-110">GetSearchPath, méthode</span><span class="sxs-lookup"><span data-stu-id="b75c6-110">GetSearchPath Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-getsearchpath-method.md)|<span data-ttu-id="b75c6-111">Obtient le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="b75c6-111">Gets the search path.</span></span>|  
|[<span data-ttu-id="b75c6-112">GetSearchPathLength, méthode</span><span class="sxs-lookup"><span data-stu-id="b75c6-112">GetSearchPathLength Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-getsearchpathlength-method.md)|<span data-ttu-id="b75c6-113">Obtient la longueur de chemin d’accès de recherche.</span><span class="sxs-lookup"><span data-stu-id="b75c6-113">Gets the search path length.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b75c6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b75c6-114">Requirements</span></span>  
 <span data-ttu-id="b75c6-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b75c6-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b75c6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b75c6-116">See also</span></span>

- [<span data-ttu-id="b75c6-117">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="b75c6-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
