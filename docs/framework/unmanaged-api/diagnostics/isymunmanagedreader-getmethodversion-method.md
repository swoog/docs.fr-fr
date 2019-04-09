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
ms.openlocfilehash: b5d4145e6c76cf95f2468a3f5ad59edcd310423e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59160873"
---
# <a name="isymunmanagedreadergetmethodversion-method"></a><span data-ttu-id="acfd6-102">ISymUnmanagedReader::GetMethodVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="acfd6-102">ISymUnmanagedReader::GetMethodVersion Method</span></span>
<span data-ttu-id="acfd6-103">Obtient la version de la méthode.</span><span class="sxs-lookup"><span data-stu-id="acfd6-103">Gets the method version.</span></span> <span data-ttu-id="acfd6-104">La version de la méthode commence à 1 et est incrémentée chaque fois que la méthode est recompilé.</span><span class="sxs-lookup"><span data-stu-id="acfd6-104">The method version starts at 1 and is incremented each time the method is recompiled.</span></span> <span data-ttu-id="acfd6-105">Recompilation peut se produire sans modification à la méthode.</span><span class="sxs-lookup"><span data-stu-id="acfd6-105">Recompilation can happen without changes to the method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="acfd6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acfd6-106">Syntax</span></span>  
  
```  
HRESULT GetMethodVersion (  
    [in]  ISymUnmanagedMethod* pMethod,  
    [out] int* version);  
```  
  
## <a name="parameters"></a><span data-ttu-id="acfd6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="acfd6-107">Parameters</span></span>  
 `pMethod`  
 <span data-ttu-id="acfd6-108">[in] La méthode pour laquelle obtenir la version.</span><span class="sxs-lookup"><span data-stu-id="acfd6-108">[in] The method for which to get the version.</span></span>  
  
 `version`  
 <span data-ttu-id="acfd6-109">[out] Pointeur vers une variable qui reçoit la version de la méthode.</span><span class="sxs-lookup"><span data-stu-id="acfd6-109">[out] A pointer to a variable that receives the method version.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="acfd6-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="acfd6-110">Return Value</span></span>  
 <span data-ttu-id="acfd6-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="acfd6-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="acfd6-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acfd6-112">Requirements</span></span>  
 <span data-ttu-id="acfd6-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="acfd6-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="acfd6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acfd6-114">See also</span></span>

- [<span data-ttu-id="acfd6-115">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="acfd6-115">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
