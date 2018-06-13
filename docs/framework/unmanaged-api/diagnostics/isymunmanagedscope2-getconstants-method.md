---
title: ISymUnmanagedScope2::GetConstants, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2.GetConstants
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2::GetConstants
helpviewer_keywords:
- ISymUnmanagedScope2::GetConstants method [.NET Framework debugging]
- GetConstants method [.NET Framework debugging]
ms.assetid: f241b620-9ec5-42fd-92ef-3b22329db72a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 73d4cc609694610aead2a3bfaeed1f5cca5f33fe
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426415"
---
# <a name="isymunmanagedscope2getconstants-method"></a><span data-ttu-id="e4554-102">ISymUnmanagedScope2::GetConstants, méthode</span><span class="sxs-lookup"><span data-stu-id="e4554-102">ISymUnmanagedScope2::GetConstants Method</span></span>
<span data-ttu-id="e4554-103">Obtient les variables constantes définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="e4554-103">Gets the local constants defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4554-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4554-104">Syntax</span></span>  
  
```  
HRESULT GetConstants(  
     [in]  ULONG32  cConstants,  
     [out] ULONG32  *pcConstants,  
     [out, size_is(cConstants),  
         length_is(*pcConstants)] ISymUnmanagedConstant*   
             constants[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e4554-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4554-105">Parameters</span></span>  
 `cConstants`  
 <span data-ttu-id="e4554-106">[in] La longueur de la mémoire tampon qui le `pcConstants` paramètre pointe vers.</span><span class="sxs-lookup"><span data-stu-id="e4554-106">[in] The length of the buffer that the `pcConstants` parameter points to.</span></span>  
  
 `pcConstants`  
 <span data-ttu-id="e4554-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir l’une des constantes.</span><span class="sxs-lookup"><span data-stu-id="e4554-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the constants.</span></span>  
  
 `constants`  
 <span data-ttu-id="e4554-108">[out] Mémoire tampon qui stocke les constantes.</span><span class="sxs-lookup"><span data-stu-id="e4554-108">[out] The buffer that stores the constants.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4554-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e4554-109">Return Value</span></span>  
 <span data-ttu-id="e4554-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e4554-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4554-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e4554-111">Requirements</span></span>  
 <span data-ttu-id="e4554-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e4554-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4554-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4554-113">See Also</span></span>  
 [<span data-ttu-id="e4554-114">ISymUnmanagedScope2, interface</span><span class="sxs-lookup"><span data-stu-id="e4554-114">ISymUnmanagedScope2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope2-interface.md)
