---
title: ISymUnmanagedVariable::GetStartOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetStartOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetStartOffset
helpviewer_keywords:
- GetStartOffset method, ISymUnmanagedVariable interface [.NET Framework debugging]
- ISymUnmanagedVariable::GetStartOffset method [.NET Framework debugging]
ms.assetid: 63021fc1-9c2d-4788-811f-fe8ca077206a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c6a30dff869075a201a669d1e703bc003b011fc3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59196279"
---
# <a name="isymunmanagedvariablegetstartoffset-method"></a><span data-ttu-id="72729-102">ISymUnmanagedVariable::GetStartOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="72729-102">ISymUnmanagedVariable::GetStartOffset Method</span></span>
<span data-ttu-id="72729-103">Obtient l’offset de début de cette variable dans son parent.</span><span class="sxs-lookup"><span data-stu-id="72729-103">Gets the start offset of this variable within its parent.</span></span> <span data-ttu-id="72729-104">S’il s’agit d’une variable locale dans une étendue, le décalage de début est compris dans les offsets définis pour la portée.</span><span class="sxs-lookup"><span data-stu-id="72729-104">If this is a local variable within a scope, the start offset will fall within the offsets defined for the scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72729-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72729-105">Syntax</span></span>  
  
```  
HRESULT GetStartOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="72729-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72729-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="72729-107">[out] Un pointeur vers un `ULONG32` qui reçoit l’offset de début.</span><span class="sxs-lookup"><span data-stu-id="72729-107">[out] A pointer to a `ULONG32` that receives the start offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="72729-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="72729-108">Return Value</span></span>  
 <span data-ttu-id="72729-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="72729-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72729-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72729-110">Requirements</span></span>  
 <span data-ttu-id="72729-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="72729-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="72729-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72729-112">See also</span></span>

- [<span data-ttu-id="72729-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="72729-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
- [<span data-ttu-id="72729-114">GetEndOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="72729-114">GetEndOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getendoffset-method.md)
