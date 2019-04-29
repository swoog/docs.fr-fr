---
title: Init, méthode
ms.date: 03/30/2017
api_name:
- IALink.Init
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- Init
helpviewer_keywords:
- Init method
ms.assetid: e48b5c64-049f-4f93-ad87-d07ae9cd5845
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 60602462376543fe934bb3c58bc4988fa8ab34bf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61949108"
---
# <a name="init-method"></a><span data-ttu-id="fd807-102">Init, méthode</span><span class="sxs-lookup"><span data-stu-id="fd807-102">Init Method</span></span>
<span data-ttu-id="fd807-103">Prépare les objets implémentant le [IALink Interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="fd807-103">Prepares objects implementing the [IALink Interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md) for use.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd807-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd807-104">Syntax</span></span>  
  
```  
HRESULT Init(  
    IMetaDataDispenserEx* pDispenser,  
    IMetaDataError* pErrorHandler  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd807-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd807-105">Parameters</span></span>  
 `pDispenser`  
 <span data-ttu-id="fd807-106">[IMetaDataDispenserEx, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md) pointeur vers le distributeur de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="fd807-106">[IMetaDataDispenserEx Interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md) pointer to the metadata dispenser.</span></span>  
  
 `pErrorHandler`  
 <span data-ttu-id="fd807-107">[IMetaDataError, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-interface.md) pointeur à une interface de gestion d’erreur facultatif.</span><span class="sxs-lookup"><span data-stu-id="fd807-107">[IMetaDataError Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-interface.md) pointer to an optional error handling interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fd807-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fd807-108">Return Value</span></span>  
 <span data-ttu-id="fd807-109">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="fd807-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd807-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd807-110">Requirements</span></span>  
 <span data-ttu-id="fd807-111">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="fd807-111">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd807-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd807-112">See also</span></span>

- [<span data-ttu-id="fd807-113">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="fd807-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="fd807-114">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="fd807-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="fd807-115">API ALink</span><span class="sxs-lookup"><span data-stu-id="fd807-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
