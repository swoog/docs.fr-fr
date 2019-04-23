---
title: IMetaDataImport::EnumMembers, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMembers
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMembers
helpviewer_keywords:
- IMetaDataImport::EnumMembers method [.NET Framework metadata]
- EnumMembers method [.NET Framework metadata]
ms.assetid: 3fb8e178-342b-4c89-9bcf-f7f834e6cb77
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e8d871f2ecbd96d5bda781b2ae11b94efd409442
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59128399"
---
# <a name="imetadataimportenummembers-method"></a><span data-ttu-id="86c44-102">IMetaDataImport::EnumMembers, méthode</span><span class="sxs-lookup"><span data-stu-id="86c44-102">IMetaDataImport::EnumMembers Method</span></span>
<span data-ttu-id="86c44-103">Énumère les jetons MemberRef représentant les membres du type spécifié.</span><span class="sxs-lookup"><span data-stu-id="86c44-103">Enumerates MemberDef tokens representing members of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86c44-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86c44-104">Syntax</span></span>  
  
```  
HRESULT EnumMembers (   
   [in, out]  HCORENUM    *phEnum,   
   [in]  mdTypeDef   cl,   
   [out] mdToken     rMembers[],   
   [in]  ULONG       cMax,   
   [out] ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86c44-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86c44-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="86c44-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="86c44-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="86c44-107">[in] Jeton TypeDef représentant le type dont les membres doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="86c44-107">[in] A TypeDef token representing the type whose members are to be enumerated.</span></span>  
  
 `rMembers`  
 <span data-ttu-id="86c44-108">[out] Tableau utilisé pour les jetons MemberDef.</span><span class="sxs-lookup"><span data-stu-id="86c44-108">[out] The array used to hold the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="86c44-109">[in] Taille maximale du tableau `rMembers`.</span><span class="sxs-lookup"><span data-stu-id="86c44-109">[in] The maximum size of the `rMembers` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="86c44-110">[out] Le nombre réel de jetons MemberDef retournés dans `rMembers`.</span><span class="sxs-lookup"><span data-stu-id="86c44-110">[out] The actual number of MemberDef tokens returned in `rMembers`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="86c44-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="86c44-111">Return Value</span></span>  
  
|<span data-ttu-id="86c44-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="86c44-112">HRESULT</span></span>|<span data-ttu-id="86c44-113">Description</span><span class="sxs-lookup"><span data-stu-id="86c44-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="86c44-114">`EnumMembers` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="86c44-114">`EnumMembers` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="86c44-115">Il n’y a aucune jetons MemberDef à énumérer.</span><span class="sxs-lookup"><span data-stu-id="86c44-115">There are no MemberDef tokens to enumerate.</span></span> <span data-ttu-id="86c44-116">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="86c44-116">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="86c44-117">Notes</span><span class="sxs-lookup"><span data-stu-id="86c44-117">Remarks</span></span>  
 <span data-ttu-id="86c44-118">Lors de l’énumération des collections de membres pour une classe, `EnumMembers` retourne uniquement les membres (champs et méthodes, mais **pas** propriétés ou événements) définies directement sur la classe.</span><span class="sxs-lookup"><span data-stu-id="86c44-118">When enumerating collections of members for a class, `EnumMembers` returns only members (fields and methods, but **not** properties or events) defined directly on the class.</span></span> <span data-ttu-id="86c44-119">Elle ne retourne pas de tous les membres qui hérite de la classe, même si la classe fournit une implémentation pour ces membres hérités.</span><span class="sxs-lookup"><span data-stu-id="86c44-119">It does not return any members that the class inherits, even if the class provides an implementation for those inherited members.</span></span> <span data-ttu-id="86c44-120">Pour énumérer les membres hérités, l’appelant doit parcourir explicitement la chaîne d’héritage.</span><span class="sxs-lookup"><span data-stu-id="86c44-120">To enumerate inherited members, the caller must explicitly walk the inheritance chain.</span></span> <span data-ttu-id="86c44-121">Notez que les règles pour la chaîne d’héritage peuvent varier en fonction de la langue ou le compilateur qui a émis les métadonnées d’origine.</span><span class="sxs-lookup"><span data-stu-id="86c44-121">Note that the rules for the inheritance chain may vary depending on the language or compiler that emitted the original metadata.</span></span>
 
 <span data-ttu-id="86c44-122">Propriétés et événements ne sont pas énumérées par `EnumMembers`.</span><span class="sxs-lookup"><span data-stu-id="86c44-122">Properties and events are not enumerated by `EnumMembers`.</span></span> <span data-ttu-id="86c44-123">Pour énumérer les, utilisez [EnumProperties](imetadataimport-enumproperties-method.md) ou [EnumEvents](imetadataimport-enumevents-method.md).</span><span class="sxs-lookup"><span data-stu-id="86c44-123">To enumerate those, use [EnumProperties](imetadataimport-enumproperties-method.md) or [EnumEvents](imetadataimport-enumevents-method.md).</span></span>
  
## <a name="requirements"></a><span data-ttu-id="86c44-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86c44-124">Requirements</span></span>  
 <span data-ttu-id="86c44-125">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86c44-125">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86c44-126">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="86c44-126">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="86c44-127">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="86c44-127">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="86c44-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="86c44-128">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="86c44-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86c44-129">See also</span></span>

- [<span data-ttu-id="86c44-130">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="86c44-130">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="86c44-131">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="86c44-131">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
