---
title: IManagedObject::GetSerializedBuffer, méthode
ms.date: 03/30/2017
api_name:
- IManagedObject.GetSerializedBuffer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetSerializedBuffer
helpviewer_keywords:
- IManagedObject::GetSerializedBuffer method [.NET Framework hosting]
- GetSerializedBuffer method [.NET Framework hosting]
ms.assetid: c17105bb-b49f-434e-8f9b-77f8c85b9220
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a94891b91f6ac14469e18ed6840a083ce5e9d64d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54516914"
---
# <a name="imanagedobjectgetserializedbuffer-method"></a><span data-ttu-id="954b2-102">IManagedObject::GetSerializedBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="954b2-102">IManagedObject::GetSerializedBuffer Method</span></span>
<span data-ttu-id="954b2-103">Obtient la représentation sous forme de chaîne de cet objet managé.</span><span class="sxs-lookup"><span data-stu-id="954b2-103">Gets the string representation of this managed object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="954b2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="954b2-104">Syntax</span></span>  
  
```  
HRESULT GetSerializedBuffer (  
    [out] BSTR *pBSTR  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="954b2-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="954b2-105">Parameters</span></span>  
 `pBSTR`  
 <span data-ttu-id="954b2-106">[out] Un pointeur vers une chaîne qui est l’objet sérialisé.</span><span class="sxs-lookup"><span data-stu-id="954b2-106">[out] A pointer to a string that is the serialized object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="954b2-107">Notes</span><span class="sxs-lookup"><span data-stu-id="954b2-107">Remarks</span></span>  
 <span data-ttu-id="954b2-108">Le `GetSerializedBuffer` méthode sérialise l’objet afin qu’elle peut être marshalée au client.</span><span class="sxs-lookup"><span data-stu-id="954b2-108">The `GetSerializedBuffer` method serializes the object so it can be marshaled to the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="954b2-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="954b2-109">Requirements</span></span>  
 <span data-ttu-id="954b2-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="954b2-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="954b2-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="954b2-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="954b2-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="954b2-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="954b2-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="954b2-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="954b2-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="954b2-114">See also</span></span>
- [<span data-ttu-id="954b2-115">IManagedObject, interface</span><span class="sxs-lookup"><span data-stu-id="954b2-115">IManagedObject Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/imanagedobject-interface.md)
