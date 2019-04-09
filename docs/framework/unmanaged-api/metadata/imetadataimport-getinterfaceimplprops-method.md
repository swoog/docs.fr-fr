---
title: IMetaDataImport::GetInterfaceImplProps, méthode
ms.date: 02/25/2019
api_name:
- IMetaDataImport.GetInterfaceImplProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetInterfaceImplProps
helpviewer_keywords:
- IMetaDataImport::GetInterfaceImplProps method [.NET Framework metadata]
- GetInterfaceImpProps method [.NET Framework metadata]
ms.assetid: be3f5985-b1e4-4036-8602-c16e8508d4af
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 76e2ebbd47a5e36a722fce33ba67d7efb4db8675
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59115932"
---
# <a name="imetadataimportgetinterfaceimplprops-method"></a><span data-ttu-id="a1e02-102">IMetaDataImport::GetInterfaceImplProps, méthode</span><span class="sxs-lookup"><span data-stu-id="a1e02-102">IMetaDataImport::GetInterfaceImplProps Method</span></span>
<span data-ttu-id="a1e02-103">Obtient un pointeur vers les jetons de métadonnées pour le <xref:System.Type> qui implémente la méthode spécifiée, et pour l’interface qui déclare cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a1e02-103">Gets a pointer to the metadata tokens for the <xref:System.Type> that implements the specified method, and for the interface that declares that method.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a1e02-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1e02-104">Syntax</span></span>  
  
```  
HRESULT GetInterfaceImplProps (  
   [in]  mdInterfaceImpl        iiImpl,  
   [out] mdTypeDef              *pClass,  
   [out] mdToken                *ptkIface  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a1e02-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1e02-105">Parameters</span></span>  
 `iiImpl`  
 <span data-ttu-id="a1e02-106">[in] Représentant la méthode pour renvoyer les jetons de classe et d’interface pour le jeton de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="a1e02-106">[in] The metadata token representing the method to return the class and interface tokens for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="a1e02-107">[out] Le jeton de métadonnées représentant la classe qui implémente la méthode.</span><span class="sxs-lookup"><span data-stu-id="a1e02-107">[out] The metadata token representing the class that implements the method.</span></span>  
  
 `ptkIface`  
 <span data-ttu-id="a1e02-108">[out] Le jeton de métadonnées qui représente l’interface qui définit la méthode implémentée.</span><span class="sxs-lookup"><span data-stu-id="a1e02-108">[out] The metadata token representing the interface that defines the implemented method.</span></span>  

## <a name="remarks"></a><span data-ttu-id="a1e02-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a1e02-109">Remarks</span></span>

 <span data-ttu-id="a1e02-110">Vous obtenez la valeur de `iImpl` en appelant le [EnumInterfaceImpls](imetadataimport-enuminterfaceimpls-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="a1e02-110">You obtain the value for `iImpl` by calling the [EnumInterfaceImpls](imetadataimport-enuminterfaceimpls-method.md) method.</span></span>
 
 <span data-ttu-id="a1e02-111">Par exemple, supposons qu’une classe a un `mdTypeDef` jeton la valeur de 0 x 02000007 et qu’elle implémente trois interfaces dont les types ont des jetons :</span><span class="sxs-lookup"><span data-stu-id="a1e02-111">For example, suppose that a class has an `mdTypeDef` token value of 0x02000007 and that it implements three interfaces whose types have tokens:</span></span> 

- <span data-ttu-id="a1e02-112">0x02000003 (TypeDef)</span><span class="sxs-lookup"><span data-stu-id="a1e02-112">0x02000003 (TypeDef)</span></span>
- <span data-ttu-id="a1e02-113">0x0100000A (TypeRef)</span><span class="sxs-lookup"><span data-stu-id="a1e02-113">0x0100000A (TypeRef)</span></span>
- <span data-ttu-id="a1e02-114">0x0200001C (TypeDef)</span><span class="sxs-lookup"><span data-stu-id="a1e02-114">0x0200001C (TypeDef)</span></span>

<span data-ttu-id="a1e02-115">Conceptuellement, ces informations sont stockées dans une table de mise en œuvre d’interface en tant que :</span><span class="sxs-lookup"><span data-stu-id="a1e02-115">Conceptually, this information is stored into an interface implementation table as:</span></span>

| <span data-ttu-id="a1e02-116">Numéro de ligne</span><span class="sxs-lookup"><span data-stu-id="a1e02-116">Row number</span></span> | <span data-ttu-id="a1e02-117">Jeton de classe</span><span class="sxs-lookup"><span data-stu-id="a1e02-117">Class token</span></span> | <span data-ttu-id="a1e02-118">Jeton de l’interface</span><span class="sxs-lookup"><span data-stu-id="a1e02-118">Interface token</span></span> |
|------------|-------------|-----------------|
| <span data-ttu-id="a1e02-119">4</span><span class="sxs-lookup"><span data-stu-id="a1e02-119">4</span></span>          |             |                 |
| <span data-ttu-id="a1e02-120">5</span><span class="sxs-lookup"><span data-stu-id="a1e02-120">5</span></span>          | <span data-ttu-id="a1e02-121">02000007</span><span class="sxs-lookup"><span data-stu-id="a1e02-121">02000007</span></span>    | <span data-ttu-id="a1e02-122">02000003</span><span class="sxs-lookup"><span data-stu-id="a1e02-122">02000003</span></span>        |
| <span data-ttu-id="a1e02-123">6</span><span class="sxs-lookup"><span data-stu-id="a1e02-123">6</span></span>          | <span data-ttu-id="a1e02-124">02000007</span><span class="sxs-lookup"><span data-stu-id="a1e02-124">02000007</span></span>    | <span data-ttu-id="a1e02-125">0100000A</span><span class="sxs-lookup"><span data-stu-id="a1e02-125">0100000A</span></span>        |
| <span data-ttu-id="a1e02-126">7</span><span class="sxs-lookup"><span data-stu-id="a1e02-126">7</span></span>          |             |                 |
| <span data-ttu-id="a1e02-127">8</span><span class="sxs-lookup"><span data-stu-id="a1e02-127">8</span></span>          | <span data-ttu-id="a1e02-128">02000007</span><span class="sxs-lookup"><span data-stu-id="a1e02-128">02000007</span></span>    | <span data-ttu-id="a1e02-129">0200001C</span><span class="sxs-lookup"><span data-stu-id="a1e02-129">0200001C</span></span>        |

<span data-ttu-id="a1e02-130">Rappelez-vous, le jeton est une valeur de 4 octets :</span><span class="sxs-lookup"><span data-stu-id="a1e02-130">Recall, the token is a 4-byte value:</span></span>

- <span data-ttu-id="a1e02-131">Les 3 octets contenant le nombre de lignes ou RID.</span><span class="sxs-lookup"><span data-stu-id="a1e02-131">The lower 3 bytes hold the row number, or RID.</span></span>
- <span data-ttu-id="a1e02-132">L’octet de poids fort conserve le type de jeton : 0 x 09 pour `mdtInterfaceImpl`.</span><span class="sxs-lookup"><span data-stu-id="a1e02-132">The upper byte holds the token type – 0x09 for `mdtInterfaceImpl`.</span></span>

`GetInterfaceImplProps` <span data-ttu-id="a1e02-133">Retourne les informations contenues dans la ligne dont le jeton que vous fournissez dans le `iImpl` argument.</span><span class="sxs-lookup"><span data-stu-id="a1e02-133">returns the information held in the row whose token you provide in the `iImpl` argument.</span></span> 
  
## <a name="requirements"></a><span data-ttu-id="a1e02-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1e02-134">Requirements</span></span>  
 <span data-ttu-id="a1e02-135">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a1e02-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a1e02-136">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a1e02-136">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a1e02-137">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a1e02-137">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="a1e02-138">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a1e02-138">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a1e02-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1e02-139">See also</span></span>

- [<span data-ttu-id="a1e02-140">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="a1e02-140">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="a1e02-141">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="a1e02-141">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
