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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207543"
---
# <a name="isymunmanagedsymbolsearchinfo-interface"></a><span data-ttu-id="d9663-102">ISymUnmanagedSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="d9663-102">ISymUnmanagedSymbolSearchInfo Interface</span></span>
<span data-ttu-id="d9663-103">Fournit des méthodes permettant d’obtenir des informations sur le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="d9663-103">Provides methods that get information about the search path.</span></span> <span data-ttu-id="d9663-104">Obtenez cette interface en appelant `QueryInterface` sur un objet qui implémente le [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="d9663-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d9663-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d9663-105">Methods</span></span>  
  
|<span data-ttu-id="d9663-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="d9663-106">Method</span></span>|<span data-ttu-id="d9663-107">Description</span><span class="sxs-lookup"><span data-stu-id="d9663-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d9663-108">GetHRESULT, méthode</span><span class="sxs-lookup"><span data-stu-id="d9663-108">GetHRESULT Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-gethresult-method.md)|<span data-ttu-id="d9663-109">Obtient le HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d9663-109">Gets the HRESULT.</span></span>|  
|[<span data-ttu-id="d9663-110">GetSearchPath, méthode</span><span class="sxs-lookup"><span data-stu-id="d9663-110">GetSearchPath Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-getsearchpath-method.md)|<span data-ttu-id="d9663-111">Obtient le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="d9663-111">Gets the search path.</span></span>|  
|[<span data-ttu-id="d9663-112">GetSearchPathLength, méthode</span><span class="sxs-lookup"><span data-stu-id="d9663-112">GetSearchPathLength Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-getsearchpathlength-method.md)|<span data-ttu-id="d9663-113">Obtient la longueur de chemin d’accès de recherche.</span><span class="sxs-lookup"><span data-stu-id="d9663-113">Gets the search path length.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d9663-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9663-114">Requirements</span></span>  
 <span data-ttu-id="d9663-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d9663-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9663-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9663-116">See also</span></span>

- [<span data-ttu-id="d9663-117">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="d9663-117">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
