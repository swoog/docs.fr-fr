---
title: ISymENCUnmanagedMethod::GetFileNameFromOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetFileNameFromOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetFileNameFromOffset
helpviewer_keywords:
- GetFileNameFromOffset method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetFileNameFromOffset method [.NET Framework debugging]
ms.assetid: 00e2e194-12f5-436e-a997-2b9d3e844d4f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: db3e9cfa73672920ff70d9128541a8f513fca00f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432654"
---
# <a name="isymencunmanagedmethodgetfilenamefromoffset-method"></a><span data-ttu-id="0476a-102">ISymENCUnmanagedMethod::GetFileNameFromOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="0476a-102">ISymENCUnmanagedMethod::GetFileNameFromOffset Method</span></span>
<span data-ttu-id="0476a-103">Obtient le nom de fichier pour la ligne associée à un offset.</span><span class="sxs-lookup"><span data-stu-id="0476a-103">Gets the file name for the line associated with an offset.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0476a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0476a-104">Syntax</span></span>  
  
```  
HRESULT GetFileNameFromOffset(  
    [in]  ULONG32  dwOffset,  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
       length_is(*pcchName)] WCHAR szName[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0476a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0476a-105">Parameters</span></span>  
 `dwOffset`  
 <span data-ttu-id="0476a-106">[in] Un `ULONG32` qui contient le décalage.</span><span class="sxs-lookup"><span data-stu-id="0476a-106">[in] A `ULONG32` that contains the offset.</span></span>  
  
 `cchName`  
 <span data-ttu-id="0476a-107">[in] A `ULONG32` qui indique la taille de la `szName` mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0476a-107">[in] A `ULONG32` that indicates the size of the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="0476a-108">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0476a-108">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the file names.</span></span>  
  
 `szName`  
 <span data-ttu-id="0476a-109">[out] Mémoire tampon qui contient les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0476a-109">[out] The buffer that contains the file names.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0476a-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0476a-110">Return Value</span></span>  
 <span data-ttu-id="0476a-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0476a-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0476a-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0476a-112">Requirements</span></span>  
 <span data-ttu-id="0476a-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="0476a-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0476a-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0476a-114">See Also</span></span>  
 [<span data-ttu-id="0476a-115">ISymENCUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="0476a-115">ISymENCUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymencunmanagedmethod-interface.md)
