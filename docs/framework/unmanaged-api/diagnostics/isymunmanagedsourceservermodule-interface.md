---
title: ISymUnmanagedSourceServerModule, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSourceServerModule
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSourceServerModule
helpviewer_keywords:
- ISymUnmanagedSourceServerModule interface [.NET Framework debugging]
ms.assetid: a19b23bd-2061-476e-b67d-252f57404f8b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3ba81c208c4b49342c6a055e09ba898871db1851
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59157603"
---
# <a name="isymunmanagedsourceservermodule-interface"></a><span data-ttu-id="5e9f3-102">ISymUnmanagedSourceServerModule, interface</span><span class="sxs-lookup"><span data-stu-id="5e9f3-102">ISymUnmanagedSourceServerModule Interface</span></span>
<span data-ttu-id="5e9f3-103">Fournit des données du serveur source pour un module.</span><span class="sxs-lookup"><span data-stu-id="5e9f3-103">Provides source server data for a module.</span></span> <span data-ttu-id="5e9f3-104">Obtenez cette interface en appelant `QueryInterface` sur un objet qui implémente le [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="5e9f3-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="5e9f3-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5e9f3-105">Methods</span></span>  
  
|<span data-ttu-id="5e9f3-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="5e9f3-106">Method</span></span>|<span data-ttu-id="5e9f3-107">Description</span><span class="sxs-lookup"><span data-stu-id="5e9f3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5e9f3-108">GetSourceServerData, méthode</span><span class="sxs-lookup"><span data-stu-id="5e9f3-108">GetSourceServerData Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-getsourceserverdata-method.md)|<span data-ttu-id="5e9f3-109">Retourne les données du serveur source pour le module.</span><span class="sxs-lookup"><span data-stu-id="5e9f3-109">Returns the source server data for the module.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5e9f3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e9f3-110">Requirements</span></span>  
 <span data-ttu-id="5e9f3-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5e9f3-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e9f3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e9f3-112">See also</span></span>

- [<span data-ttu-id="5e9f3-113">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="5e9f3-113">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
