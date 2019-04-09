---
title: ISymUnmanagedBinder2, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder2 Interface
helpviewer_keywords:
- ISymUnmanagedBinder2 interface [.NET Framework debugging]
ms.assetid: 7a59f405-73e8-4434-8bcc-a9dc45ea08e6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 38de9fa878db18222d2666ba86420ca856e4b121
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59199113"
---
# <a name="isymunmanagedbinder2-interface"></a><span data-ttu-id="f3baf-102">ISymUnmanagedBinder2, interface</span><span class="sxs-lookup"><span data-stu-id="f3baf-102">ISymUnmanagedBinder2 Interface</span></span>
<span data-ttu-id="f3baf-103">Représente un classeur de symboles du code non managé et étend le [ISymUnmanagedBinder](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="f3baf-103">Represents a symbol binder for unmanaged code, and extends the [ISymUnmanagedBinder](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md) interface.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="f3baf-104">Il est un risque de sécurité pour ouvrir un fichier du programme (PDB) de la base de données à partir d’une source non fiable.</span><span class="sxs-lookup"><span data-stu-id="f3baf-104">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f3baf-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f3baf-105">Methods</span></span>  
  
|<span data-ttu-id="f3baf-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="f3baf-106">Method</span></span>|<span data-ttu-id="f3baf-107">Description</span><span class="sxs-lookup"><span data-stu-id="f3baf-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f3baf-108">GetReaderForFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="f3baf-108">GetReaderForFile2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)|<span data-ttu-id="f3baf-109">Une interface de métadonnées et un nom de fichier, retourne le correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface qui lit les symboles de débogage associés au module.</span><span class="sxs-lookup"><span data-stu-id="f3baf-109">Given a metadata interface and a file name, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface that will read the debugging symbols associated with the module.</span></span> <span data-ttu-id="f3baf-110">Fournit une recherche plus étendue que le [ISymUnmanagedBinder::GetReaderForFile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f3baf-110">Provides a more extensive search than the [ISymUnmanagedBinder::GetReaderForFile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f3baf-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3baf-111">Requirements</span></span>  
 <span data-ttu-id="f3baf-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f3baf-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3baf-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3baf-113">See also</span></span>

- [<span data-ttu-id="f3baf-114">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="f3baf-114">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="f3baf-115">ISymUnmanagedBinder, interface</span><span class="sxs-lookup"><span data-stu-id="f3baf-115">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)
- [<span data-ttu-id="f3baf-116">ISymUnmanagedBinder3, interface</span><span class="sxs-lookup"><span data-stu-id="f3baf-116">ISymUnmanagedBinder3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)
