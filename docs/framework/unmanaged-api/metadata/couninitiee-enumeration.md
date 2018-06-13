---
title: COUNINITIEE, énumération
ms.date: 03/30/2017
api_name:
- COUNINITIEE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COUNINITIEE
helpviewer_keywords:
- COUNINITIEE enumeration [.NET Framework metadata]
ms.assetid: c42baa79-f469-4330-95a2-baf7f021c2fc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dcd7dc7c51caa94308760c0086384c8eea184ee9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443595"
---
# <a name="couninitiee-enumeration"></a><span data-ttu-id="9cd39-102">COUNINITIEE, énumération</span><span class="sxs-lookup"><span data-stu-id="9cd39-102">COUNINITIEE Enumeration</span></span>
<span data-ttu-id="9cd39-103">Spécifie les constantes utilisées par [CoUninitializeEE](../../../../docs/framework/unmanaged-api/hosting/couninitializeee-function.md) lors de l’initialisation du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="9cd39-103">Specifies constants used by [CoUninitializeEE](../../../../docs/framework/unmanaged-api/hosting/couninitializeee-function.md) when initializing the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9cd39-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cd39-104">Syntax</span></span>  
  
```  
typedef enum tagCOUNINITEE  
{  
    COUNINITEE_DEFAULT  = 0x0,   
    COUNINITEE_DLL      = 0x1  
} COUNINITIEE;  
```  
  
## <a name="members"></a><span data-ttu-id="9cd39-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9cd39-105">Members</span></span>  
  
|<span data-ttu-id="9cd39-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9cd39-106">Member</span></span>|<span data-ttu-id="9cd39-107">Description</span><span class="sxs-lookup"><span data-stu-id="9cd39-107">Description</span></span>|  
|------------|-----------------|  
|`COUNINITEE_DEFAULT`|<span data-ttu-id="9cd39-108">Indique le mode de désinitialisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="9cd39-108">Indicates default uninitialization mode.</span></span>|  
|`COUNINITEE_DLL`|<span data-ttu-id="9cd39-109">Indique le mode de désinitialisation pour décharger un assembly.</span><span class="sxs-lookup"><span data-stu-id="9cd39-109">Indicates uninitialization mode for unloading an assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9cd39-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9cd39-110">Requirements</span></span>  
 <span data-ttu-id="9cd39-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9cd39-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9cd39-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9cd39-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9cd39-113">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9cd39-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9cd39-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9cd39-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9cd39-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cd39-115">See Also</span></span>  
 [<span data-ttu-id="9cd39-116">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9cd39-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
