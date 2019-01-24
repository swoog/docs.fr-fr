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
ms.openlocfilehash: fb73980faa64464c572945fe5ad04e015dc8805b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54720650"
---
# <a name="cvstruct-structure"></a><span data-ttu-id="ce03a-102">CVStruct, structure</span><span class="sxs-lookup"><span data-stu-id="ce03a-102">CVStruct Structure</span></span>
<span data-ttu-id="ce03a-103">Contient des informations utilisées lors de l'installation d'un module ou d'une image composite.</span><span class="sxs-lookup"><span data-stu-id="ce03a-103">Contains information that is used when installing a module or a composite image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce03a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce03a-104">Syntax</span></span>  
  
```  
typedef struct {  
    short Major;  
    short Minor;  
    short Sub;  
    short Build;  
} CVStruct;  
```  
  
## <a name="members"></a><span data-ttu-id="ce03a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ce03a-105">Members</span></span>  
  
|<span data-ttu-id="ce03a-106">Membre</span><span class="sxs-lookup"><span data-stu-id="ce03a-106">Member</span></span>|<span data-ttu-id="ce03a-107">Description</span><span class="sxs-lookup"><span data-stu-id="ce03a-107">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="ce03a-108">Majeur</span><span class="sxs-lookup"><span data-stu-id="ce03a-108">Major</span></span>|<span data-ttu-id="ce03a-109">Numéro de build de version principale.</span><span class="sxs-lookup"><span data-stu-id="ce03a-109">Major version build number.</span></span>|  
|<span data-ttu-id="ce03a-110">Mineur</span><span class="sxs-lookup"><span data-stu-id="ce03a-110">Minor</span></span>|<span data-ttu-id="ce03a-111">Numéro de build de version mineure.</span><span class="sxs-lookup"><span data-stu-id="ce03a-111">Minor version build number.</span></span>|  
|<span data-ttu-id="ce03a-112">Sub</span><span class="sxs-lookup"><span data-stu-id="ce03a-112">Sub</span></span>|<span data-ttu-id="ce03a-113">Numéro de version secondaire.</span><span class="sxs-lookup"><span data-stu-id="ce03a-113">Sub-build number.</span></span>|  
|<span data-ttu-id="ce03a-114">Build</span><span class="sxs-lookup"><span data-stu-id="ce03a-114">Build</span></span>|<span data-ttu-id="ce03a-115">numéro de build.</span><span class="sxs-lookup"><span data-stu-id="ce03a-115">Build number.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ce03a-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce03a-116">Requirements</span></span>  
 <span data-ttu-id="ce03a-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ce03a-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce03a-118">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ce03a-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ce03a-119">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ce03a-119">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ce03a-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce03a-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce03a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce03a-121">See also</span></span>
- [<span data-ttu-id="ce03a-122">Structures de métadonnées</span><span class="sxs-lookup"><span data-stu-id="ce03a-122">Metadata Structures</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)
