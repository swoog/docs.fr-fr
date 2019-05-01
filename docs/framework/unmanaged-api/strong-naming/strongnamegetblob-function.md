---
title: StrongNameGetBlob, fonction
ms.date: 03/30/2017
api_name:
- StrongNameGetBlob
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameGetBlob
helpviewer_keywords:
- StrongNameGetBlob function [.NET Framework strong naming]
ms.assetid: 15d09166-be00-4696-913f-2c1fbc7ac2e1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e23232b55a841672ee193b980c310995ba688e00
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049360"
---
# <a name="strongnamegetblob-function"></a><span data-ttu-id="7b1dd-102">StrongNameGetBlob, fonction</span><span class="sxs-lookup"><span data-stu-id="7b1dd-102">StrongNameGetBlob Function</span></span>
<span data-ttu-id="7b1dd-103">Remplit la mémoire tampon spécifiée avec la représentation binaire du fichier exécutable à l’adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-103">Fills the specified buffer with the binary representation of the executable file at the specified address.</span></span>  
  
 <span data-ttu-id="7b1dd-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-104">This function has been deprecated.</span></span> <span data-ttu-id="7b1dd-105">Utilisez le [ICLRStrongName::StrongNameGetBLob](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblob-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-105">Use the [ICLRStrongName::StrongNameGetBLob](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblob-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b1dd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b1dd-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameGetBlob (  
    [in]  LPCWSTR    wszFilePath,  
    [in]  BYTE       *pbBlob,  
    [in, out] DWORD  *pcbBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7b1dd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b1dd-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="7b1dd-108">[in] Un chemin d’accès valide au fichier exécutable à charger.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-108">[in] A valid path to the executable file to be loaded.</span></span>  
  
 `pbBlob`  
 <span data-ttu-id="7b1dd-109">[in] La mémoire tampon dans laquelle charger le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-109">[in] The buffer into which to load the executable file.</span></span>  
  
 `pcbBlob`  
 <span data-ttu-id="7b1dd-110">[in, out] La taille maximale en octets, demandée de `pbBlob`.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-110">[in, out] The requested maximum size, in bytes, of `pbBlob`.</span></span> <span data-ttu-id="7b1dd-111">Au retour, la taille réelle, en octets, de `pbBlob`.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-111">Upon return, the actual size, in bytes, of `pbBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7b1dd-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7b1dd-112">Return Value</span></span>  
 <span data-ttu-id="7b1dd-113">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-113">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7b1dd-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7b1dd-114">Remarks</span></span>  
 <span data-ttu-id="7b1dd-115">Si le `StrongNameGetBlob` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="7b1dd-115">If the `StrongNameGetBlob` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b1dd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b1dd-116">Requirements</span></span>  
 <span data-ttu-id="7b1dd-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7b1dd-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b1dd-118">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="7b1dd-118">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="7b1dd-119">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7b1dd-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7b1dd-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b1dd-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b1dd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b1dd-121">See also</span></span>

- [<span data-ttu-id="7b1dd-122">StrongNameGetBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="7b1dd-122">StrongNameGetBlob Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblob-method.md)
- [<span data-ttu-id="7b1dd-123">StrongNameGetBlobFromImage, méthode</span><span class="sxs-lookup"><span data-stu-id="7b1dd-123">StrongNameGetBlobFromImage Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md)
- [<span data-ttu-id="7b1dd-124">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="7b1dd-124">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
