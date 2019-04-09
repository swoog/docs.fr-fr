---
title: IMetaDataValidate::ValidatorInit, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataValidate.ValidatorInit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataValidate::ValidatorInit
helpviewer_keywords:
- IMetaDataValidate::ValidatorInit method [.NET Framework metadata]
- ValidatorInit method [.NET Framework metadata]
ms.assetid: 6bafd75a-e2d0-4aea-aed1-074374d5dff6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 31ff2c62810061cd8b774e934167a5ee3acf040c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195889"
---
# <a name="imetadatavalidatevalidatorinit-method"></a><span data-ttu-id="831b9-102">IMetaDataValidate::ValidatorInit, méthode</span><span class="sxs-lookup"><span data-stu-id="831b9-102">IMetaDataValidate::ValidatorInit Method</span></span>
<span data-ttu-id="831b9-103">Définit un indicateur qui spécifie le type du module dans la portée de métadonnées actuelle et enregistre la méthode de rappel spécifiée pour les erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="831b9-103">Sets a flag that specifies the type of the module in the current metadata scope, and registers the specified callback method for validation errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="831b9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="831b9-104">Syntax</span></span>  
  
```  
HRESULT ValidatorInit (  
   [in] DWORD       dwModuleType,  
   [in] IUnknown    *pUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="831b9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="831b9-105">Parameters</span></span>  
 `dwModule`  
 <span data-ttu-id="831b9-106">[in] Une valeur de la [CorValidatorModuleType](../../../../docs/framework/unmanaged-api/metadata/corvalidatormoduletype-enumeration.md) énumération qui spécifie le type du module dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="831b9-106">[in] A value of the [CorValidatorModuleType](../../../../docs/framework/unmanaged-api/metadata/corvalidatormoduletype-enumeration.md) enumeration that specifies the type of the module in the current metadata scope.</span></span>  
  
 `pUnk`  
 <span data-ttu-id="831b9-107">[in] Un pointeur vers un [IUnknown](/cpp/atl/iunknown) instance qui sert de fonction de rappel pour les erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="831b9-107">[in] A pointer to an [IUnknown](/cpp/atl/iunknown) instance that serves as a function callback for validation errors.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="831b9-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="831b9-108">Requirements</span></span>  
 <span data-ttu-id="831b9-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="831b9-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="831b9-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="831b9-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="831b9-111">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="831b9-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="831b9-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="831b9-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="831b9-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="831b9-113">See also</span></span>

- [<span data-ttu-id="831b9-114">IMetaDataValidate, interface</span><span class="sxs-lookup"><span data-stu-id="831b9-114">IMetaDataValidate Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatavalidate-interface.md)
