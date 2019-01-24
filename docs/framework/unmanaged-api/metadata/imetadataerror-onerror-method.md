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
ms.openlocfilehash: 7ebb7fdbcf8c17991928df2dc621ec651b9cd4f5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54678718"
---
# <a name="imetadataerroronerror-method"></a><span data-ttu-id="874b8-102">IMetaDataError::OnError, méthode</span><span class="sxs-lookup"><span data-stu-id="874b8-102">IMetaDataError::OnError Method</span></span>
<span data-ttu-id="874b8-103">Fournit une notification des erreurs qui se produisent pendant la fusion des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="874b8-103">Provides notification of errors that occur during the metadata merge.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="874b8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="874b8-104">Syntax</span></span>  
  
```  
HRESULT OnError (  
    [in] HRESULT   hrError,   
    [in] mdToken   token  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="874b8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="874b8-105">Parameters</span></span>  
 `hrError`  
 <span data-ttu-id="874b8-106">[in] La valeur d’erreur HRESULT retournée à la méthode appelante.</span><span class="sxs-lookup"><span data-stu-id="874b8-106">[in] The HRESULT error value returned to the calling method.</span></span>  
  
 `token`  
 <span data-ttu-id="874b8-107">[in] Le jeton de métadonnées de l’objet de code qui était en cours de fusion lorsque l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="874b8-107">[in] The metadata token of the code object that was being merged when the error occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="874b8-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="874b8-108">Requirements</span></span>  
 <span data-ttu-id="874b8-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="874b8-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="874b8-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="874b8-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="874b8-111">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="874b8-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="874b8-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="874b8-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="874b8-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="874b8-113">See also</span></span>
- [<span data-ttu-id="874b8-114">IMetaDataError, interface</span><span class="sxs-lookup"><span data-stu-id="874b8-114">IMetaDataError Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-interface.md)
