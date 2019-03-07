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
ms.openlocfilehash: ea0cba1f1b9154ccb14d75f7c377a8153c24f2b0
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57499477"
---
# <a name="isymunmanagedreadergetuserentrypoint-method"></a><span data-ttu-id="e94e3-102">ISymUnmanagedReader::GetUserEntryPoint, méthode</span><span class="sxs-lookup"><span data-stu-id="e94e3-102">ISymUnmanagedReader::GetUserEntryPoint Method</span></span>
<span data-ttu-id="e94e3-103">Retourne la méthode qui a été spécifiée comme point d’entrée utilisateur pour le module, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e94e3-103">Returns the method that was specified as the user entry point for the module, if any.</span></span> <span data-ttu-id="e94e3-104">Par exemple, cette méthode peut être la méthode de l’utilisateur principal plutôt que les stubs générés par le compilateur avant la méthode principale.</span><span class="sxs-lookup"><span data-stu-id="e94e3-104">For example, this method could be the user's main method rather than compiler-generated stubs before the main method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e94e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e94e3-105">Syntax</span></span>  
  
```  
HRESULT GetUserEntryPoint (  
    [out, retval]  mdMethodDef  *pToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e94e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e94e3-106">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="e94e3-107">[out] Pointeur vers une variable qui reçoit le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e94e3-107">[out] A pointer to a variable that receives the entry point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e94e3-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e94e3-108">Return Value</span></span>  
 <span data-ttu-id="e94e3-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e94e3-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e94e3-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e94e3-110">Requirements</span></span>  
 <span data-ttu-id="e94e3-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e94e3-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e94e3-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e94e3-112">See also</span></span>
- [<span data-ttu-id="e94e3-113">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="e94e3-113">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
