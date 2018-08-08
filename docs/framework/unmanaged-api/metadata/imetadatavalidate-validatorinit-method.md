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
ms.openlocfilehash: 053c94bc540b130510f155506b6fad32f032a475
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449544"
---
# <a name="imetadatavalidatevalidatorinit-method"></a><span data-ttu-id="b14e3-102">IMetaDataValidate::ValidatorInit, méthode</span><span class="sxs-lookup"><span data-stu-id="b14e3-102">IMetaDataValidate::ValidatorInit Method</span></span>
<span data-ttu-id="b14e3-103">Définit un indicateur qui spécifie le type du module dans la portée de métadonnées actuelle et enregistre la méthode de rappel spécifiée pour les erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="b14e3-103">Sets a flag that specifies the type of the module in the current metadata scope, and registers the specified callback method for validation errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b14e3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b14e3-104">Syntax</span></span>  
  
```  
HRESULT ValidatorInit (  
   [in] DWORD       dwModuleType,  
   [in] IUnknown    *pUnk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b14e3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b14e3-105">Parameters</span></span>  
 `dwModule`  
 <span data-ttu-id="b14e3-106">[in] Une valeur de la [CorValidatorModuleType](../../../../docs/framework/unmanaged-api/metadata/corvalidatormoduletype-enumeration.md) énumération qui spécifie le type du module dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="b14e3-106">[in] A value of the [CorValidatorModuleType](../../../../docs/framework/unmanaged-api/metadata/corvalidatormoduletype-enumeration.md) enumeration that specifies the type of the module in the current metadata scope.</span></span>  
  
 `pUnk`  
 <span data-ttu-id="b14e3-107">[in] Un pointeur vers un <<!--zzxref:IUnknown --> `IUnknown`> instance qui sert de fonction de rappel pour les erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="b14e3-107">[in] A pointer to an <<!--zzxref:IUnknown --> `IUnknown`> instance that serves as a function callback for validation errors.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b14e3-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b14e3-108">Requirements</span></span>  
 <span data-ttu-id="b14e3-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b14e3-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b14e3-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b14e3-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b14e3-111">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b14e3-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b14e3-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b14e3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b14e3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b14e3-113">See Also</span></span>  
 [<span data-ttu-id="b14e3-114">IMetaDataValidate, interface</span><span class="sxs-lookup"><span data-stu-id="b14e3-114">IMetaDataValidate Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatavalidate-interface.md)
