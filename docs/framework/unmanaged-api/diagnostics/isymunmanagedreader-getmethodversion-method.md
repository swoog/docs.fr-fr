---
title: ISymUnmanagedReader::GetMethodVersion, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethodVersion
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethodVersion
helpviewer_keywords:
- GetMethodVersion method [.NET Framework debugging]
- ISymUnmanagedReader::GetMethodVersion method [.NET Framework debugging]
ms.assetid: d6f9ac84-302a-4f5e-b990-e76f4269fceb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 76d850363940ff53135fc66ec057ee67822fa40d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424662"
---
# <a name="isymunmanagedreadergetmethodversion-method"></a><span data-ttu-id="ae21f-102">ISymUnmanagedReader::GetMethodVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="ae21f-102">ISymUnmanagedReader::GetMethodVersion Method</span></span>
<span data-ttu-id="ae21f-103">Obtient la version de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ae21f-103">Gets the method version.</span></span> <span data-ttu-id="ae21f-104">La version de la méthode commence à 1 et est incrémentée chaque fois que la méthode est recompilée.</span><span class="sxs-lookup"><span data-stu-id="ae21f-104">The method version starts at 1 and is incremented each time the method is recompiled.</span></span> <span data-ttu-id="ae21f-105">Recompilation peut se produire sans apporter de modifications à la méthode.</span><span class="sxs-lookup"><span data-stu-id="ae21f-105">Recompilation can happen without changes to the method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae21f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae21f-106">Syntax</span></span>  
  
```  
HRESULT GetMethodVersion (  
    [in]  ISymUnmanagedMethod* pMethod,  
    [out] int* version);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ae21f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae21f-107">Parameters</span></span>  
 `pMethod`  
 <span data-ttu-id="ae21f-108">[in] La méthode pour laquelle obtenir la version.</span><span class="sxs-lookup"><span data-stu-id="ae21f-108">[in] The method for which to get the version.</span></span>  
  
 `version`  
 <span data-ttu-id="ae21f-109">[out] Pointeur vers une variable qui reçoit la version de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ae21f-109">[out] A pointer to a variable that receives the method version.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ae21f-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ae21f-110">Return Value</span></span>  
 <span data-ttu-id="ae21f-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ae21f-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae21f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae21f-112">Requirements</span></span>  
 <span data-ttu-id="ae21f-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ae21f-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae21f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae21f-114">See Also</span></span>  
 [<span data-ttu-id="ae21f-115">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="ae21f-115">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
