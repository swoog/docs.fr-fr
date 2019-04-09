---
title: CreateApplicationContext, fonction
ms.date: 03/30/2017
api_name:
- CreateApplicationContext
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- CreateApplicationContext
helpviewer_keywords:
- CreateApplicationContext function [.NET Framework fusion]
ms.assetid: 7bf8a141-b2c0-4058-9885-1cef7dcaa811
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d98829b29100824e5d606e23aaf287c9f6e81d69
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59170961"
---
# <a name="createapplicationcontext-function"></a><span data-ttu-id="77dec-102">CreateApplicationContext, fonction</span><span class="sxs-lookup"><span data-stu-id="77dec-102">CreateApplicationContext Function</span></span>
<span data-ttu-id="77dec-103">Cette fonction prend en charge l’infrastructure .NET Framework et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="77dec-103">This function supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="77dec-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77dec-104">Syntax</span></span>  
  
```  
HRESULT CreateApplicationContext (  
    [in]  IAssemblyName  *pName,  
    [out] LPPAPPLICATIONCONTEXT  *ppCtx  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="77dec-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77dec-105">Parameters</span></span>  
 `pName`  
 <span data-ttu-id="77dec-106">[in] Pointeur vers un nom convivial.</span><span class="sxs-lookup"><span data-stu-id="77dec-106">[in] A pointer to a friendly name.</span></span>  
  
 `ppCtx`  
 <span data-ttu-id="77dec-107">[out] Pointeur vers un contexte d’application.</span><span class="sxs-lookup"><span data-stu-id="77dec-107">[out] A pointer to an application context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="77dec-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77dec-108">Requirements</span></span>  
 <span data-ttu-id="77dec-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="77dec-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="77dec-110">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="77dec-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="77dec-111">**Bibliothèque :** Inclus en tant que ressource dans le fichier Fusion.dll</span><span class="sxs-lookup"><span data-stu-id="77dec-111">**Library:** Included as a resource in Fusion.dll</span></span>  
  
 **<span data-ttu-id="77dec-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="77dec-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="77dec-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77dec-113">See also</span></span>

- [<span data-ttu-id="77dec-114">IAssemblyCache, interface</span><span class="sxs-lookup"><span data-stu-id="77dec-114">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
- [<span data-ttu-id="77dec-115">Fonctions statiques globales de la fusion</span><span class="sxs-lookup"><span data-stu-id="77dec-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
- [<span data-ttu-id="77dec-116">Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="77dec-116">Global Assembly Cache</span></span>](../../../../docs/framework/app-domains/gac.md)
