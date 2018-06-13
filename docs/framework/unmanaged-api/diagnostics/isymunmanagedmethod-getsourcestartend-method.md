---
title: ISymUnmanagedMethod::GetSourceStartEnd, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSourceStartEnd
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSourceStartEnd
helpviewer_keywords:
- GetSourceStartEnd method [.NET Framework debugging]
- ISymUnmanagedMethod::GetSourceStartEnd method [.NET Framework debugging]
ms.assetid: 2a420900-01f1-4461-8777-3a34a6dc1426
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1e15bab136540c73f8e1cff0e6bb52ec1d6c0063
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426222"
---
# <a name="isymunmanagedmethodgetsourcestartend-method"></a><span data-ttu-id="20b90-102">ISymUnmanagedMethod::GetSourceStartEnd, méthode</span><span class="sxs-lookup"><span data-stu-id="20b90-102">ISymUnmanagedMethod::GetSourceStartEnd Method</span></span>
<span data-ttu-id="20b90-103">Obtient les positions de document de début et de fin de la source de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="20b90-103">Gets the start and end document positions for the source of this method.</span></span> <span data-ttu-id="20b90-104">La première position du tableau correspond au début, et la deuxième position du tableau est à la fin.</span><span class="sxs-lookup"><span data-stu-id="20b90-104">The first array position is the start, and the second array position is the end.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20b90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20b90-105">Syntax</span></span>  
  
```  
HRESULT GetSourceStartEnd(  
    [in]  ISymUnmanagedDocument  *docs[2],  
    [in]  ULONG32                lines[2],  
    [in]  ULONG32                columns[2],  
    [out] BOOL                   *pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="20b90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20b90-106">Parameters</span></span>  
 `docs`  
 <span data-ttu-id="20b90-107">[in] Le début et de fin de documents sources.</span><span class="sxs-lookup"><span data-stu-id="20b90-107">[in] The starting and ending source documents.</span></span>  
  
 `lines`  
 <span data-ttu-id="20b90-108">[in] Documents de sources de début et de fin de ligne qui correspond.</span><span class="sxs-lookup"><span data-stu-id="20b90-108">[in] The starting and ending lines in the corresponding source documents.</span></span>  
  
 `columns`  
 <span data-ttu-id="20b90-109">[in] Documents de sources de début et fin des colonnes, qui correspond.</span><span class="sxs-lookup"><span data-stu-id="20b90-109">[in] The starting and ending columns in the corresponding source documents.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="20b90-110">[out] `true` si les positions ont été définies ; sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="20b90-110">[out] `true` if positions were defined; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="20b90-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="20b90-111">Return Value</span></span>  
 <span data-ttu-id="20b90-112">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="20b90-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20b90-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="20b90-113">Requirements</span></span>  
 <span data-ttu-id="20b90-114">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="20b90-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20b90-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20b90-115">See Also</span></span>  
 [<span data-ttu-id="20b90-116">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="20b90-116">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
