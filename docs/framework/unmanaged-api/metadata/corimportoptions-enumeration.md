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
ms.openlocfilehash: 7078b2eb98c15b7229132076da8af4691032bb08
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33441790"
---
# <a name="corimportoptions-enumeration"></a><span data-ttu-id="93682-102">CorImportOptions, énumération</span><span class="sxs-lookup"><span data-stu-id="93682-102">CorImportOptions Enumeration</span></span>
<span data-ttu-id="93682-103">Contient des valeurs d'indicateur qui contrôlent le comportement lors de l'importation d'un assembly en dehors de la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="93682-103">Contains flag values that control the behavior during importation of an assembly outside the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="93682-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="93682-104">Syntax</span></span>  
  
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
  
## <a name="members"></a><span data-ttu-id="93682-105">Membres</span><span class="sxs-lookup"><span data-stu-id="93682-105">Members</span></span>  
  
|<span data-ttu-id="93682-106">Membre</span><span class="sxs-lookup"><span data-stu-id="93682-106">Member</span></span>|<span data-ttu-id="93682-107">Description</span><span class="sxs-lookup"><span data-stu-id="93682-107">Description</span></span>|  
|------------|-----------------|  
|`MDImportOptionDefault`|<span data-ttu-id="93682-108">Indique le comportement par défaut, qui consiste à ignorer les enregistrements supprimés.</span><span class="sxs-lookup"><span data-stu-id="93682-108">Indicates the default behavior, which is to skip deleted records.</span></span>|  
|`MDImportOptionAll`|<span data-ttu-id="93682-109">Indique que toutes les métadonnées doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="93682-109">Indicates that all metadata should be enumerated.</span></span>|  
|`MDImportOptionAllTypeDefs`|<span data-ttu-id="93682-110">Indique que tous les TypeDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="93682-110">Indicates that all TypeDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllMethodDefs`|<span data-ttu-id="93682-111">Indique que tous les MethodDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="93682-111">Indicates that all MethodDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllFieldDefs`|<span data-ttu-id="93682-112">Indique que tous les FieldDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="93682-112">Indicates that all FieldDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllProperties`|<span data-ttu-id="93682-113">Indique que tous les PropertyDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="93682-113">Indicates that all PropertyDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllEvents`|<span data-ttu-id="93682-114">Indique que tous les EventDefs, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="93682-114">Indicates that all EventDefs, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllCustomAttributes`|<span data-ttu-id="93682-115">Indique que tous les attributs personnalisés, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="93682-115">Indicates that all custom attributes, including deleted ones, should be enumerated.</span></span>|  
|`MDImportOptionAllExportedTypes`|<span data-ttu-id="93682-116">Indique que tous les types exportés, y compris ceux qui sont supprimés, doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="93682-116">Indicates that all exported types, including deleted ones, should be enumerated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="93682-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="93682-117">Requirements</span></span>  
 <span data-ttu-id="93682-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="93682-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="93682-119">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="93682-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="93682-120">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="93682-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93682-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93682-121">See Also</span></span>  
 [<span data-ttu-id="93682-122">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="93682-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
