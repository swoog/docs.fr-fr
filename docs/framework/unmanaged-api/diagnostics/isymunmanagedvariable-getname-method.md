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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59176239"
---
# <a name="isymunmanagedvariablegetname-method"></a><span data-ttu-id="fb481-102">ISymUnmanagedVariable::GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="fb481-102">ISymUnmanagedVariable::GetName Method</span></span>
<span data-ttu-id="fb481-103">Obtient le nom de cette variable.</span><span class="sxs-lookup"><span data-stu-id="fb481-103">Gets the name of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb481-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb481-104">Syntax</span></span>  
  
```  
HRESULT GetName(  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
        length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fb481-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb481-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="fb481-106">[in] La longueur de la mémoire tampon qui le `pcchName` paramètre pointe vers.</span><span class="sxs-lookup"><span data-stu-id="fb481-106">[in] The length of the buffer that the `pcchName` parameter points to.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="fb481-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir le nom, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="fb481-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the name, including the null termination.</span></span>  
  
 `szName`  
 <span data-ttu-id="fb481-108">[out] La mémoire tampon qui stocke le nom.</span><span class="sxs-lookup"><span data-stu-id="fb481-108">[out] The buffer that stores the name.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fb481-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fb481-109">Return Value</span></span>  
 <span data-ttu-id="fb481-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fb481-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fb481-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb481-111">Requirements</span></span>  
 <span data-ttu-id="fb481-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fb481-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb481-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb481-113">See also</span></span>

- [<span data-ttu-id="fb481-114">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="fb481-114">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
