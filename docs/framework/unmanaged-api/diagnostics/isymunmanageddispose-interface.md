---
title: ISymUnmanagedDispose, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDispose
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDispose
helpviewer_keywords:
- ISymUnmanagedDispose interface [.NET Framework debugging]
ms.assetid: b1d74e83-a200-4d00-8fbd-27918808616d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 973fc35bb99bea6b3302760763069b9df6c548e4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424402"
---
# <a name="isymunmanageddispose-interface"></a><span data-ttu-id="fc529-102">ISymUnmanagedDispose, interface</span><span class="sxs-lookup"><span data-stu-id="fc529-102">ISymUnmanagedDispose Interface</span></span>
<span data-ttu-id="fc529-103">Libère les ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="fc529-103">Disposes of unmanaged resources.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fc529-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fc529-104">Methods</span></span>  
  
|<span data-ttu-id="fc529-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="fc529-105">Method</span></span>|<span data-ttu-id="fc529-106">Description</span><span class="sxs-lookup"><span data-stu-id="fc529-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fc529-107">Destroy, méthode</span><span class="sxs-lookup"><span data-stu-id="fc529-107">Destroy Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddispose-destroy-method.md)|<span data-ttu-id="fc529-108">Provoque l’objet sous-jacent libérer toutes les références internes et retourne un échec sur tous les appels de méthode suivants.</span><span class="sxs-lookup"><span data-stu-id="fc529-108">Causes the underlying object to release all internal references and return failure on any subsequent method calls.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fc529-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fc529-109">Requirements</span></span>  
 <span data-ttu-id="fc529-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fc529-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc529-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc529-111">See Also</span></span>  
 [<span data-ttu-id="fc529-112">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="fc529-112">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
