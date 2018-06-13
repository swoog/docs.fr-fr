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
ms.openlocfilehash: 29501eeb6085dbc235112d98e8099fcfa4565000
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427793"
---
# <a name="isymunmanagedbinder2-interface"></a><span data-ttu-id="e740e-102">ISymUnmanagedBinder2, interface</span><span class="sxs-lookup"><span data-stu-id="e740e-102">ISymUnmanagedBinder2 Interface</span></span>
<span data-ttu-id="e740e-103">Représente un classeur de symboles pour le code non managé et étend la [ISymUnmanagedBinder](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="e740e-103">Represents a symbol binder for unmanaged code, and extends the [ISymUnmanagedBinder](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md) interface.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e740e-104">Il s’agit d’un risque de sécurité pour ouvrir un fichier du programme (PDB) de la base de données à partir d’une source non fiable.</span><span class="sxs-lookup"><span data-stu-id="e740e-104">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e740e-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e740e-105">Methods</span></span>  
  
|<span data-ttu-id="e740e-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="e740e-106">Method</span></span>|<span data-ttu-id="e740e-107">Description</span><span class="sxs-lookup"><span data-stu-id="e740e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e740e-108">GetReaderForFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="e740e-108">GetReaderForFile2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)|<span data-ttu-id="e740e-109">Une interface de métadonnées et un nom de fichier, retourne le correct <<!--zz xref:ISymUnmanagedReader --> `ISymUnmanagedReader`> interface qui lit les symboles de débogage associés au module.</span><span class="sxs-lookup"><span data-stu-id="e740e-109">Given a metadata interface and a file name, returns the correct <<!--zz xref:ISymUnmanagedReader --> `ISymUnmanagedReader`> interface that will read the debugging symbols associated with the module.</span></span> <span data-ttu-id="e740e-110">Fournit une recherche plus étendue que le [ISymUnmanagedBinder::GetReaderForFile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e740e-110">Provides a more extensive search than the [ISymUnmanagedBinder::GetReaderForFile](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md) method.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e740e-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e740e-111">Requirements</span></span>  
 <span data-ttu-id="e740e-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e740e-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e740e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e740e-113">See Also</span></span>  
 [<span data-ttu-id="e740e-114">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="e740e-114">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [<span data-ttu-id="e740e-115">ISymUnmanagedBinder, interface</span><span class="sxs-lookup"><span data-stu-id="e740e-115">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)  
 [<span data-ttu-id="e740e-116">ISymUnmanagedBinder3, interface</span><span class="sxs-lookup"><span data-stu-id="e740e-116">ISymUnmanagedBinder3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)
