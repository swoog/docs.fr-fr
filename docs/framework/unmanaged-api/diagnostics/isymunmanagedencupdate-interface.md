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
ms.openlocfilehash: 05cbe098b73dd817546dd72f0fc98ad548f75386
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425416"
---
# <a name="isymunmanagedencupdate-interface"></a><span data-ttu-id="f2d6d-102">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="f2d6d-102">ISymUnmanagedENCUpdate Interface</span></span>
<span data-ttu-id="f2d6d-103">Fournit des fonctions pour la fonctionnalité Modifier & Continuer.</span><span class="sxs-lookup"><span data-stu-id="f2d6d-103">Provides functions for the Edit and Continue feature.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f2d6d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f2d6d-104">Methods</span></span>  
  
|<span data-ttu-id="f2d6d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f2d6d-105">Method</span></span>|<span data-ttu-id="f2d6d-106">Description</span><span class="sxs-lookup"><span data-stu-id="f2d6d-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f2d6d-107">GetLocalVariableCount, méthode</span><span class="sxs-lookup"><span data-stu-id="f2d6d-107">GetLocalVariableCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-getlocalvariablecount-method.md)|<span data-ttu-id="f2d6d-108">Obtient le nombre de variables locales.</span><span class="sxs-lookup"><span data-stu-id="f2d6d-108">Gets the number of local variables.</span></span>|  
|[<span data-ttu-id="f2d6d-109">GetLocalVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="f2d6d-109">GetLocalVariables Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-getlocalvariables-method.md)|<span data-ttu-id="f2d6d-110">Obtient les variables locales.</span><span class="sxs-lookup"><span data-stu-id="f2d6d-110">Gets the local variables.</span></span>|  
|[<span data-ttu-id="f2d6d-111">InitializeForEnc, méthode</span><span class="sxs-lookup"><span data-stu-id="f2d6d-111">InitializeForEnc Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-initializeforenc-method.md)|<span data-ttu-id="f2d6d-112">Permet le calcul des limites de méthode avant le premier appel à la [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f2d6d-112">Allows method boundaries to be computed before the first call to the [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) method.</span></span>|  
|[<span data-ttu-id="f2d6d-113">UpdateMethodLines, méthode</span><span class="sxs-lookup"><span data-stu-id="f2d6d-113">UpdateMethodLines Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatemethodlines-method.md)|<span data-ttu-id="f2d6d-114">Permet de mettre à jour les informations de ligne pour une méthode qui n’a pas été recompilée, mais dont les lignes ont été déplacées indépendamment.</span><span class="sxs-lookup"><span data-stu-id="f2d6d-114">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="f2d6d-115">Un delta pour chaque instruction est autorisée.</span><span class="sxs-lookup"><span data-stu-id="f2d6d-115">A delta for each statement is allowed.</span></span>|  
|[<span data-ttu-id="f2d6d-116">UpdateSymbolStore2, méthode</span><span class="sxs-lookup"><span data-stu-id="f2d6d-116">UpdateSymbolStore2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md)|<span data-ttu-id="f2d6d-117">Permet à un compilateur d’omettre des fonctions qui n’ont pas été modifiées flux du programme (PDB) de la base de données, sous réserve que les informations de ligne répond aux exigences.</span><span class="sxs-lookup"><span data-stu-id="f2d6d-117">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided that the line information meets the requirements.</span></span> <span data-ttu-id="f2d6d-118">Les informations de ligne correct peuvent être déterminées avec les anciennes informations de ligne PDB et un delta pour toutes les lignes de la fonction.</span><span class="sxs-lookup"><span data-stu-id="f2d6d-118">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f2d6d-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f2d6d-119">Requirements</span></span>  
 <span data-ttu-id="f2d6d-120">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f2d6d-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2d6d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2d6d-121">See Also</span></span>  
 [<span data-ttu-id="f2d6d-122">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="f2d6d-122">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
