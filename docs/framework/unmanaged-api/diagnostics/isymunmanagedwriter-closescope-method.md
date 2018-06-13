---
title: ISymUnmanagedWriter::CloseScope, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseScope
helpviewer_keywords:
- CloseScope method [.NET Framework debugging]
- ISymUnmanagedWriter::CloseScope method [.NET Framework debugging]
ms.assetid: 6dade525-7770-4cb4-bafd-4bb995ad0d87
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a11f689f1fa93e1122ffcc78187c4287db7ea534
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427022"
---
# <a name="isymunmanagedwriterclosescope-method"></a><span data-ttu-id="bc9b1-102">ISymUnmanagedWriter::CloseScope, méthode</span><span class="sxs-lookup"><span data-stu-id="bc9b1-102">ISymUnmanagedWriter::CloseScope Method</span></span>
<span data-ttu-id="bc9b1-103">Ferme la portée lexicale actuelle.</span><span class="sxs-lookup"><span data-stu-id="bc9b1-103">Closes the current lexical scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc9b1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc9b1-104">Syntax</span></span>  
  
```  
HRESULT CloseScope(  
    [in] ULONG32 endOffset);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bc9b1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc9b1-105">Parameters</span></span>  
 `endOffset`  
 <span data-ttu-id="bc9b1-106">[in] Le décalage à partir du début de la méthode du point à la fin de la dernière instruction dans la portée lexicale, en octets.</span><span class="sxs-lookup"><span data-stu-id="bc9b1-106">[in] The offset from the beginning of the method of the point at the end of the last instruction in the lexical scope, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bc9b1-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bc9b1-107">Return Value</span></span>  
 <span data-ttu-id="bc9b1-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bc9b1-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bc9b1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bc9b1-109">Remarks</span></span>  
 <span data-ttu-id="bc9b1-110">Une fois qu’une portée est fermée, aucuns plus de variables ne peuvent être définies qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="bc9b1-110">Once a scope is closed, no more variables can be defined within it.</span></span>  
  
 <span data-ttu-id="bc9b1-111">[ISymUnmanagedWriter::OpenScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md) retourne un identificateur de portée opaque qui peut être utilisé avec [ISymUnmanagedWriter::SetScopeRange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md) pour définir ultérieurement une étendue de démarrage et le décalage de fin.</span><span class="sxs-lookup"><span data-stu-id="bc9b1-111">[ISymUnmanagedWriter::OpenScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md) returns an opaque scope identifier that can be used with [ISymUnmanagedWriter::SetScopeRange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md) to later define a scope's starting and ending offset.</span></span> <span data-ttu-id="bc9b1-112">Dans ce cas, les offsets passés à `ISymUnmanagedWriter::OpenScope` et `ISymUnmanagedWriter::CloseScope` sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="bc9b1-112">In this case, the offsets passed to `ISymUnmanagedWriter::OpenScope` and `ISymUnmanagedWriter::CloseScope` are ignored.</span></span> <span data-ttu-id="bc9b1-113">Les identificateurs de portée sont valides uniquement dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="bc9b1-113">Scope identifiers are valid only in the current method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bc9b1-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bc9b1-114">Requirements</span></span>  
 <span data-ttu-id="bc9b1-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="bc9b1-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc9b1-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc9b1-116">See Also</span></span>  
 [<span data-ttu-id="bc9b1-117">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="bc9b1-117">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
