---
title: ISymUnmanagedVariable::GetName, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetName
helpviewer_keywords:
- GetName method, ISymUnmanagedVariable interface [.NET Framework debugging]
- ISymUnmanagedVariable::GetName method [.NET Framework debugging]
ms.assetid: eedf1ef0-9d4a-4847-a201-4e99572dfe5e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5aa6f01f161ce7c497cc103493e3bf4506fa3394
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57475019"
---
# <a name="isymunmanagedvariablegetname-method"></a><span data-ttu-id="d4c08-102">ISymUnmanagedVariable::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="d4c08-102">ISymUnmanagedVariable::GetName Method</span></span>
<span data-ttu-id="d4c08-103">Obtient le nom de cette variable.</span><span class="sxs-lookup"><span data-stu-id="d4c08-103">Gets the name of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d4c08-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4c08-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
        length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d4c08-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4c08-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="d4c08-106">[in] La longueur de la mémoire tampon qui le `pcchName` paramètre pointe vers.</span><span class="sxs-lookup"><span data-stu-id="d4c08-106">[in] The length of the buffer that the `pcchName` parameter points to.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="d4c08-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir le nom, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="d4c08-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the name, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="d4c08-108">[out] La mémoire tampon qui stocke le nom.</span><span class="sxs-lookup"><span data-stu-id="d4c08-108">[out] The buffer that stores the name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d4c08-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d4c08-109">Return Value</span></span>  
 <span data-ttu-id="d4c08-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d4c08-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d4c08-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d4c08-111">Requirements</span></span>  
 <span data-ttu-id="d4c08-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d4c08-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4c08-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4c08-113">See also</span></span>
- [<span data-ttu-id="d4c08-114">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="d4c08-114">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
