---
title: StrongNameHashSize, fonction
ms.date: 03/30/2017
api_name:
- StrongNameHashSize
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameHashSize
helpviewer_keywords:
- StrongNameHashSize function [.NET Framework strong naming]
ms.assetid: 738c98d7-a60c-45fe-a296-220af05e6991
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c7e807b502e0905f9ae785203289447c71d25e04
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62041016"
---
# <a name="strongnamehashsize-function"></a><span data-ttu-id="0d436-102">StrongNameHashSize, fonction</span><span class="sxs-lookup"><span data-stu-id="0d436-102">StrongNameHashSize Function</span></span>
<span data-ttu-id="0d436-103">Obtient la taille de mémoire tampon requise pour un hachage, à l’aide de l’algorithme de hachage spécifié.</span><span class="sxs-lookup"><span data-stu-id="0d436-103">Gets the buffer size required for a hash, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="0d436-104">Cette fonction a été déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0d436-104">This function has been deprecated.</span></span> <span data-ttu-id="0d436-105">Utilisez le [ICLRStrongName::StrongNameHashSize](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamehashsize-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="0d436-105">Use the [ICLRStrongName::StrongNameHashSize](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamehashsize-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d436-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d436-106">Syntax</span></span>  
  
```  
BOOLEAN StrongNameHashSize (  
    [in]  ULONG   ulHashAlg,  
    [out] DWORD   *pcbSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0d436-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d436-107">Parameters</span></span>  
 `ulHashAlg`  
 <span data-ttu-id="0d436-108">[in] L’algorithme de hachage utilisé pour calculer la taille du tampon.</span><span class="sxs-lookup"><span data-stu-id="0d436-108">[in] The hash algorithm used to compute the buffer size.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="0d436-109">[out] La taille de la mémoire tampon retournée, en octets.</span><span class="sxs-lookup"><span data-stu-id="0d436-109">[out] The returned buffer size, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0d436-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0d436-110">Return Value</span></span>  
 <span data-ttu-id="0d436-111">`true` de réussite ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="0d436-111">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0d436-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0d436-112">Remarks</span></span>  
 <span data-ttu-id="0d436-113">Si le `StrongNameHashSize` (fonction) ne pas aboutir, appelez le [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) fonction pour récupérer la dernière erreur générée.</span><span class="sxs-lookup"><span data-stu-id="0d436-113">If the `StrongNameHashSize` function does not complete successfully, call the [StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d436-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d436-114">Requirements</span></span>  
 <span data-ttu-id="0d436-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0d436-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d436-116">**En-tête :** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="0d436-116">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="0d436-117">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0d436-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="0d436-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d436-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d436-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d436-119">See also</span></span>

- [<span data-ttu-id="0d436-120">StrongNameHashSize, méthode</span><span class="sxs-lookup"><span data-stu-id="0d436-120">StrongNameHashSize Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamehashsize-method.md)
- [<span data-ttu-id="0d436-121">ICLRStrongName, interface</span><span class="sxs-lookup"><span data-stu-id="0d436-121">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
