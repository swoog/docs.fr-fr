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
ms.openlocfilehash: ee1cfe52caa9d727a132d7adc23b03575293db65
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54716776"
---
# <a name="corvalidatormoduletype-enumeration"></a><span data-ttu-id="e4971-102">CorValidatorModuleType, énumération</span><span class="sxs-lookup"><span data-stu-id="e4971-102">CorValidatorModuleType Enumeration</span></span>
<span data-ttu-id="e4971-103">Spécifie le type d’un module.</span><span class="sxs-lookup"><span data-stu-id="e4971-103">Specifies the type of a module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4971-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4971-104">Syntax</span></span>  
  
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
  
## <a name="members"></a><span data-ttu-id="e4971-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e4971-105">Members</span></span>  
  
|<span data-ttu-id="e4971-106">Membre</span><span class="sxs-lookup"><span data-stu-id="e4971-106">Member</span></span>|<span data-ttu-id="e4971-107">Description</span><span class="sxs-lookup"><span data-stu-id="e4971-107">Description</span></span>|  
|------------|-----------------|  
|`ValidatorModuleTypeInvalid`|<span data-ttu-id="e4971-108">Le module est un type non valide.</span><span class="sxs-lookup"><span data-stu-id="e4971-108">The module is an invalid type.</span></span>|  
|`ValidatorModuleTypeMin`|<span data-ttu-id="e4971-109">La valeur minimale de la `CorValidatorModuleType` enum.</span><span class="sxs-lookup"><span data-stu-id="e4971-109">The minimum value of the `CorValidatorModuleType` enum.</span></span>|  
|`ValidatorModuleTypePE`|<span data-ttu-id="e4971-110">Le module est un fichier exécutable portable (PE).</span><span class="sxs-lookup"><span data-stu-id="e4971-110">The module is a portable executable (PE) file.</span></span>|  
|`ValidatorModuleTypeObj`|<span data-ttu-id="e4971-111">Le module est un fichier .obj.</span><span class="sxs-lookup"><span data-stu-id="e4971-111">The module is a .obj file.</span></span>|  
|`ValidatorModuleTypeEnc`|<span data-ttu-id="e4971-112">Le module est une session de débogueur modifier et continuer.</span><span class="sxs-lookup"><span data-stu-id="e4971-112">The module is an edit-and-continue debugger session.</span></span>|  
|`ValidatorModuleTypeIncr`|<span data-ttu-id="e4971-113">Le module est un qui a été générée de façon incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="e4971-113">The module is one that has been incrementally built.</span></span>|  
|`ValidatorModuleTypeMax`|<span data-ttu-id="e4971-114">La valeur maximale de la `CorValidatorModuleType` enum.</span><span class="sxs-lookup"><span data-stu-id="e4971-114">The maximum value of the `CorValidatorModuleType` enum.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e4971-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e4971-115">Requirements</span></span>  
 <span data-ttu-id="e4971-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e4971-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4971-117">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e4971-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e4971-118">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e4971-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e4971-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4971-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4971-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4971-120">See also</span></span>
- [<span data-ttu-id="e4971-121">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="e4971-121">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
