---
title: CVStruct, structure
ms.date: 03/30/2017
api_name:
- CVStruct
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CVStruct
helpviewer_keywords:
- CVStruct structure [.NET Framework metadata]
ms.assetid: e9e4e497-d5fb-464b-991c-3bdd824664fd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 195f311d58f2169d715bb33986ee6e591622f377
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445041"
---
# <a name="cvstruct-structure"></a><span data-ttu-id="7f252-102">CVStruct, structure</span><span class="sxs-lookup"><span data-stu-id="7f252-102">CVStruct Structure</span></span>
<span data-ttu-id="7f252-103">Contient des informations utilisées lors de l'installation d'un module ou d'une image composite.</span><span class="sxs-lookup"><span data-stu-id="7f252-103">Contains information that is used when installing a module or a composite image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f252-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f252-104">Syntax</span></span>  
  
```  
typedef struct {  
    short Major;  
    short Minor;  
    short Sub;  
    short Build;  
} CVStruct;  
```  
  
## <a name="members"></a><span data-ttu-id="7f252-105">Membres</span><span class="sxs-lookup"><span data-stu-id="7f252-105">Members</span></span>  
  
|<span data-ttu-id="7f252-106">Membre</span><span class="sxs-lookup"><span data-stu-id="7f252-106">Member</span></span>|<span data-ttu-id="7f252-107">Description</span><span class="sxs-lookup"><span data-stu-id="7f252-107">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="7f252-108">Majeur</span><span class="sxs-lookup"><span data-stu-id="7f252-108">Major</span></span>|<span data-ttu-id="7f252-109">Numéro de version majeure.</span><span class="sxs-lookup"><span data-stu-id="7f252-109">Major version build number.</span></span>|  
|<span data-ttu-id="7f252-110">Mineur</span><span class="sxs-lookup"><span data-stu-id="7f252-110">Minor</span></span>|<span data-ttu-id="7f252-111">Numéro de version mineure.</span><span class="sxs-lookup"><span data-stu-id="7f252-111">Minor version build number.</span></span>|  
|<span data-ttu-id="7f252-112">Sub</span><span class="sxs-lookup"><span data-stu-id="7f252-112">Sub</span></span>|<span data-ttu-id="7f252-113">Numéro de version secondaire.</span><span class="sxs-lookup"><span data-stu-id="7f252-113">Sub-build number.</span></span>|  
|<span data-ttu-id="7f252-114">Générer</span><span class="sxs-lookup"><span data-stu-id="7f252-114">Build</span></span>|<span data-ttu-id="7f252-115">Numéro de build.</span><span class="sxs-lookup"><span data-stu-id="7f252-115">Build number.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7f252-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7f252-116">Requirements</span></span>  
 <span data-ttu-id="7f252-117">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7f252-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f252-118">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="7f252-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7f252-119">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7f252-119">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7f252-120">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f252-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f252-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f252-121">See Also</span></span>  
 [<span data-ttu-id="7f252-122">Structures de métadonnées</span><span class="sxs-lookup"><span data-stu-id="7f252-122">Metadata Structures</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)
