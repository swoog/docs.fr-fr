---
title: ISymUnmanagedWriter::Abort, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Abort
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Abort
helpviewer_keywords:
- ISymUnmanagedWriter::Abort method [.NET Framework debugging]
- Abort method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: 416b220f-38d4-48e0-bb49-d2faa7366702
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 090183cad17aff6faf5e79639eadff086c1a26ce
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59119533"
---
# <a name="isymunmanagedwriterabort-method"></a><span data-ttu-id="4ee34-102">ISymUnmanagedWriter::Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="4ee34-102">ISymUnmanagedWriter::Abort Method</span></span>
<span data-ttu-id="4ee34-103">Ferme le writer de symbole sans valider les symboles dans le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="4ee34-103">Closes the symbol writer without committing the symbols to the symbol store.</span></span> <span data-ttu-id="4ee34-104">Après cet appel, le writer de symbole devient non valide pour les nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="4ee34-104">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="4ee34-105">Pour valider les symboles et fermer le writer de symbole, utilisez le [ISymUnmanagedWriter::Close](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-close-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="4ee34-105">To commit the symbols and close the symbol writer, use the [ISymUnmanagedWriter::Close](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-close-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ee34-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ee34-106">Syntax</span></span>  
  
```  
HRESULT Abort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="4ee34-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4ee34-107">Return Value</span></span>  
 <span data-ttu-id="4ee34-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4ee34-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4ee34-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ee34-109">Requirements</span></span>  
 <span data-ttu-id="4ee34-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="4ee34-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ee34-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ee34-111">See also</span></span>

- [<span data-ttu-id="4ee34-112">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="4ee34-112">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
