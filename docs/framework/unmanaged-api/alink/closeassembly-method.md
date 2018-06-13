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
ms.openlocfilehash: 68698aab0fd0872c6e6f67e4ec531ab0226e784f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401951"
---
# <a name="closeassembly-method"></a><span data-ttu-id="927a0-102">CloseAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="927a0-102">CloseAssembly Method</span></span>
<span data-ttu-id="927a0-103">Finalise les opérations d’assembly.</span><span class="sxs-lookup"><span data-stu-id="927a0-103">Finalizes assembly operations.</span></span> <span data-ttu-id="927a0-104">Appelez cette méthode avant de commencer un nouvel assembly ou un module indépendant.</span><span class="sxs-lookup"><span data-stu-id="927a0-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="927a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="927a0-105">Syntax</span></span>  
  
```  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="927a0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="927a0-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="927a0-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="927a0-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="927a0-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="927a0-108">Return Value</span></span>  
 <span data-ttu-id="927a0-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="927a0-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="927a0-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="927a0-110">Requirements</span></span>  
 <span data-ttu-id="927a0-111">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="927a0-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="927a0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="927a0-112">See Also</span></span>  
 [<span data-ttu-id="927a0-113">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="927a0-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="927a0-114">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="927a0-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="927a0-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="927a0-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
