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
ms.openlocfilehash: 98a83a64a692955d5627e891e7fb3a3ef6f53476
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33442567"
---
# <a name="cornativelinkflags-enumeration"></a><span data-ttu-id="0ba31-102">CorNativeLinkFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="0ba31-102">CorNativeLinkFlags Enumeration</span></span>
<span data-ttu-id="0ba31-103">Fournit des valeurs d'indicateur utilisées par l'éditeur de liens lors de la liaison du code natif.</span><span class="sxs-lookup"><span data-stu-id="0ba31-103">Provides flag values used by the linker when linking native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ba31-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ba31-104">Syntax</span></span>  
  
```  
typedef enum  
{  
    nlfNone         = 0x00,  
    nlfLastError    = 0x01,  
    nlfNoMangle     = 0x02,  
    nlfMaxValue     = 0x03  
} CorNativeLinkFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="0ba31-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0ba31-105">Members</span></span>  
  
|<span data-ttu-id="0ba31-106">Membre</span><span class="sxs-lookup"><span data-stu-id="0ba31-106">Member</span></span>|<span data-ttu-id="0ba31-107">Description</span><span class="sxs-lookup"><span data-stu-id="0ba31-107">Description</span></span>|  
|------------|-----------------|  
|`nlfNone`|<span data-ttu-id="0ba31-108">Ne spécifie aucun indicateur.</span><span class="sxs-lookup"><span data-stu-id="0ba31-108">Indicates no flags.</span></span>|  
|`nlfLastError`|<span data-ttu-id="0ba31-109">Indique un `setLastError` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="0ba31-109">Indicates a `setLastError` keyword.</span></span>|  
|`nlfNoMangle`|<span data-ttu-id="0ba31-110">Indique un `nomangle` (mot clé).</span><span class="sxs-lookup"><span data-stu-id="0ba31-110">Indicates a `nomangle` keyword.</span></span>|  
|`nlfMaxValue`|<span data-ttu-id="0ba31-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="0ba31-111">Not used.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0ba31-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0ba31-112">Requirements</span></span>  
 <span data-ttu-id="0ba31-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0ba31-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ba31-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="0ba31-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="0ba31-115">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0ba31-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0ba31-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0ba31-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ba31-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ba31-117">See Also</span></span>  
 [<span data-ttu-id="0ba31-118">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="0ba31-118">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
