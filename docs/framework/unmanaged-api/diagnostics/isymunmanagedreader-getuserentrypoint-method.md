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
ms.openlocfilehash: 0267ae8b57c837b097d496c8e119085d03417e36
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59211268"
---
# <a name="isymunmanagedreadergetuserentrypoint-method"></a><span data-ttu-id="3daff-102">ISymUnmanagedReader::GetUserEntryPoint, méthode</span><span class="sxs-lookup"><span data-stu-id="3daff-102">ISymUnmanagedReader::GetUserEntryPoint Method</span></span>
<span data-ttu-id="3daff-103">Retourne la méthode qui a été spécifiée comme point d’entrée utilisateur pour le module, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3daff-103">Returns the method that was specified as the user entry point for the module, if any.</span></span> <span data-ttu-id="3daff-104">Par exemple, cette méthode peut être la méthode de l’utilisateur principal plutôt que les stubs générés par le compilateur avant la méthode principale.</span><span class="sxs-lookup"><span data-stu-id="3daff-104">For example, this method could be the user's main method rather than compiler-generated stubs before the main method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3daff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3daff-105">Syntax</span></span>  
  
```  
HRESULT GetUserEntryPoint (  
    [out, retval]  mdMethodDef  *pToken);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3daff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3daff-106">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="3daff-107">[out] Pointeur vers une variable qui reçoit le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3daff-107">[out] A pointer to a variable that receives the entry point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3daff-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3daff-108">Return Value</span></span>  
 <span data-ttu-id="3daff-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3daff-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3daff-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3daff-110">Requirements</span></span>  
 <span data-ttu-id="3daff-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="3daff-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3daff-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3daff-112">See also</span></span>

- [<span data-ttu-id="3daff-113">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="3daff-113">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
