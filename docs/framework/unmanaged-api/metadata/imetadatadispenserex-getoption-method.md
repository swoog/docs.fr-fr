---
title: IMetaDataDispenserEx::GetOption, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.GetOption
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::GetOption
helpviewer_keywords:
- GetOption method [.NET Framework metadata]
- IMetaDataDispenserEx::GetOption method [.NET Framework metadata]
ms.assetid: d7f794e5-8e25-4d65-850a-7c34fbfce87d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fe9bc9aea4ceb0f5b5c03416f43894b482c3294e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59136628"
---
# <a name="imetadatadispenserexgetoption-method"></a><span data-ttu-id="65e26-102">IMetaDataDispenserEx::GetOption, méthode</span><span class="sxs-lookup"><span data-stu-id="65e26-102">IMetaDataDispenserEx::GetOption Method</span></span>
<span data-ttu-id="65e26-103">Obtient la valeur de l’option spécifiée pour la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="65e26-103">Gets the value of the specified option for the current metadata scope.</span></span> <span data-ttu-id="65e26-104">L’option contrôle la gestion des appels à la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="65e26-104">The option controls how calls to the current metadata scope are handled.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="65e26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65e26-105">Syntax</span></span>  
  
```  
HRESULT GetOption (  
    [in]  REFGUID         optionId,   
    [out] const VARIANT   *pValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="65e26-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65e26-106">Parameters</span></span>  
 `optionId`  
 <span data-ttu-id="65e26-107">[in] Pointeur vers un GUID qui spécifie l’option à récupérer.</span><span class="sxs-lookup"><span data-stu-id="65e26-107">[in] A pointer to a GUID that specifies the option to be retrieved.</span></span> <span data-ttu-id="65e26-108">Consultez la section Notes pour obtenir la liste de GUID pris en charge.</span><span class="sxs-lookup"><span data-stu-id="65e26-108">See the Remarks section for a list of supported GUIDs.</span></span>  
  
 `pValue`  
 <span data-ttu-id="65e26-109">[out] La valeur de l’option retournée.</span><span class="sxs-lookup"><span data-stu-id="65e26-109">[out] The value of the returned option.</span></span> <span data-ttu-id="65e26-110">Le type de cette valeur sera une variante du type de l’option spécifiée.</span><span class="sxs-lookup"><span data-stu-id="65e26-110">The type of this value will be a variant of the specified option's type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="65e26-111">Notes</span><span class="sxs-lookup"><span data-stu-id="65e26-111">Remarks</span></span>  
 <span data-ttu-id="65e26-112">La liste suivante répertorie les GUID qui sont prises en charge pour cette méthode.</span><span class="sxs-lookup"><span data-stu-id="65e26-112">The following list shows the GUIDs that are supported for this method.</span></span> <span data-ttu-id="65e26-113">Pour obtenir une description, consultez le [IMetaDataDispenserEx::SetOption](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-setoption-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="65e26-113">For descriptions, see the [IMetaDataDispenserEx::SetOption](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-setoption-method.md) method.</span></span> <span data-ttu-id="65e26-114">Si `optionId` est pas dans cette liste, cette méthode retourne les HRESULT `E_INVALIDARG`, indiquant un paramètre incorrect.</span><span class="sxs-lookup"><span data-stu-id="65e26-114">If `optionId` is not in this list, this method returns HRESULT `E_INVALIDARG`, indicating an incorrect parameter.</span></span>  
  
-   <span data-ttu-id="65e26-115">MetaDataCheckDuplicatesFor</span><span class="sxs-lookup"><span data-stu-id="65e26-115">MetaDataCheckDuplicatesFor</span></span>  
  
-   <span data-ttu-id="65e26-116">MetaDataRefToDefCheck</span><span class="sxs-lookup"><span data-stu-id="65e26-116">MetaDataRefToDefCheck</span></span>  
  
-   <span data-ttu-id="65e26-117">MetaDataNotificationForTokenMovement</span><span class="sxs-lookup"><span data-stu-id="65e26-117">MetaDataNotificationForTokenMovement</span></span>  
  
-   <span data-ttu-id="65e26-118">MetaDataSetENC</span><span class="sxs-lookup"><span data-stu-id="65e26-118">MetaDataSetENC</span></span>  
  
-   <span data-ttu-id="65e26-119">MetaDataErrorIfEmitOutOfOrder</span><span class="sxs-lookup"><span data-stu-id="65e26-119">MetaDataErrorIfEmitOutOfOrder</span></span>  
  
-   <span data-ttu-id="65e26-120">MetaDataGenerateTCEAdapters</span><span class="sxs-lookup"><span data-stu-id="65e26-120">MetaDataGenerateTCEAdapters</span></span>  
  
-   <span data-ttu-id="65e26-121">MetaDataLinkerOptions</span><span class="sxs-lookup"><span data-stu-id="65e26-121">MetaDataLinkerOptions</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="65e26-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65e26-122">Requirements</span></span>  
 <span data-ttu-id="65e26-123">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="65e26-123">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="65e26-124">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="65e26-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="65e26-125">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="65e26-125">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="65e26-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="65e26-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="65e26-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65e26-127">See also</span></span>

- [<span data-ttu-id="65e26-128">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="65e26-128">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [<span data-ttu-id="65e26-129">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="65e26-129">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
