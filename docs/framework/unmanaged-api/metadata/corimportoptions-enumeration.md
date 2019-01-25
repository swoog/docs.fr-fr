---
title: CorImportOptions, énumération
ms.date: 03/30/2017
api_name:
- CorImportOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorImportOptions
helpviewer_keywords:
- CorImportOptions enumeration [.NET Framework metadata]
ms.assetid: 4e5d03cb-97c9-4ff4-8dbd-17d94ee374d3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8a4cc17bdcaea5099d0d2b0195ae4fa28e3d4744
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54744601"
---
# <a name="corimportoptions-enumeration"></a><span data-ttu-id="49a93-102">CorImportOptions, énumération</span><span class="sxs-lookup"><span data-stu-id="49a93-102">CorImportOptions Enumeration</span></span>
<span data-ttu-id="49a93-103">Contient des valeurs d'indicateur qui contrôlent le comportement lors de l'importation d'un assembly en dehors de la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="49a93-103">Contains flag values that control the behavior during importation of an assembly outside the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49a93-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49a93-104">Syntax</span></span>  
  
```  
typedef enum CorImportOptions {  
  
    MDImportOptionDefault                = 0x00000000,  
    MDImportOptionAll                    = 0xFFFFFFFF,  
    MDImportOptionAllTypeDefs            = 0x00000001,  
    MDImportOptionAllMethodDefs          = 0x00000002,  
    MDImportOptionAllFieldDefs           = 0x00000004,  
    MDImportOptionAllProperties          = 0x00000008,  
    MDImportOptionAllEvents              = 0x00000010,  
    MDImportOptionAllCustomAttributes    = 0x00000020,  
    MDImportOptionAllExportedTypes       = 0x00000040  
  
} CorImportOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="49a93-105">Membres</span><span class="sxs-lookup"><span data-stu-id="49a93-105">Members</span></span>  
  
|<span data-ttu-id="49a93-106">Membre</span><span class="sxs-lookup"><span data-stu-id="49a93-106">Member</span></span>|<span data-ttu-id="49a93-107">Description</span><span class="sxs-lookup"><span data-stu-id="49a93-107">Description</span></span>|  
|------------|-----------------|  
|`MDImportOptionDefault`|<span data-ttu-id="49a93-108">Indique le comportement par défaut, qui consiste à ignorer les enregistrements supprimés.</span><span class="sxs-lookup"><span data-stu-id="49a93-108">Indicates the default behavior, which is to skip deleted records.</span></span>|  
|`MDImportOptionAll`|<span data-ttu-id="49a93-109">Indique que toutes les métadonnées doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="49a93-109">Indicates that all metadata should be enumerated.</span></span>|  
|`MDImportOptionAllTypeDefs`|<span data-ttu-id="49a93-110">Indique que tous les TypeDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="49a93-110">Indicates that all TypeDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllMethodDefs`|<span data-ttu-id="49a93-111">Indique que tous les MethodDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="49a93-111">Indicates that all MethodDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllFieldDefs`|<span data-ttu-id="49a93-112">Indique que tous les FieldDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="49a93-112">Indicates that all FieldDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllProperties`|<span data-ttu-id="49a93-113">Indique que tous les PropertyDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="49a93-113">Indicates that all PropertyDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllEvents`|<span data-ttu-id="49a93-114">Indique que tous les EventDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="49a93-114">Indicates that all EventDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllCustomAttributes`|<span data-ttu-id="49a93-115">Indique que tous les attributs personnalisés, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="49a93-115">Indicates that all custom attributes, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllExportedTypes`|<span data-ttu-id="49a93-116">Indique que tous les types exportés, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="49a93-116">Indicates that all exported types, including deleted ones, should be enumerated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="49a93-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="49a93-117">Requirements</span></span>  
 <span data-ttu-id="49a93-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="49a93-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49a93-119">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="49a93-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="49a93-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49a93-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49a93-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49a93-121">See also</span></span>
- [<span data-ttu-id="49a93-122">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="49a93-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
