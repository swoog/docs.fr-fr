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
ms.openlocfilehash: 039dab1b4ca86cb26de739e74b152f108f074c43
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426170"
---
# <a name="isymunmanagednamespacegetnamespaces-method"></a><span data-ttu-id="2c148-102">ISymUnmanagedNamespace::GetNamespaces, méthode</span><span class="sxs-lookup"><span data-stu-id="2c148-102">ISymUnmanagedNamespace::GetNamespaces Method</span></span>
<span data-ttu-id="2c148-103">Obtient les enfants de cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="2c148-103">Gets the children of this namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c148-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c148-104">Syntax</span></span>  
  
```  
HRESULT GetNamespaces(  
    [in]  ULONG32  cNameSpaces,  
    [out] ULONG32  *pcNameSpaces,  
    [out, size_is(cNameSpaces), length_is(*pcNameSpaces)]  
        ISymUnmanagedNamespace* namespaces[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2c148-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c148-105">Parameters</span></span>  
 `cNameSpaces`  
 <span data-ttu-id="2c148-106">[in] A `ULONG32` qui indique la taille de la `namespaces` tableau.</span><span class="sxs-lookup"><span data-stu-id="2c148-106">[in] A `ULONG32` that indicates the size of the `namespaces` array.</span></span>  
  
 `pcNameSpaces`  
 <span data-ttu-id="2c148-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="2c148-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the namespaces.</span></span>  
  
 `namespaces`  
 <span data-ttu-id="2c148-108">[out] Pointeur vers la mémoire tampon qui contient les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="2c148-108">[out] A pointer to the buffer that contains the namespaces.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2c148-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2c148-109">Return Value</span></span>  
 <span data-ttu-id="2c148-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2c148-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2c148-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2c148-111">Requirements</span></span>  
 <span data-ttu-id="2c148-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2c148-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c148-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c148-113">See Also</span></span>  
 [<span data-ttu-id="2c148-114">ISymUnmanagedNamespace, interface</span><span class="sxs-lookup"><span data-stu-id="2c148-114">ISymUnmanagedNamespace Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md)
