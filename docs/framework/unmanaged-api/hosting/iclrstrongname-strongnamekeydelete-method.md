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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59143986"
---
# <a name="iclrstrongnamestrongnamekeydelete-method"></a><span data-ttu-id="a0fcb-102">Méthode ICLRStrongName::StrongNameKeyDelete</span><span class="sxs-lookup"><span data-stu-id="a0fcb-102">ICLRStrongName::StrongNameKeyDelete Method</span></span>
<span data-ttu-id="a0fcb-103">Supprime le conteneur de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="a0fcb-103">Deletes the specified key container.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a0fcb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0fcb-104">Syntax</span></span>  
  
```  
HRESULT StrongNameKeyDelete (  
    [in]  LPCWSTR   wszKeyContainer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a0fcb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0fcb-105">Parameters</span></span>  
 `wszKeyContainer`  
 <span data-ttu-id="a0fcb-106">[in] Le nom du conteneur de clé à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a0fcb-106">[in] The name of the key container to delete.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a0fcb-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a0fcb-107">Return Value</span></span>  
 `S_OK` <span data-ttu-id="a0fcb-108">Si la méthode a réussi ; Sinon, une valeur HRESULT qui indique un échec (consultez [valeurs HRESULT courantes](https://go.microsoft.com/fwlink/?LinkId=213878) pour obtenir la liste).</span><span class="sxs-lookup"><span data-stu-id="a0fcb-108">if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a0fcb-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a0fcb-109">Remarks</span></span>  
 <span data-ttu-id="a0fcb-110">Utilisez le [ICLRStrongName::StrongNameKeyInstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) méthode pour importer une paire de clés publique/privée dans un conteneur.</span><span class="sxs-lookup"><span data-stu-id="a0fcb-110">Use the [ICLRStrongName::StrongNameKeyInstall](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md) method to import a public/private key pair into a container.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a0fcb-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0fcb-111">Requirements</span></span>  
 <span data-ttu-id="a0fcb-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a0fcb-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a0fcb-113">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="a0fcb-113">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a0fcb-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a0fcb-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="a0fcb-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a0fcb-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a0fcb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0fcb-116">See also</span></span>

- [<span data-ttu-id="a0fcb-117">StrongNameKeyInstall, méthode</span><span class="sxs-lookup"><span data-stu-id="a0fcb-117">StrongNameKeyInstall Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamekeyinstall-method.md)
- [<span data-ttu-id="a0fcb-118">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="a0fcb-118">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
