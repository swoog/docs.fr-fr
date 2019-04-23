---
title: IMetaDataError::OnError, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataError.OnError
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataError::OnError
helpviewer_keywords:
- IMetaDataError::OnError method [.NET Framework metadata]
- OnError method, IMetaDataError interface [.NET Framework metadata]
ms.assetid: c1e744b8-a6fb-4d9c-a971-8babc875d8f0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 68fe41afa1999295a32b930b779991e2bbddb19a
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59117324"
---
# <a name="imetadataerroronerror-method"></a><span data-ttu-id="00995-102">IMetaDataError::OnError, méthode</span><span class="sxs-lookup"><span data-stu-id="00995-102">IMetaDataError::OnError Method</span></span>
<span data-ttu-id="00995-103">Fournit une notification des erreurs qui se produisent pendant la fusion des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="00995-103">Provides notification of errors that occur during the metadata merge.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00995-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00995-104">Syntax</span></span>  
  
```  
HRESULT OnError (  
    [in] HRESULT   hrError,   
    [in] mdToken   token  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="00995-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00995-105">Parameters</span></span>  
 `hrError`  
 <span data-ttu-id="00995-106">[in] La valeur d’erreur HRESULT retournée à la méthode appelante.</span><span class="sxs-lookup"><span data-stu-id="00995-106">[in] The HRESULT error value returned to the calling method.</span></span>  
  
 `token`  
 <span data-ttu-id="00995-107">[in] Le jeton de métadonnées de l’objet de code qui était en cours de fusion lorsque l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="00995-107">[in] The metadata token of the code object that was being merged when the error occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00995-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00995-108">Requirements</span></span>  
 <span data-ttu-id="00995-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="00995-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00995-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="00995-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="00995-111">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="00995-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="00995-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00995-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00995-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00995-113">See also</span></span>

- [<span data-ttu-id="00995-114">IMetaDataError, interface</span><span class="sxs-lookup"><span data-stu-id="00995-114">IMetaDataError Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-interface.md)
