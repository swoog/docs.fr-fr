---
title: AXL_AUTHENTICODE_SIGNER_INFO, structure
ms.date: 03/30/2017
ms.assetid: 81c0f8b4-ce35-4716-8651-b642d40648a2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4b9f54c7c57d122ac1214b9f31cc4e1d1cddd71c
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44184323"
---
# <a name="axlauthenticodesignerinfo-structure"></a><span data-ttu-id="3c9fa-102">AXL_AUTHENTICODE_SIGNER_INFO, structure</span><span class="sxs-lookup"><span data-stu-id="3c9fa-102">AXL_AUTHENTICODE_SIGNER_INFO Structure</span></span>
<span data-ttu-id="3c9fa-103">Définit les informations du signataire Authenticode.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-103">Defines the Authenticode signer information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c9fa-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c9fa-104">Syntax</span></span>  
  
```  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    LPCWSTR pwszHash  
    LPCWSTR pwszDescription;  
    LPCWSTR pwszDescriptionUrl;  
    PCCERT_CHAIN_CONTEXT pChainContext  
} AXL_AUTHENTICODE_SIGNER_INFO, * PAXL_AUTHENTICODE_SIGNER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="3c9fa-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3c9fa-105">Members</span></span>  
  
|<span data-ttu-id="3c9fa-106">Membre</span><span class="sxs-lookup"><span data-stu-id="3c9fa-106">Member</span></span>|<span data-ttu-id="3c9fa-107">Description</span><span class="sxs-lookup"><span data-stu-id="3c9fa-107">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="3c9fa-108">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-108">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="3c9fa-109">Le code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-109">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="3c9fa-110">L'algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-110">The hash algorithm.</span></span>|  
|`pwszHash`|<span data-ttu-id="3c9fa-111">Le hachage.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-111">The hash.</span></span>|  
|`pwszDescription`|<span data-ttu-id="3c9fa-112">La description.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-112">The description.</span></span>|  
|`pwszDescriptionUrl`|<span data-ttu-id="3c9fa-113">L'URL de la description.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-113">The URL of the description.</span></span>|  
|`pChainContext`|<span data-ttu-id="3c9fa-114">Le contexte de chaîne du signataire.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-114">The chain context of the signer.</span></span> <span data-ttu-id="3c9fa-115">Consultez le [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span><span class="sxs-lookup"><span data-stu-id="3c9fa-115">See the [CERT_CONTEXT](/windows/desktop/api/wincrypt/ns-wincrypt-_cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3c9fa-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c9fa-116">See Also</span></span>  
 [<span data-ttu-id="3c9fa-117">Authenticode</span><span class="sxs-lookup"><span data-stu-id="3c9fa-117">Authenticode</span></span>](../../../../docs/framework/unmanaged-api/authenticode/index.md)
