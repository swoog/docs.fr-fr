---
title: IMetaDataEmit::DefineTypeRefByName, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineTypeRefByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineTypeRefByName
helpviewer_keywords:
- DefineTypeRefByName method [.NET Framework metadata]
- IMetaDataEmit::DefineTypeRefByName method [.NET Framework metadata]
ms.assetid: c30a4ce3-2d3e-411a-98df-e62ac4a5dd50
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d93c55cec3d35fd4208a4a8a7c9b235dd10fb9ca
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59156167"
---
# <a name="imetadataemitdefinetyperefbyname-method"></a><span data-ttu-id="f20ee-102">IMetaDataEmit::DefineTypeRefByName, méthode</span><span class="sxs-lookup"><span data-stu-id="f20ee-102">IMetaDataEmit::DefineTypeRefByName Method</span></span>
<span data-ttu-id="f20ee-103">Obtient les métadonnées jeton pour un type qui est défini dans la portée spécifiée, qui est en dehors de la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="f20ee-103">Gets a metadata token for a type that is defined in the specified scope, which is outside the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f20ee-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f20ee-104">Syntax</span></span>  
  
```  
HRESULT DefineTypeRefByName (   
    [in]  mdToken     tkResolutionScope,   
    [in]  LPCWSTR     szName,   
    [out] mdTypeRef   *ptr   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f20ee-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f20ee-105">Parameters</span></span>  
 `tkResolutionScope`  
 <span data-ttu-id="f20ee-106">[in] Le jeton en spécifiant la résolution de portée.</span><span class="sxs-lookup"><span data-stu-id="f20ee-106">[in] The token specifying the resolution scope.</span></span> <span data-ttu-id="f20ee-107">Les types de jetons suivants sont valides :</span><span class="sxs-lookup"><span data-stu-id="f20ee-107">The following token types are valid:</span></span>  
  
-   `mdModuleRef`<span data-ttu-id="f20ee-108">, si le type est défini dans le même assembly dans lequel l’appelant est défini.</span><span class="sxs-lookup"><span data-stu-id="f20ee-108">, if the type is defined in the same assembly in which the caller is defined.</span></span>  
  
-   `mdAssemblyRef`<span data-ttu-id="f20ee-109">, si le type est défini dans un assembly autre que celui dans lequel l’appelant est défini.</span><span class="sxs-lookup"><span data-stu-id="f20ee-109">, if the type is defined in an assembly other than the one in which the caller is defined.</span></span>  
  
-   `mdTypeRef`<span data-ttu-id="f20ee-110">, si le type est un type imbriqué.</span><span class="sxs-lookup"><span data-stu-id="f20ee-110">, if the type is a nested type.</span></span>  
  
-   `mdModule`<span data-ttu-id="f20ee-111">, si le type est défini dans le même module que celui dans lequel l’appelant est défini.</span><span class="sxs-lookup"><span data-stu-id="f20ee-111">, if the type is defined in the same module in which the caller is defined.</span></span>  
  
-   <span data-ttu-id="f20ee-112">Valeur null, si le type est défini dans le monde entier.</span><span class="sxs-lookup"><span data-stu-id="f20ee-112">Null, if the type is defined globally.</span></span>  
  
 `szName`  
 <span data-ttu-id="f20ee-113">[in] Le nom du type cible au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="f20ee-113">[in] The name of the target type in Unicode.</span></span>  
  
 `ptr`  
 <span data-ttu-id="f20ee-114">[out] Un pointeur vers le `mdTypeRef` jeton qui est assigné au type.</span><span class="sxs-lookup"><span data-stu-id="f20ee-114">[out] A pointer to the `mdTypeRef` token that is assigned to the type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f20ee-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f20ee-115">Requirements</span></span>  
 <span data-ttu-id="f20ee-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f20ee-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f20ee-117">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="f20ee-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f20ee-118">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f20ee-118">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="f20ee-119">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="f20ee-119">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="f20ee-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f20ee-120">See also</span></span>

- [<span data-ttu-id="f20ee-121">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="f20ee-121">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="f20ee-122">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="f20ee-122">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
