---
title: ISymUnmanagedWriter4, interface
ms.date: 03/30/2017
ms.assetid: 4af5e8c0-987d-405e-b934-8b9e70fcae6e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8a5e44541a18f10588e899f59a166406c149691f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54650048"
---
# <a name="isymunmanagedwriter4-interface"></a><span data-ttu-id="155ac-102">ISymUnmanagedWriter4, interface</span><span class="sxs-lookup"><span data-stu-id="155ac-102">ISymUnmanagedWriter4 Interface</span></span>
<span data-ttu-id="155ac-103">Isymunmanagedwriter4, interface.</span><span class="sxs-lookup"><span data-stu-id="155ac-103">ISymUnmanagedWriter4 interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="155ac-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="155ac-104">Syntax</span></span>  
  
```idl  
[object,uuid(BC7E3F53-F458-4C23-9DBD-A189E6E96594),pointer_default(unique)]interface ISymUnmanagedWriter4 : ISymUnmanagedWriter3  
```  
  
## <a name="methods"></a><span data-ttu-id="155ac-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="155ac-105">Methods</span></span>  
 <span data-ttu-id="155ac-106">Cette interface contient les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="155ac-106">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="155ac-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="155ac-107">Method</span></span>|<span data-ttu-id="155ac-108">Description</span><span class="sxs-lookup"><span data-stu-id="155ac-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="155ac-109">GetDebugInfoWithPadding, méthode</span><span class="sxs-lookup"><span data-stu-id="155ac-109">GetDebugInfoWithPadding Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-getdebuginfowithpadding-method.md)|<span data-ttu-id="155ac-110">Fonctionne comme [GetDebugInfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) , à ceci près que la chaîne de chemin d’accès est remplie avec des zéros qui suivent le caractère null de fin pour rendre les données de chaîne de taille fixe de `MAX_PATH`.</span><span class="sxs-lookup"><span data-stu-id="155ac-110">Functions the same as [GetDebugInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) except that the path string is padded with zeros following the terminating null character to make the string data a fixed size of `MAX_PATH`.</span></span> <span data-ttu-id="155ac-111">Marge intérieure est obtenu uniquement si la longueur de chaîne de chemin d’accès lui-même est inférieure à `MAX_PATH`.</span><span class="sxs-lookup"><span data-stu-id="155ac-111">Padding is only given if the path string length itself is less than `MAX_PATH`.</span></span><br /><br /> <span data-ttu-id="155ac-112">Cela rend plus facile à écrire des outils que les fichiers PE de différence.</span><span class="sxs-lookup"><span data-stu-id="155ac-112">This makes it easier to write tools that difference PE files.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="155ac-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="155ac-113">Requirements</span></span>  
 <span data-ttu-id="155ac-114">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="155ac-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="155ac-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="155ac-115">See also</span></span>
- [<span data-ttu-id="155ac-116">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="155ac-116">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="155ac-117">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="155ac-117">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
