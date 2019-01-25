---
title: CloseEnum, méthode
ms.date: 03/30/2017
api_name:
- CloseEnum
- IALink.CloseEnum
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseEnum
helpviewer_keywords:
- CloseEnum method
ms.assetid: aa4a091e-13fe-4264-91de-e12f1c767c87
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 009f7d20dfd6efc279b3187af8f5c95132ae51e7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525233"
---
# <a name="closeenum-method"></a><span data-ttu-id="1e962-102">CloseEnum, méthode</span><span class="sxs-lookup"><span data-stu-id="1e962-102">CloseEnum Method</span></span>
<span data-ttu-id="1e962-103">Ferme l’énumération indiquée et libère les ressources associées.</span><span class="sxs-lookup"><span data-stu-id="1e962-103">Closes the indicated enumeration and frees associated resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e962-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e962-104">Syntax</span></span>  
  
```  
HRESULT CloseEnum(  
    HALINKENUM hEnum  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1e962-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e962-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="1e962-106">Handle d’énumération à fermer.</span><span class="sxs-lookup"><span data-stu-id="1e962-106">Handle of enumeration to be closed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1e962-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1e962-107">Return Value</span></span>  
 <span data-ttu-id="1e962-108">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="1e962-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1e962-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e962-109">Requirements</span></span>  
 <span data-ttu-id="1e962-110">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="1e962-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e962-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e962-111">See also</span></span>
- [<span data-ttu-id="1e962-112">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="1e962-112">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="1e962-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="1e962-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="1e962-114">API ALink</span><span class="sxs-lookup"><span data-stu-id="1e962-114">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
