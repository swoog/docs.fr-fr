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
ms.openlocfilehash: 5825f0425947f109ed834879684357fef7b70959
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49123772"
---
# <a name="isymunmanagedwriterdefinesequencepoints-method"></a><span data-ttu-id="02bc1-102">ISymUnmanagedWriter::DefineSequencePoints, méthode</span><span class="sxs-lookup"><span data-stu-id="02bc1-102">ISymUnmanagedWriter::DefineSequencePoints Method</span></span>
<span data-ttu-id="02bc1-103">Définit un groupe de points de séquence dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="02bc1-103">Defines a group of sequence points within the current method.</span></span> <span data-ttu-id="02bc1-104">Chaque ligne de début et de la colonne de départ définit le début d’une instruction dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="02bc1-104">Each starting line and starting column define the start of a statement within a method.</span></span> <span data-ttu-id="02bc1-105">Chaque ligne de fin et la colonne de fin définissent la fin d’une instruction dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="02bc1-105">Each ending line and ending column define the end of a statement within a method.</span></span> <span data-ttu-id="02bc1-106">Les tableaux doivent être triés dans l’ordre croissant des offsets.</span><span class="sxs-lookup"><span data-stu-id="02bc1-106">The arrays should be sorted in increasing order of offsets.</span></span> <span data-ttu-id="02bc1-107">L’offset est toujours mesuré depuis le début de la méthode, en octets.</span><span class="sxs-lookup"><span data-stu-id="02bc1-107">The offset is always measured from the start of the method, in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="02bc1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02bc1-108">Syntax</span></span>  
  
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
  
#### <a name="parameters"></a><span data-ttu-id="02bc1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02bc1-109">Parameters</span></span>  
 `document`  
 <span data-ttu-id="02bc1-110">[in] L’objet de document pour lequel les points de séquence sont définies.</span><span class="sxs-lookup"><span data-stu-id="02bc1-110">[in] The document object for which the sequence points are being defined.</span></span>  
  
 `spCount`  
 <span data-ttu-id="02bc1-111">[in] Un `ULONG32` qui indique la taille de la `offsets`, `lines`, `columns`, `endLines`, et `endColumns` mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="02bc1-111">[in] A `ULONG32` that indicates the size of each of the `offsets`, `lines`, `columns`, `endLines`, and `endColumns` buffers.</span></span>  
  
 `offsets`  
 <span data-ttu-id="02bc1-112">[in] Le décalage des points de séquence mesuré à partir du début de la méthode.</span><span class="sxs-lookup"><span data-stu-id="02bc1-112">[in] The offset of the sequence points measured from the beginning of the method.</span></span>  
  
 `lines`  
 <span data-ttu-id="02bc1-113">[in] Les numéros de ligne de début des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="02bc1-113">[in] The starting line numbers of the sequence points.</span></span>  
  
 `columns`  
 <span data-ttu-id="02bc1-114">[in] Les numéros de colonne de départ des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="02bc1-114">[in] The starting column numbers of the sequence points.</span></span>  
  
 `endLines`  
 <span data-ttu-id="02bc1-115">[in] Les numéros de ligne de fin des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="02bc1-115">[in] The ending line numbers of the sequence points.</span></span> <span data-ttu-id="02bc1-116">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="02bc1-116">This parameter is optional.</span></span>  
  
 `endColumns`  
 <span data-ttu-id="02bc1-117">[in] Les numéros de colonne de fin des points de séquence.</span><span class="sxs-lookup"><span data-stu-id="02bc1-117">[in] The ending column numbers of the sequence points.</span></span> <span data-ttu-id="02bc1-118">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="02bc1-118">This parameter is optional.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="02bc1-119">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="02bc1-119">Return Value</span></span>  
 <span data-ttu-id="02bc1-120">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="02bc1-120">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="02bc1-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02bc1-121">Requirements</span></span>  
 <span data-ttu-id="02bc1-122">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="02bc1-122">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02bc1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02bc1-123">See Also</span></span>  
 [<span data-ttu-id="02bc1-124">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="02bc1-124">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
