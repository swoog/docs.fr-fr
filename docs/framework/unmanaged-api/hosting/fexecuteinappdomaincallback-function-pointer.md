---
title: FExecuteInAppDomainCallback (pointeur fonction)
ms.date: 03/30/2017
api_name:
- FExecuteInAppDomainCallback
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- FExecuteInAppDomainCallback
helpviewer_keywords:
- FExecuteInAppDomainCallback function pointer [.NET Framework hosting]
ms.assetid: 2709f18f-3eee-497f-bc33-3ab7a485599b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9981e97e3be58f6646612dc5c3a50a9e7650e376
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108444"
---
# <a name="fexecuteinappdomaincallback-function-pointer"></a><span data-ttu-id="aabf0-102">FExecuteInAppDomainCallback (pointeur fonction)</span><span class="sxs-lookup"><span data-stu-id="aabf0-102">FExecuteInAppDomainCallback Function Pointer</span></span>
<span data-ttu-id="aabf0-103">Pointe vers une fonction qui est appelée par le common language runtime (CLR) pour exécuter le code managé.</span><span class="sxs-lookup"><span data-stu-id="aabf0-103">Points to a function that is called by the common language runtime (CLR) to execute managed code.</span></span>  
  
 <span data-ttu-id="aabf0-104">Ce pointeur de fonction a été déconseillé dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="aabf0-104">This function pointer has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aabf0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aabf0-105">Syntax</span></span>  
  
```  
typedef HRESULT (__stdcall *FExecuteInAppDomainCallback) (  
    [in] void  *cookie  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aabf0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aabf0-106">Parameters</span></span>  
 `cookie`  
 <span data-ttu-id="aabf0-107">[in] Un pointeur vers la mémoire allouée par l’appelant opaque qui contient le code managé doit être exécuté.</span><span class="sxs-lookup"><span data-stu-id="aabf0-107">[in] A pointer to opaque caller-allocated memory that contains the managed code to be executed.</span></span>  
  
 <span data-ttu-id="aabf0-108">L’allocation et la durée de vie de cette mémoire sont contrôlées par l’appelant (autrement dit, le CLR).</span><span class="sxs-lookup"><span data-stu-id="aabf0-108">The allocation and lifetime of this memory are controlled by the caller (that is, the CLR).</span></span> <span data-ttu-id="aabf0-109">Cela n’est pas mémoire de tas managé CLR.</span><span class="sxs-lookup"><span data-stu-id="aabf0-109">This is not CLR managed-heap memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aabf0-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aabf0-110">Requirements</span></span>  
 <span data-ttu-id="aabf0-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aabf0-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aabf0-112">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="aabf0-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="aabf0-113">**Bibliothèque :** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="aabf0-113">**Library:** MSCorWks.dll</span></span>  
  
 **<span data-ttu-id="aabf0-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="aabf0-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="aabf0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aabf0-115">See also</span></span>

- [<span data-ttu-id="aabf0-116">Fonction d'hébergement du CLR déconseillées</span><span class="sxs-lookup"><span data-stu-id="aabf0-116">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
