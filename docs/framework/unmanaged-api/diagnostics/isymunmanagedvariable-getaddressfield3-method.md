---
title: ISymUnmanagedVariable::GetAddressField3, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField3
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField3
helpviewer_keywords:
- ISymUnmanagedVariable::GetAddressField3 method [.NET Framework debugging]
- GetAddressField3 method [.NET Framework debugging]
ms.assetid: 4d834721-ad8d-439d-b356-c6b4aef022fc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c8b03b96c8cab43046d109d0dd11ae135cb70c9f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59163603"
---
# <a name="isymunmanagedvariablegetaddressfield3-method"></a><span data-ttu-id="37d9c-102">ISymUnmanagedVariable::GetAddressField3, méthode</span><span class="sxs-lookup"><span data-stu-id="37d9c-102">ISymUnmanagedVariable::GetAddressField3 Method</span></span>
<span data-ttu-id="37d9c-103">Obtient le troisième champ d’adresse pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="37d9c-103">Gets the third address field for this variable.</span></span> <span data-ttu-id="37d9c-104">Sa signification dépend du type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="37d9c-104">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="37d9c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37d9c-105">Syntax</span></span>  
  
```  
HRESULT GetAddressField3(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="37d9c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37d9c-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="37d9c-107">[out] Un pointeur vers un `ULONG32` qui reçoit le troisième champ d’adresse.</span><span class="sxs-lookup"><span data-stu-id="37d9c-107">[out] A pointer to a `ULONG32` that receives the third address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="37d9c-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="37d9c-108">Return Value</span></span>  
 <span data-ttu-id="37d9c-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="37d9c-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="37d9c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37d9c-110">Requirements</span></span>  
 <span data-ttu-id="37d9c-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="37d9c-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37d9c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37d9c-112">See also</span></span>

- [<span data-ttu-id="37d9c-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="37d9c-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
- [<span data-ttu-id="37d9c-114">GetAddressField1, méthode</span><span class="sxs-lookup"><span data-stu-id="37d9c-114">GetAddressField1 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield1-method.md)
- [<span data-ttu-id="37d9c-115">GetAddressField2, méthode</span><span class="sxs-lookup"><span data-stu-id="37d9c-115">GetAddressField2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield2-method.md)
- [<span data-ttu-id="37d9c-116">GetAddressKind, méthode</span><span class="sxs-lookup"><span data-stu-id="37d9c-116">GetAddressKind Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddresskind-method.md)
