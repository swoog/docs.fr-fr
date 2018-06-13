---
title: ISymENCUnmanagedMethod::GetSourceExtentInDocument, méthode
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetSourceExtentInDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetSourceExtentInDocument
helpviewer_keywords:
- GetSourceExtentInDocument method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetSourceExtentInDocument method [.NET Framework debugging]
ms.assetid: 9c5566ab-4ec7-4b61-9753-839bb90ae78c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dc3a986326f9b47194558ca86bcbeabb61dbaeb3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425537"
---
# <a name="isymencunmanagedmethodgetsourceextentindocument-method"></a><span data-ttu-id="fae09-102">ISymENCUnmanagedMethod::GetSourceExtentInDocument, méthode</span><span class="sxs-lookup"><span data-stu-id="fae09-102">ISymENCUnmanagedMethod::GetSourceExtentInDocument Method</span></span>
<span data-ttu-id="fae09-103">Obtient le plus petit de début ligne et la plus grande ligne de fin de la méthode dans un document spécifique.</span><span class="sxs-lookup"><span data-stu-id="fae09-103">Gets the smallest start line and largest end line for the method in a specific document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fae09-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fae09-104">Syntax</span></span>  
  
```  
HRESULT GetSourceExtentInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [out] ULONG32* pstartLine,  
    [out] ULONG32* pendLine);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fae09-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fae09-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="fae09-106">[in] Pointeur vers le document.</span><span class="sxs-lookup"><span data-stu-id="fae09-106">[in] A pointer to the document.</span></span>  
  
 `pstartLine`  
 <span data-ttu-id="fae09-107">[out] Un pointeur vers un `ULONG32` qui reçoit la ligne de début.</span><span class="sxs-lookup"><span data-stu-id="fae09-107">[out] A pointer to a `ULONG32` that receives the start line.</span></span>  
  
 `pendLine`  
 <span data-ttu-id="fae09-108">[out] Un pointeur vers un `ULONG32` qui reçoit la ligne de fin.</span><span class="sxs-lookup"><span data-stu-id="fae09-108">[out] A pointer to a `ULONG32` that receives the end line.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fae09-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fae09-109">Return Value</span></span>  
 <span data-ttu-id="fae09-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fae09-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fae09-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fae09-111">Requirements</span></span>  
 <span data-ttu-id="fae09-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fae09-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fae09-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fae09-113">See Also</span></span>  
 [<span data-ttu-id="fae09-114">ISymENCUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="fae09-114">ISymENCUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
