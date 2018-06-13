---
title: ISymUnmanagedDocument::FindClosestLine, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.FindClosestLine
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::FindClosestLine
helpviewer_keywords:
- FindClosestLine method [.NET Framework debugging]
- ISymUnmanagedDocument::FindClosestLine method [.NET Framework debugging]
ms.assetid: 628f2a04-e529-407d-841e-3b3da219a9cb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f31dad53f42fdd8f7ac3a0cb995b507ecc3590d5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424441"
---
# <a name="isymunmanageddocumentfindclosestline-method"></a><span data-ttu-id="e2926-102">ISymUnmanagedDocument::FindClosestLine, méthode</span><span class="sxs-lookup"><span data-stu-id="e2926-102">ISymUnmanagedDocument::FindClosestLine Method</span></span>
<span data-ttu-id="e2926-103">Retourne la ligne la plus proche qui est un point de séquence, en fonction d’une ligne dans ce document, qui peut être ou non un point de séquence.</span><span class="sxs-lookup"><span data-stu-id="e2926-103">Returns the closest line that is a sequence point, given a line in this document that may or may not be a sequence point.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2926-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2926-104">Syntax</span></span>  
  
```  
HRESULT FindClosestLine(  
    [in]  ULONG32  line,  
    [out, retval] ULONG32*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e2926-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2926-105">Parameters</span></span>  
 `line`  
 <span data-ttu-id="e2926-106">[in] Une ligne dans ce document.</span><span class="sxs-lookup"><span data-stu-id="e2926-106">[in] A line in this document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="e2926-107">[out] Pointeur vers une variable qui reçoit la ligne.</span><span class="sxs-lookup"><span data-stu-id="e2926-107">[out] A pointer to a variable that receives the line.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e2926-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e2926-108">Return Value</span></span>  
 <span data-ttu-id="e2926-109">S_OK si la méthode réussit ; Sinon, un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e2926-109">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2926-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2926-110">See Also</span></span>  
 [<span data-ttu-id="e2926-111">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="e2926-111">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
