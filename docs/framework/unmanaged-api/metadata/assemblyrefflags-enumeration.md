---
title: AssemblyRefFlags, énumération
ms.date: 03/30/2017
api_name:
- AssemblyRefFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyRefFlags
helpviewer_keywords:
- AssemblyRefFlags enumeration [.NET Framework metadata]
ms.assetid: decd4f46-f3b2-466f-9501-e74f2b86b846
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: de120516655c1a0578e88ecc2890701ed9fc2f6d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443698"
---
# <a name="assemblyrefflags-enumeration"></a><span data-ttu-id="a7b59-102">AssemblyRefFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="a7b59-102">AssemblyRefFlags Enumeration</span></span>
<span data-ttu-id="a7b59-103">Contient des valeurs qui décrivent les fonctionnalités d’une référence d’assembly.</span><span class="sxs-lookup"><span data-stu-id="a7b59-103">Contains values that describe features of an assembly reference.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7b59-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7b59-104">Syntax</span></span>  
  
```  
typedef enum {  
    arfFullOriginator = 0x0001  
} AssemblyRefFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="a7b59-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a7b59-105">Members</span></span>  
  
|<span data-ttu-id="a7b59-106">Membre</span><span class="sxs-lookup"><span data-stu-id="a7b59-106">Member</span></span>|<span data-ttu-id="a7b59-107">Description</span><span class="sxs-lookup"><span data-stu-id="a7b59-107">Description</span></span>|  
|------------|-----------------|  
|`arfFullOriginator`|<span data-ttu-id="a7b59-108">Spécifie que la référence d’assembly contient des informations complètes non hachées sur le serveur de publication de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a7b59-108">Specifies that the assembly reference contains full, unhashed information about the publisher of the assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a7b59-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a7b59-109">Requirements</span></span>  
 <span data-ttu-id="a7b59-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a7b59-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a7b59-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a7b59-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a7b59-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a7b59-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7b59-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7b59-113">See Also</span></span>  
 [<span data-ttu-id="a7b59-114">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="a7b59-114">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)  
 [<span data-ttu-id="a7b59-115">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="a7b59-115">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)  
 [<span data-ttu-id="a7b59-116">DefineAssemblyRef, méthode</span><span class="sxs-lookup"><span data-stu-id="a7b59-116">DefineAssemblyRef Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md)
