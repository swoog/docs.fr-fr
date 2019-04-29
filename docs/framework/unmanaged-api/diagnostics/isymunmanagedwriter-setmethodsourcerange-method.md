---
title: ISymUnmanagedWriter::SetMethodSourceRange, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetMethodSourceRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetMethodSourceRange
helpviewer_keywords:
- SetMethodSourceRange method [.NET Framework debugging]
- ISymUnmanagedWriter::SetMethodSourceRange method [.NET Framework debugging]
ms.assetid: c698b86e-ace7-4b21-9549-f52d6a034959
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 734857428c205b6d806a4279213afb1193f914c8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61650764"
---
# <a name="isymunmanagedwritersetmethodsourcerange-method"></a><span data-ttu-id="231cb-102">ISymUnmanagedWriter::SetMethodSourceRange, méthode</span><span class="sxs-lookup"><span data-stu-id="231cb-102">ISymUnmanagedWriter::SetMethodSourceRange Method</span></span>
<span data-ttu-id="231cb-103">Spécifie les véritables début et la fin d’une méthode dans un fichier source.</span><span class="sxs-lookup"><span data-stu-id="231cb-103">Specifies the true start and end of a method within a source file.</span></span> <span data-ttu-id="231cb-104">Utilisez cette méthode pour spécifier l’étendue d’une méthode indépendamment les points de séquence qui existent au sein de la méthode.</span><span class="sxs-lookup"><span data-stu-id="231cb-104">Use this method to specify the extent of a method independently of the sequence points that exist within the method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="231cb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="231cb-105">Syntax</span></span>  
  
```  
HRESULT SetMethodSourceRange(  
    [in] ISymUnmanagedDocumentWriter  *startDoc,  
    [in] ULONG32                      startLine,  
    [in] ULONG32                      startColumn,  
    [in] ISymUnmanagedDocumentWriter  *endDoc,  
    [in] ULONG32                      endLine,  
    [in] ULONG32                      endColumn);  
```  
  
## <a name="parameters"></a><span data-ttu-id="231cb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="231cb-106">Parameters</span></span>  
 `startDoc`  
 <span data-ttu-id="231cb-107">[in] Pointeur vers le document contenant la position de départ.</span><span class="sxs-lookup"><span data-stu-id="231cb-107">[in] A pointer to the document containing the starting position.</span></span>  
  
 `startLine`  
 <span data-ttu-id="231cb-108">[in] Le numéro de ligne de départ.</span><span class="sxs-lookup"><span data-stu-id="231cb-108">[in] The starting line number.</span></span>  
  
 `startColumn`  
 <span data-ttu-id="231cb-109">[in] La colonne de départ.</span><span class="sxs-lookup"><span data-stu-id="231cb-109">[in] The starting column.</span></span>  
  
 `endDoc`  
 <span data-ttu-id="231cb-110">[in] Pointeur vers le document contenant la position de fin.</span><span class="sxs-lookup"><span data-stu-id="231cb-110">[in] A pointer to the document containing the ending position.</span></span>  
  
 `endLine`  
 <span data-ttu-id="231cb-111">[in] Numéro de ligne de fin.</span><span class="sxs-lookup"><span data-stu-id="231cb-111">[in] The ending line number.</span></span>  
  
 `endColumn`  
 <span data-ttu-id="231cb-112">[in] Numéro de colonne de fin.</span><span class="sxs-lookup"><span data-stu-id="231cb-112">[in] The ending column number.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="231cb-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="231cb-113">Return Value</span></span>  
 <span data-ttu-id="231cb-114">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="231cb-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="231cb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="231cb-115">Requirements</span></span>  
 <span data-ttu-id="231cb-116">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="231cb-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="231cb-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="231cb-117">See also</span></span>

- [<span data-ttu-id="231cb-118">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="231cb-118">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
