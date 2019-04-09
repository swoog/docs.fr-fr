---
title: IMetaDataImport::EnumUnresolvedMethods, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumUnresolvedMethods
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumUnresolvedMethods
helpviewer_keywords:
- EnumUnresolvedMethods method [.NET Framework metadata]
- IMetaDataImport::EnumUnresolvedMethods method [.NET Framework metadata]
ms.assetid: eb3187d7-74cf-44b1-aeeb-7a8d2b60e3b7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2e6e53f69f58c2f5778083d9b8f8be466b952cdd
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59090249"
---
# <a name="imetadataimportenumunresolvedmethods-method"></a><span data-ttu-id="28382-102">IMetaDataImport::EnumUnresolvedMethods, méthode</span><span class="sxs-lookup"><span data-stu-id="28382-102">IMetaDataImport::EnumUnresolvedMethods Method</span></span>
<span data-ttu-id="28382-103">Énumère les jetons MemberDef représentant les méthodes non résolues dans la portée des métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="28382-103">Enumerates MemberDef tokens representing the unresolved methods in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28382-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28382-104">Syntax</span></span>  
  
```  
HRESULT EnumUnresolvedMethods (  
   [in, out] HCORENUM    *phEnum,  
   [out]     mdToken     rMethods[],  
   [in]      ULONG       cMax,  
   [out]     ULONG       *pcTokens  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="28382-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28382-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="28382-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="28382-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="28382-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="28382-107">This must be NULL for the first call of this method.</span></span>  
  
 `rMethods`  
 <span data-ttu-id="28382-108">[out] Tableau utilisé pour stocker les jetons MemberDef.</span><span class="sxs-lookup"><span data-stu-id="28382-108">[out] The array used to store the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="28382-109">[in] Taille maximale du tableau `rMethods`.</span><span class="sxs-lookup"><span data-stu-id="28382-109">[in] The maximum size of the `rMethods` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="28382-110">[out] Le nombre de jetons MemberDef retournés dans `rMethods`.</span><span class="sxs-lookup"><span data-stu-id="28382-110">[out] The number of MemberDef tokens returned in `rMethods`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="28382-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="28382-111">Return Value</span></span>  
  
|<span data-ttu-id="28382-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="28382-112">HRESULT</span></span>|<span data-ttu-id="28382-113">Description</span><span class="sxs-lookup"><span data-stu-id="28382-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|`EnumUnresolvedMethods` <span data-ttu-id="28382-114">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="28382-114">returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="28382-115">Il n’existe pas de jetons à énumérer.</span><span class="sxs-lookup"><span data-stu-id="28382-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="28382-116">Dans ce cas, `pcTokens` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="28382-116">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="28382-117">Notes</span><span class="sxs-lookup"><span data-stu-id="28382-117">Remarks</span></span>  
 <span data-ttu-id="28382-118">Une méthode non résolue est un qui a été déclarée, mais ne pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="28382-118">An unresolved method is one that has been declared but not implemented.</span></span> <span data-ttu-id="28382-119">Une méthode est incluse dans l’énumération si la méthode est marquée `miForwardRef` et `mdPinvokeImpl` ou `miRuntime` est défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="28382-119">A method is included in the enumeration if the method is marked `miForwardRef` and either `mdPinvokeImpl` or `miRuntime` is set to zero.</span></span> <span data-ttu-id="28382-120">En d’autres termes, une méthode non résolue est une méthode de classe qui est marquée `miForwardRef` mais qui n’est pas implémenté en code non managé (atteint via PInvoke) ni implémenté en interne par le runtime lui-même</span><span class="sxs-lookup"><span data-stu-id="28382-120">In other words, an unresolved method is a class method that is marked `miForwardRef` but which is not implemented in unmanaged code (reached via PInvoke) nor implemented internally by the runtime itself</span></span>  
  
 <span data-ttu-id="28382-121">L’énumération exclut toutes les méthodes qui sont définies à portée de module (globales) ou dans les interfaces ou classes abstraites.</span><span class="sxs-lookup"><span data-stu-id="28382-121">The enumeration excludes all methods that are defined either at module scope (globals) or in interfaces or abstract classes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28382-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28382-122">Requirements</span></span>  
 <span data-ttu-id="28382-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="28382-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28382-124">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="28382-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="28382-125">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="28382-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="28382-126">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="28382-126">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="28382-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28382-127">See also</span></span>

- [<span data-ttu-id="28382-128">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="28382-128">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="28382-129">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="28382-129">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
