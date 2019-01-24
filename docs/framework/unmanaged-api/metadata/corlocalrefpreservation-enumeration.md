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
ms.openlocfilehash: e9ed3cdac726fbdbf9ee2b33f42565d8594bc36e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54669677"
---
# <a name="corlocalrefpreservation-enumeration"></a><span data-ttu-id="735a9-102">CorLocalRefPreservation, énumération</span><span class="sxs-lookup"><span data-stu-id="735a9-102">CorLocalRefPreservation Enumeration</span></span>
<span data-ttu-id="735a9-103">Contient des valeurs d'indicateur pour le traitement des références locales.</span><span class="sxs-lookup"><span data-stu-id="735a9-103">Contains flag values for the treatment of local references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="735a9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="735a9-104">Syntax</span></span>  
  
```  
typedef enum CorLocalRefPreservation  
{  
    MDPreserveLocalRefsNone     =   0x00000000,  
    MDPreserveLocalTypeRef      =   0x00000001,  
    MDPreserveLocalMemberRef    =   0x00000002  
} CorLocalRefPreservation;  
```  
  
## <a name="members"></a><span data-ttu-id="735a9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="735a9-105">Members</span></span>  
  
|<span data-ttu-id="735a9-106">Membre</span><span class="sxs-lookup"><span data-stu-id="735a9-106">Member</span></span>|<span data-ttu-id="735a9-107">Description</span><span class="sxs-lookup"><span data-stu-id="735a9-107">Description</span></span>|  
|------------|-----------------|  
|`MDPreserveLocalRefsNone`|<span data-ttu-id="735a9-108">Ne conserver aucune référence locale.</span><span class="sxs-lookup"><span data-stu-id="735a9-108">Preserve no local references.</span></span>|  
|`MDPreserveLocalTypeRef`|<span data-ttu-id="735a9-109">Conserve les références de type local.</span><span class="sxs-lookup"><span data-stu-id="735a9-109">Preserve local type references.</span></span>|  
|`MDPreserveLocalMemberRef`|<span data-ttu-id="735a9-110">Conserve les références de membre locale.</span><span class="sxs-lookup"><span data-stu-id="735a9-110">Preserve local member references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="735a9-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="735a9-111">Requirements</span></span>  
 <span data-ttu-id="735a9-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="735a9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="735a9-113">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="735a9-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="735a9-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="735a9-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="735a9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="735a9-115">See also</span></span>
- [<span data-ttu-id="735a9-116">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="735a9-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
