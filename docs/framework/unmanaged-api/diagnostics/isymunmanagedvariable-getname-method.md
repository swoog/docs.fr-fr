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
ms.openlocfilehash: e863640e18ca64de084331327e0fa39468b54b60
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59176239"
---
# <a name="isymunmanagedvariablegetname-method"></a><span data-ttu-id="9c9a3-102">ISymUnmanagedVariable::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="9c9a3-102">ISymUnmanagedVariable::GetName Method</span></span>
<span data-ttu-id="9c9a3-103">Obtient le nom de cette variable.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-103">Gets the name of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c9a3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c9a3-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
        length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9c9a3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c9a3-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="9c9a3-106">[in] La longueur de la mémoire tampon qui le `pcchName` paramètre pointe vers.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-106">[in] The length of the buffer that the `pcchName` parameter points to.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="9c9a3-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir le nom, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the name, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="9c9a3-108">[out] La mémoire tampon qui stocke le nom.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-108">[out] The buffer that stores the name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9c9a3-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9c9a3-109">Return Value</span></span>  
 <span data-ttu-id="9c9a3-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9c9a3-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c9a3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c9a3-111">Requirements</span></span>  
 <span data-ttu-id="9c9a3-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9c9a3-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c9a3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c9a3-113">See also</span></span>

- [<span data-ttu-id="9c9a3-114">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="9c9a3-114">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
