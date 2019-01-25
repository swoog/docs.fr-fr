---
title: CorNativeLinkFlags, énumération
ms.date: 03/30/2017
api_name:
- CorNativeLinkFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNativeLinkFlags
helpviewer_keywords:
- CorNativeLinkFlags enumeration [.NET Framework metadata]
ms.assetid: 8027df7c-cfad-4724-bda0-7538d9519070
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cf0fdb1e46bfbd17505e255d539547a00eb4764c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54694553"
---
# <a name="cornativelinkflags-enumeration"></a><span data-ttu-id="9e4df-102">CorNativeLinkFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="9e4df-102">CorNativeLinkFlags Enumeration</span></span>
<span data-ttu-id="9e4df-103">Fournit des valeurs d'indicateur utilisées par l'éditeur de liens lors de la liaison du code natif.</span><span class="sxs-lookup"><span data-stu-id="9e4df-103">Provides flag values used by the linker when linking native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9e4df-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e4df-104">Syntax</span></span>  
  
```  
typedef enum  
{  
    nlfNone         = 0x00,  
    nlfLastError    = 0x01,  
    nlfNoMangle     = 0x02,  
    nlfMaxValue     = 0x03  
} CorNativeLinkFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="9e4df-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9e4df-105">Members</span></span>  
  
|<span data-ttu-id="9e4df-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9e4df-106">Member</span></span>|<span data-ttu-id="9e4df-107">Description</span><span class="sxs-lookup"><span data-stu-id="9e4df-107">Description</span></span>|  
|------------|-----------------|  
|`nlfNone`|<span data-ttu-id="9e4df-108">Ne spécifie aucun indicateur.</span><span class="sxs-lookup"><span data-stu-id="9e4df-108">Indicates no flags.</span></span>|  
|`nlfLastError`|<span data-ttu-id="9e4df-109">Indique un `setLastError` mot clé.</span><span class="sxs-lookup"><span data-stu-id="9e4df-109">Indicates a `setLastError` keyword.</span></span>|  
|`nlfNoMangle`|<span data-ttu-id="9e4df-110">Indique un `nomangle` mot clé.</span><span class="sxs-lookup"><span data-stu-id="9e4df-110">Indicates a `nomangle` keyword.</span></span>|  
|`nlfMaxValue`|<span data-ttu-id="9e4df-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="9e4df-111">Not used.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9e4df-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9e4df-112">Requirements</span></span>  
 <span data-ttu-id="9e4df-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9e4df-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9e4df-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9e4df-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9e4df-115">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9e4df-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9e4df-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9e4df-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9e4df-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e4df-117">See also</span></span>
- [<span data-ttu-id="9e4df-118">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9e4df-118">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
