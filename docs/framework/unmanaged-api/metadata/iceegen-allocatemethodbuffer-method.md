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
ms.openlocfilehash: f56376d4400f4e24aefe2d1e5d4ad504b1d281cf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446002"
---
# <a name="iceegenallocatemethodbuffer-method"></a><span data-ttu-id="06b42-102">ICeeGen::AllocateMethodBuffer, méthode</span><span class="sxs-lookup"><span data-stu-id="06b42-102">ICeeGen::AllocateMethodBuffer Method</span></span>
<span data-ttu-id="06b42-103">Crée une mémoire tampon de la taille spécifiée pour une méthode et obtient l’adresse virtuelle relative de la méthode.</span><span class="sxs-lookup"><span data-stu-id="06b42-103">Creates a buffer of the specified size for a method, and gets the relative virtual address of the method.</span></span>  
  
 <span data-ttu-id="06b42-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="06b42-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06b42-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06b42-105">Syntax</span></span>  
  
```  
HRESULT AllocateMethodBuffer (   
    [in]  ULONG    cchBuffer,   
    [out] UCHAR    **lpBuffer,  
    [out] ULONG    *RVA  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="06b42-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06b42-106">Parameters</span></span>  
 `cchBuffer`  
 <span data-ttu-id="06b42-107">[in] La longueur de la mémoire tampon à créer.</span><span class="sxs-lookup"><span data-stu-id="06b42-107">[in] The length of the buffer to create.</span></span>  
  
 `lpBuffer`  
 <span data-ttu-id="06b42-108">[out] La mémoire tampon retournée.</span><span class="sxs-lookup"><span data-stu-id="06b42-108">[out] The returned buffer.</span></span>  
  
 `RVA`  
 <span data-ttu-id="06b42-109">[out] L’adresse virtuelle relative de la méthode.</span><span class="sxs-lookup"><span data-stu-id="06b42-109">[out] The relative virtual address of the method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="06b42-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="06b42-110">Requirements</span></span>  
 <span data-ttu-id="06b42-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="06b42-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06b42-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="06b42-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="06b42-113">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="06b42-113">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="06b42-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="06b42-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06b42-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06b42-115">See Also</span></span>  
 [<span data-ttu-id="06b42-116">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="06b42-116">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
