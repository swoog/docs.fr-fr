---
title: ISymUnmanagedReader::GetMethod, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetMethod
helpviewer_keywords:
- GetMethod method, ISymUnmanagedReader interface [.NET Framework debugging]
- ISymUnmanagedReader::GetMethod method [.NET Framework debugging]
ms.assetid: ae6cfb29-bc2c-4606-af86-1d32ebd31020
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ab6228866434b35525b16e97b8cba718b849dea1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61993341"
---
# <a name="isymunmanagedreadergetmethod-method"></a><span data-ttu-id="7e4fc-102">ISymUnmanagedReader::GetMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="7e4fc-102">ISymUnmanagedReader::GetMethod Method</span></span>
<span data-ttu-id="7e4fc-103">Obtient une méthode de lecteur de symboles, un jeton de méthode donné.</span><span class="sxs-lookup"><span data-stu-id="7e4fc-103">Gets a symbol reader method, given a method token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e4fc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e4fc-104">Syntax</span></span>  
  
```  
HRESULT GetMethod (  
    [in]  mdMethodDef  token,  
    [out, retval] ISymUnmanagedMethod**  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7e4fc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e4fc-105">Parameters</span></span>  
 `token`  
 <span data-ttu-id="7e4fc-106">[in] Le jeton de méthode.</span><span class="sxs-lookup"><span data-stu-id="7e4fc-106">[in] The method token.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="7e4fc-107">[out] Pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="7e4fc-107">[out] A pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7e4fc-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7e4fc-108">Return Value</span></span>  
 <span data-ttu-id="7e4fc-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7e4fc-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e4fc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e4fc-110">Requirements</span></span>  
 <span data-ttu-id="7e4fc-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7e4fc-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e4fc-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e4fc-112">See also</span></span>

- [<span data-ttu-id="7e4fc-113">ISymUnmanagedReader, interface</span><span class="sxs-lookup"><span data-stu-id="7e4fc-113">ISymUnmanagedReader Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md)
