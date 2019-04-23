---
title: ISymUnmanagedMethod::GetOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetOffset
helpviewer_keywords:
- GetOffset method, ISymUnmanagedMethod interface [.NET Framework debugging]
- ISymUnmanagedMethod::GetOffset method [.NET Framework debugging]
ms.assetid: 8bf3cb62-89bf-4159-ad53-de606aba89e8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a42dc624d4de9cddebad287f6d90590f96b30272
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59223652"
---
# <a name="isymunmanagedmethodgetoffset-method"></a><span data-ttu-id="8baef-102">ISymUnmanagedMethod::GetOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="8baef-102">ISymUnmanagedMethod::GetOffset Method</span></span>
<span data-ttu-id="8baef-103">Retourne le décalage au sein de cette méthode qui correspond à une position donnée dans un document.</span><span class="sxs-lookup"><span data-stu-id="8baef-103">Returns the offset within this method that corresponds to a given position within a document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8baef-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8baef-104">Syntax</span></span>  
  
```  
HRESULT GetOffset(  
    [in]  ISymUnmanagedDocument*  document,  
    [in]  ULONG32                 line,  
    [in]  ULONG32                 column,  
    [out, retval] ULONG32*        pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8baef-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8baef-105">Parameters</span></span>  
 `document`  
 <span data-ttu-id="8baef-106">[in] Pointeur vers le document pour lequel l’offset est demandé.</span><span class="sxs-lookup"><span data-stu-id="8baef-106">[in] A pointer to the document for which the offset is requested.</span></span>  
  
 `line`  
 <span data-ttu-id="8baef-107">[in] Ligne du document pour lequel l’offset est demandé.</span><span class="sxs-lookup"><span data-stu-id="8baef-107">[in] The document line for which the offset is requested.</span></span>  
  
 `column`  
 <span data-ttu-id="8baef-108">[in] Colonne du document pour lequel l’offset est demandé.</span><span class="sxs-lookup"><span data-stu-id="8baef-108">[in] The document column for which the offset is requested.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="8baef-109">[out] Un pointeur vers un `ULONG32` qui reçoit les offsets.</span><span class="sxs-lookup"><span data-stu-id="8baef-109">[out] A pointer to a `ULONG32` that receives the offsets.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8baef-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8baef-110">Return Value</span></span>  
 <span data-ttu-id="8baef-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8baef-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8baef-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8baef-112">Requirements</span></span>  
 <span data-ttu-id="8baef-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8baef-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8baef-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8baef-114">See also</span></span>

- [<span data-ttu-id="8baef-115">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="8baef-115">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
