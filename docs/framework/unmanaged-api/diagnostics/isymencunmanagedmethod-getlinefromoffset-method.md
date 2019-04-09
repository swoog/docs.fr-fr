---
title: ISymENCUnmanagedMethod::GetLineFromOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetLineFromOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetLineFromOffset
helpviewer_keywords:
- GetLineFromOffset method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetLineFromOffset method [.NET Framework debugging]
ms.assetid: cc09bad2-fb34-4d13-a521-6ec7b1a1d915
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3106c6680750826306cffb31e599ee2260bf4ad7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59136446"
---
# <a name="isymencunmanagedmethodgetlinefromoffset-method"></a><span data-ttu-id="08273-102">ISymENCUnmanagedMethod::GetLineFromOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="08273-102">ISymENCUnmanagedMethod::GetLineFromOffset Method</span></span>
<span data-ttu-id="08273-103">Obtient les informations de ligne associées à un décalage.</span><span class="sxs-lookup"><span data-stu-id="08273-103">Gets the line information associated with an offset.</span></span> <span data-ttu-id="08273-104">Si le paramètre offset (`dwOffset`) n’est pas un point de séquence, cette méthode obtient les informations de ligne associées à l’offset précédent.</span><span class="sxs-lookup"><span data-stu-id="08273-104">If the offset parameter (`dwOffset`) is not a sequence point, this method gets the line information associated with the previous offset.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08273-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08273-105">Syntax</span></span>  
  
```  
HRESULT GetLineFromOffset(  
     [in]  ULONG32   dwOffset,  
     [out] ULONG32*  pline,  
     [out] ULONG32*  pcolumn,  
     [out] ULONG32*  pendLine,  
     [out] ULONG32*  pendColumn,  
     [out] ULONG32*  pdwStartOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="08273-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08273-106">Parameters</span></span>  
 `dwOffset`  
 <span data-ttu-id="08273-107">[in] Un `ULONG32` qui contient l’offset.</span><span class="sxs-lookup"><span data-stu-id="08273-107">[in] A `ULONG32` that contains the offset.</span></span>  
  
 `pline`  
 <span data-ttu-id="08273-108">[out] Un pointeur vers un `ULONG32` qui reçoit la ligne.</span><span class="sxs-lookup"><span data-stu-id="08273-108">[out] A pointer to a `ULONG32` that receives the line.</span></span>  
  
 `pcolumn`  
 <span data-ttu-id="08273-109">[out] Un pointeur vers un `ULONG32` qui reçoit la colonne.</span><span class="sxs-lookup"><span data-stu-id="08273-109">[out] A pointer to a `ULONG32` that receives the column.</span></span>  
  
 `pendLine`  
 <span data-ttu-id="08273-110">[out] Un pointeur vers un `ULONG32` qui reçoit la ligne de fin.</span><span class="sxs-lookup"><span data-stu-id="08273-110">[out] A pointer to a `ULONG32` that receives the end line.</span></span>  
  
 `pendColumn`  
 <span data-ttu-id="08273-111">[out] Un pointeur vers un `ULONG32` qui reçoit la colonne de fin.</span><span class="sxs-lookup"><span data-stu-id="08273-111">[out] A pointer to a `ULONG32` that receives the end column.</span></span>  
  
 `pdwStartOffset`  
 <span data-ttu-id="08273-112">[out] Un pointeur vers un `ULONG32` qui reçoit le point de séquence associé.</span><span class="sxs-lookup"><span data-stu-id="08273-112">[out] A pointer to a `ULONG32` that receives the associated sequence point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="08273-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="08273-113">Return Value</span></span>  
 <span data-ttu-id="08273-114">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="08273-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08273-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08273-115">Requirements</span></span>  
 <span data-ttu-id="08273-116">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="08273-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08273-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08273-117">See also</span></span>

- [<span data-ttu-id="08273-118">ISymENCUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="08273-118">ISymENCUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
