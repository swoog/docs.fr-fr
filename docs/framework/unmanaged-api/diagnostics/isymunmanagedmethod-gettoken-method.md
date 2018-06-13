---
title: ISymUnmanagedMethod::GetToken, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetToken
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetToken
helpviewer_keywords:
- ISymUnmanagedMethod::GetToken method [.NET Framework debugging]
- GetToken method, ISymUnmanagedMethod interface [.NET Framework debugging]
ms.assetid: 4effbe95-c36e-4a45-8b2a-ee21339415fb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 89ae648e38b6349bfad0a37724a9bdc1ae05e365
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425283"
---
# <a name="isymunmanagedmethodgettoken-method"></a><span data-ttu-id="aa301-102">ISymUnmanagedMethod::GetToken, méthode</span><span class="sxs-lookup"><span data-stu-id="aa301-102">ISymUnmanagedMethod::GetToken Method</span></span>
<span data-ttu-id="aa301-103">Retourne le jeton de métadonnées pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="aa301-103">Returns the metadata token for this method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aa301-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa301-104">Syntax</span></span>  
  
```  
HRESULT GetToken(  
   [out, retval]  mdMethodDef  *pToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aa301-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa301-105">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="aa301-106">[out] Un pointeur vers un `mdMethodDef` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="aa301-106">[out] A pointer to a `mdMethodDef` that receives the size, in characters, of the buffer required to contain the metadata.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="aa301-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="aa301-107">Return Value</span></span>  
 <span data-ttu-id="aa301-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="aa301-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aa301-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aa301-109">Requirements</span></span>  
 <span data-ttu-id="aa301-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="aa301-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aa301-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa301-111">See Also</span></span>  
 [<span data-ttu-id="aa301-112">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="aa301-112">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
