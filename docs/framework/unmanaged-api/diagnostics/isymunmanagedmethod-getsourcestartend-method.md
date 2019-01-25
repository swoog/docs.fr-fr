---
title: ISymUnmanagedMethod::GetSourceStartEnd, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSourceStartEnd
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSourceStartEnd
helpviewer_keywords:
- GetSourceStartEnd method [.NET Framework debugging]
- ISymUnmanagedMethod::GetSourceStartEnd method [.NET Framework debugging]
ms.assetid: 2a420900-01f1-4461-8777-3a34a6dc1426
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4ecb726f275a694fded2c486448a60b28fadb168
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54561866"
---
# <a name="isymunmanagedmethodgetsourcestartend-method"></a><span data-ttu-id="4659d-102">ISymUnmanagedMethod::GetSourceStartEnd, méthode</span><span class="sxs-lookup"><span data-stu-id="4659d-102">ISymUnmanagedMethod::GetSourceStartEnd Method</span></span>
<span data-ttu-id="4659d-103">Obtient les positions de document de début et de fin de la source de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4659d-103">Gets the start and end document positions for the source of this method.</span></span> <span data-ttu-id="4659d-104">La première position du tableau correspond au début, et la position du deuxième tableau est la fin.</span><span class="sxs-lookup"><span data-stu-id="4659d-104">The first array position is the start, and the second array position is the end.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4659d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4659d-105">Syntax</span></span>  
  
```  
HRESULT GetSourceStartEnd(  
    [in]  ISymUnmanagedDocument  *docs[2],  
    [in]  ULONG32                lines[2],  
    [in]  ULONG32                columns[2],  
    [out] BOOL                   *pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4659d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4659d-106">Parameters</span></span>  
 `docs`  
 <span data-ttu-id="4659d-107">[in] Le début et fin documents sources.</span><span class="sxs-lookup"><span data-stu-id="4659d-107">[in] The starting and ending source documents.</span></span>  
  
 `lines`  
 <span data-ttu-id="4659d-108">[in] Documents de sources de début et fin des lignes dans le correspondantes.</span><span class="sxs-lookup"><span data-stu-id="4659d-108">[in] The starting and ending lines in the corresponding source documents.</span></span>  
  
 `columns`  
 <span data-ttu-id="4659d-109">[in] Documents de sources de début et fin des colonnes dans le correspondantes.</span><span class="sxs-lookup"><span data-stu-id="4659d-109">[in] The starting and ending columns in the corresponding source documents.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="4659d-110">[out] `true` si les positions ont été définies ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="4659d-110">[out] `true` if positions were defined; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4659d-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4659d-111">Return Value</span></span>  
 <span data-ttu-id="4659d-112">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4659d-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4659d-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4659d-113">Requirements</span></span>  
 <span data-ttu-id="4659d-114">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="4659d-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4659d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4659d-115">See also</span></span>
- [<span data-ttu-id="4659d-116">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="4659d-116">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
