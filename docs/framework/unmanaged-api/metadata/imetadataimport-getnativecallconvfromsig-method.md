---
title: IMetaDataImport::GetNativeCallConvFromSig, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetNativeCallConvFromSig
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetNativeCallConvFromSig
helpviewer_keywords:
- GetNativeCallConvFromSig method [.NET Framework metadata]
- IMetaDataImport::GetNativeCallConvFromSig method [.NET Framework metadata]
ms.assetid: 50e04026-4d4a-47d9-96c1-f4677d6d938b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ef1ac83b383a9f6bbee7f55441d2abfcb081afa6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59122744"
---
# <a name="imetadataimportgetnativecallconvfromsig-method"></a><span data-ttu-id="8a501-102">IMetaDataImport::GetNativeCallConvFromSig, méthode</span><span class="sxs-lookup"><span data-stu-id="8a501-102">IMetaDataImport::GetNativeCallConvFromSig Method</span></span>
<span data-ttu-id="8a501-103">Obtient la convention d’appel native pour la méthode représentée par le pointeur de signature spécifié.</span><span class="sxs-lookup"><span data-stu-id="8a501-103">Gets the native calling convention for the method that is represented by the specified signature pointer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a501-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a501-104">Syntax</span></span>  
  
```  
HRESULT GetNativeCallConvFromSig (  
   [in]  void const  *pvSig,  
   [in]  ULONG       cbSig,  
   [out] ULONG       *pCallConv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a501-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a501-105">Parameters</span></span>  
 `pvSig`  
 <span data-ttu-id="8a501-106">[in] Pointeur vers la signature de métadonnées de la méthode pour retourner la convention d’appel pour.</span><span class="sxs-lookup"><span data-stu-id="8a501-106">[in] A pointer to the metadata signature of the method to return the calling convention for.</span></span>  
  
 `cbSig`  
 <span data-ttu-id="8a501-107">[in] La taille en octets de `pvSig`.</span><span class="sxs-lookup"><span data-stu-id="8a501-107">[in] The size in bytes of `pvSig`.</span></span>  
  
 `pCallConv`  
 <span data-ttu-id="8a501-108">[out] Pointeur vers la convention d’appel native.</span><span class="sxs-lookup"><span data-stu-id="8a501-108">[out] A pointer to the native calling convention.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a501-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a501-109">Requirements</span></span>  
 <span data-ttu-id="8a501-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8a501-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a501-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="8a501-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8a501-112">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8a501-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="8a501-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a501-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a501-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a501-114">See also</span></span>

- <xref:System.Runtime.InteropServices.CallingConvention>
- [<span data-ttu-id="8a501-115">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="8a501-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="8a501-116">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="8a501-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
