---
title: CoInitializeEE, fonction
ms.date: 03/30/2017
api_name:
- CoInitializeEE
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeEE
helpviewer_keywords:
- CoInitializeEE function [.NET Framework hosting]
ms.assetid: 7e42a928-5068-4ba6-b8c3-806551a01fa8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ca85a12191db51818da2a08910dc9524d1ac9498
ms.sourcegitcommit: 79066169e93d9d65203028b21983574ad9dcf6b4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57211817"
---
# <a name="coinitializeee-function"></a><span data-ttu-id="fe2b3-102">CoInitializeEE, fonction</span><span class="sxs-lookup"><span data-stu-id="fe2b3-102">CoInitializeEE Function</span></span>
<span data-ttu-id="fe2b3-103">Garantit que le moteur d’exécution du common language runtime est chargé dans un processus.</span><span class="sxs-lookup"><span data-stu-id="fe2b3-103">Ensures that the common language runtime execution engine is loaded into a process.</span></span> <span data-ttu-id="fe2b3-104">Cette fonction est déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fe2b3-104">This function is deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span> <span data-ttu-id="fe2b3-105">Utilisez le [ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="fe2b3-105">Use the [ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe2b3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe2b3-106">Syntax</span></span>  
  
```  
HRESULT CoInitializeEE (  
   [in] DWORD fFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fe2b3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe2b3-107">Parameters</span></span>  
 `fFlags`  
 <span data-ttu-id="fe2b3-108">[in] Parmi les [COINITIEE](../../../../docs/framework/unmanaged-api/metadata/coinitiee-enumeration.md) constantes d’énumération.</span><span class="sxs-lookup"><span data-stu-id="fe2b3-108">[in] One of the [COINITIEE](../../../../docs/framework/unmanaged-api/metadata/coinitiee-enumeration.md) enumeration constants.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fe2b3-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fe2b3-109">Return Value</span></span>  
 <span data-ttu-id="fe2b3-110">Cette méthode retourne des codes d’erreur COM standard, tel que défini dans Winerror.h et les valeurs dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fe2b3-110">This method returns standard COM error codes as defined in Winerror.h, and the values in the following table.</span></span>  
  
|<span data-ttu-id="fe2b3-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fe2b3-111">Return code</span></span>|<span data-ttu-id="fe2b3-112">Description</span><span class="sxs-lookup"><span data-stu-id="fe2b3-112">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="fe2b3-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="fe2b3-113">S_OK</span></span>|<span data-ttu-id="fe2b3-114">Le moteur d’exécution a été chargé avec succès.</span><span class="sxs-lookup"><span data-stu-id="fe2b3-114">The execution engine was loaded successfully.</span></span>|  
|<span data-ttu-id="fe2b3-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fe2b3-115">S_FALSE</span></span>|<span data-ttu-id="fe2b3-116">Le moteur d’exécution est déjà chargé.</span><span class="sxs-lookup"><span data-stu-id="fe2b3-116">The execution engine is already loaded.</span></span>|  
|<span data-ttu-id="fe2b3-117">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="fe2b3-117">E_FAIL</span></span>|<span data-ttu-id="fe2b3-118">Le moteur d’exécution n’a pas pu être chargé.</span><span class="sxs-lookup"><span data-stu-id="fe2b3-118">The execution engine could not be loaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="fe2b3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fe2b3-119">Remarks</span></span>  
 <span data-ttu-id="fe2b3-120">Cette méthode charge le moteur d’exécution s’il n’a pas été chargé précédemment.</span><span class="sxs-lookup"><span data-stu-id="fe2b3-120">This method loads the execution engine if it has not been previously loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe2b3-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe2b3-121">Requirements</span></span>  
 <span data-ttu-id="fe2b3-122">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fe2b3-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fe2b3-123">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="fe2b3-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fe2b3-124">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fe2b3-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="fe2b3-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fe2b3-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe2b3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe2b3-126">See also</span></span>
- [<span data-ttu-id="fe2b3-127">Fonctions statiques globales des métadonnées</span><span class="sxs-lookup"><span data-stu-id="fe2b3-127">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
