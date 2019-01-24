---
title: CorRegFlags, énumération
ms.date: 03/30/2017
api_name:
- CorRegFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRegFlags
helpviewer_keywords:
- CorRegFlags enumeration [.NET Framework metadata]
ms.assetid: 8d3080ee-39fe-4c57-8950-51323632d045
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 52b59a4e52d3e0cda7353ec1b39c5307bd7b218e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54532264"
---
# <a name="corregflags-enumeration"></a><span data-ttu-id="be1ed-102">CorRegFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="be1ed-102">CorRegFlags Enumeration</span></span>
<span data-ttu-id="be1ed-103">Fournit des valeurs d’indicateur utilisées pour l’inscription lors de l’installation d’un module ou une image composite.</span><span class="sxs-lookup"><span data-stu-id="be1ed-103">Provides flag values used for registration when installing a module or composite image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be1ed-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be1ed-104">Syntax</span></span>  
  
```  
typedef enum   
{  
    regNoCopy  = 0x00000001,  
    regConfig  = 0x00000002,  
    regHasRefs = 0x00000004  
} CorRegFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="be1ed-105">Membres</span><span class="sxs-lookup"><span data-stu-id="be1ed-105">Members</span></span>  
  
|<span data-ttu-id="be1ed-106">Membre</span><span class="sxs-lookup"><span data-stu-id="be1ed-106">Member</span></span>|<span data-ttu-id="be1ed-107">Description</span><span class="sxs-lookup"><span data-stu-id="be1ed-107">Description</span></span>|  
|------------|-----------------|  
|`regNoCopy`|<span data-ttu-id="be1ed-108">Spécifie que les fichiers ne doivent pas être copiées dans la destination.</span><span class="sxs-lookup"><span data-stu-id="be1ed-108">Specifies that files should not be copied into the destination.</span></span>|  
|`regConfig`|<span data-ttu-id="be1ed-109">Spécifie que le module ou composite est une configuration.</span><span class="sxs-lookup"><span data-stu-id="be1ed-109">Specifies that the module or composite is a configuration.</span></span>|  
|`regHasRefs`|<span data-ttu-id="be1ed-110">Spécifie que le module ou composite a des références de classe.</span><span class="sxs-lookup"><span data-stu-id="be1ed-110">Specifies that the module or composite has class references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="be1ed-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="be1ed-111">Requirements</span></span>  
 <span data-ttu-id="be1ed-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="be1ed-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be1ed-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="be1ed-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="be1ed-114">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="be1ed-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="be1ed-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be1ed-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be1ed-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be1ed-116">See also</span></span>
- [<span data-ttu-id="be1ed-117">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="be1ed-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
