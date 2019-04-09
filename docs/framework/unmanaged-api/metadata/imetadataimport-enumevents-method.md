---
title: IMetaDataImport::EnumEvents, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumEvents
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumEvents
helpviewer_keywords:
- IMetaDataImport::EnumEvents method [.NET Framework metadata]
- EnumEvents method [.NET Framework metadata]
ms.assetid: e1efedcb-3dd7-42ae-a399-21c24728aec5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b2ba46c025c2d031f0526c6a9da5f6ab07023741
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208447"
---
# <a name="imetadataimportenumevents-method"></a><span data-ttu-id="3a932-102">IMetaDataImport::EnumEvents, méthode</span><span class="sxs-lookup"><span data-stu-id="3a932-102">IMetaDataImport::EnumEvents Method</span></span>
<span data-ttu-id="3a932-103">Énumère les jetons de définition d'événements pour le jeton TypeDef spécifié.</span><span class="sxs-lookup"><span data-stu-id="3a932-103">Enumerates event definition tokens for the specified TypeDef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a932-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a932-104">Syntax</span></span>  
  
```  
HRESULT EnumEvents (   
   [in, out] HCORENUM    *phEnum,   
   [in]      mdTypeDef   td,   
   [out]     mdEvent     rEvents[],   
   [in]      ULONG       cMax,  
   [out]    ULONG        *pcEvents  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3a932-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a932-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="3a932-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="3a932-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `td`  
 <span data-ttu-id="3a932-107">[in] Le jeton TypeDef dont les définitions d’événement doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="3a932-107">[in] The TypeDef token whose event definitions are to be enumerated.</span></span>  
  
 `rEvents`  
 <span data-ttu-id="3a932-108">[out] Tableau d’événements retournés.</span><span class="sxs-lookup"><span data-stu-id="3a932-108">[out] The array of returned events.</span></span>  
  
 `cMax`  
 <span data-ttu-id="3a932-109">[in] Taille maximale du tableau `rEvents`.</span><span class="sxs-lookup"><span data-stu-id="3a932-109">[in] The maximum size of the `rEvents` array.</span></span>  
  
 `pcEvents`  
 <span data-ttu-id="3a932-110">[out] Le nombre réel d’événements renvoyés dans `rEvents`.</span><span class="sxs-lookup"><span data-stu-id="3a932-110">[out] The actual number of events returned in `rEvents`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3a932-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3a932-111">Return Value</span></span>  
  
|<span data-ttu-id="3a932-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3a932-112">HRESULT</span></span>|<span data-ttu-id="3a932-113">Description</span><span class="sxs-lookup"><span data-stu-id="3a932-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|`EnumEvents` <span data-ttu-id="3a932-114">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="3a932-114">returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="3a932-115">Il n’existe aucun événement à énumérer.</span><span class="sxs-lookup"><span data-stu-id="3a932-115">There are no events to enumerate.</span></span> <span data-ttu-id="3a932-116">Dans ce cas, `pcEvents` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3a932-116">In that case, `pcEvents` is zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3a932-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a932-117">Requirements</span></span>  
 <span data-ttu-id="3a932-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3a932-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a932-119">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3a932-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3a932-120">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3a932-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="3a932-121">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3a932-121">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3a932-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a932-122">See also</span></span>

- [<span data-ttu-id="3a932-123">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="3a932-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="3a932-124">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="3a932-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
