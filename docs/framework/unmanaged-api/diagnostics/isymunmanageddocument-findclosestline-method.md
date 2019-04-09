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
ms.openlocfilehash: ab7df9b77b1820f291c1b1873b4dfb39e326bc34
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59193159"
---
# <a name="isymunmanageddocumentfindclosestline-method"></a><span data-ttu-id="4c0f7-102">ISymUnmanagedDocument::FindClosestLine, méthode</span><span class="sxs-lookup"><span data-stu-id="4c0f7-102">ISymUnmanagedDocument::FindClosestLine Method</span></span>
<span data-ttu-id="4c0f7-103">Retourne la ligne la plus proche constituant un point de séquence, la fonction d’une ligne dans ce document qui peut être ou non un point de séquence.</span><span class="sxs-lookup"><span data-stu-id="4c0f7-103">Returns the closest line that is a sequence point, given a line in this document that may or may not be a sequence point.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c0f7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c0f7-104">Syntax</span></span>  
  
```  
HRESULT FindClosestLine(  
    [in]  ULONG32  line,  
    [out, retval] ULONG32*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4c0f7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c0f7-105">Parameters</span></span>  
 `line`  
 <span data-ttu-id="4c0f7-106">[in] Une ligne dans ce document.</span><span class="sxs-lookup"><span data-stu-id="4c0f7-106">[in] A line in this document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="4c0f7-107">[out] Pointeur vers une variable qui reçoit la ligne.</span><span class="sxs-lookup"><span data-stu-id="4c0f7-107">[out] A pointer to a variable that receives the line.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4c0f7-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4c0f7-108">Return Value</span></span>  
 <span data-ttu-id="4c0f7-109">S_OK si la méthode réussit ; Sinon, un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4c0f7-109">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c0f7-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c0f7-110">See also</span></span>

- [<span data-ttu-id="4c0f7-111">ISymUnmanagedDocument, interface</span><span class="sxs-lookup"><span data-stu-id="4c0f7-111">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
