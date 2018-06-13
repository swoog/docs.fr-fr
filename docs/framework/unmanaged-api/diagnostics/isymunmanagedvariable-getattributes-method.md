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
ms.openlocfilehash: dc0f72168e076f661bfefc17c851d7d353e5e742
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426750"
---
# <a name="isymunmanagedvariablegetattributes-method"></a><span data-ttu-id="19f67-102">ISymUnmanagedVariable::GetAttributes, méthode</span><span class="sxs-lookup"><span data-stu-id="19f67-102">ISymUnmanagedVariable::GetAttributes Method</span></span>
<span data-ttu-id="19f67-103">Obtient les indicateurs d’attribut pour cette variable.</span><span class="sxs-lookup"><span data-stu-id="19f67-103">Gets the attribute flags for this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19f67-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19f67-104">Syntax</span></span>  
  
```  
HRESULT GetAttributes(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="19f67-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19f67-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="19f67-106">[out] Un pointeur vers un `ULONG32` qui reçoit les attributs.</span><span class="sxs-lookup"><span data-stu-id="19f67-106">[out] A pointer to a `ULONG32` that receives the attributes.</span></span> <span data-ttu-id="19f67-107">La valeur retournée sera une des valeurs définies dans le [CorSymVarFlag](../../../../docs/framework/unmanaged-api/diagnostics/corsymvarflag-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="19f67-107">The returned value will be one of the values defined in the [CorSymVarFlag](../../../../docs/framework/unmanaged-api/diagnostics/corsymvarflag-enumeration.md) enumeration.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="19f67-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="19f67-108">Return Value</span></span>  
 <span data-ttu-id="19f67-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="19f67-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19f67-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="19f67-110">Requirements</span></span>  
 <span data-ttu-id="19f67-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="19f67-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19f67-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19f67-112">See Also</span></span>  
 [<span data-ttu-id="19f67-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="19f67-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
