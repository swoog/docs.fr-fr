---
title: DestroyICeeFileGen, fonction
ms.date: 03/30/2017
api_name:
- DestroyICeeFileGen
api_location:
- mscoree.dll
- mscorpehost.dll
- mscorpe.dll
api_type:
- COM
f1_keywords:
- DestroyICeeFileGen
helpviewer_keywords:
- DestroyICeeFileGen function [.NET Framework hosting]
ms.assetid: dc1e2235-e721-4cb2-a0b8-6b0c030d7bab
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 37ff40e1c009b8e1e0509a4a3333d5a2a70bbfd2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59159885"
---
# <a name="destroyiceefilegen-function"></a><span data-ttu-id="5452a-102">DestroyICeeFileGen, fonction</span><span class="sxs-lookup"><span data-stu-id="5452a-102">DestroyICeeFileGen Function</span></span>
<span data-ttu-id="5452a-103">Détruit un [ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md) objet.</span><span class="sxs-lookup"><span data-stu-id="5452a-103">Destroys an [ICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/iceefilegen-class.md) object.</span></span>  
  
 <span data-ttu-id="5452a-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="5452a-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5452a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5452a-105">Syntax</span></span>  
  
```  
HRESULT DestroyICeeFileGen (  
    [in] ICeeFileGen  **ceeFileGen  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5452a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5452a-106">Parameters</span></span>  
 `ceeFileGen`  
 <span data-ttu-id="5452a-107">[in] Le `ICeeFileGen` objet à détruire.</span><span class="sxs-lookup"><span data-stu-id="5452a-107">[in] The `ICeeFileGen` object to destroy.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5452a-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5452a-108">Return Value</span></span>  
 <span data-ttu-id="5452a-109">Cette méthode retourne des codes d’erreur COM standard.</span><span class="sxs-lookup"><span data-stu-id="5452a-109">This method returns standard COM error codes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5452a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5452a-110">Remarks</span></span>  
 `DestroyICeeFileGen` <span data-ttu-id="5452a-111">détruit le `ICeeFileGen` objet créé par le [CreateICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/createiceefilegen-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="5452a-111">destroys the `ICeeFileGen` object created by the [CreateICeeFileGen](../../../../docs/framework/unmanaged-api/hosting/createiceefilegen-function.md) function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5452a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5452a-112">Requirements</span></span>  
 <span data-ttu-id="5452a-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5452a-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5452a-114">**En-tête :** ICeeFileGen.h</span><span class="sxs-lookup"><span data-stu-id="5452a-114">**Header:** ICeeFileGen.h</span></span>  
  
 <span data-ttu-id="5452a-115">**Bibliothèque :** MSCorPE.dll</span><span class="sxs-lookup"><span data-stu-id="5452a-115">**Library:** MSCorPE.dll</span></span>  
  
 **<span data-ttu-id="5452a-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="5452a-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5452a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5452a-117">See also</span></span>

- [<span data-ttu-id="5452a-118">Fonction d'hébergement du CLR déconseillées</span><span class="sxs-lookup"><span data-stu-id="5452a-118">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
