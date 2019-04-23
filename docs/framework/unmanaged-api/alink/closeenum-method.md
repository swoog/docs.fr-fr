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
ms.openlocfilehash: fd7d63596690e2a5d0bc26448884ec09ecd63231
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59129517"
---
# <a name="closeenum-method"></a><span data-ttu-id="65250-102">CloseEnum, méthode</span><span class="sxs-lookup"><span data-stu-id="65250-102">CloseEnum Method</span></span>
<span data-ttu-id="65250-103">Ferme l’énumération indiquée et libère les ressources associées.</span><span class="sxs-lookup"><span data-stu-id="65250-103">Closes the indicated enumeration and frees associated resources.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65250-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65250-104">Syntax</span></span>  
  
```  
HRESULT CloseEnum(  
    HALINKENUM hEnum  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="65250-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65250-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="65250-106">Handle d’énumération à fermer.</span><span class="sxs-lookup"><span data-stu-id="65250-106">Handle of enumeration to be closed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="65250-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="65250-107">Return Value</span></span>  
 <span data-ttu-id="65250-108">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="65250-108">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65250-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65250-109">Requirements</span></span>  
 <span data-ttu-id="65250-110">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="65250-110">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65250-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65250-111">See also</span></span>

- [<span data-ttu-id="65250-112">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="65250-112">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="65250-113">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="65250-113">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="65250-114">API ALink</span><span class="sxs-lookup"><span data-stu-id="65250-114">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
