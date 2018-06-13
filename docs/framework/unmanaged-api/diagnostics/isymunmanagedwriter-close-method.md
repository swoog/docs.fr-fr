---
title: ISymUnmanagedWriter::Close, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Close
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Close
helpviewer_keywords:
- Close method, ISymUnmanagedWriter interface [.NET Framework debugging]
- ISymUnmanagedWriter::Close method [.NET Framework debugging]
ms.assetid: 4cce59e1-80b9-4fc4-b3aa-126f1c5876bc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 30747fa25528f5679264ebfb67addf401b7d01d9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426327"
---
# <a name="isymunmanagedwriterclose-method"></a><span data-ttu-id="73fcb-102">ISymUnmanagedWriter::Close, méthode</span><span class="sxs-lookup"><span data-stu-id="73fcb-102">ISymUnmanagedWriter::Close Method</span></span>
<span data-ttu-id="73fcb-103">Ferme le writer de symbole après avoir validé les symboles dans le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="73fcb-103">Closes the symbol writer after committing the symbols to the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="73fcb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73fcb-104">Syntax</span></span>  
  
```  
HRESULT Close();  
```  
  
## <a name="return-value"></a><span data-ttu-id="73fcb-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="73fcb-105">Return Value</span></span>  
 <span data-ttu-id="73fcb-106">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="73fcb-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="73fcb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="73fcb-107">Remarks</span></span>  
 <span data-ttu-id="73fcb-108">Après cet appel, le writer de symbole devient non valide pour les autres mises à jour.</span><span class="sxs-lookup"><span data-stu-id="73fcb-108">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="73fcb-109">Pour fermer le writer de symbole sans valider les symboles, utilisez le [ISymUnmanagedWriter::Abort](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-abort-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="73fcb-109">To close the symbol writer without committing the symbols, use the [ISymUnmanagedWriter::Abort](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-abort-method.md) method instead.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="73fcb-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="73fcb-110">Requirements</span></span>  
 <span data-ttu-id="73fcb-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="73fcb-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="73fcb-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73fcb-112">See Also</span></span>  
 [<span data-ttu-id="73fcb-113">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="73fcb-113">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
