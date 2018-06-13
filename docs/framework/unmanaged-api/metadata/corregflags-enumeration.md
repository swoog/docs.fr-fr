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
ms.openlocfilehash: f7b935b8f59e434c9da364be1986dbed654a1efd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445807"
---
# <a name="corregflags-enumeration"></a><span data-ttu-id="ae579-102">CorRegFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="ae579-102">CorRegFlags Enumeration</span></span>
<span data-ttu-id="ae579-103">Fournit des valeurs d’indicateur utilisées pour l’inscription lors de l’installation d’un module ou une image composite.</span><span class="sxs-lookup"><span data-stu-id="ae579-103">Provides flag values used for registration when installing a module or composite image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae579-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae579-104">Syntax</span></span>  
  
```  
typedef enum   
{  
    regNoCopy  = 0x00000001,  
    regConfig  = 0x00000002,  
    regHasRefs = 0x00000004  
} CorRegFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="ae579-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ae579-105">Members</span></span>  
  
|<span data-ttu-id="ae579-106">Membre</span><span class="sxs-lookup"><span data-stu-id="ae579-106">Member</span></span>|<span data-ttu-id="ae579-107">Description</span><span class="sxs-lookup"><span data-stu-id="ae579-107">Description</span></span>|  
|------------|-----------------|  
|`regNoCopy`|<span data-ttu-id="ae579-108">Spécifie que les fichiers ne doivent pas être copiées dans la destination.</span><span class="sxs-lookup"><span data-stu-id="ae579-108">Specifies that files should not be copied into the destination.</span></span>|  
|`regConfig`|<span data-ttu-id="ae579-109">Spécifie que le module ou composite est une configuration.</span><span class="sxs-lookup"><span data-stu-id="ae579-109">Specifies that the module or composite is a configuration.</span></span>|  
|`regHasRefs`|<span data-ttu-id="ae579-110">Spécifie que le module ou composite a des références de classe.</span><span class="sxs-lookup"><span data-stu-id="ae579-110">Specifies that the module or composite has class references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ae579-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae579-111">Requirements</span></span>  
 <span data-ttu-id="ae579-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ae579-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae579-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ae579-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ae579-114">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ae579-114">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ae579-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae579-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae579-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae579-116">See Also</span></span>  
 [<span data-ttu-id="ae579-117">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="ae579-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
