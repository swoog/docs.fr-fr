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
ms.openlocfilehash: 80012d030d0ea51ab3d150a7fd346b78e29dbde5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430098"
---
# <a name="createapplicationcontext-function"></a><span data-ttu-id="2fc89-102">CreateApplicationContext, fonction</span><span class="sxs-lookup"><span data-stu-id="2fc89-102">CreateApplicationContext Function</span></span>
<span data-ttu-id="2fc89-103">Cette fonction prend en charge l’infrastructure .NET Framework et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="2fc89-103">This function supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2fc89-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fc89-104">Syntax</span></span>  
  
```  
HRESULT CreateApplicationContext (  
    [in]  IAssemblyName  *pName,  
    [out] LPPAPPLICATIONCONTEXT  *ppCtx  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2fc89-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fc89-105">Parameters</span></span>  
 `pName`  
 <span data-ttu-id="2fc89-106">[in] Pointeur vers un nom convivial.</span><span class="sxs-lookup"><span data-stu-id="2fc89-106">[in] A pointer to a friendly name.</span></span>  
  
 `ppCtx`  
 <span data-ttu-id="2fc89-107">[out] Pointeur vers un contexte d’application.</span><span class="sxs-lookup"><span data-stu-id="2fc89-107">[out] A pointer to an application context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2fc89-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2fc89-108">Requirements</span></span>  
 <span data-ttu-id="2fc89-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2fc89-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2fc89-110">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="2fc89-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="2fc89-111">**Bibliothèque :** inclus en tant que ressource dans le fichier Fusion.dll</span><span class="sxs-lookup"><span data-stu-id="2fc89-111">**Library:** Included as a resource in Fusion.dll</span></span>  
  
 <span data-ttu-id="2fc89-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2fc89-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2fc89-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fc89-113">See Also</span></span>  
 [<span data-ttu-id="2fc89-114">IAssemblyCache, interface</span><span class="sxs-lookup"><span data-stu-id="2fc89-114">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)  
 [<span data-ttu-id="2fc89-115">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="2fc89-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)  
 [<span data-ttu-id="2fc89-116">Global Assembly Cache</span><span class="sxs-lookup"><span data-stu-id="2fc89-116">Global Assembly Cache</span></span>](../../../../docs/framework/app-domains/gac.md)
