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
ms.openlocfilehash: 7b4c334d82320066bf9459907660fe6b7e2acefd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425319"
---
# <a name="isymunmanagedreadergetuserentrypoint-method"></a><span data-ttu-id="ddc75-102">ISymUnmanagedReader::GetUserEntryPoint, méthode</span><span class="sxs-lookup"><span data-stu-id="ddc75-102">ISymUnmanagedReader::GetUserEntryPoint Method</span></span>
<span data-ttu-id="ddc75-103">Retourne la méthode qui a été spécifiée en tant que point d’entrée utilisateur pour le module, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ddc75-103">Returns the method that was specified as the user entry point for the module, if any.</span></span> <span data-ttu-id="ddc75-104">Par exemple, cette méthode peut être méthode principale de l’utilisateur plutôt que des stubs générés par le compilateur avant la méthode principale.</span><span class="sxs-lookup"><span data-stu-id="ddc75-104">For example, this method could be the user's main method rather than compiler-generated stubs before the main method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ddc75-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddc75-105">Syntax</span></span>  
  
```  
HRESULT GetUserEntryPoint (  
    [out, retval]  mdMethodDef  *pToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ddc75-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddc75-106">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="ddc75-107">[out] Pointeur vers une variable qui reçoit le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ddc75-107">[out] A pointer to a variable that receives the entry point.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ddc75-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ddc75-108">Return Value</span></span>  
 <span data-ttu-id="ddc75-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ddc75-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ddc75-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ddc75-110">Requirements</span></span>  
 <span data-ttu-id="ddc75-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ddc75-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ddc75-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddc75-112">See Also</span></span>  
 [<span data-ttu-id="ddc75-113">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="ddc75-113">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
