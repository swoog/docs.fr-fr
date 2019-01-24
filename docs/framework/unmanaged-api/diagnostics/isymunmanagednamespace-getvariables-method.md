---
title: ISymUnmanagedNamespace::GetVariables, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedNamespace.GetVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedNamespace::GetVariables
helpviewer_keywords:
- ISymUnmanagedNamespace::GetVariables method [.NET Framework debugging]
- GetVariables method, ISymUnmanagedNamespace interface [.NET Framework debugging]
ms.assetid: ea7c1617-f3ce-4220-8288-f2b50eaf0f0f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 11a5eb01a3e354b4360bea59af1e63ffeb0576aa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730111"
---
# <a name="isymunmanagednamespacegetvariables-method"></a><span data-ttu-id="df150-102">ISymUnmanagedNamespace::GetVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="df150-102">ISymUnmanagedNamespace::GetVariables Method</span></span>
<span data-ttu-id="df150-103">Retourne toutes les variables définies avec une portée globale dans cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="df150-103">Returns all variables defined at global scope within this namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df150-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df150-104">Syntax</span></span>  
  
```  
HRESULT GetVariables(  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is(cVars), length_is(*pcVars)]  
        ISymUnmanagedVariable *pVars[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="df150-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df150-105">Parameters</span></span>  
 `cVars`  
 <span data-ttu-id="df150-106">[in] Un `ULONG32` qui indique la taille de la `pVars` tableau.</span><span class="sxs-lookup"><span data-stu-id="df150-106">[in] A `ULONG32` that indicates the size of the `pVars` array.</span></span>  
  
 `pcVars`  
 <span data-ttu-id="df150-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="df150-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the namespaces.</span></span>  
  
 `pVars`  
 <span data-ttu-id="df150-108">[out] Pointeur vers une mémoire tampon qui contient les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="df150-108">[out] A pointer to a buffer that contains the namespaces.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="df150-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="df150-109">Return Value</span></span>  
 <span data-ttu-id="df150-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="df150-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df150-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="df150-111">Requirements</span></span>  
 <span data-ttu-id="df150-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="df150-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df150-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df150-113">See also</span></span>
- [<span data-ttu-id="df150-114">ISymUnmanagedNamespace, interface</span><span class="sxs-lookup"><span data-stu-id="df150-114">ISymUnmanagedNamespace Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md)
