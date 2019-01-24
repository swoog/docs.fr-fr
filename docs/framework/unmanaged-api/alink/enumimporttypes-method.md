---
title: EnumImportTypes, méthode
ms.date: 03/30/2017
api_name:
- EnumImportTypes
- IALink.EnumImportTypes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EnumImportTypes
helpviewer_keywords:
- EnumImportTypes method
ms.assetid: 83a0e4e7-ec06-40cb-9b63-700b9695bb04
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4e437868138d7ae31d233853ecc0f709de3ee39d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54512721"
---
# <a name="enumimporttypes-method"></a><span data-ttu-id="ef457-102">EnumImportTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="ef457-102">EnumImportTypes Method</span></span>
<span data-ttu-id="ef457-103">Énumère chaque type dans chaque étendue.</span><span class="sxs-lookup"><span data-stu-id="ef457-103">Enumerates each type in each scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef457-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef457-104">Syntax</span></span>  
  
```  
HRESULT EnumImportTypes(  
    HALINKENUM   hEnum,  
    DWORD        dwMax,  
    mdTypeDef    aTypeDefs[],  
    DWORD*       pdwCount  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ef457-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef457-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="ef457-106">Handle pour l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="ef457-106">Handle for enumerator.</span></span>  
  
 `dwMax`  
 <span data-ttu-id="ef457-107">Nombre maximal de types à récupérer.</span><span class="sxs-lookup"><span data-stu-id="ef457-107">Maximum number of types to retrieve.</span></span>  
  
 `aTypeDefs`  
 <span data-ttu-id="ef457-108">Reçoit des jetons, ne pouvant excéder type `dwMax`.</span><span class="sxs-lookup"><span data-stu-id="ef457-108">Recieves type tokens, not to exceed `dwMax`.</span></span>  
  
 `pdwCount`  
 <span data-ttu-id="ef457-109">Reçoit le nombre réel de type dans `aTypeDefs`.</span><span class="sxs-lookup"><span data-stu-id="ef457-109">Receives actual number of type in `aTypeDefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ef457-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ef457-110">Return Value</span></span>  
 <span data-ttu-id="ef457-111">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="ef457-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ef457-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ef457-112">Requirements</span></span>  
 <span data-ttu-id="ef457-113">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="ef457-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef457-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef457-114">See also</span></span>
- [<span data-ttu-id="ef457-115">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="ef457-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="ef457-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="ef457-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="ef457-117">API ALink</span><span class="sxs-lookup"><span data-stu-id="ef457-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
