---
title: ISymUnmanagedENCUpdate, interface
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate
helpviewer_keywords:
- ISymUnmanagedENCUpdate interface [.NET Framework debugging]
ms.assetid: 63a9ef45-01a6-46da-b958-5c6dc2dc232c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 634716b36a0e5826cd7667a9ae948e8172724a1e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54630864"
---
# <a name="isymunmanagedencupdate-interface"></a><span data-ttu-id="4a050-102">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="4a050-102">ISymUnmanagedENCUpdate Interface</span></span>
<span data-ttu-id="4a050-103">Fournit des fonctions pour la fonctionnalité Modifier & Continuer.</span><span class="sxs-lookup"><span data-stu-id="4a050-103">Provides functions for the Edit and Continue feature.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4a050-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4a050-104">Methods</span></span>  
  
|<span data-ttu-id="4a050-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="4a050-105">Method</span></span>|<span data-ttu-id="4a050-106">Description</span><span class="sxs-lookup"><span data-stu-id="4a050-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4a050-107">GetLocalVariableCount, méthode</span><span class="sxs-lookup"><span data-stu-id="4a050-107">GetLocalVariableCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-getlocalvariablecount-method.md)|<span data-ttu-id="4a050-108">Obtient le nombre de variables locales.</span><span class="sxs-lookup"><span data-stu-id="4a050-108">Gets the number of local variables.</span></span>|  
|[<span data-ttu-id="4a050-109">GetLocalVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="4a050-109">GetLocalVariables Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-getlocalvariables-method.md)|<span data-ttu-id="4a050-110">Obtient les variables locales.</span><span class="sxs-lookup"><span data-stu-id="4a050-110">Gets the local variables.</span></span>|  
|[<span data-ttu-id="4a050-111">InitializeForEnc, méthode</span><span class="sxs-lookup"><span data-stu-id="4a050-111">InitializeForEnc Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-initializeforenc-method.md)|<span data-ttu-id="4a050-112">Permet le calcul des limites de méthode avant le premier appel à la [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="4a050-112">Allows method boundaries to be computed before the first call to the [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) method.</span></span>|  
|[<span data-ttu-id="4a050-113">UpdateMethodLines, méthode</span><span class="sxs-lookup"><span data-stu-id="4a050-113">UpdateMethodLines Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatemethodlines-method.md)|<span data-ttu-id="4a050-114">Permet la mise à jour les informations de ligne pour une méthode qui n’a pas été compilé, mais dont les lignes ont été déplacées indépendamment.</span><span class="sxs-lookup"><span data-stu-id="4a050-114">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="4a050-115">Un delta pour chaque instruction est autorisé.</span><span class="sxs-lookup"><span data-stu-id="4a050-115">A delta for each statement is allowed.</span></span>|  
|[<span data-ttu-id="4a050-116">UpdateSymbolStore2, méthode</span><span class="sxs-lookup"><span data-stu-id="4a050-116">UpdateSymbolStore2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md)|<span data-ttu-id="4a050-117">Permet à un compilateur d’omettre des fonctions qui n’ont pas été modifiées flux du programme (PDB) de la base de données, sous réserve que les informations de ligne répond aux exigences.</span><span class="sxs-lookup"><span data-stu-id="4a050-117">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided that the line information meets the requirements.</span></span> <span data-ttu-id="4a050-118">Les informations de ligne correctes peuvent être déterminées avec les anciennes informations de ligne PDB et un delta pour toutes les lignes de la fonction.</span><span class="sxs-lookup"><span data-stu-id="4a050-118">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="4a050-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4a050-119">Requirements</span></span>  
 <span data-ttu-id="4a050-120">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="4a050-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a050-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a050-121">See also</span></span>
- [<span data-ttu-id="4a050-122">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="4a050-122">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
