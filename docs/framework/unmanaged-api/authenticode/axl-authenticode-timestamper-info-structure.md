---
title: AXL_AUTHENTICODE_TIMESTAMPER_INFO, structure
ms.date: 03/30/2017
ms.assetid: 89e41a81-0f41-45ad-8f20-a120e4ff24fb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3d82ed3299f967457fe967d096a238da6143751a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61948918"
---
# <a name="axlauthenticodetimestamperinfo-structure"></a><span data-ttu-id="b8467-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO, structure</span><span class="sxs-lookup"><span data-stu-id="b8467-102">AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure</span></span>
<span data-ttu-id="b8467-103">Définit les informations de l'horodateur Authenticode.</span><span class="sxs-lookup"><span data-stu-id="b8467-103">Defines the Authenticode time stamper information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b8467-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8467-104">Syntax</span></span>  
  
```  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    FILETIME ftTimestamp  
    PCCERT_CHAIN_CONTEXT pChainContext;  
} AXL_AUTHENTICODE_TIMESTAMPER_INFO, * PAXL_AUTHENTICODE_TIMESTAMPER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="b8467-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b8467-105">Members</span></span>  
  
|<span data-ttu-id="b8467-106">Membre</span><span class="sxs-lookup"><span data-stu-id="b8467-106">Member</span></span>|<span data-ttu-id="b8467-107">Description</span><span class="sxs-lookup"><span data-stu-id="b8467-107">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="b8467-108">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="b8467-108">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="b8467-109">Le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b8467-109">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="b8467-110">L'algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="b8467-110">The hash algorithm.</span></span>|  
|`ftTimestamp`|<span data-ttu-id="b8467-111">La date/heure de l'horodatage.</span><span class="sxs-lookup"><span data-stu-id="b8467-111">The time of the time stamp.</span></span>|  
|`pChainContext`|<span data-ttu-id="b8467-112">La chaîne de contexte de l'horodateur.</span><span class="sxs-lookup"><span data-stu-id="b8467-112">The time stamper’s chain context.</span></span>  <span data-ttu-id="b8467-113">Consultez le [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span><span class="sxs-lookup"><span data-stu-id="b8467-113">See the [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b8467-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8467-114">See also</span></span>

- [<span data-ttu-id="b8467-115">Authenticode</span><span class="sxs-lookup"><span data-stu-id="b8467-115">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
