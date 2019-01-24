---
title: ISymUnmanagedReader::GetVariables, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetVariables
helpviewer_keywords:
- ISymUnmanagedReader::GetVariables method [.NET Framework debugging]
- GetVariables method, ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: 16dc49cb-2c60-4ac8-9c35-020e9afba3f8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ec1e2b59c15c956a4657b224a937829dbd3b14cb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549900"
---
# <a name="isymunmanagedreadergetvariables-method"></a><span data-ttu-id="705bf-102">ISymUnmanagedReader::GetVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="705bf-102">ISymUnmanagedReader::GetVariables Method</span></span>
<span data-ttu-id="705bf-103">Retourne une variable non locale, en fonction de son parent et son nom.</span><span class="sxs-lookup"><span data-stu-id="705bf-103">Returns a non-local variable, given its parent and name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="705bf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="705bf-104">Syntax</span></span>  
  
```  
HRESULT GetVariables (  
    [in]  mdToken  parent,  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is (cVars),  
        length_is (*pcVars)] ISymUnmanagedVariable *pVars[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="705bf-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="705bf-105">Parameters</span></span>  
 `parent`  
 <span data-ttu-id="705bf-106">[in] Le parent de la variable.</span><span class="sxs-lookup"><span data-stu-id="705bf-106">[in] The parent of the variable.</span></span>  
  
 `cVars`  
 <span data-ttu-id="705bf-107">[in] Taille du tableau `pVars`.</span><span class="sxs-lookup"><span data-stu-id="705bf-107">[in] The size of the `pVars` array.</span></span>  
  
 `pcVars`  
 <span data-ttu-id="705bf-108">[out] Un pointeur vers la variable qui reçoit le nombre de variables retournées dans `pVars`.</span><span class="sxs-lookup"><span data-stu-id="705bf-108">[out] A pointer to the variable that receives the number of variables returned in `pVars`.</span></span>  
  
 `pVars`  
 <span data-ttu-id="705bf-109">[out] Pointeur vers la variable qui reçoit les variables.</span><span class="sxs-lookup"><span data-stu-id="705bf-109">[out] A pointer to the variable that receives the variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="705bf-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="705bf-110">Return Value</span></span>  
 <span data-ttu-id="705bf-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="705bf-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="705bf-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="705bf-112">Requirements</span></span>  
 <span data-ttu-id="705bf-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="705bf-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="705bf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="705bf-114">See also</span></span>
- [<span data-ttu-id="705bf-115">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="705bf-115">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
