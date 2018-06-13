---
title: ICeeGen::GetSectionDataLen, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionDataLen
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionDataLen
helpviewer_keywords:
- ICeeGen::GetSectionDataLen method [.NET Framework metadata]
- GetSectionDataLen method [.NET Framework metadata]
ms.assetid: e2a06ee4-b8ee-49c7-935a-c1031a29eef2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b85cdee4a65e91c51fdb014bdcc4797b99214daf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33446129"
---
# <a name="iceegengetsectiondatalen-method"></a><span data-ttu-id="6c16b-102">ICeeGen::GetSectionDataLen, méthode</span><span class="sxs-lookup"><span data-stu-id="6c16b-102">ICeeGen::GetSectionDataLen Method</span></span>
<span data-ttu-id="6c16b-103">Obtient la longueur de la section spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6c16b-103">Gets the length of the specified section.</span></span>  
  
 <span data-ttu-id="6c16b-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="6c16b-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6c16b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c16b-105">Syntax</span></span>  
  
```  
HRESULT GetSectionDataLen (  
    [in]  HCEESECTION  section,  
    [out] ULONG        *dataLen  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6c16b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c16b-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="6c16b-107">[in] La section de données dont la longueur sera récupérée.</span><span class="sxs-lookup"><span data-stu-id="6c16b-107">[in] The data section whose length will be retrieved.</span></span>  
  
 `dataLen`  
 <span data-ttu-id="6c16b-108">[out] La longueur retournée de la section spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6c16b-108">[out] The returned length of the specified section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6c16b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="6c16b-109">Remarks</span></span>  
 <span data-ttu-id="6c16b-110">Appelez `GetSectionDataLen` uniquement si vous avez des exigences de section spéciale qui ne sont pas gérés par d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="6c16b-110">Call `GetSectionDataLen` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6c16b-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6c16b-111">Requirements</span></span>  
 <span data-ttu-id="6c16b-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6c16b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6c16b-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="6c16b-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6c16b-114">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6c16b-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6c16b-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6c16b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c16b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c16b-116">See Also</span></span>  
 [<span data-ttu-id="6c16b-117">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="6c16b-117">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
