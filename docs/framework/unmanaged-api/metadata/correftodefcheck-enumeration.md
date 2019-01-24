---
title: CorRefToDefCheck, énumération
ms.date: 03/30/2017
api_name:
- CorRefToDefCheck
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRefToDefCheck
helpviewer_keywords:
- CorRefToDefCheck enumeration [.NET Framework metadata]
ms.assetid: f9a80f1a-55af-4459-b095-8441aae16119
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a54b20ecf34ecf1824420fcbb3d45fba64017b76
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54657192"
---
# <a name="correftodefcheck-enumeration"></a><span data-ttu-id="dd101-102">CorRefToDefCheck, énumération</span><span class="sxs-lookup"><span data-stu-id="dd101-102">CorRefToDefCheck Enumeration</span></span>
<span data-ttu-id="dd101-103">Spécifie des indicateurs pour contrôler les éléments référencés qui sont convertis en définitions afin d'optimiser le code.</span><span class="sxs-lookup"><span data-stu-id="dd101-103">Specifies flags to control which referenced items are converted to their definitions in order to optimize the code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd101-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd101-104">Syntax</span></span>  
  
```  
typedef enum CorRefToDefCheck {  
    MDRefToDefDefault           = 0x00000003,  
    MDRefToDefAll               = 0xffffffff,  
    MDRefToDefNone              = 0x00000000,  
    MDTypeRefToDef              = 0x00000001,  
    MDMemberRefToDef            = 0x00000002  
} CorRefToDefCheck;  
```  
  
## <a name="members"></a><span data-ttu-id="dd101-105">Membres</span><span class="sxs-lookup"><span data-stu-id="dd101-105">Members</span></span>  
  
|<span data-ttu-id="dd101-106">Membre</span><span class="sxs-lookup"><span data-stu-id="dd101-106">Member</span></span>|<span data-ttu-id="dd101-107">Description</span><span class="sxs-lookup"><span data-stu-id="dd101-107">Description</span></span>|  
|------------|-----------------|  
|`MDRefToDefDefault`|<span data-ttu-id="dd101-108">Spécifie que les références de type et membre doivent être convertis en définitions.</span><span class="sxs-lookup"><span data-stu-id="dd101-108">Specifies that type references and member references should be converted to definitions.</span></span> <span data-ttu-id="dd101-109">C’est la valeur par défaut (`MDTypeRefToDef` &#124; `MDMemberRefToDef`).</span><span class="sxs-lookup"><span data-stu-id="dd101-109">This is the default value (`MDTypeRefToDef` &#124; `MDMemberRefToDef`).</span></span>|  
|`MDRefToDefAll`|<span data-ttu-id="dd101-110">Spécifie que tous les éléments référencés doivent être convertis en définitions.</span><span class="sxs-lookup"><span data-stu-id="dd101-110">Specifies that all referenced items should be converted to definitions.</span></span>|  
|`MDRefToDefNone`|<span data-ttu-id="dd101-111">Spécifie qu’aucun élément référencé ne doit être convertie en définitions.</span><span class="sxs-lookup"><span data-stu-id="dd101-111">Specifies that no referenced items should be converted to definitions.</span></span>|  
|`MDTypeRefToDef`|<span data-ttu-id="dd101-112">Spécifie que seules les références de type doivent être convertis en définitions de type.</span><span class="sxs-lookup"><span data-stu-id="dd101-112">Specifies that only type references should be converted to type definitions.</span></span>|  
|`MDMemberRefToDef`|<span data-ttu-id="dd101-113">Spécifie que seules les références de membre doivent être convertis en définitions.</span><span class="sxs-lookup"><span data-stu-id="dd101-113">Specifies that only member references should be converted to definitions.</span></span> <span data-ttu-id="dd101-114">Autrement dit, les références de membre doivent être converties vers les définitions de méthode ou de définitions de champ.</span><span class="sxs-lookup"><span data-stu-id="dd101-114">That is, member references should be converted to either method definitions or field definitions.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="dd101-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dd101-115">Requirements</span></span>  
 <span data-ttu-id="dd101-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dd101-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd101-117">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="dd101-117">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="dd101-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dd101-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd101-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd101-119">See also</span></span>
- [<span data-ttu-id="dd101-120">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="dd101-120">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
