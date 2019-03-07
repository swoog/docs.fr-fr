---
title: EndMerge, méthode
ms.date: 03/30/2017
api_name:
- IALink.EndMerge
- EndMerge
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EndMerge
helpviewer_keywords:
- EndMerge method
ms.assetid: 1d03bb15-a2c8-4a04-8fc6-b126c89c3778
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7d4b102485db0199f748f6c5b6c4ab40d21429e9
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57494408"
---
# <a name="endmerge-method"></a><span data-ttu-id="7f40c-102">EndMerge, méthode</span><span class="sxs-lookup"><span data-stu-id="7f40c-102">EndMerge Method</span></span>
<span data-ttu-id="7f40c-103">Indique que tous les attributs personnalisés ont été fusionnés dans la portée d’émission.</span><span class="sxs-lookup"><span data-stu-id="7f40c-103">Indicates that all custom attributes have been merged into the emit scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f40c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f40c-104">Syntax</span></span>  
  
```  
HRESULT EndMerge(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="7f40c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f40c-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="7f40c-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="7f40c-106">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7f40c-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7f40c-107">Return Value</span></span>  
 <span data-ttu-id="7f40c-108">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="7f40c-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f40c-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7f40c-109">Requirements</span></span>  
 <span data-ttu-id="7f40c-110">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="7f40c-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f40c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f40c-111">See also</span></span>
- [<span data-ttu-id="7f40c-112">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="7f40c-112">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="7f40c-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="7f40c-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="7f40c-114">API ALink</span><span class="sxs-lookup"><span data-stu-id="7f40c-114">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
