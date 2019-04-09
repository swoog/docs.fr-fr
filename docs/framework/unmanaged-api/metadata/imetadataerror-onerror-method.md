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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59117324"
---
# <a name="imetadataerroronerror-method"></a><span data-ttu-id="b1458-102">IMetaDataError::OnError, méthode</span><span class="sxs-lookup"><span data-stu-id="b1458-102">IMetaDataError::OnError Method</span></span>
<span data-ttu-id="b1458-103">Fournit une notification des erreurs qui se produisent pendant la fusion des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="b1458-103">Provides notification of errors that occur during the metadata merge.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1458-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1458-104">Syntax</span></span>  
  
```  
HRESULT OnError (  
    [in] HRESULT   hrError,   
    [in] mdToken   token  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b1458-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1458-105">Parameters</span></span>  
 `hrError`  
 <span data-ttu-id="b1458-106">[in] La valeur d’erreur HRESULT retournée à la méthode appelante.</span><span class="sxs-lookup"><span data-stu-id="b1458-106">[in] The HRESULT error value returned to the calling method.</span></span>  
  
 `token`  
 <span data-ttu-id="b1458-107">[in] Le jeton de métadonnées de l’objet de code qui était en cours de fusion lorsque l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b1458-107">[in] The metadata token of the code object that was being merged when the error occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b1458-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1458-108">Requirements</span></span>  
 <span data-ttu-id="b1458-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b1458-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1458-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b1458-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b1458-111">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b1458-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="b1458-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b1458-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b1458-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1458-113">See also</span></span>

- [<span data-ttu-id="b1458-114">IMetaDataError, interface</span><span class="sxs-lookup"><span data-stu-id="b1458-114">IMetaDataError Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-interface.md)
