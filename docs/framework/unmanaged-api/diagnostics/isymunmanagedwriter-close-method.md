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
ms.openlocfilehash: 780c19acd3d6980c0fb3e31d01e569a61fd04d6d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647307"
---
# <a name="isymunmanagedwriterclose-method"></a><span data-ttu-id="0eef6-102">ISymUnmanagedWriter::Close, méthode</span><span class="sxs-lookup"><span data-stu-id="0eef6-102">ISymUnmanagedWriter::Close Method</span></span>
<span data-ttu-id="0eef6-103">Ferme le writer de symbole après avoir validé les symboles dans le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="0eef6-103">Closes the symbol writer after committing the symbols to the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0eef6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0eef6-104">Syntax</span></span>  
  
```  
HRESULT Close();  
```  
  
## <a name="return-value"></a><span data-ttu-id="0eef6-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0eef6-105">Return Value</span></span>  
 <span data-ttu-id="0eef6-106">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0eef6-106">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0eef6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0eef6-107">Remarks</span></span>  
 <span data-ttu-id="0eef6-108">Après cet appel, le writer de symbole devient non valide pour les nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="0eef6-108">After this call, the symbol writer becomes invalid for further updates.</span></span> <span data-ttu-id="0eef6-109">Pour fermer le writer de symbole sans valider les symboles, utilisez le [ISymUnmanagedWriter::Abort](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-abort-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="0eef6-109">To close the symbol writer without committing the symbols, use the [ISymUnmanagedWriter::Abort](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-abort-method.md) method instead.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0eef6-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0eef6-110">Requirements</span></span>  
 <span data-ttu-id="0eef6-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="0eef6-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0eef6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0eef6-112">See also</span></span>
- [<span data-ttu-id="0eef6-113">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="0eef6-113">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
