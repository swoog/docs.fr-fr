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
ms.openlocfilehash: 0cf1bfa03fd14d6324af60781003a8072a267a7e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045056"
---
# <a name="couninitiee-enumeration"></a><span data-ttu-id="9faff-102">COUNINITIEE, énumération</span><span class="sxs-lookup"><span data-stu-id="9faff-102">COUNINITIEE Enumeration</span></span>
<span data-ttu-id="9faff-103">Spécifie les constantes utilisées par [CoUninitializeEE](../../../../docs/framework/unmanaged-api/hosting/couninitializeee-function.md) lors de l’initialisation du common language runtime.</span><span class="sxs-lookup"><span data-stu-id="9faff-103">Specifies constants used by [CoUninitializeEE](../../../../docs/framework/unmanaged-api/hosting/couninitializeee-function.md) when initializing the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9faff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9faff-104">Syntax</span></span>  
  
```  
typedef enum tagCOUNINITEE  
{  
    COUNINITEE_DEFAULT  = 0x0,   
    COUNINITEE_DLL      = 0x1  
} COUNINITIEE;  
```  
  
## <a name="members"></a><span data-ttu-id="9faff-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9faff-105">Members</span></span>  
  
|<span data-ttu-id="9faff-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9faff-106">Member</span></span>|<span data-ttu-id="9faff-107">Description</span><span class="sxs-lookup"><span data-stu-id="9faff-107">Description</span></span>|  
|------------|-----------------|  
|`COUNINITEE_DEFAULT`|<span data-ttu-id="9faff-108">Indique le mode de désinitialisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="9faff-108">Indicates default uninitialization mode.</span></span>|  
|`COUNINITEE_DLL`|<span data-ttu-id="9faff-109">Indique le mode de désinitialisation pour décharger un assembly.</span><span class="sxs-lookup"><span data-stu-id="9faff-109">Indicates uninitialization mode for unloading an assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9faff-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9faff-110">Requirements</span></span>  
 <span data-ttu-id="9faff-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9faff-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9faff-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="9faff-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9faff-113">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9faff-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9faff-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9faff-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9faff-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9faff-115">See also</span></span>

- [<span data-ttu-id="9faff-116">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9faff-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
