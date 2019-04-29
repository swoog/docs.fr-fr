---
title: ISymUnmanagedConstant::GetName, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetName
helpviewer_keywords:
- ISymUnmanagedConstant::GetName method [.NET Framework debugging]
- GetName method, ISymUnmanagedConstant interface [.NET Framework debugging]
ms.assetid: cbaca4e1-4473-459b-ba34-f1f59ce7c0ba
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1da8d89cf9ae2eed7b846774434d6ea472afbb94
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61939969"
---
# <a name="isymunmanagedconstantgetname-method"></a><span data-ttu-id="06bc7-102">ISymUnmanagedConstant::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="06bc7-102">ISymUnmanagedConstant::GetName Method</span></span>
<span data-ttu-id="06bc7-103">Obtient le nom de la constante.</span><span class="sxs-lookup"><span data-stu-id="06bc7-103">Gets the name of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06bc7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06bc7-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
        length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="06bc7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06bc7-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="06bc7-106">[in] La longueur de la mémoire tampon qui le `szName` paramètre pointe vers.</span><span class="sxs-lookup"><span data-stu-id="06bc7-106">[in] The length of the buffer that the `szName` parameter points to.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="06bc7-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir le nom, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="06bc7-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the name, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="06bc7-108">[out] La mémoire tampon qui stocke le nom.</span><span class="sxs-lookup"><span data-stu-id="06bc7-108">[out] The buffer that stores the name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="06bc7-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="06bc7-109">Return Value</span></span>  
 <span data-ttu-id="06bc7-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="06bc7-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06bc7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06bc7-111">Requirements</span></span>  
 <span data-ttu-id="06bc7-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="06bc7-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06bc7-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06bc7-113">See also</span></span>

- [<span data-ttu-id="06bc7-114">ISymUnmanagedConstant, interface</span><span class="sxs-lookup"><span data-stu-id="06bc7-114">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)
- [<span data-ttu-id="06bc7-115">GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="06bc7-115">GetSignature Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getsignature-method.md)
- [<span data-ttu-id="06bc7-116">GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="06bc7-116">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getvalue-method.md)
