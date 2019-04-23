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
ms.openlocfilehash: b419962982fc80591ed565cceb28afb88a39495e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59199139"
---
# <a name="enumcustomattributes-method"></a><span data-ttu-id="8b540-102">EnumCustomAttributes, méthode</span><span class="sxs-lookup"><span data-stu-id="8b540-102">EnumCustomAttributes Method</span></span>
<span data-ttu-id="8b540-103">Récupère les attributs personnalisés de niveau assembly.</span><span class="sxs-lookup"><span data-stu-id="8b540-103">Retrieves assembly-level custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b540-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b540-104">Syntax</span></span>  
  
```  
HRESULT EnumCustomAttributes(  
    HALINKENUM hEnum,  
    mdToken tkType,  
    mdCustomAttribute rCustomValues[],  
    ULONG cMax,  
    ULONG* pcCustomValues  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="8b540-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b540-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="8b540-106">Handle de l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="8b540-106">Handle of enumerator.</span></span>  
  
 `tkType`  
 <span data-ttu-id="8b540-107">Type des attributs à énumérer.</span><span class="sxs-lookup"><span data-stu-id="8b540-107">Type of attributes to be enumerated.</span></span> <span data-ttu-id="8b540-108">Utilisez `mdTokenNill` pour tous les attributs.</span><span class="sxs-lookup"><span data-stu-id="8b540-108">Use `mdTokenNill` for all attributes.</span></span>  
  
 `rCustomValues`  
 <span data-ttu-id="8b540-109">Reçoit les jetons d’attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="8b540-109">Receives custom attributes tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="8b540-110">Spécifie la taille de `rCustomValues` tableau.</span><span class="sxs-lookup"><span data-stu-id="8b540-110">Specifies size of `rCustomValues` array.</span></span>  
  
 `pcCustomValues`  
 <span data-ttu-id="8b540-111">Si vous le souhaitez reçoit le nombre de valeurs de jeton.</span><span class="sxs-lookup"><span data-stu-id="8b540-111">Optionally receives count of token values.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8b540-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8b540-112">Return Value</span></span>  
 <span data-ttu-id="8b540-113">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="8b540-113">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8b540-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b540-114">Requirements</span></span>  
 <span data-ttu-id="8b540-115">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="8b540-115">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b540-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b540-116">See also</span></span>

- [<span data-ttu-id="8b540-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="8b540-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="8b540-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="8b540-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="8b540-119">API ALink</span><span class="sxs-lookup"><span data-stu-id="8b540-119">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
