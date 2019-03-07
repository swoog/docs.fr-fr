---
title: EnumCustomAttributes, méthode
ms.date: 03/30/2017
api_name:
- EnumCustomAttributes
- IALink.EnumCustomAttributes
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EnumCustomAttributes
helpviewer_keywords:
- EnumCustomAttributes method
ms.assetid: 08dff60c-f01b-4050-8865-ea3f95361c9f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e351c61f7e8bfc254a6fc8ea12c8a94fc393e3fc
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57478152"
---
# <a name="enumcustomattributes-method"></a><span data-ttu-id="66bb4-102">EnumCustomAttributes, méthode</span><span class="sxs-lookup"><span data-stu-id="66bb4-102">EnumCustomAttributes Method</span></span>
<span data-ttu-id="66bb4-103">Récupère les attributs personnalisés de niveau assembly.</span><span class="sxs-lookup"><span data-stu-id="66bb4-103">Retrieves assembly-level custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66bb4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="66bb4-104">Syntax</span></span>  
  
```  
HRESULT EnumCustomAttributes(  
    HALINKENUM hEnum,  
    mdToken tkType,  
    mdCustomAttribute rCustomValues[],  
    ULONG cMax,  
    ULONG* pcCustomValues  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="66bb4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66bb4-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="66bb4-106">Handle de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="66bb4-106">Handle of enumerator.</span></span>  
  
 `tkType`  
 <span data-ttu-id="66bb4-107">Type des attributs à énumérer.</span><span class="sxs-lookup"><span data-stu-id="66bb4-107">Type of attributes to be enumerated.</span></span> <span data-ttu-id="66bb4-108">Utilisez `mdTokenNill` pour tous les attributs.</span><span class="sxs-lookup"><span data-stu-id="66bb4-108">Use `mdTokenNill` for all attributes.</span></span>  
  
 `rCustomValues`  
 <span data-ttu-id="66bb4-109">Reçoit les jetons d’attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="66bb4-109">Receives custom attributes tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="66bb4-110">Spécifie la taille de `rCustomValues` tableau.</span><span class="sxs-lookup"><span data-stu-id="66bb4-110">Specifies size of `rCustomValues` array.</span></span>  
  
 `pcCustomValues`  
 <span data-ttu-id="66bb4-111">Si vous le souhaitez reçoit le nombre de valeurs de jeton.</span><span class="sxs-lookup"><span data-stu-id="66bb4-111">Optionally receives count of token values.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="66bb4-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="66bb4-112">Return Value</span></span>  
 <span data-ttu-id="66bb4-113">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="66bb4-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="66bb4-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="66bb4-114">Requirements</span></span>  
 <span data-ttu-id="66bb4-115">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="66bb4-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66bb4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66bb4-116">See also</span></span>
- [<span data-ttu-id="66bb4-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="66bb4-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="66bb4-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="66bb4-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="66bb4-119">API ALink</span><span class="sxs-lookup"><span data-stu-id="66bb4-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
