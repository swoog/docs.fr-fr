---
title: ISymUnmanagedENCUpdate::UpdateSymbolStore2, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.UpdateSymbolStore2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2
helpviewer_keywords:
- ISymUnmanagedENCUpdate::UpdateSymbolStore2 method [.NET Framework debugging]
- UpdateSymbolStore2 method [.NET Framework debugging]
ms.assetid: 35588317-6184-485c-ab41-4b15fc1765d9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 78d9e27299c9d7ed7d6cb9b09dd659ba081c5fde
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43876253"
---
# <a name="isymunmanagedencupdateupdatesymbolstore2-method"></a><span data-ttu-id="793a0-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2, méthode</span><span class="sxs-lookup"><span data-stu-id="793a0-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2 Method</span></span>
<span data-ttu-id="793a0-103">Permet à un compilateur d’omettre des fonctions qui n’ont pas été modifiées flux du programme (PDB) de la base de données, fournie par les informations de ligne répond aux exigences.</span><span class="sxs-lookup"><span data-stu-id="793a0-103">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided the line information meets the requirements.</span></span> <span data-ttu-id="793a0-104">Les informations de ligne correctes peuvent être déterminées avec les anciennes informations de ligne PDB et un delta pour toutes les lignes de la fonction.</span><span class="sxs-lookup"><span data-stu-id="793a0-104">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="793a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="793a0-105">Syntax</span></span>  
  
```  
HRESULT UpdateSymbolStore2(  
    [in]  IStream      *pIStream,  
    [in]  SYMLINEDELTA* pDeltaLines,  
    [in]  ULONG         cDeltaLines);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="793a0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="793a0-106">Parameters</span></span>  
 `pIStream`  
 <span data-ttu-id="793a0-107">[in] Un pointeur vers un [IStream](/windows/desktop/api/objidl/nn-objidl-istream) qui contient les informations de ligne.</span><span class="sxs-lookup"><span data-stu-id="793a0-107">[in] A pointer to an [IStream](/windows/desktop/api/objidl/nn-objidl-istream) that contains the line information.</span></span>  
  
 `pDeltaLines`  
 <span data-ttu-id="793a0-108">[in] Un pointeur vers un [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) structure qui contient les lignes qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="793a0-108">[in] A pointer to a [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) structure that contains the lines that have changed.</span></span>  
  
 `cDeltaLines`  
 <span data-ttu-id="793a0-109">[in] Un `ULONG` qui représente le nombre de lignes qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="793a0-109">[in] A `ULONG` that represents the number of lines that have changed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="793a0-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="793a0-110">Return Value</span></span>  
 <span data-ttu-id="793a0-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="793a0-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="793a0-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="793a0-112">Requirements</span></span>  
 <span data-ttu-id="793a0-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="793a0-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="793a0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="793a0-114">See Also</span></span>  
 [<span data-ttu-id="793a0-115">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="793a0-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
