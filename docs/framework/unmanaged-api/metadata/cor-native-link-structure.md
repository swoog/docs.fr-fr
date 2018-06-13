---
title: COR_NATIVE_LINK, structure
ms.date: 03/30/2017
api_name:
- COR_NATIVE_LINK
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_NATIVE_LINK
helpviewer_keywords:
- COR_NATIVE_LINK structure [.NET Framework metadata]
ms.assetid: 6ef78d3c-1c69-4141-b687-dcb065b7a74d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d0d9b8a9a1014d98c51f1471f8203be07f7ff49c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33440955"
---
# <a name="cornativelink-structure"></a><span data-ttu-id="1ffc1-102">COR_NATIVE_LINK, structure</span><span class="sxs-lookup"><span data-stu-id="1ffc1-102">COR_NATIVE_LINK Structure</span></span>
<span data-ttu-id="1ffc1-103">Contient des informations utilisées pour lier du code natif.</span><span class="sxs-lookup"><span data-stu-id="1ffc1-103">Contains information that is used to link native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ffc1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ffc1-104">Syntax</span></span>  
  
```  
typedef struct   
{  
    BYTE        m_linkType;  
    BYTE        m_flags;  
    mdMemberRef m_entryPoint;  
} COR_NATIVE_LINK;  
```  
  
## <a name="members"></a><span data-ttu-id="1ffc1-105">Membres</span><span class="sxs-lookup"><span data-stu-id="1ffc1-105">Members</span></span>  
  
|<span data-ttu-id="1ffc1-106">Membre</span><span class="sxs-lookup"><span data-stu-id="1ffc1-106">Member</span></span>|<span data-ttu-id="1ffc1-107">Description</span><span class="sxs-lookup"><span data-stu-id="1ffc1-107">Description</span></span>|  
|------------|-----------------|  
|`m_linkType`|<span data-ttu-id="1ffc1-108">Type à être lié en code natif.</span><span class="sxs-lookup"><span data-stu-id="1ffc1-108">The type to be linked in native code.</span></span> <span data-ttu-id="1ffc1-109">Cette valeur est un de le [CorNativeLinkType](../../../../docs/framework/unmanaged-api/metadata/cornativelinktype-enumeration.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="1ffc1-109">This value is one of the [CorNativeLinkType](../../../../docs/framework/unmanaged-api/metadata/cornativelinktype-enumeration.md) values.</span></span>|  
|`m_flags`|<span data-ttu-id="1ffc1-110">Indicateurs utilisés par l’éditeur de liens lors de la liaison du code natif.</span><span class="sxs-lookup"><span data-stu-id="1ffc1-110">Flags used by the linker when linking native code.</span></span> <span data-ttu-id="1ffc1-111">Cette valeur est un de le [CorNativeLinkFlags](../../../../docs/framework/unmanaged-api/metadata/cornativelinkflags-enumeration.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="1ffc1-111">This value is one of the [CorNativeLinkFlags](../../../../docs/framework/unmanaged-api/metadata/cornativelinkflags-enumeration.md) values.</span></span>|  
|`m_entryPoint`|<span data-ttu-id="1ffc1-112">Le jeton de métadonnées MemberRef qui représente le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="1ffc1-112">The MemberRef metadata token that represents the entry point.</span></span> <span data-ttu-id="1ffc1-113">Le format est `lib:entrypoint`.</span><span class="sxs-lookup"><span data-stu-id="1ffc1-113">The format is `lib:entrypoint`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1ffc1-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1ffc1-114">Requirements</span></span>  
 <span data-ttu-id="1ffc1-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1ffc1-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ffc1-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="1ffc1-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1ffc1-117">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1ffc1-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="1ffc1-118">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1ffc1-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ffc1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ffc1-119">See Also</span></span>  
 [<span data-ttu-id="1ffc1-120">Structures de métadonnées</span><span class="sxs-lookup"><span data-stu-id="1ffc1-120">Metadata Structures</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)  
 [<span data-ttu-id="1ffc1-121">CorNativeLinkType, énumération</span><span class="sxs-lookup"><span data-stu-id="1ffc1-121">CorNativeLinkType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/metadata/cornativelinktype-enumeration.md)  
 [<span data-ttu-id="1ffc1-122">CorNativeLinkFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="1ffc1-122">CorNativeLinkFlags Enumeration</span></span>](../../../../docs/framework/unmanaged-api/metadata/cornativelinkflags-enumeration.md)
