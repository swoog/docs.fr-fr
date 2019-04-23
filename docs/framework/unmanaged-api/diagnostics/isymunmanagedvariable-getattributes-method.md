---
title: ISymUnmanagedVariable::GetAttributes, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAttributes
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAttributes
helpviewer_keywords:
- GetAttributes method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAttributes method [.NET Framework debugging]
ms.assetid: 80f168af-a6a6-4c8f-b9e6-8a82dc834ed5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d7ba794060330de3934f8d4ca6434b09672d12bb
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59090587"
---
# <a name="isymunmanagedvariablegetattributes-method"></a><span data-ttu-id="09a52-102">ISymUnmanagedVariable::GetAttributes, méthode</span><span class="sxs-lookup"><span data-stu-id="09a52-102">ISymUnmanagedVariable::GetAttributes Method</span></span>
<span data-ttu-id="09a52-103">Obtient les indicateurs d’attribut pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="09a52-103">Gets the attribute flags for this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09a52-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09a52-104">Syntax</span></span>  
  
```  
HRESULT GetAttributes(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="09a52-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09a52-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="09a52-106">[out] Un pointeur vers un `ULONG32` qui reçoit les attributs.</span><span class="sxs-lookup"><span data-stu-id="09a52-106">[out] A pointer to a `ULONG32` that receives the attributes.</span></span> <span data-ttu-id="09a52-107">La valeur retournée sera une des valeurs définies dans le [CorSymVarFlag](../../../../docs/framework/unmanaged-api/diagnostics/corsymvarflag-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="09a52-107">The returned value will be one of the values defined in the [CorSymVarFlag](../../../../docs/framework/unmanaged-api/diagnostics/corsymvarflag-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="09a52-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="09a52-108">Return Value</span></span>  
 <span data-ttu-id="09a52-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="09a52-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="09a52-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09a52-110">Requirements</span></span>  
 <span data-ttu-id="09a52-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="09a52-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09a52-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09a52-112">See also</span></span>

- [<span data-ttu-id="09a52-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="09a52-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
