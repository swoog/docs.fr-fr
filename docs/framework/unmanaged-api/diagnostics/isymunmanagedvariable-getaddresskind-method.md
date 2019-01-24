---
title: ISymUnmanagedVariable::GetAddressKind, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressKind
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressKind
helpviewer_keywords:
- GetAddressKind method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressKind method [.NET Framework debugging]
ms.assetid: a71563c0-62f2-4eb4-970c-825d61827613
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f5b4cb07cbc1ea3f8f297b96a124b8f5a04f0fce
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54647268"
---
# <a name="isymunmanagedvariablegetaddresskind-method"></a><span data-ttu-id="9305c-102">ISymUnmanagedVariable::GetAddressKind, méthode</span><span class="sxs-lookup"><span data-stu-id="9305c-102">ISymUnmanagedVariable::GetAddressKind Method</span></span>
<span data-ttu-id="9305c-103">Obtient le type d’adresse de cette variable.</span><span class="sxs-lookup"><span data-stu-id="9305c-103">Gets the kind of address of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9305c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9305c-104">Syntax</span></span>  
  
```  
HRESULT GetAddressKind(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9305c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9305c-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="9305c-106">[out] Un pointeur vers un `ULONG32` qui reçoit la valeur.</span><span class="sxs-lookup"><span data-stu-id="9305c-106">[out] A pointer to a `ULONG32` that receives the value.</span></span> <span data-ttu-id="9305c-107">Les valeurs possibles sont définies dans le [CorSymAddrKind](../../../../docs/framework/unmanaged-api/diagnostics/corsymaddrkind-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="9305c-107">The possible values are defined in the [CorSymAddrKind](../../../../docs/framework/unmanaged-api/diagnostics/corsymaddrkind-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9305c-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9305c-108">Return Value</span></span>  
 <span data-ttu-id="9305c-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9305c-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9305c-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9305c-110">Requirements</span></span>  
 <span data-ttu-id="9305c-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9305c-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9305c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9305c-112">See also</span></span>
- [<span data-ttu-id="9305c-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="9305c-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
