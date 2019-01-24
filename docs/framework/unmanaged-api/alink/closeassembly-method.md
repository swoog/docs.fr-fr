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
ms.openlocfilehash: aa415926f4a818f697812f1a3c5531cb0ab7081b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54510167"
---
# <a name="closeassembly-method"></a><span data-ttu-id="9946e-102">CloseAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="9946e-102">CloseAssembly Method</span></span>
<span data-ttu-id="9946e-103">Finalise les opérations d’assembly.</span><span class="sxs-lookup"><span data-stu-id="9946e-103">Finalizes assembly operations.</span></span> <span data-ttu-id="9946e-104">Appelez cette méthode avant de commencer un nouvel assembly ou un module indépendant.</span><span class="sxs-lookup"><span data-stu-id="9946e-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9946e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9946e-105">Syntax</span></span>  
  
```  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9946e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9946e-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="9946e-107">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="9946e-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9946e-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9946e-108">Return Value</span></span>  
 <span data-ttu-id="9946e-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="9946e-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9946e-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9946e-110">Requirements</span></span>  
 <span data-ttu-id="9946e-111">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="9946e-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9946e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9946e-112">See also</span></span>
- [<span data-ttu-id="9946e-113">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="9946e-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="9946e-114">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="9946e-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="9946e-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="9946e-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
