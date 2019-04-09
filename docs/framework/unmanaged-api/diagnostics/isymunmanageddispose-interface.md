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
ms.openlocfilehash: 8e81cea13fb8d25701ccbe163f112904baf47a9f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59143160"
---
# <a name="isymunmanageddispose-interface"></a><span data-ttu-id="68127-102">ISymUnmanagedDispose, interface</span><span class="sxs-lookup"><span data-stu-id="68127-102">ISymUnmanagedDispose Interface</span></span>
<span data-ttu-id="68127-103">Libère les ressources non managées.</span><span class="sxs-lookup"><span data-stu-id="68127-103">Disposes of unmanaged resources.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="68127-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="68127-104">Methods</span></span>  
  
|<span data-ttu-id="68127-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="68127-105">Method</span></span>|<span data-ttu-id="68127-106">Description</span><span class="sxs-lookup"><span data-stu-id="68127-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="68127-107">Destroy, méthode</span><span class="sxs-lookup"><span data-stu-id="68127-107">Destroy Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddispose-destroy-method.md)|<span data-ttu-id="68127-108">Provoque l’objet sous-jacent libérer toutes les références internes et renvoient une erreur sur les appels de méthode suivants.</span><span class="sxs-lookup"><span data-stu-id="68127-108">Causes the underlying object to release all internal references and return failure on any subsequent method calls.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="68127-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68127-109">Requirements</span></span>  
 <span data-ttu-id="68127-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="68127-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68127-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68127-111">See also</span></span>

- [<span data-ttu-id="68127-112">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="68127-112">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
