---
title: AXL_AUTHENTICODE_TIMESTAMPER_INFO, structure
ms.date: 03/30/2017
ms.assetid: 89e41a81-0f41-45ad-8f20-a120e4ff24fb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3d82ed3299f967457fe967d096a238da6143751a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59219159"
---
# <a name="axlauthenticodetimestamperinfo-structure"></a><span data-ttu-id="128a2-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO, structure</span><span class="sxs-lookup"><span data-stu-id="128a2-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure</span></span>
<span data-ttu-id="128a2-103">Définit les informations de l'horodateur Authenticode.</span><span class="sxs-lookup"><span data-stu-id="128a2-103">Defines the Authenticode time stamper information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="128a2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="128a2-104">Syntax</span></span>  
  
```  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    FILETIME ftTimestamp  
    PCCERT_CHAIN_CONTEXT pChainContext;  
} AXL_AUTHENTICODE_TIMESTAMPER_INFO, * PAXL_AUTHENTICODE_TIMESTAMPER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="128a2-105">Membres</span><span class="sxs-lookup"><span data-stu-id="128a2-105">Members</span></span>  
  
|<span data-ttu-id="128a2-106">Membre</span><span class="sxs-lookup"><span data-stu-id="128a2-106">Member</span></span>|<span data-ttu-id="128a2-107">Description</span><span class="sxs-lookup"><span data-stu-id="128a2-107">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="128a2-108">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="128a2-108">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="128a2-109">Le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="128a2-109">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="128a2-110">L'algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="128a2-110">The hash algorithm.</span></span>|  
|`ftTimestamp`|<span data-ttu-id="128a2-111">La date/heure de l'horodatage.</span><span class="sxs-lookup"><span data-stu-id="128a2-111">The time of the time stamp.</span></span>|  
|`pChainContext`|<span data-ttu-id="128a2-112">La chaîne de contexte de l'horodateur.</span><span class="sxs-lookup"><span data-stu-id="128a2-112">The time stamper’s chain context.</span></span>  <span data-ttu-id="128a2-113">Consultez le [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span><span class="sxs-lookup"><span data-stu-id="128a2-113">See the [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="128a2-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="128a2-114">See also</span></span>

- [<span data-ttu-id="128a2-115">Authenticode</span><span class="sxs-lookup"><span data-stu-id="128a2-115">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
