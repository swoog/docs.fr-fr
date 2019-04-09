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
ms.openlocfilehash: 378322c28d59b2a6e7c09f2f2c4bf55bb019d01d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59171833"
---
# <a name="isymunmanagedencupdate-interface"></a><span data-ttu-id="13369-102">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="13369-102">ISymUnmanagedENCUpdate Interface</span></span>
<span data-ttu-id="13369-103">Fournit des fonctions pour la fonctionnalité Modifier & Continuer.</span><span class="sxs-lookup"><span data-stu-id="13369-103">Provides functions for the Edit and Continue feature.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="13369-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="13369-104">Methods</span></span>  
  
|<span data-ttu-id="13369-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="13369-105">Method</span></span>|<span data-ttu-id="13369-106">Description</span><span class="sxs-lookup"><span data-stu-id="13369-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="13369-107">GetLocalVariableCount, méthode</span><span class="sxs-lookup"><span data-stu-id="13369-107">GetLocalVariableCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-getlocalvariablecount-method.md)|<span data-ttu-id="13369-108">Obtient le nombre de variables locales.</span><span class="sxs-lookup"><span data-stu-id="13369-108">Gets the number of local variables.</span></span>|  
|[<span data-ttu-id="13369-109">GetLocalVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="13369-109">GetLocalVariables Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-getlocalvariables-method.md)|<span data-ttu-id="13369-110">Obtient les variables locales.</span><span class="sxs-lookup"><span data-stu-id="13369-110">Gets the local variables.</span></span>|  
|[<span data-ttu-id="13369-111">InitializeForEnc, méthode</span><span class="sxs-lookup"><span data-stu-id="13369-111">InitializeForEnc Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-initializeforenc-method.md)|<span data-ttu-id="13369-112">Permet le calcul des limites de méthode avant le premier appel à la [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="13369-112">Allows method boundaries to be computed before the first call to the [ISymUnmanagedENCUpdate::UpdateSymbolStore2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md) method.</span></span>|  
|[<span data-ttu-id="13369-113">UpdateMethodLines, méthode</span><span class="sxs-lookup"><span data-stu-id="13369-113">UpdateMethodLines Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatemethodlines-method.md)|<span data-ttu-id="13369-114">Permet la mise à jour les informations de ligne pour une méthode qui n’a pas été compilé, mais dont les lignes ont été déplacées indépendamment.</span><span class="sxs-lookup"><span data-stu-id="13369-114">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="13369-115">Un delta pour chaque instruction est autorisé.</span><span class="sxs-lookup"><span data-stu-id="13369-115">A delta for each statement is allowed.</span></span>|  
|[<span data-ttu-id="13369-116">UpdateSymbolStore2, méthode</span><span class="sxs-lookup"><span data-stu-id="13369-116">UpdateSymbolStore2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-updatesymbolstore2-method.md)|<span data-ttu-id="13369-117">Permet à un compilateur d’omettre des fonctions qui n’ont pas été modifiées flux du programme (PDB) de la base de données, sous réserve que les informations de ligne répond aux exigences.</span><span class="sxs-lookup"><span data-stu-id="13369-117">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided that the line information meets the requirements.</span></span> <span data-ttu-id="13369-118">Les informations de ligne correctes peuvent être déterminées avec les anciennes informations de ligne PDB et un delta pour toutes les lignes de la fonction.</span><span class="sxs-lookup"><span data-stu-id="13369-118">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="13369-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13369-119">Requirements</span></span>  
 <span data-ttu-id="13369-120">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="13369-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13369-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13369-121">See also</span></span>

- [<span data-ttu-id="13369-122">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="13369-122">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
