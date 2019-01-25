---
title: ISymUnmanagedWriter::DefineSequencePoints, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineSequencePoints
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineSequencePoints
helpviewer_keywords:
- DefineSequencePoints method [.NET Framework debugging]
- ISymUnmanagedWriter::DefineSequencePoints method [.NET Framework debugging]
ms.assetid: 64202baf-be6b-40ba-8162-8cc6c0c9b8e1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 76d3be88065d4f29020a794db30c616774db1f4f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54580848"
---
# <a name="isymunmanagedwriterdefinesequencepoints-method"></a><span data-ttu-id="50971-102">ISymUnmanagedWriter::DefineSequencePoints, méthode</span><span class="sxs-lookup"><span data-stu-id="50971-102">ISymUnmanagedWriter::DefineSequencePoints Method</span></span>
<span data-ttu-id="50971-103">Définit un groupe de points de séquence dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="50971-103">Defines a group of sequence points within the current method.</span></span> <span data-ttu-id="50971-104">Chaque ligne de début et de la colonne de départ définit le début d’une instruction dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="50971-104">Each starting line and starting column define the start of a statement within a method.</span></span> <span data-ttu-id="50971-105">Chaque ligne de fin et la colonne de fin définissent la fin d’une instruction dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="50971-105">Each ending line and ending column define the end of a statement within a method.</span></span> <span data-ttu-id="50971-106">Les tableaux doivent être triés dans l’ordre croissant des offsets.</span><span class="sxs-lookup"><span data-stu-id="50971-106">The arrays should be sorted in increasing order of offsets.</span></span> <span data-ttu-id="50971-107">L’offset est toujours mesuré depuis le début de la méthode, en octets.</span><span class="sxs-lookup"><span data-stu-id="50971-107">The offset is always measured from the start of the method, in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50971-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50971-108">Syntax</span></span>  
  
```  
HRESULT DefineSequencePoints(  
    [in] ISymUnmanagedDocumentWriter*  document,  
    [in] ULONG32 spCount,  
    [in, size_is(spCount)] ULONG32     offsets[],  
    [in, size_is(spCount)] ULONG32     lines[],  
    [in, size_is(spCount)] ULONG32     columns[],  
    [in, size_is(spCount)] ULONG32     endLines[],  
    [in, size_is(spCount)] ULONG32     endColumns[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="50971-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50971-109">Parameters</span></span>  
 `document`  
 <span data-ttu-id="50971-110">[in] L’objet de document pour lequel les points de séquence sont définies.</span><span class="sxs-lookup"><span data-stu-id="50971-110">[in] The document object for which the sequence points are being defined.</span></span>  
  
 `spCount`  
 <span data-ttu-id="50971-111">[in] Un `ULONG32` qui indique la taille de la `offsets`, `lines`, `columns`, `endLines`, et `endColumns` mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="50971-111">[in] A `ULONG32` that indicates the size of each of the `offsets`, `lines`, `columns`, `endLines`, and `endColumns` buffers.</span></span>  
  
 `offsets`  
 <span data-ttu-id="50971-112">[in] Le décalage des points de séquence mesuré à partir du début de la méthode.</span><span class="sxs-lookup"><span data-stu-id="50971-112">[in] The offset of the sequence points measured from the beginning of the method.</span></span>  
  
 `lines`  
 <span data-ttu-id="50971-113">[in] Les numéros de ligne de début des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="50971-113">[in] The starting line numbers of the sequence points.</span></span>  
  
 `columns`  
 <span data-ttu-id="50971-114">[in] Les numéros de colonne de départ des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="50971-114">[in] The starting column numbers of the sequence points.</span></span>  
  
 `endLines`  
 <span data-ttu-id="50971-115">[in] Les numéros de ligne de fin des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="50971-115">[in] The ending line numbers of the sequence points.</span></span> <span data-ttu-id="50971-116">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="50971-116">This parameter is optional.</span></span>  
  
 `endColumns`  
 <span data-ttu-id="50971-117">[in] Les numéros de colonne de fin des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="50971-117">[in] The ending column numbers of the sequence points.</span></span> <span data-ttu-id="50971-118">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="50971-118">This parameter is optional.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="50971-119">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="50971-119">Return Value</span></span>  
 <span data-ttu-id="50971-120">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="50971-120">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50971-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="50971-121">Requirements</span></span>  
 <span data-ttu-id="50971-122">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="50971-122">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50971-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50971-123">See also</span></span>
- [<span data-ttu-id="50971-124">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="50971-124">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
