---
title: ISymUnmanagedMethod::GetSequencePointCount, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSequencePointCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSequencePointCount
helpviewer_keywords:
- ISymUnmanagedMethod::GetSequencePointCount method [.NET Framework debugging]
- GetSequencePointCount method [.NET Framework debugging]
ms.assetid: 836133e8-6108-4b9b-b0a9-bce4e08dccda
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9eac17ec9599caba88ddaa73d28abcae538a4d19
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59215064"
---
# <a name="isymunmanagedmethodgetsequencepointcount-method"></a><span data-ttu-id="17652-102">ISymUnmanagedMethod::GetSequencePointCount, méthode</span><span class="sxs-lookup"><span data-stu-id="17652-102">ISymUnmanagedMethod::GetSequencePointCount Method</span></span>
<span data-ttu-id="17652-103">Obtient le nombre de points de séquence au sein de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="17652-103">Gets the count of sequence points within this method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17652-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17652-104">Syntax</span></span>  
  
```  
HRESULT GetSequencePointCount(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="17652-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17652-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="17652-106">[out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les points de séquence.</span><span class="sxs-lookup"><span data-stu-id="17652-106">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the sequence points.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="17652-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="17652-107">Return Value</span></span>  
 <span data-ttu-id="17652-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="17652-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="17652-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17652-109">Requirements</span></span>  
 <span data-ttu-id="17652-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="17652-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17652-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17652-111">See also</span></span>

- [<span data-ttu-id="17652-112">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="17652-112">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
