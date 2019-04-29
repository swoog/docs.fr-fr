---
title: ISymUnmanagedVariable::GetAddressField1, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField1
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField1
helpviewer_keywords:
- GetAddressField1 method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressField1 method [.NET Framework debugging]
ms.assetid: 25788ed1-0ce3-4b97-96fc-88f8997812a3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 67634024b04e82aa3a3c0b96dc260114c4c16371
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61797629"
---
# <a name="isymunmanagedvariablegetaddressfield1-method"></a><span data-ttu-id="be4aa-102">ISymUnmanagedVariable::GetAddressField1, méthode</span><span class="sxs-lookup"><span data-stu-id="be4aa-102">ISymUnmanagedVariable::GetAddressField1 Method</span></span>
<span data-ttu-id="be4aa-103">Obtient le premier champ d’adresse pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="be4aa-103">Gets the first address field for this variable.</span></span> <span data-ttu-id="be4aa-104">Sa signification dépend du type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="be4aa-104">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be4aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be4aa-105">Syntax</span></span>  
  
```  
HRESULT GetAddressField1(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="be4aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be4aa-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="be4aa-107">[out] Un pointeur vers un `ULONG32` qui reçoit le premier champ d’adresse.</span><span class="sxs-lookup"><span data-stu-id="be4aa-107">[out] A pointer to a `ULONG32` that receives the first address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="be4aa-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="be4aa-108">Return Value</span></span>  
 <span data-ttu-id="be4aa-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="be4aa-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be4aa-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be4aa-110">Requirements</span></span>  
 <span data-ttu-id="be4aa-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="be4aa-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be4aa-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be4aa-112">See also</span></span>

- [<span data-ttu-id="be4aa-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="be4aa-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
- [<span data-ttu-id="be4aa-114">GetAddressField2, méthode</span><span class="sxs-lookup"><span data-stu-id="be4aa-114">GetAddressField2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield2-method.md)
- [<span data-ttu-id="be4aa-115">GetAddressField3, méthode</span><span class="sxs-lookup"><span data-stu-id="be4aa-115">GetAddressField3 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield3-method.md)
- [<span data-ttu-id="be4aa-116">GetAddressKind, méthode</span><span class="sxs-lookup"><span data-stu-id="be4aa-116">GetAddressKind Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddresskind-method.md)
