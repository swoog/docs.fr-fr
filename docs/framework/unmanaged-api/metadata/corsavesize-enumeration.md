---
title: CorSaveSize, énumération
ms.date: 03/30/2017
api_name:
- CorSaveSize
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSaveSize
helpviewer_keywords:
- CorSaveSize enumeration [.NET Framework metadata]
ms.assetid: eb95ce39-5688-43c1-a34d-578794b32faa
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bc36468a2016822e884ec3a36a23c75477a00a2d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59217196"
---
# <a name="corsavesize-enumeration"></a><span data-ttu-id="9f54a-102">CorSaveSize, énumération</span><span class="sxs-lookup"><span data-stu-id="9f54a-102">CorSaveSize Enumeration</span></span>
<span data-ttu-id="9f54a-103">Contient des valeurs indiquant le niveau de précision requis lors de l'interrogation de la taille d'une opération d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9f54a-103">Contains values indicating the level of precision required when querying for the size of a save operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f54a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f54a-104">Syntax</span></span>  
  
```  
typedef enum CorSaveSize {  
    cssAccurate                = 0x0000,   
    cssQuick                   = 0x0001,   
    cssDiscardTransientCAs     = 0x0002  
} CorSaveSize;  
```  
  
## <a name="members"></a><span data-ttu-id="9f54a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9f54a-105">Members</span></span>  
  
|<span data-ttu-id="9f54a-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9f54a-106">Member</span></span>|<span data-ttu-id="9f54a-107">Description</span><span class="sxs-lookup"><span data-stu-id="9f54a-107">Description</span></span>|  
|------------|-----------------|  
|`cssAccurate`|<span data-ttu-id="9f54a-108">Spécifie que la valeur de retour doit être exacte.</span><span class="sxs-lookup"><span data-stu-id="9f54a-108">Specifies that the return value should be exact.</span></span>|  
|`cssQuick`|<span data-ttu-id="9f54a-109">Spécifie que la valeur de retour doit être estimée.</span><span class="sxs-lookup"><span data-stu-id="9f54a-109">Specifies that the return value should be estimated.</span></span>|  
|`cssDiscardTransientCAs`|<span data-ttu-id="9f54a-110">Spécifie que les types pouvant être éliminées doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="9f54a-110">Specifies that discardable types should be removed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9f54a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f54a-111">Requirements</span></span>  
 <span data-ttu-id="9f54a-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9f54a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f54a-113">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="9f54a-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="9f54a-114">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9f54a-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9f54a-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f54a-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f54a-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f54a-116">See also</span></span>

- [<span data-ttu-id="9f54a-117">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="9f54a-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
