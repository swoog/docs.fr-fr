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
ms.openlocfilehash: 5dce9653d3fef534ac6567e36a4c8213e13ab231
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429167"
---
# <a name="isymunmanagedsymbolsearchinfo-interface"></a><span data-ttu-id="fb3e6-102">ISymUnmanagedSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="fb3e6-102">ISymUnmanagedSymbolSearchInfo Interface</span></span>
<span data-ttu-id="fb3e6-103">Fournit des méthodes qui obtiennent des informations sur le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="fb3e6-103">Provides methods that get information about the search path.</span></span> <span data-ttu-id="fb3e6-104">Obtenez cette interface en appelant `QueryInterface` sur un objet qui implémente le [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fb3e6-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fb3e6-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fb3e6-105">Methods</span></span>  
  
|<span data-ttu-id="fb3e6-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="fb3e6-106">Method</span></span>|<span data-ttu-id="fb3e6-107">Description</span><span class="sxs-lookup"><span data-stu-id="fb3e6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fb3e6-108">GetHRESULT, méthode</span><span class="sxs-lookup"><span data-stu-id="fb3e6-108">GetHRESULT Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-gethresult-method.md)|<span data-ttu-id="fb3e6-109">Obtient la valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="fb3e6-109">Gets the HRESULT.</span></span>|  
|[<span data-ttu-id="fb3e6-110">GetSearchPath, méthode</span><span class="sxs-lookup"><span data-stu-id="fb3e6-110">GetSearchPath Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-getsearchpath-method.md)|<span data-ttu-id="fb3e6-111">Obtient le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="fb3e6-111">Gets the search path.</span></span>|  
|[<span data-ttu-id="fb3e6-112">GetSearchPathLength, méthode</span><span class="sxs-lookup"><span data-stu-id="fb3e6-112">GetSearchPathLength Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-getsearchpathlength-method.md)|<span data-ttu-id="fb3e6-113">Obtient la longueur de chemin d’accès de recherche.</span><span class="sxs-lookup"><span data-stu-id="fb3e6-113">Gets the search path length.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fb3e6-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fb3e6-114">Requirements</span></span>  
 <span data-ttu-id="fb3e6-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fb3e6-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb3e6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb3e6-116">See Also</span></span>  
 [<span data-ttu-id="fb3e6-117">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="fb3e6-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
