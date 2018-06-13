---
title: ISymUnmanagedReader2::GetMethodsInDocument, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2.GetMethodsInDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument
helpviewer_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument method [.NET Framework debugging]
- GetMethodsInDocument method [.NET Framework debugging]
ms.assetid: c7ae84d6-81e8-4cb7-a1f9-d48b6cde5d79
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 762649e260817c43291de416d2f1a92a8f03afb5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427367"
---
# <a name="isymunmanagedreader2getmethodsindocument-method"></a><span data-ttu-id="71a89-102">ISymUnmanagedReader2::GetMethodsInDocument, méthode</span><span class="sxs-lookup"><span data-stu-id="71a89-102">ISymUnmanagedReader2::GetMethodsInDocument Method</span></span>
<span data-ttu-id="71a89-103">Obtient chaque méthode qui a des informations de ligne dans le document fourni.</span><span class="sxs-lookup"><span data-stu-id="71a89-103">Gets every method that has line information in the provided document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="71a89-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71a89-104">Syntax</span></span>  
  
```  
HRESULT GetMethodsInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [in]  ULONG32 cMethod,  
    [out] ULONG32* pcMethod,  
    [out, size_is(cMethod),  
        length_is(*pcMethod)] ISymUnmanagedMethod* pRetVal[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="71a89-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71a89-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="71a89-106">[in] Pointeur vers le document.</span><span class="sxs-lookup"><span data-stu-id="71a89-106">[in] A pointer to the document.</span></span>  
  
 `cMethod`  
 <span data-ttu-id="71a89-107">[in] A `ULONG32` qui indique la taille de la `pRetVal` tableau.</span><span class="sxs-lookup"><span data-stu-id="71a89-107">[in] A `ULONG32` that indicates the size of the  `pRetVal` array.</span></span>  
  
 `pcMethod`  
 <span data-ttu-id="71a89-108">[out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les méthodes.</span><span class="sxs-lookup"><span data-stu-id="71a89-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the methods.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="71a89-109">[out] Pointeur vers la mémoire tampon qui reçoit les méthodes.</span><span class="sxs-lookup"><span data-stu-id="71a89-109">[out] A pointer to the buffer that receives the methods.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="71a89-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="71a89-110">Return Value</span></span>  
 <span data-ttu-id="71a89-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="71a89-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="71a89-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="71a89-112">Requirements</span></span>  
 <span data-ttu-id="71a89-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="71a89-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71a89-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71a89-114">See Also</span></span>  
 [<span data-ttu-id="71a89-115">ISymUnmanagedReader2, interface</span><span class="sxs-lookup"><span data-stu-id="71a89-115">ISymUnmanagedReader2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)
