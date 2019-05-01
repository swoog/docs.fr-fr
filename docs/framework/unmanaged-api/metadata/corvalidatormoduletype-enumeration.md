---
title: CorValidatorModuleType, énumération
ms.date: 03/30/2017
api_name:
- CorValidatorModuleType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorValidatorModuleType
helpviewer_keywords:
- CorValidatorModuleType enumeration [.NET Framework metadata]
ms.assetid: 748f1ab2-fbcb-4f55-89ec-8d23d81ebc80
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 14eee096c25967d321e4693b260501827d944a80
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045173"
---
# <a name="corvalidatormoduletype-enumeration"></a><span data-ttu-id="f0e90-102">CorValidatorModuleType, énumération</span><span class="sxs-lookup"><span data-stu-id="f0e90-102">CorValidatorModuleType Enumeration</span></span>
<span data-ttu-id="f0e90-103">Spécifie le type d’un module.</span><span class="sxs-lookup"><span data-stu-id="f0e90-103">Specifies the type of a module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0e90-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0e90-104">Syntax</span></span>  
  
```  
typedef enum  
{  
    ValidatorModuleTypeInvalid  = 0x0,  
    ValidatorModuleTypeMin      = 0x00000001,  
    ValidatorModuleTypePE       = 0x00000001,  
    ValidatorModuleTypeObj      = 0x00000002,  
    ValidatorModuleTypeEnc      = 0x00000003,  
    ValidatorModuleTypeIncr     = 0x00000004,  
    ValidatorModuleTypeMax      = 0x00000004  
} CorValidatorModuleType;  
```  
  
## <a name="members"></a><span data-ttu-id="f0e90-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f0e90-105">Members</span></span>  
  
|<span data-ttu-id="f0e90-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f0e90-106">Member</span></span>|<span data-ttu-id="f0e90-107">Description</span><span class="sxs-lookup"><span data-stu-id="f0e90-107">Description</span></span>|  
|------------|-----------------|  
|`ValidatorModuleTypeInvalid`|<span data-ttu-id="f0e90-108">Le module est un type non valide.</span><span class="sxs-lookup"><span data-stu-id="f0e90-108">The module is an invalid type.</span></span>|  
|`ValidatorModuleTypeMin`|<span data-ttu-id="f0e90-109">La valeur minimale de la `CorValidatorModuleType` enum.</span><span class="sxs-lookup"><span data-stu-id="f0e90-109">The minimum value of the `CorValidatorModuleType` enum.</span></span>|  
|`ValidatorModuleTypePE`|<span data-ttu-id="f0e90-110">Le module est un fichier exécutable portable (PE).</span><span class="sxs-lookup"><span data-stu-id="f0e90-110">The module is a portable executable (PE) file.</span></span>|  
|`ValidatorModuleTypeObj`|<span data-ttu-id="f0e90-111">Le module est un fichier .obj.</span><span class="sxs-lookup"><span data-stu-id="f0e90-111">The module is a .obj file.</span></span>|  
|`ValidatorModuleTypeEnc`|<span data-ttu-id="f0e90-112">Le module est une session de débogueur modifier et continuer.</span><span class="sxs-lookup"><span data-stu-id="f0e90-112">The module is an edit-and-continue debugger session.</span></span>|  
|`ValidatorModuleTypeIncr`|<span data-ttu-id="f0e90-113">Le module est un qui a été générée de façon incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="f0e90-113">The module is one that has been incrementally built.</span></span>|  
|`ValidatorModuleTypeMax`|<span data-ttu-id="f0e90-114">La valeur maximale de la `CorValidatorModuleType` enum.</span><span class="sxs-lookup"><span data-stu-id="f0e90-114">The maximum value of the `CorValidatorModuleType` enum.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f0e90-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0e90-115">Requirements</span></span>  
 <span data-ttu-id="f0e90-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f0e90-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0e90-117">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f0e90-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f0e90-118">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f0e90-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f0e90-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0e90-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0e90-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0e90-120">See also</span></span>

- [<span data-ttu-id="f0e90-121">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="f0e90-121">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
