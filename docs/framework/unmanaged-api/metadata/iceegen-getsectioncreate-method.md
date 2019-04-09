---
title: ICeeGen::GetSectionCreate, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionCreate
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionCreate
helpviewer_keywords:
- ICeeGen::GetSectionCreate method [.NET Framework metadata]
- GetSectionCreate method [.NET Framework metadata]
ms.assetid: 154b2460-59ce-4874-a9f2-1b3353486ac5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9768dfd43b6b60df1660c48cb6d6f498b049e256
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59103309"
---
# <a name="iceegengetsectioncreate-method"></a><span data-ttu-id="c54b8-102">ICeeGen::GetSectionCreate, méthode</span><span class="sxs-lookup"><span data-stu-id="c54b8-102">ICeeGen::GetSectionCreate Method</span></span>
<span data-ttu-id="c54b8-103">Génère et obtient une section de code utilisant le nom spécifié et les valeurs d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="c54b8-103">Generates and gets a code section using the specified name and flag values.</span></span>  
  
 <span data-ttu-id="c54b8-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c54b8-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c54b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c54b8-105">Syntax</span></span>  
  
```  
HRESULT GetSectionCreate (  
    [in]  const char     *name,  
    [in]  DWORD          flags,  
    [out] HCEESECTION    *section  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c54b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c54b8-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="c54b8-107">[in] Un pointeur vers une chaîne qui spécifie le nom de la section doit être créé.</span><span class="sxs-lookup"><span data-stu-id="c54b8-107">[in] A pointer to a string that specifies the name of the section to be created.</span></span>  
  
 `flags`  
 <span data-ttu-id="c54b8-108">[in] Indicateurs qui spécifient des options.</span><span class="sxs-lookup"><span data-stu-id="c54b8-108">[in] Flags that specify options.</span></span>  
  
 `section`  
 <span data-ttu-id="c54b8-109">[out] Pointeur vers la section de code nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="c54b8-109">[out] A pointer to the newly created code section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c54b8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c54b8-110">Remarks</span></span>  
 <span data-ttu-id="c54b8-111">Appelez `GetSectionCreate` uniquement si vous avez des exigences de section spéciale qui ne sont pas gérées par d’autres méthodes.</span><span class="sxs-lookup"><span data-stu-id="c54b8-111">Call `GetSectionCreate` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c54b8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c54b8-112">Requirements</span></span>  
 <span data-ttu-id="c54b8-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c54b8-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c54b8-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c54b8-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c54b8-115">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c54b8-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="c54b8-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c54b8-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c54b8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c54b8-117">See also</span></span>

- [<span data-ttu-id="c54b8-118">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="c54b8-118">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
