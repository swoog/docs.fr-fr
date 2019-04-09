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
ms.openlocfilehash: eb6b303fa7569712c854e8dc4e7513d8608e2519
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59104960"
---
# <a name="corregflags-enumeration"></a><span data-ttu-id="59980-102">CorRegFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="59980-102">CorRegFlags Enumeration</span></span>
<span data-ttu-id="59980-103">Fournit des valeurs d’indicateur utilisées pour l’inscription lors de l’installation d’un module ou une image composite.</span><span class="sxs-lookup"><span data-stu-id="59980-103">Provides flag values used for registration when installing a module or composite image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59980-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59980-104">Syntax</span></span>  
  
```  
typedef enum   
{  
    regNoCopy  = 0x00000001,  
    regConfig  = 0x00000002,  
    regHasRefs = 0x00000004  
} CorRegFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="59980-105">Membres</span><span class="sxs-lookup"><span data-stu-id="59980-105">Members</span></span>  
  
|<span data-ttu-id="59980-106">Membre</span><span class="sxs-lookup"><span data-stu-id="59980-106">Member</span></span>|<span data-ttu-id="59980-107">Description</span><span class="sxs-lookup"><span data-stu-id="59980-107">Description</span></span>|  
|------------|-----------------|  
|`regNoCopy`|<span data-ttu-id="59980-108">Spécifie que les fichiers ne doivent pas être copiées dans la destination.</span><span class="sxs-lookup"><span data-stu-id="59980-108">Specifies that files should not be copied into the destination.</span></span>|  
|`regConfig`|<span data-ttu-id="59980-109">Spécifie que le module ou composite est une configuration.</span><span class="sxs-lookup"><span data-stu-id="59980-109">Specifies that the module or composite is a configuration.</span></span>|  
|`regHasRefs`|<span data-ttu-id="59980-110">Spécifie que le module ou composite a des références de classe.</span><span class="sxs-lookup"><span data-stu-id="59980-110">Specifies that the module or composite has class references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="59980-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59980-111">Requirements</span></span>  
 <span data-ttu-id="59980-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="59980-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="59980-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="59980-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="59980-114">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="59980-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="59980-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="59980-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="59980-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59980-116">See also</span></span>

- [<span data-ttu-id="59980-117">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="59980-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
