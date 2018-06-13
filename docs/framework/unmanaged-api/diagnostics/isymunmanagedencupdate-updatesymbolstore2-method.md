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
ms.openlocfilehash: 02eaaa1c3336b6e99b8c8deabb944e292e35a2a7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425174"
---
# <a name="isymunmanagedencupdateupdatesymbolstore2-method"></a><span data-ttu-id="b4889-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2, méthode</span><span class="sxs-lookup"><span data-stu-id="b4889-102">ISymUnmanagedENCUpdate::UpdateSymbolStore2 Method</span></span>
<span data-ttu-id="b4889-103">Permet à un compilateur d’omettre des fonctions qui n’ont pas été modifiées flux du programme (PDB) de la base de données, fourni les informations de ligne répond aux exigences.</span><span class="sxs-lookup"><span data-stu-id="b4889-103">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided the line information meets the requirements.</span></span> <span data-ttu-id="b4889-104">Les informations de ligne correct peuvent être déterminées avec les anciennes informations de ligne PDB et un delta pour toutes les lignes de la fonction.</span><span class="sxs-lookup"><span data-stu-id="b4889-104">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4889-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4889-105">Syntax</span></span>  
  
```  
HRESULT UpdateSymbolStore2(  
    [in]  IStream      *pIStream,  
    [in]  SYMLINEDELTA* pDeltaLines,  
    [in]  ULONG         cDeltaLines);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b4889-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4889-106">Parameters</span></span>  
 `pIStream`  
 <span data-ttu-id="b4889-107">[in] Un pointeur vers un [IStream](https://msdn.microsoft.com/library/aa380034.aspx) qui contient les informations de ligne.</span><span class="sxs-lookup"><span data-stu-id="b4889-107">[in] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034.aspx) that contains the line information.</span></span>  
  
 `pDeltaLines`  
 <span data-ttu-id="b4889-108">[in] Un pointeur vers un [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) structure qui contient les lignes qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="b4889-108">[in] A pointer to a [SYMLINEDELTA](../../../../docs/framework/unmanaged-api/diagnostics/symlinedelta-structure.md) structure that contains the lines that have changed.</span></span>  
  
 `cDeltaLines`  
 <span data-ttu-id="b4889-109">[in] Un `ULONG` qui représente le nombre de lignes qui ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="b4889-109">[in] A `ULONG` that represents the number of lines that have changed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b4889-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b4889-110">Return Value</span></span>  
 <span data-ttu-id="b4889-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b4889-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b4889-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b4889-112">Requirements</span></span>  
 <span data-ttu-id="b4889-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b4889-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4889-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4889-114">See Also</span></span>  
 [<span data-ttu-id="b4889-115">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="b4889-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
