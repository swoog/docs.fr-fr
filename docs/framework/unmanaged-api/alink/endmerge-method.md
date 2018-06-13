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
ms.openlocfilehash: e8f9eecd6d6d74717eb7c1e389bfa24e40afc950
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402572"
---
# <a name="endmerge-method"></a><span data-ttu-id="73df5-102">EndMerge, méthode</span><span class="sxs-lookup"><span data-stu-id="73df5-102">EndMerge Method</span></span>
<span data-ttu-id="73df5-103">Indique que tous les attributs personnalisés ont été fusionnées dans la portée d’émission.</span><span class="sxs-lookup"><span data-stu-id="73df5-103">Indicates that all custom attributes have been merged into the emit scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="73df5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73df5-104">Syntax</span></span>  
  
```  
HRESULT EndMerge(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="73df5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73df5-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="73df5-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="73df5-106">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="73df5-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="73df5-107">Return Value</span></span>  
 <span data-ttu-id="73df5-108">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="73df5-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="73df5-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="73df5-109">Requirements</span></span>  
 <span data-ttu-id="73df5-110">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="73df5-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="73df5-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73df5-111">See Also</span></span>  
 [<span data-ttu-id="73df5-112">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="73df5-112">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="73df5-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="73df5-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="73df5-114">API ALink</span><span class="sxs-lookup"><span data-stu-id="73df5-114">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
