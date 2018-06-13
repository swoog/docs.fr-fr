---
title: ISymUnmanagedWriter4, interface
ms.date: 03/30/2017
ms.assetid: 4af5e8c0-987d-405e-b934-8b9e70fcae6e
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5e8478aed662142b9ff4b73f9cb192f8d2306e2a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429684"
---
# <a name="isymunmanagedwriter4-interface"></a><span data-ttu-id="8557f-102">ISymUnmanagedWriter4, interface</span><span class="sxs-lookup"><span data-stu-id="8557f-102">ISymUnmanagedWriter4 Interface</span></span>
<span data-ttu-id="8557f-103">Isymunmanagedwriter4, interface.</span><span class="sxs-lookup"><span data-stu-id="8557f-103">ISymUnmanagedWriter4 interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8557f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8557f-104">Syntax</span></span>  
  
```idl  
[object,uuid(BC7E3F53-F458-4C23-9DBD-A189E6E96594),pointer_default(unique)]interface ISymUnmanagedWriter4 : ISymUnmanagedWriter3  
```  
  
## <a name="methods"></a><span data-ttu-id="8557f-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8557f-105">Methods</span></span>  
 <span data-ttu-id="8557f-106">Cette interface contient les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8557f-106">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="8557f-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="8557f-107">Method</span></span>|<span data-ttu-id="8557f-108">Description</span><span class="sxs-lookup"><span data-stu-id="8557f-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8557f-109">GetDebugInfoWithPadding, méthode</span><span class="sxs-lookup"><span data-stu-id="8557f-109">GetDebugInfoWithPadding Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-getdebuginfowithpadding-method.md)|<span data-ttu-id="8557f-110">Fonctionne comme [GetDebugInfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) , sauf que la chaîne de chemin d’accès est complétée avec des zéros qui suivent le caractère null de fin pour rendre les données de chaîne de taille fixe de `MAX_PATH`.</span><span class="sxs-lookup"><span data-stu-id="8557f-110">Functions the same as [GetDebugInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-getdebuginfo-method.md) except that the path string is padded with zeros following the terminating null character to make the string data a fixed size of `MAX_PATH`.</span></span> <span data-ttu-id="8557f-111">Marge intérieure ne reçoit que si la longueur de chaîne de chemin d’accès lui-même est inférieure à `MAX_PATH`.</span><span class="sxs-lookup"><span data-stu-id="8557f-111">Padding is only given if the path string length itself is less than `MAX_PATH`.</span></span><br /><br /> <span data-ttu-id="8557f-112">Cela rend plus facile d’écrire des outils que les fichiers PE de différence.</span><span class="sxs-lookup"><span data-stu-id="8557f-112">This makes it easier to write tools that difference PE files.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8557f-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8557f-113">Requirements</span></span>  
 <span data-ttu-id="8557f-114">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8557f-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8557f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8557f-115">See Also</span></span>  
 [<span data-ttu-id="8557f-116">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="8557f-116">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)  
 [<span data-ttu-id="8557f-117">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="8557f-117">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
