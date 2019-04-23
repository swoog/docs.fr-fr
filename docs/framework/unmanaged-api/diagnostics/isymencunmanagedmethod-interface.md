---
title: ISymENCUnmanagedMethod, interface
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod
helpviewer_keywords:
- ISymENCUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: faebf594-67d5-4abf-b9c1-547fd3a1ff87
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4474269688094ea6c81b06659727acfb9c2ad6c3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59095709"
---
# <a name="isymencunmanagedmethod-interface"></a><span data-ttu-id="a0ed6-102">ISymENCUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="a0ed6-102">ISymENCUnmanagedMethod Interface</span></span>
<span data-ttu-id="a0ed6-103">Fournit des informations pour la fonctionnalité Modifier & Continuer.</span><span class="sxs-lookup"><span data-stu-id="a0ed6-103">Provides information for the Edit and Continue feature.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a0ed6-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0ed6-104">Methods</span></span>  
  
|<span data-ttu-id="a0ed6-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0ed6-105">Method</span></span>|<span data-ttu-id="a0ed6-106">Description</span><span class="sxs-lookup"><span data-stu-id="a0ed6-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a0ed6-107">GetDocumentsForMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="a0ed6-107">GetDocumentsForMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-getdocumentsformethod-method.md)|<span data-ttu-id="a0ed6-108">Obtient les documents de cette méthode a des lignes.</span><span class="sxs-lookup"><span data-stu-id="a0ed6-108">Gets the documents that this method has lines in.</span></span>|  
|[<span data-ttu-id="a0ed6-109">GetDocumentsForMethodCount, méthode</span><span class="sxs-lookup"><span data-stu-id="a0ed6-109">GetDocumentsForMethodCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-getdocumentsformethodcount-method.md)|<span data-ttu-id="a0ed6-110">Obtient le nombre de documents que cette méthode a des lignes.</span><span class="sxs-lookup"><span data-stu-id="a0ed6-110">Gets the number of documents that this method has lines in.</span></span>|  
|[<span data-ttu-id="a0ed6-111">GetFileNameFromOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="a0ed6-111">GetFileNameFromOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-getfilenamefromoffset-method.md)|<span data-ttu-id="a0ed6-112">Obtient le nom de fichier pour la ligne associée à un décalage.</span><span class="sxs-lookup"><span data-stu-id="a0ed6-112">Gets the file name for the line associated with an offset.</span></span>|  
|[<span data-ttu-id="a0ed6-113">GetLineFromOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="a0ed6-113">GetLineFromOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-getlinefromoffset-method.md)|<span data-ttu-id="a0ed6-114">Obtient les informations de ligne associées à un décalage.</span><span class="sxs-lookup"><span data-stu-id="a0ed6-114">Gets the line information associated with an offset.</span></span>|  
|[<span data-ttu-id="a0ed6-115">GetSourceExtentInDocument, méthode</span><span class="sxs-lookup"><span data-stu-id="a0ed6-115">GetSourceExtentInDocument Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-getsourceextentindocument-method.md)|<span data-ttu-id="a0ed6-116">Obtient le plus petit de début et plus grande fin ligne pour la méthode dans un document spécifique.</span><span class="sxs-lookup"><span data-stu-id="a0ed6-116">Gets the smallest start line and largest end line for the method in a specific document.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a0ed6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0ed6-117">Requirements</span></span>  
 <span data-ttu-id="a0ed6-118">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="a0ed6-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a0ed6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0ed6-119">See also</span></span>

- [<span data-ttu-id="a0ed6-120">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="a0ed6-120">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
