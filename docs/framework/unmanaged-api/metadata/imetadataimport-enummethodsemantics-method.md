---
title: IMetaDataImport::EnumMethodSemantics, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumMethodSemantics
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumMethodSemantics
helpviewer_keywords:
- EnumMethodSemantics method [.NET Framework metadata]
- IMetaDataImport::EnumMethodSemantics method [.NET Framework metadata]
ms.assetid: e7e3c630-9691-46d6-94df-b5593a7bb08a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 16cfa6df6251cd67860155cb8092e77a835eaaef
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59223263"
---
# <a name="imetadataimportenummethodsemantics-method"></a><span data-ttu-id="3c71e-102">IMetaDataImport::EnumMethodSemantics, méthode</span><span class="sxs-lookup"><span data-stu-id="3c71e-102">IMetaDataImport::EnumMethodSemantics Method</span></span>
<span data-ttu-id="3c71e-103">Énumère les propriétés et les événements de modification de propriétés auxquels la méthode spécifiée est associée.</span><span class="sxs-lookup"><span data-stu-id="3c71e-103">Enumerates the properties and the property-change events to which the specified method is related.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c71e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c71e-104">Syntax</span></span>  
  
```  
HRESULT EnumMethodSemantics (  
   [in, out] HCORENUM    *phEnum,  
   [in]  mdMethodDef     mb,   
   [out] mdToken         rEventProp[],  
   [in]  ULONG           cMax,  
   [out] ULONG           *pcEventProp  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3c71e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c71e-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="3c71e-106">[in, out] Pointeur vers l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="3c71e-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="3c71e-107">Cela doit être NULL pour le premier appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3c71e-107">This must be NULL for the first call of this method.</span></span>  
  
 `mb`  
 <span data-ttu-id="3c71e-108">[in] Jeton MethodDef qui limite l’étendue de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="3c71e-108">[in] A MethodDef token that limits the scope of the enumeration.</span></span>  
  
 `rEventProp`  
 <span data-ttu-id="3c71e-109">[out] Tableau utilisé pour stocker les événements ou les propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c71e-109">[out] The array used to store the events or properties.</span></span>  
  
 `cMax`  
 <span data-ttu-id="3c71e-110">[in] Taille maximale du tableau `rEventProp`.</span><span class="sxs-lookup"><span data-stu-id="3c71e-110">[in] The maximum size of the `rEventProp` array.</span></span>  
  
 `pcEventProp`  
 <span data-ttu-id="3c71e-111">[out] Le nombre d’événements ou les propriétés retournées dans `rEventProp`.</span><span class="sxs-lookup"><span data-stu-id="3c71e-111">[out] The number of events or properties returned in `rEventProp`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3c71e-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3c71e-112">Return Value</span></span>  
  
|<span data-ttu-id="3c71e-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3c71e-113">HRESULT</span></span>|<span data-ttu-id="3c71e-114">Description</span><span class="sxs-lookup"><span data-stu-id="3c71e-114">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|`EnumMethodSemantics` <span data-ttu-id="3c71e-115">retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="3c71e-115">returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="3c71e-116">Il n’existe aucun événements ou propriétés à énumérer.</span><span class="sxs-lookup"><span data-stu-id="3c71e-116">There are no events or properties to enumerate.</span></span> <span data-ttu-id="3c71e-117">Dans ce cas, `pcEventProp` est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3c71e-117">In that case, `pcEventProp` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3c71e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="3c71e-118">Remarks</span></span>  
 <span data-ttu-id="3c71e-119">Définissent de nombreux types common language runtime *propriété* `Changed` événements et `On` *propriété* `Changed` méthodes liées à leurs propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c71e-119">Many common language runtime types define *Property*`Changed` events and `On`*Property*`Changed` methods related to their properties.</span></span> <span data-ttu-id="3c71e-120">Par exemple, le <xref:System.Windows.Forms.Control?displayProperty=nameWithType> type définit un <xref:System.Windows.Forms.Control.Font%2A> propriété, un <xref:System.Windows.Forms.Control.FontChanged> événement et un <xref:System.Windows.Forms.Control.OnFontChanged%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="3c71e-120">For example, the <xref:System.Windows.Forms.Control?displayProperty=nameWithType> type defines a <xref:System.Windows.Forms.Control.Font%2A> property, a <xref:System.Windows.Forms.Control.FontChanged> event, and an <xref:System.Windows.Forms.Control.OnFontChanged%2A> method.</span></span> <span data-ttu-id="3c71e-121">La méthode d’accesseur set de la <xref:System.Windows.Forms.Control.Font%2A> les appels de propriété <xref:System.Windows.Forms.Control.OnFontChanged%2A> (méthode), qui à son tour déclenche le <xref:System.Windows.Forms.Control.FontChanged> événement.</span><span class="sxs-lookup"><span data-stu-id="3c71e-121">The set accessor method of the <xref:System.Windows.Forms.Control.Font%2A> property calls <xref:System.Windows.Forms.Control.OnFontChanged%2A> method, which in turn raises the <xref:System.Windows.Forms.Control.FontChanged> event.</span></span> <span data-ttu-id="3c71e-122">Vous appelleriez `EnumMethodSemantics` à l’aide de le MethodDef pour <xref:System.Windows.Forms.Control.OnFontChanged%2A> pour obtenir des références à la <xref:System.Windows.Forms.Control.Font%2A> propriété et le <xref:System.Windows.Forms.Control.FontChanged> événement.</span><span class="sxs-lookup"><span data-stu-id="3c71e-122">You would call `EnumMethodSemantics` using the MethodDef for <xref:System.Windows.Forms.Control.OnFontChanged%2A> to get references to the <xref:System.Windows.Forms.Control.Font%2A> property and the <xref:System.Windows.Forms.Control.FontChanged> event.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c71e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c71e-123">Requirements</span></span>  
 <span data-ttu-id="3c71e-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3c71e-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c71e-125">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="3c71e-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="3c71e-126">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3c71e-126">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="3c71e-127">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3c71e-127">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3c71e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c71e-128">See also</span></span>

- [<span data-ttu-id="3c71e-129">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="3c71e-129">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="3c71e-130">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="3c71e-130">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
