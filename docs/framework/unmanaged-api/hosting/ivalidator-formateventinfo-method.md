---
title: IValidator::FormatEventInfo, méthode
ms.date: 03/30/2017
api_name:
- IValidator.FormatEventInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- FormatEventInfo
helpviewer_keywords:
- IValidator::FormatEventInfo method [.NET Framework hosting]
- FormatEventInfo method, IValidator interface [.NET Framework hosting]
ms.assetid: 4c0c7477-05ba-461b-b21b-cbfba95f1db1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 17217146d8e5ed53feb8305ca4ac16c8f96ddeb7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54653855"
---
# <a name="ivalidatorformateventinfo-method"></a><span data-ttu-id="1c718-102">IValidator::FormatEventInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="1c718-102">IValidator::FormatEventInfo Method</span></span>
<span data-ttu-id="1c718-103">Obtient le message d’erreur correspondant à l’erreur de validation spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c718-103">Gets the error message corresponding to the specified validation error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c718-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c718-104">Syntax</span></span>  
  
```  
HRESULT FormatEventInfo(  
    [in] HRESULT            hVECode,  
    [in] VEContext          Context,  
    [in, out] LPWSTR        msg,  
    [in] unsigned long      ulMaxLength,  
    [in] SAFEARRAY(VARIANT) psa  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1c718-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c718-105">Parameters</span></span>  
 `hVECode`  
 <span data-ttu-id="1c718-106">[in] La valeur HRESULT qui a été passée au gestionnaire d’erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="1c718-106">[in] The HRESULT value that was passed to the validation error handler.</span></span>  
  
 `Context`  
 <span data-ttu-id="1c718-107">[in] Un `VEContext` instance qui contient des informations de contexte sur l’erreur de validation.</span><span class="sxs-lookup"><span data-stu-id="1c718-107">[in] A `VEContext` instance that contains context information about the validation error.</span></span>  
  
 `msg`  
 <span data-ttu-id="1c718-108">[in, out] Chaîne qui contient le message d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="1c718-108">[in, out] A string that contains the returned error message.</span></span>  
  
 `ulMaxLength`  
 <span data-ttu-id="1c718-109">[in] La longueur maximale du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c718-109">[in] The maximum length of the error message.</span></span>  
  
 `psa`  
 <span data-ttu-id="1c718-110">[in] Un tableau sécurisé qui contient des paramètres supplémentaires décrivant l’erreur.</span><span class="sxs-lookup"><span data-stu-id="1c718-110">[in] A safe array that contains additional parameters describing the error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1c718-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1c718-111">Requirements</span></span>  
 <span data-ttu-id="1c718-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1c718-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c718-113">**En-tête :** IValidator.idl, IValidator.h</span><span class="sxs-lookup"><span data-stu-id="1c718-113">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="1c718-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1c718-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1c718-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1c718-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1c718-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c718-116">See also</span></span>

