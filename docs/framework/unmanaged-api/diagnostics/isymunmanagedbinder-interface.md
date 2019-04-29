---
title: ISymUnmanagedBinder, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder
helpviewer_keywords:
- ISymUnmanagedBinder interface [.NET Framework debugging]
ms.assetid: b22fbe19-b30f-4696-8175-e6b91da9edab
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b6d91f68ac737ce28cdbef926119bb3711bc1096
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940060"
---
# <a name="isymunmanagedbinder-interface"></a><span data-ttu-id="92505-102">ISymUnmanagedBinder, interface</span><span class="sxs-lookup"><span data-stu-id="92505-102">ISymUnmanagedBinder Interface</span></span>
<span data-ttu-id="92505-103">Représente un classeur de symboles du code non managé.</span><span class="sxs-lookup"><span data-stu-id="92505-103">Represents a symbol binder for unmanaged code.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="92505-104">Il est un risque de sécurité pour ouvrir un fichier du programme (PDB) de la base de données à partir d’une source non fiable.</span><span class="sxs-lookup"><span data-stu-id="92505-104">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="92505-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92505-105">Methods</span></span>  
  
|<span data-ttu-id="92505-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="92505-106">Method</span></span>|<span data-ttu-id="92505-107">Description</span><span class="sxs-lookup"><span data-stu-id="92505-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="92505-108">GetReaderForFile, méthode</span><span class="sxs-lookup"><span data-stu-id="92505-108">GetReaderForFile Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderforfile-method.md)|<span data-ttu-id="92505-109">Une interface de métadonnées et un nom de fichier, retourne le correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure qui lira les symboles de débogage associés au module.</span><span class="sxs-lookup"><span data-stu-id="92505-109">Given a metadata interface and a file name, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure that will read the debugging symbols associated with the module.</span></span>|  
|[<span data-ttu-id="92505-110">GetReaderFromStream, méthode</span><span class="sxs-lookup"><span data-stu-id="92505-110">GetReaderFromStream Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-getreaderfromstream-method.md)|<span data-ttu-id="92505-111">Une interface de métadonnées et un flux qui contient le magasin de symboles, retourne le correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure qui lira le débogage des symboles à partir du magasin de symboles donné.</span><span class="sxs-lookup"><span data-stu-id="92505-111">Given a metadata interface and a stream that contains the symbol store, returns the correct [ISymUnmanagedReader](isymunmanagedreader-interface.md) structure that will read the debugging symbols from the given symbol store.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="92505-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92505-112">Requirements</span></span>  
 <span data-ttu-id="92505-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="92505-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92505-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92505-114">See also</span></span>

- [<span data-ttu-id="92505-115">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="92505-115">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="92505-116">ISymUnmanagedBinder2, interface</span><span class="sxs-lookup"><span data-stu-id="92505-116">ISymUnmanagedBinder2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-interface.md)
- [<span data-ttu-id="92505-117">ISymUnmanagedBinder3, interface</span><span class="sxs-lookup"><span data-stu-id="92505-117">ISymUnmanagedBinder3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-interface.md)
