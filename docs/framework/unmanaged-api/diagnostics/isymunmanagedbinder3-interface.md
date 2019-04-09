---
title: ISymUnmanagedBinder3, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedBinder3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedBinder3 Interface
helpviewer_keywords:
- ISymUnmanagedBinder3 interface [.NET Framework debugging]
ms.assetid: 37527a84-4b03-4f08-8135-94d898599089
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fdfd8e8fc419809a3a490639ada1c533f286fe8b
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59157506"
---
# <a name="isymunmanagedbinder3-interface"></a><span data-ttu-id="30ea5-102">ISymUnmanagedBinder3, interface</span><span class="sxs-lookup"><span data-stu-id="30ea5-102">ISymUnmanagedBinder3 Interface</span></span>
<span data-ttu-id="30ea5-103">Étend l’interface de classeur de symboles.</span><span class="sxs-lookup"><span data-stu-id="30ea5-103">Extends the symbol binder interface.</span></span> <span data-ttu-id="30ea5-104">Obtenez cette interface en appelant `QueryInterface` sur un objet qui implémente le `ISymUnmanagedBinder` interface.</span><span class="sxs-lookup"><span data-stu-id="30ea5-104">Obtain this interface by calling `QueryInterface` on an object that implements the `ISymUnmanagedBinder` interface.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="30ea5-105">Il est un risque de sécurité pour ouvrir un fichier du programme (PDB) de la base de données à partir d’une source non fiable.</span><span class="sxs-lookup"><span data-stu-id="30ea5-105">It is a security risk to open a program database (PDB) file from an untrusted source.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="30ea5-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="30ea5-106">Methods</span></span>  
  
|<span data-ttu-id="30ea5-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="30ea5-107">Method</span></span>|<span data-ttu-id="30ea5-108">Description</span><span class="sxs-lookup"><span data-stu-id="30ea5-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="30ea5-109">GetReaderFromCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="30ea5-109">GetReaderFromCallback Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder3-getreaderfromcallback-method.md)|<span data-ttu-id="30ea5-110">Permet à l’utilisateur d’implémenter ou de fournir via un rappel un `IID_IDiaReadExeAtRVACallback` ou `IID_IDiaReadExeAtOffsetCallback` pour obtenir les informations de répertoire de débogage de la mémoire</span><span class="sxs-lookup"><span data-stu-id="30ea5-110">Allows the user to implement or supply via callback either an `IID_IDiaReadExeAtRVACallback` or `IID_IDiaReadExeAtOffsetCallback` to obtain the Debug directory information from memory</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="30ea5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30ea5-111">Requirements</span></span>  
 <span data-ttu-id="30ea5-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="30ea5-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30ea5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30ea5-113">See also</span></span>

- [<span data-ttu-id="30ea5-114">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="30ea5-114">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="30ea5-115">ISymUnmanagedBinder, interface</span><span class="sxs-lookup"><span data-stu-id="30ea5-115">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)
- [<span data-ttu-id="30ea5-116">ISymUnmanagedBinder2, interface</span><span class="sxs-lookup"><span data-stu-id="30ea5-116">ISymUnmanagedBinder2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-interface.md)
