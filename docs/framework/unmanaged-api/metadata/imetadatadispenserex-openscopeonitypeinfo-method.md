---
title: IMetaDataDispenserEx::OpenScopeOnITypeInfo, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.OpenScopeOnITypeInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::OpenScopeOnITypeInfo
helpviewer_keywords:
- OpenScopeOnITypeInfo method [.NET Framework metadata]
- IMetaDataDispenserEx::OpenScopeOnITypeInfo method [.NET Framework metadata]
ms.assetid: 3480bbdb-c442-44a0-b7c6-333354503c52
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 122a31fab3bf7bf10eb2490a955fb8245ea0408b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471028"
---
# <a name="imetadatadispenserexopenscopeonitypeinfo-method"></a><span data-ttu-id="c410d-102">IMetaDataDispenserEx::OpenScopeOnITypeInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="c410d-102">IMetaDataDispenserEx::OpenScopeOnITypeInfo Method</span></span>
<span data-ttu-id="c410d-103">Cette méthode n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="c410d-103">This method is not implemented.</span></span> <span data-ttu-id="c410d-104">Si elle est appelée, elle retourne E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c410d-104">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c410d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c410d-105">Syntax</span></span>  
  
```  
HRESULT OpenScopeOnITypeInfo (  
    [in]  ITypeInfo   *pITI,  
    [in]  DWORD       dwOpenFlags,  
    [in]  REFIID      riid,  
    [out] IUnknown    **ppIUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c410d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c410d-106">Parameters</span></span>  
 `pITI`  
 <span data-ttu-id="c410d-107">[in] Pointeur vers un [ITypeInfo](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo) interface qui fournit les informations de type sur lequel ouvrir la portée.</span><span class="sxs-lookup"><span data-stu-id="c410d-107">[in] Pointer to an [ITypeInfo](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo) interface that provides the type information on which to open the scope.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="c410d-108">[in] Les indicateurs de mode d’ouverture.</span><span class="sxs-lookup"><span data-stu-id="c410d-108">[in] The open mode flags.</span></span>  
  
 `riid`  
 <span data-ttu-id="c410d-109">[in] L’interface souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c410d-109">[in] The desired interface.</span></span>  
  
 `ppIUnk`  
 <span data-ttu-id="c410d-110">[out] Pointeur vers un pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="c410d-110">[out] Pointer to a pointer to the returned interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c410d-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c410d-111">Requirements</span></span>  
 <span data-ttu-id="c410d-112">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c410d-112">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c410d-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c410d-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c410d-114">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c410d-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c410d-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c410d-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c410d-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c410d-116">See also</span></span>
- [<span data-ttu-id="c410d-117">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="c410d-117">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [<span data-ttu-id="c410d-118">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="c410d-118">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
