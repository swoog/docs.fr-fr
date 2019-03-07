---
title: CloseAssembly, méthode
ms.date: 03/30/2017
api_name:
- IALink.CloseAssembly
- CloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseAssembly
helpviewer_keywords:
- CloseAssembly method
ms.assetid: f66a43bc-a5c5-4190-acbe-63fd27640634
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c89fd080e61db78ed21c03c2aa63c97337c09585
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57497546"
---
# <a name="closeassembly-method"></a><span data-ttu-id="0e8b8-102">CloseAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="0e8b8-102">CloseAssembly Method</span></span>
<span data-ttu-id="0e8b8-103">Finalise les opérations d’assembly.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-103">Finalizes assembly operations.</span></span> <span data-ttu-id="0e8b8-104">Appelez cette méthode avant de commencer un nouvel assembly ou un module indépendant.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e8b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e8b8-105">Syntax</span></span>  
  
```  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="0e8b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e8b8-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="0e8b8-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0e8b8-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0e8b8-108">Return Value</span></span>  
 <span data-ttu-id="0e8b8-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e8b8-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0e8b8-110">Requirements</span></span>  
 <span data-ttu-id="0e8b8-111">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="0e8b8-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e8b8-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e8b8-112">See also</span></span>
- [<span data-ttu-id="0e8b8-113">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="0e8b8-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="0e8b8-114">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="0e8b8-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="0e8b8-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="0e8b8-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
