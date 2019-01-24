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
ms.openlocfilehash: b4c79cb3df37a9ed10e46567be63aad29fee37c4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550186"
---
# <a name="isymunmanagedwriterabort-method"></a><span data-ttu-id="b43ba-102">ISymUnmanagedWriter::Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="b43ba-102">ISymUnmanagedWriter::Abort Method</span></span>
<span data-ttu-id="b43ba-103">Ferme le writer de symbole sans valider les symboles dans le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="b43ba-103">Closes the symbol writer without committing the symbols to the symbol store.</span></span> <span data-ttu-id="b43ba-104">Après cet appel, le writer de symbole devient non valide pour les nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b43ba-104">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="b43ba-105">Pour valider les symboles et fermer le writer de symbole, utilisez le [ISymUnmanagedWriter::Close](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-close-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="b43ba-105">To commit the symbols and close the symbol writer, use the [ISymUnmanagedWriter::Close](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-close-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b43ba-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b43ba-106">Syntax</span></span>  
  
```  
HRESULT Abort();  
```  
  
## <a name="return-value"></a><span data-ttu-id="b43ba-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b43ba-107">Return Value</span></span>  
 <span data-ttu-id="b43ba-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b43ba-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b43ba-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b43ba-109">Requirements</span></span>  
 <span data-ttu-id="b43ba-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b43ba-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b43ba-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b43ba-111">See also</span></span>
- [<span data-ttu-id="b43ba-112">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="b43ba-112">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
