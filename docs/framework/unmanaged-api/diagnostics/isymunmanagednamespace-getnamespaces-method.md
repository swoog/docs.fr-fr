---
title: ISymUnmanagedNamespace::GetNamespaces, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedNamespace.GetNamespaces
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedNamespace::GetNamespaces
helpviewer_keywords:
- ISymUnmanagedNamespace::GetNamespaces method [.NET Framework debugging]
- GetNamespaces method, ISymUnmanagedNamespace interface [.NET Framework debugging]
ms.assetid: 0ea9d9af-8709-4a46-872b-f54d9e840088
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3d7ac84971f7d0e97f7ccd26710151d1aeefe729
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59207212"
---
# <a name="isymunmanagednamespacegetnamespaces-method"></a><span data-ttu-id="c9ba4-102">ISymUnmanagedNamespace::GetNamespaces, méthode</span><span class="sxs-lookup"><span data-stu-id="c9ba4-102">ISymUnmanagedNamespace::GetNamespaces Method</span></span>
<span data-ttu-id="c9ba4-103">Obtient les enfants de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-103">Gets the children of this namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9ba4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9ba4-104">Syntax</span></span>  
  
```  
HRESULT GetNamespaces(  
    [in]  ULONG32  cNameSpaces,  
    [out] ULONG32  *pcNameSpaces,  
    [out, size_is(cNameSpaces), length_is(*pcNameSpaces)]  
        ISymUnmanagedNamespace* namespaces[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c9ba4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9ba4-105">Parameters</span></span>  
 `cNameSpaces`  
 <span data-ttu-id="c9ba4-106">[in] Un `ULONG32` qui indique la taille de la `namespaces` tableau.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-106">[in] A `ULONG32` that indicates the size of the `namespaces` array.</span></span>  
  
 `pcNameSpaces`  
 <span data-ttu-id="c9ba4-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the namespaces.</span></span>  
  
 `namespaces`  
 <span data-ttu-id="c9ba4-108">[out] Pointeur vers la mémoire tampon qui contient les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-108">[out] A pointer to the buffer that contains the namespaces.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c9ba4-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c9ba4-109">Return Value</span></span>  
 <span data-ttu-id="c9ba4-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c9ba4-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9ba4-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9ba4-111">Requirements</span></span>  
 <span data-ttu-id="c9ba4-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="c9ba4-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9ba4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9ba4-113">See also</span></span>

- [<span data-ttu-id="c9ba4-114">ISymUnmanagedNamespace, interface</span><span class="sxs-lookup"><span data-stu-id="c9ba4-114">ISymUnmanagedNamespace Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md)
