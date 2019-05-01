---
title: IMetaDataEmit::SetFieldRVA, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetFieldRVA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetFieldRVA
helpviewer_keywords:
- IMetaDataEmit::SetFieldRVA method [.NET Framework metadata]
- SetFieldRVA method [.NET Framework metadata]
ms.assetid: 6dc37f9d-87ee-4cb3-9216-ced600184ce8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4ebde1d506a120a99e1c637c660b45d698994f5a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61992470"
---
# <a name="imetadataemitsetfieldrva-method"></a><span data-ttu-id="bcc53-102">IMetaDataEmit::SetFieldRVA, méthode</span><span class="sxs-lookup"><span data-stu-id="bcc53-102">IMetaDataEmit::SetFieldRVA Method</span></span>
<span data-ttu-id="bcc53-103">Définit une valeur de variable globale pour l’adresse virtuelle relative du champ référencé par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="bcc53-103">Sets a global variable value for the relative virtual address of the field referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bcc53-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcc53-104">Syntax</span></span>  
  
```  
HRESULT SetFieldRVA (   
    [in]  mdFieldDef  fd,   
    [in]  ULONG       ulRVA   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bcc53-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcc53-105">Parameters</span></span>  
 `fd`  
 <span data-ttu-id="bcc53-106">[in] Le jeton pour le champ cible.</span><span class="sxs-lookup"><span data-stu-id="bcc53-106">[in] The token for the target field.</span></span>  
  
 `ulRVA`  
 <span data-ttu-id="bcc53-107">[in] L’adresse d’une zone de code ou de données.</span><span class="sxs-lookup"><span data-stu-id="bcc53-107">[in] The address of a code or data area.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bcc53-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcc53-108">Requirements</span></span>  
 <span data-ttu-id="bcc53-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bcc53-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcc53-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="bcc53-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="bcc53-111">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bcc53-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bcc53-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcc53-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bcc53-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcc53-113">See also</span></span>

- [<span data-ttu-id="bcc53-114">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="bcc53-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="bcc53-115">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="bcc53-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
