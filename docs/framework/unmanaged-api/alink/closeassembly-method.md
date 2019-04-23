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
ms.openlocfilehash: 94c1c083d010cd82fd9e9e2f02b23e81d88fedd5
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59116439"
---
# <a name="closeassembly-method"></a><span data-ttu-id="1e08f-102">CloseAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="1e08f-102">CloseAssembly Method</span></span>
<span data-ttu-id="1e08f-103">Finalise les opérations d’assembly.</span><span class="sxs-lookup"><span data-stu-id="1e08f-103">Finalizes assembly operations.</span></span> <span data-ttu-id="1e08f-104">Appelez cette méthode avant de commencer un nouvel assembly ou un module indépendant.</span><span class="sxs-lookup"><span data-stu-id="1e08f-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e08f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e08f-105">Syntax</span></span>  
  
```  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="1e08f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e08f-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="1e08f-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="1e08f-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1e08f-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1e08f-108">Return Value</span></span>  
 <span data-ttu-id="1e08f-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="1e08f-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e08f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e08f-110">Requirements</span></span>  
 <span data-ttu-id="1e08f-111">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="1e08f-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e08f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e08f-112">See also</span></span>

- [<span data-ttu-id="1e08f-113">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="1e08f-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="1e08f-114">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="1e08f-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="1e08f-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="1e08f-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
