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
ms.openlocfilehash: 7024140ed9b870b5db38dba7e9b13321dd37386a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62046161"
---
# <a name="cornativelink-structure"></a><span data-ttu-id="6e28b-102">COR_NATIVE_LINK, structure</span><span class="sxs-lookup"><span data-stu-id="6e28b-102">COR_NATIVE_LINK Structure</span></span>
<span data-ttu-id="6e28b-103">Contient des informations utilisées pour lier du code natif.</span><span class="sxs-lookup"><span data-stu-id="6e28b-103">Contains information that is used to link native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e28b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6e28b-104">Syntax</span></span>  
  
```  
typedef struct   
{  
    BYTE        m_linkType;  
    BYTE        m_flags;  
    mdMemberRef m_entryPoint;  
} COR_NATIVE_LINK;  
```  
  
## <a name="members"></a><span data-ttu-id="6e28b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="6e28b-105">Members</span></span>  
  
|<span data-ttu-id="6e28b-106">Membre</span><span class="sxs-lookup"><span data-stu-id="6e28b-106">Member</span></span>|<span data-ttu-id="6e28b-107">Description</span><span class="sxs-lookup"><span data-stu-id="6e28b-107">Description</span></span>|  
|------------|-----------------|  
|`m_linkType`|<span data-ttu-id="6e28b-108">Le type à lier en code natif.</span><span class="sxs-lookup"><span data-stu-id="6e28b-108">The type to be linked in native code.</span></span> <span data-ttu-id="6e28b-109">Cette valeur est un de la [CorNativeLinkType](../../../../docs/framework/unmanaged-api/metadata/cornativelinktype-enumeration.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="6e28b-109">This value is one of the [CorNativeLinkType](../../../../docs/framework/unmanaged-api/metadata/cornativelinktype-enumeration.md) values.</span></span>|  
|`m_flags`|<span data-ttu-id="6e28b-110">Indicateurs utilisés par l’éditeur de liens lors de la liaison du code natif.</span><span class="sxs-lookup"><span data-stu-id="6e28b-110">Flags used by the linker when linking native code.</span></span> <span data-ttu-id="6e28b-111">Cette valeur est un de la [CorNativeLinkFlags](../../../../docs/framework/unmanaged-api/metadata/cornativelinkflags-enumeration.md) valeurs.</span><span class="sxs-lookup"><span data-stu-id="6e28b-111">This value is one of the [CorNativeLinkFlags](../../../../docs/framework/unmanaged-api/metadata/cornativelinkflags-enumeration.md) values.</span></span>|  
|`m_entryPoint`|<span data-ttu-id="6e28b-112">Le jeton de métadonnées MemberRef qui représente le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6e28b-112">The MemberRef metadata token that represents the entry point.</span></span> <span data-ttu-id="6e28b-113">Le format est `lib:entrypoint`.</span><span class="sxs-lookup"><span data-stu-id="6e28b-113">The format is `lib:entrypoint`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6e28b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6e28b-114">Requirements</span></span>  
 <span data-ttu-id="6e28b-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6e28b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e28b-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="6e28b-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6e28b-117">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6e28b-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6e28b-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e28b-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e28b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e28b-119">See also</span></span>

- [<span data-ttu-id="6e28b-120">Structures de métadonnées</span><span class="sxs-lookup"><span data-stu-id="6e28b-120">Metadata Structures</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)
- [<span data-ttu-id="6e28b-121">CorNativeLinkType, énumération</span><span class="sxs-lookup"><span data-stu-id="6e28b-121">CorNativeLinkType Enumeration</span></span>](../../../../docs/framework/unmanaged-api/metadata/cornativelinktype-enumeration.md)
- [<span data-ttu-id="6e28b-122">CorNativeLinkFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="6e28b-122">CorNativeLinkFlags Enumeration</span></span>](../../../../docs/framework/unmanaged-api/metadata/cornativelinkflags-enumeration.md)
