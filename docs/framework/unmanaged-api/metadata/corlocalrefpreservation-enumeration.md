---
title: CorLocalRefPreservation, énumération
ms.date: 03/30/2017
api_name:
- CorLocalRefPreservation
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorLocalRefPreservation
helpviewer_keywords:
- CorLocalRefPreservation enumeration [.NET Framework metadata]
ms.assetid: 44757163-1228-4213-a4c4-d4de503cc75d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 845994b96445d8ec2a0e37affc5164b432894a91
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59102191"
---
# <a name="corlocalrefpreservation-enumeration"></a><span data-ttu-id="601e5-102">CorLocalRefPreservation, énumération</span><span class="sxs-lookup"><span data-stu-id="601e5-102">CorLocalRefPreservation Enumeration</span></span>
<span data-ttu-id="601e5-103">Contient des valeurs d'indicateur pour le traitement des références locales.</span><span class="sxs-lookup"><span data-stu-id="601e5-103">Contains flag values for the treatment of local references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="601e5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="601e5-104">Syntax</span></span>  
  
```  
typedef enum CorLocalRefPreservation  
{  
    MDPreserveLocalRefsNone     =   0x00000000,  
    MDPreserveLocalTypeRef      =   0x00000001,  
    MDPreserveLocalMemberRef    =   0x00000002  
} CorLocalRefPreservation;  
```  
  
## <a name="members"></a><span data-ttu-id="601e5-105">Membres</span><span class="sxs-lookup"><span data-stu-id="601e5-105">Members</span></span>  
  
|<span data-ttu-id="601e5-106">Membre</span><span class="sxs-lookup"><span data-stu-id="601e5-106">Member</span></span>|<span data-ttu-id="601e5-107">Description</span><span class="sxs-lookup"><span data-stu-id="601e5-107">Description</span></span>|  
|------------|-----------------|  
|`MDPreserveLocalRefsNone`|<span data-ttu-id="601e5-108">Ne conserver aucune référence locale.</span><span class="sxs-lookup"><span data-stu-id="601e5-108">Preserve no local references.</span></span>|  
|`MDPreserveLocalTypeRef`|<span data-ttu-id="601e5-109">Conserve les références de type local.</span><span class="sxs-lookup"><span data-stu-id="601e5-109">Preserve local type references.</span></span>|  
|`MDPreserveLocalMemberRef`|<span data-ttu-id="601e5-110">Conserve les références de membre locale.</span><span class="sxs-lookup"><span data-stu-id="601e5-110">Preserve local member references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="601e5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="601e5-111">Requirements</span></span>  
 <span data-ttu-id="601e5-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="601e5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="601e5-113">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="601e5-113">**Header:** CorHdr.h</span></span>  
  
 **<span data-ttu-id="601e5-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="601e5-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="601e5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="601e5-115">See also</span></span>

- [<span data-ttu-id="601e5-116">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="601e5-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
