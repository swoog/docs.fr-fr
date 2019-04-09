---
title: ICeeGen::AllocateMethodBuffer, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.AllocateMethodBuffer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::AllocateMethodBuffer
helpviewer_keywords:
- AllocateMethodBuffer method [.NET Framework metadata]
- ICeeGen::AllocateMethodBuffer method [.NET Framework metadata]
ms.assetid: 845ab77e-9639-47f5-99fb-f3b619e3e779
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7be1bd2934fbb2e09a39c3042fa9ae314e89d629
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59083762"
---
# <a name="iceegenallocatemethodbuffer-method"></a><span data-ttu-id="152d5-102">ICeeGen::AllocateMethodBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="152d5-102">ICeeGen::AllocateMethodBuffer Method</span></span>
<span data-ttu-id="152d5-103">Crée une mémoire tampon de la taille spécifiée pour une méthode et obtient l’adresse virtuelle relative de la méthode.</span><span class="sxs-lookup"><span data-stu-id="152d5-103">Creates a buffer of the specified size for a method, and gets the relative virtual address of the method.</span></span>  
  
 <span data-ttu-id="152d5-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="152d5-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="152d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="152d5-105">Syntax</span></span>  
  
```  
HRESULT AllocateMethodBuffer (   
    [in]  ULONG    cchBuffer,   
    [out] UCHAR    **lpBuffer,  
    [out] ULONG    *RVA  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="152d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="152d5-106">Parameters</span></span>  
 `cchBuffer`  
 <span data-ttu-id="152d5-107">[in] La longueur de la mémoire tampon à créer.</span><span class="sxs-lookup"><span data-stu-id="152d5-107">[in] The length of the buffer to create.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="152d5-108">[out] La mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="152d5-108">[out] The returned buffer.</span></span>  
  
 `RVA`  
 <span data-ttu-id="152d5-109">[out] L’adresse virtuelle relative de la méthode.</span><span class="sxs-lookup"><span data-stu-id="152d5-109">[out] The relative virtual address of the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="152d5-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="152d5-110">Requirements</span></span>  
 <span data-ttu-id="152d5-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="152d5-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="152d5-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="152d5-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="152d5-113">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="152d5-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="152d5-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="152d5-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="152d5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="152d5-115">See also</span></span>

- [<span data-ttu-id="152d5-116">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="152d5-116">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
