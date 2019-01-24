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
ms.openlocfilehash: 90f5924bc03a9896442fd61a4c618d18ed999faf
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54638871"
---
# <a name="isymunmanageddispose-interface"></a><span data-ttu-id="803b7-102">ISymUnmanagedDispose, interface</span><span class="sxs-lookup"><span data-stu-id="803b7-102">ISymUnmanagedDispose Interface</span></span>
<span data-ttu-id="803b7-103">Libère les ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="803b7-103">Disposes of unmanaged resources.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="803b7-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="803b7-104">Methods</span></span>  
  
|<span data-ttu-id="803b7-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="803b7-105">Method</span></span>|<span data-ttu-id="803b7-106">Description</span><span class="sxs-lookup"><span data-stu-id="803b7-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="803b7-107">Destroy, méthode</span><span class="sxs-lookup"><span data-stu-id="803b7-107">Destroy Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddispose-destroy-method.md)|<span data-ttu-id="803b7-108">Provoque l’objet sous-jacent libérer toutes les références internes et renvoient une erreur sur les appels de méthode suivants.</span><span class="sxs-lookup"><span data-stu-id="803b7-108">Causes the underlying object to release all internal references and return failure on any subsequent method calls.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="803b7-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="803b7-109">Requirements</span></span>  
 <span data-ttu-id="803b7-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="803b7-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="803b7-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="803b7-111">See also</span></span>
- [<span data-ttu-id="803b7-112">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="803b7-112">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
