---
title: ICeeGen::GetIlSection, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.GetIlSection
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetIlSection
helpviewer_keywords:
- GetIlSection method [.NET Framework metadata]
- ICeeGen::GetIlSection method [.NET Framework metadata]
ms.assetid: 6f2db2ca-203f-4ac3-9530-208642ca385e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6025b5914d4e96d10d83fc47a6baea7aa09605d6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445142"
---
# <a name="iceegengetilsection-method"></a><span data-ttu-id="711e6-102">ICeeGen::GetIlSection, méthode</span><span class="sxs-lookup"><span data-stu-id="711e6-102">ICeeGen::GetIlSection Method</span></span>
<span data-ttu-id="711e6-103">Obtient la section de la base de code de langage intermédiaire référencée par le handle spécifié.</span><span class="sxs-lookup"><span data-stu-id="711e6-103">Gets the section of the intermediate language code base referenced by the specified handle.</span></span>  
  
 <span data-ttu-id="711e6-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="711e6-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="711e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="711e6-105">Syntax</span></span>  
  
```  
HRESULT GetIlSection (  
    [in] HCEESECTION  *section  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="711e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="711e6-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="711e6-107">[in] Descripteur de la section à obtenir.</span><span class="sxs-lookup"><span data-stu-id="711e6-107">[in] The handle to the section to get.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="711e6-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="711e6-108">Requirements</span></span>  
 <span data-ttu-id="711e6-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="711e6-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="711e6-110">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="711e6-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="711e6-111">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="711e6-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="711e6-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="711e6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="711e6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="711e6-113">See Also</span></span>  
 [<span data-ttu-id="711e6-114">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="711e6-114">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
