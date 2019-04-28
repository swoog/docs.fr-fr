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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61922133"
---
# <a name="isymunmanagedsourceservermodule-interface"></a><span data-ttu-id="79158-102">ISymUnmanagedSourceServerModule, interface</span><span class="sxs-lookup"><span data-stu-id="79158-102">ISymUnmanagedSourceServerModule Interface</span></span>
<span data-ttu-id="79158-103">Fournit des données du serveur source pour un module.</span><span class="sxs-lookup"><span data-stu-id="79158-103">Provides source server data for a module.</span></span> <span data-ttu-id="79158-104">Obtenez cette interface en appelant `QueryInterface` sur un objet qui implémente le [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="79158-104">Obtain this interface by calling `QueryInterface` on an object that implements the [ISymUnmanagedReader](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="79158-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="79158-105">Methods</span></span>  
  
|<span data-ttu-id="79158-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="79158-106">Method</span></span>|<span data-ttu-id="79158-107">Description</span><span class="sxs-lookup"><span data-stu-id="79158-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="79158-108">GetSourceServerData, méthode</span><span class="sxs-lookup"><span data-stu-id="79158-108">GetSourceServerData Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsourceservermodule-getsourceserverdata-method.md)|<span data-ttu-id="79158-109">Retourne les données du serveur source pour le module.</span><span class="sxs-lookup"><span data-stu-id="79158-109">Returns the source server data for the module.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="79158-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79158-110">Requirements</span></span>  
 <span data-ttu-id="79158-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="79158-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79158-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79158-112">See also</span></span>

- [<span data-ttu-id="79158-113">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="79158-113">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
