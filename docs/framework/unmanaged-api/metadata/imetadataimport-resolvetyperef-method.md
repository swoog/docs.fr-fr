---
title: IMetaDataImport::ResolveTypeRef, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.ResolveTypeRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::ResolveTypeRef
helpviewer_keywords:
- ResolveTypeRef method [.NET Framework metadata]
- IMetaDataImport::ResolveTypeRef method [.NET Framework metadata]
ms.assetid: 556bccfb-61bc-4761-b1d5-de4b1c18a38f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f929e6b338d4fd48b2a6ef9588523377e0dd8faa
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59096060"
---
# <a name="imetadataimportresolvetyperef-method"></a><span data-ttu-id="e297b-102">IMetaDataImport::ResolveTypeRef, méthode</span><span class="sxs-lookup"><span data-stu-id="e297b-102">IMetaDataImport::ResolveTypeRef Method</span></span>
<span data-ttu-id="e297b-103">Résout un <xref:System.Type> référence représenté par le jeton TypeRef spécifié.</span><span class="sxs-lookup"><span data-stu-id="e297b-103">Resolves a <xref:System.Type> reference represented by the specified TypeRef token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e297b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e297b-104">Syntax</span></span>  
  
```  
HRESULT ResolveTypeRef (  
   [in]  mdTypeRef       tr,  
   [in]  REFIID          riid,  
   [out] IUnknown        **ppIScope,  
   [out] mdTypeDef       *ptd  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e297b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e297b-105">Parameters</span></span>  
 `tr`  
 <span data-ttu-id="e297b-106">[in] Le jeton de métadonnées TypeRef pour retourner les informations de type référencée.</span><span class="sxs-lookup"><span data-stu-id="e297b-106">[in] The TypeRef metadata token to return the referenced type information for.</span></span>  
  
 `riid`  
 <span data-ttu-id="e297b-107">[in] IID de l’interface à retourner dans `ppIScope`.</span><span class="sxs-lookup"><span data-stu-id="e297b-107">[in] The IID of the interface to return in `ppIScope`.</span></span> <span data-ttu-id="e297b-108">En règle générale, il s’agirait IID_IMetaDataImport.</span><span class="sxs-lookup"><span data-stu-id="e297b-108">Typically, this would be IID_IMetaDataImport.</span></span>  
  
 `ppIScope`  
 <span data-ttu-id="e297b-109">[out] Une interface à la portée de module dans lequel le type référencé est défini.</span><span class="sxs-lookup"><span data-stu-id="e297b-109">[out] An interface to the module scope in which the referenced type is defined.</span></span>  
  
 `ptd`  
 <span data-ttu-id="e297b-110">[out] Pointeur vers un jeton TypeDef qui représente le type référencé.</span><span class="sxs-lookup"><span data-stu-id="e297b-110">[out] A pointer to a TypeDef token that represents the referenced type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e297b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e297b-111">Remarks</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e297b-112">N’utilisez pas cette méthode si plusieurs domaines d’application sont chargés.</span><span class="sxs-lookup"><span data-stu-id="e297b-112">Do not use this method if multiple application domains are loaded.</span></span> <span data-ttu-id="e297b-113">La méthode ne respecte pas les limites du domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="e297b-113">The method does not respect application domain boundaries.</span></span> <span data-ttu-id="e297b-114">Si plusieurs versions d’un assembly sont chargées, et ils contiennent le même type avec le même espace de noms, la méthode retourne la portée de module du premier type qu’il trouve.</span><span class="sxs-lookup"><span data-stu-id="e297b-114">If multiple versions of an assembly are loaded, and they contain the same type with the same namespace, the method returns the module scope of the first type it finds.</span></span>  
  
 <span data-ttu-id="e297b-115">Le `ResolveTypeRef` méthode recherche la définition de type dans d’autres modules.</span><span class="sxs-lookup"><span data-stu-id="e297b-115">The `ResolveTypeRef` method searches for the type definition in other modules.</span></span> <span data-ttu-id="e297b-116">Si la définition de type est trouvée, `ResolveTypeRef` retourne une interface pour cette portée de module, ainsi que le jeton TypeDef pour le type.</span><span class="sxs-lookup"><span data-stu-id="e297b-116">If the type definition is found, `ResolveTypeRef` returns an interface to that module scope as well as the TypeDef token for the type.</span></span>  
  
 <span data-ttu-id="e297b-117">Si la référence de type doivent être résolus a une portée de résolution AssemblyRef, la `ResolveTypeRef` méthode recherche une correspondance uniquement dans les portées de métadonnées qui ont déjà été ouverte avec appels à la [IMetaDataDispenser::OpenScope](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md)méthode ou le [IMetaDataDispenser::OpenScopeOnMemory](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscopeonmemory-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e297b-117">If the type reference to be resolved has a resolution scope of AssemblyRef, the `ResolveTypeRef` method searches for a match only in the metadata scopes that have already been opened with calls to either the [IMetaDataDispenser::OpenScope](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md) method or the [IMetaDataDispenser::OpenScopeOnMemory](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscopeonmemory-method.md) method.</span></span> <span data-ttu-id="e297b-118">Il s’agit, car `ResolveTypeRef` ne peut pas déterminer d’uniquement l’étendue AssemblyRef où sur le disque ou dans le global assembly cache l’assembly est stocké.</span><span class="sxs-lookup"><span data-stu-id="e297b-118">This is because `ResolveTypeRef` cannot determine from only the AssemblyRef scope where on disk or in the global assembly cache the assembly is stored.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e297b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e297b-119">Requirements</span></span>  
 <span data-ttu-id="e297b-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e297b-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e297b-121">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e297b-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e297b-122">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e297b-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e297b-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e297b-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e297b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e297b-124">See also</span></span>

- [<span data-ttu-id="e297b-125">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="e297b-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="e297b-126">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="e297b-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
