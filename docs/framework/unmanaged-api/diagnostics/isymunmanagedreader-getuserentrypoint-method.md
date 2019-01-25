---
title: ISymUnmanagedReader::GetUserEntryPoint, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetUserEntryPoint
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetUserEntryPoint
helpviewer_keywords:
- GetUserEntryPoint method [.NET Framework debugging]
- ISymUnmanagedReader::GetUserEntryPoint method [.NET Framework debugging]
ms.assetid: 3fd3a34c-d176-46e9-9996-fb1646cff9b0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a8519577bb2b9d3ff8fa2138ba007d04d9fde159
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730150"
---
# <a name="isymunmanagedreadergetuserentrypoint-method"></a><span data-ttu-id="59ff8-102">ISymUnmanagedReader::GetUserEntryPoint, méthode</span><span class="sxs-lookup"><span data-stu-id="59ff8-102">ISymUnmanagedReader::GetUserEntryPoint Method</span></span>
<span data-ttu-id="59ff8-103">Retourne la méthode qui a été spécifiée comme point d’entrée utilisateur pour le module, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="59ff8-103">Returns the method that was specified as the user entry point for the module, if any.</span></span> <span data-ttu-id="59ff8-104">Par exemple, cette méthode peut être la méthode de l’utilisateur principal plutôt que les stubs générés par le compilateur avant la méthode principale.</span><span class="sxs-lookup"><span data-stu-id="59ff8-104">For example, this method could be the user's main method rather than compiler-generated stubs before the main method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59ff8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59ff8-105">Syntax</span></span>  
  
```  
HRESULT GetUserEntryPoint (  
    [out, retval]  mdMethodDef  *pToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="59ff8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59ff8-106">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="59ff8-107">[out] Pointeur vers une variable qui reçoit le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="59ff8-107">[out] A pointer to a variable that receives the entry point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="59ff8-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="59ff8-108">Return Value</span></span>  
 <span data-ttu-id="59ff8-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="59ff8-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59ff8-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="59ff8-110">Requirements</span></span>  
 <span data-ttu-id="59ff8-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="59ff8-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59ff8-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59ff8-112">See also</span></span>
- [<span data-ttu-id="59ff8-113">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="59ff8-113">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
