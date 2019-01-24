---
title: CorErrorIfEmitOutOfOrder, énumération
ms.date: 03/30/2017
api_name:
- CorErrorIfEmitOutOfOrder
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorErrorIfEmitOutOfOrder
helpviewer_keywords:
- CorErrorIfEmitOutOfOrder enumeration [.NET Framework metadata]
ms.assetid: 6d758aad-29a7-44fe-9481-bbff5b799a32
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 084f0bbab130cd4e7334184fe9baa322c0487942
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616769"
---
# <a name="corerrorifemitoutoforder-enumeration"></a><span data-ttu-id="1eabe-102">CorErrorIfEmitOutOfOrder, énumération</span><span class="sxs-lookup"><span data-stu-id="1eabe-102">CorErrorIfEmitOutOfOrder Enumeration</span></span>
<span data-ttu-id="1eabe-103">Contient des valeurs d'indicateur qui précisent les conditions dans lesquelles un message d'erreur doit être généré quand les métadonnées sont émises de manière désordonnée.</span><span class="sxs-lookup"><span data-stu-id="1eabe-103">Contains flag values that indicate the conditions under which an error message should be generated when metadata is emitted out of order.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1eabe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1eabe-104">Syntax</span></span>  
  
```  
typedef enum CorErrorIfEmitOutOfOrder {  
  
    MDErrorOutOfOrderDefault    = 0x00000000,  
    MDErrorOutOfOrderNone       = 0x00000000,  
    MDErrorOutOfOrderAll        = 0xffffffff,  
    MDMethodOutOfOrder          = 0x00000001,  
    MDFieldOutOfOrder           = 0x00000002,  
    MDParamOutOfOrder           = 0x00000004,  
    MDPropertyOutOfOrder        = 0x00000008,  
    MDEventOutOfOrder           = 0x00000010  
  
} CorErrorIfEmitOutOfOrder;  
```  
  
## <a name="members"></a><span data-ttu-id="1eabe-105">Membres</span><span class="sxs-lookup"><span data-stu-id="1eabe-105">Members</span></span>  
  
|<span data-ttu-id="1eabe-106">Membre</span><span class="sxs-lookup"><span data-stu-id="1eabe-106">Member</span></span>|<span data-ttu-id="1eabe-107">Description</span><span class="sxs-lookup"><span data-stu-id="1eabe-107">Description</span></span>|  
|------------|-----------------|  
|`MDErrorOutOfOrderDefault`|<span data-ttu-id="1eabe-108">Indique le comportement par défaut, qui ne génère pas de messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1eabe-108">Indicates the default behavior, which does not generate error messages.</span></span>|  
|`MDErrorOutOfOrderNone`|<span data-ttu-id="1eabe-109">Indique que le compilateur ne doit pas générer des messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1eabe-109">Indicates that the compiler should not generate error messages.</span></span>|  
|`MDErrorOutOfOrderAll`|<span data-ttu-id="1eabe-110">Indique que le compilateur doit générer un message d’erreur lorsqu’un champ de propriété, événement, méthode ou paramètre est émis de manière désordonnée.</span><span class="sxs-lookup"><span data-stu-id="1eabe-110">Indicates that the compiler should generate an error message when a field, property, event, method, or parameter is emitted out of order.</span></span>|  
|`MDMethodOutOfOrder`|<span data-ttu-id="1eabe-111">Indique que le compilateur doit générer un message d’erreur lorsqu’une méthode est émise en désordre.</span><span class="sxs-lookup"><span data-stu-id="1eabe-111">Indicates that the compiler should generate an error message when a method is emitted out of order.</span></span>|  
|`MDFieldOutOfOrder`|<span data-ttu-id="1eabe-112">Indique que le compilateur doit générer un message d’erreur lorsqu’un champ est émis en désordre.</span><span class="sxs-lookup"><span data-stu-id="1eabe-112">Indicates that the compiler should generate an error message when a field is emitted out of order.</span></span>|  
|`MDParamOutOfOrder`|<span data-ttu-id="1eabe-113">Indique que le compilateur doit générer un message d’erreur lorsqu’un paramètre est émis de manière désordonnée.</span><span class="sxs-lookup"><span data-stu-id="1eabe-113">Indicates that the compiler should generate an error message when a parameter is emitted out of order.</span></span>|  
|`MDPropertyOutOfOrder`|<span data-ttu-id="1eabe-114">Indique que le compilateur doit générer un message d’erreur lorsqu’une propriété est émise en désordre.</span><span class="sxs-lookup"><span data-stu-id="1eabe-114">Indicates that the compiler should generate an error message when a property is emitted out of order.</span></span>|  
|`MDEventOutOfOrder`|<span data-ttu-id="1eabe-115">Indique que le compilateur doit générer un message d’erreur lorsqu’un événement est émis en désordre.</span><span class="sxs-lookup"><span data-stu-id="1eabe-115">Indicates that the compiler should generate an error message when an event is emitted out of order.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1eabe-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1eabe-116">Requirements</span></span>  
 <span data-ttu-id="1eabe-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1eabe-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1eabe-118">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="1eabe-118">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="1eabe-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1eabe-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1eabe-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1eabe-120">See also</span></span>
- [<span data-ttu-id="1eabe-121">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="1eabe-121">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
