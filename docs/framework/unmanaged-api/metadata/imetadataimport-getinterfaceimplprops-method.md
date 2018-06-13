---
title: IMetaDataImport::GetInterfaceImplProps, méthode
ms.date: 03/30/2017
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
ms.openlocfilehash: 9fca044b5dce260a1eed55b01531e7ae21a16ebd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446160"
---
# <a name="imetadataimportgetinterfaceimplprops-method"></a><span data-ttu-id="cce24-102">IMetaDataImport::GetInterfaceImplProps, méthode</span><span class="sxs-lookup"><span data-stu-id="cce24-102">IMetaDataImport::GetInterfaceImplProps Method</span></span>
<span data-ttu-id="cce24-103">Obtient un pointeur vers les jetons de métadonnées pour le <xref:System.Type> qui implémente la méthode spécifiée, et pour l’interface qui déclare cette méthode.</span><span class="sxs-lookup"><span data-stu-id="cce24-103">Gets a pointer to the metadata tokens for the <xref:System.Type> that implements the specified method, and for the interface that declares that method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cce24-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cce24-104">Syntax</span></span>  
  
```  
HRESULT GetInterfaceImplProps (  
   [in]  mdInterfaceImpl        iiImpl,  
   [out] mdTypeDef              *pClass,  
   [out] mdToken                *ptkIface  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cce24-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cce24-105">Parameters</span></span>  
 `iiImpl`  
 <span data-ttu-id="cce24-106">[in] Représente la méthode pour retourner les jetons de classe et d’interface pour le jeton de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cce24-106">[in] The metadata token representing the method to return the class and interface tokens for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="cce24-107">[out] Le jeton de métadonnées représentant la classe qui implémente la méthode.</span><span class="sxs-lookup"><span data-stu-id="cce24-107">[out] The metadata token representing the class that implements the method.</span></span>  
  
 `ptkIface`  
 <span data-ttu-id="cce24-108">[out] Le jeton de métadonnées qui représente l’interface qui définit la méthode implémentée.</span><span class="sxs-lookup"><span data-stu-id="cce24-108">[out] The metadata token representing the interface that defines the implemented method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cce24-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cce24-109">Requirements</span></span>  
 <span data-ttu-id="cce24-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cce24-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cce24-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="cce24-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cce24-112">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cce24-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="cce24-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cce24-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cce24-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cce24-114">See Also</span></span>  
 [<span data-ttu-id="cce24-115">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="cce24-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="cce24-116">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="cce24-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
