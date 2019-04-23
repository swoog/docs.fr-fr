---
title: Méthode ICLRStrongName::StrongNameKeyDelete
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyDelete
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyDelete
helpviewer_keywords:
- StrongNameKeyDelete method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameKeyDelete method [.NET Framework hosting]
ms.assetid: 0163412f-f617-4428-89e0-03992fec31e8
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 412aa8fd30294ac9681a5edd02bb4bdfe25b3fab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59143986"
---
# <a name="iclrstrongnamestrongnamekeydelete-method"></a><span data-ttu-id="060c9-102">Méthode ICLRStrongName::StrongNameKeyDelete</span><span class="sxs-lookup"><span data-stu-id="060c9-102">ICLRStrongName::StrongNameKeyDelete Method</span></span>
<span data-ttu-id="060c9-103">Supprime le conteneur de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="060c9-103">Deletes the specified key container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="060c9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="060c9-104">Syntax</span></span>  
  
```  
HRESULT StrongNameKeyDelete (  
    [in]  LPCWSTR   wszKeyContainer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="060c9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="060c9-105">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="060c9-106">[in] Le nom du conteneur de clé à supprimer.</span><span class="sxs-lookup"><span data-stu-id="060c9-106">[in] The name of the key container to delete.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="060c9-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="060c9-107">Return Value</span></span>  
 <span data-ttu-id="060c9-108">`S_OK` Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="060c9-108">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="060c9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="060c9-109">Remarks</span></span>  
 <span data-ttu-id="060c9-110">Utilisez le [ICLRStrongName::StrongNameKeyInstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) méthode pour importer une paire de clés publique/privée dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="060c9-110">Use the [ICLRStrongName::StrongNameKeyInstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) method to import a public/private key pair into a container.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="060c9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="060c9-111">Requirements</span></span>  
 <span data-ttu-id="060c9-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="060c9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="060c9-113">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="060c9-113">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="060c9-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="060c9-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="060c9-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="060c9-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="060c9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="060c9-116">See also</span></span>

- [<span data-ttu-id="060c9-117">StrongNameKeyInstall, méthode</span><span class="sxs-lookup"><span data-stu-id="060c9-117">StrongNameKeyInstall Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [<span data-ttu-id="060c9-118">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="060c9-118">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
