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
ms.openlocfilehash: 90319886dfe149a3d2d76451c1a8526299cf5b89
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401646"
---
# <a name="enumimporttypes-method"></a><span data-ttu-id="97344-102">EnumImportTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="97344-102">EnumImportTypes Method</span></span>
<span data-ttu-id="97344-103">Énumère chaque type dans chaque étendue.</span><span class="sxs-lookup"><span data-stu-id="97344-103">Enumerates each type in each scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97344-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97344-104">Syntax</span></span>  
  
```  
HRESULT EnumImportTypes(  
    HALINKENUM   hEnum,  
    DWORD        dwMax,  
    mdTypeDef    aTypeDefs[],  
    DWORD*       pdwCount  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="97344-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97344-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="97344-106">Handle pour l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="97344-106">Handle for enumerator.</span></span>  
  
 `dwMax`  
 <span data-ttu-id="97344-107">Nombre maximal de types à récupérer.</span><span class="sxs-lookup"><span data-stu-id="97344-107">Maximum number of types to retrieve.</span></span>  
  
 `aTypeDefs`  
 <span data-ttu-id="97344-108">Reçoit des jetons, dans la limite de type `dwMax`.</span><span class="sxs-lookup"><span data-stu-id="97344-108">Recieves type tokens, not to exceed `dwMax`.</span></span>  
  
 `pdwCount`  
 <span data-ttu-id="97344-109">Reçoit le nombre réel de type dans `aTypeDefs`.</span><span class="sxs-lookup"><span data-stu-id="97344-109">Receives actual number of type in `aTypeDefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="97344-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="97344-110">Return Value</span></span>  
 <span data-ttu-id="97344-111">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="97344-111">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="97344-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="97344-112">Requirements</span></span>  
 <span data-ttu-id="97344-113">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="97344-113">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97344-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97344-114">See Also</span></span>  
 [<span data-ttu-id="97344-115">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="97344-115">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="97344-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="97344-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="97344-117">API ALink</span><span class="sxs-lookup"><span data-stu-id="97344-117">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
