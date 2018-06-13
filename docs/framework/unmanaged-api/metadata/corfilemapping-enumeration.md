---
title: CorFileMapping, énumération
ms.date: 03/30/2017
api_name:
- CorFileMapping
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFileMapping
helpviewer_keywords:
- CorFileMapping enumeration [.NET Framework metadata]
ms.assetid: 3ca41592-b8da-475a-8032-a15627730003
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3c8864aa604b0483130eac5aa0d7c0640abbac99
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443721"
---
# <a name="corfilemapping-enumeration"></a><span data-ttu-id="053a9-102">CorFileMapping, énumération</span><span class="sxs-lookup"><span data-stu-id="053a9-102">CorFileMapping Enumeration</span></span>
<span data-ttu-id="053a9-103">Contient des valeurs qui décrivent le type de mappage de fichier retourné par un appel à la [IMetaDataInfo::GetFileMapping](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="053a9-103">Contains values that describe the type of file mapping that is returned from a call to the [IMetaDataInfo::GetFileMapping](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="053a9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="053a9-104">Syntax</span></span>  
  
```  
typedef enum CorFileMapping {  
  
    fmFlat                  =   0x0000,  
    fmExecutableImage       =   0x0001  
  
} CorFileMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="053a9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="053a9-105">Members</span></span>  
  
|<span data-ttu-id="053a9-106">Membre</span><span class="sxs-lookup"><span data-stu-id="053a9-106">Member</span></span>|<span data-ttu-id="053a9-107">Description</span><span class="sxs-lookup"><span data-stu-id="053a9-107">Description</span></span>|  
|------------|-----------------|  
|`fmFlat`|<span data-ttu-id="053a9-108">Le fichier est mappé comme un fichier de données.</span><span class="sxs-lookup"><span data-stu-id="053a9-108">The file is mapped as a data file.</span></span> <span data-ttu-id="053a9-109">Autrement dit, le `SEC_IMAGE` indicateur n’a pas été transmis à Microsoft Win32 `CreateFileMapping` (fonction).</span><span class="sxs-lookup"><span data-stu-id="053a9-109">That is, the `SEC_IMAGE` flag was not passed to the Microsoft Win32 `CreateFileMapping` function.</span></span>|  
|`fmExecutableImage`|<span data-ttu-id="053a9-110">Le fichier est mappé pour l’exécution, en utilisant le `LoadLibrary` (fonction) ou le `CreateFileMapping` fonctionne avec le `SEC_IMAGE` indicateur.</span><span class="sxs-lookup"><span data-stu-id="053a9-110">The file is mapped for execution, by using either the `LoadLibrary` function or the `CreateFileMapping` function with the `SEC_IMAGE` flag.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="053a9-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="053a9-111">Requirements</span></span>  
 <span data-ttu-id="053a9-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="053a9-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="053a9-113">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="053a9-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="053a9-114">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="053a9-114">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="053a9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="053a9-115">See Also</span></span>  
 [<span data-ttu-id="053a9-116">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="053a9-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)  
 [<span data-ttu-id="053a9-117">GetFileMapping, méthode</span><span class="sxs-lookup"><span data-stu-id="053a9-117">GetFileMapping Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md)
