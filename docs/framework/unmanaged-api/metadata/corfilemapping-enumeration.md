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
ms.openlocfilehash: a3056836d289383161f9fa538c3c6349f88b6ba6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59175615"
---
# <a name="corfilemapping-enumeration"></a><span data-ttu-id="07517-102">CorFileMapping, énumération</span><span class="sxs-lookup"><span data-stu-id="07517-102">CorFileMapping Enumeration</span></span>
<span data-ttu-id="07517-103">Contient des valeurs qui décrivent le type de mappage de fichier est retourné à partir d’un appel à la [IMetaDataInfo::GetFileMapping](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="07517-103">Contains values that describe the type of file mapping that is returned from a call to the [IMetaDataInfo::GetFileMapping](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07517-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07517-104">Syntax</span></span>  
  
```  
typedef enum CorFileMapping {  
  
    fmFlat                  =   0x0000,  
    fmExecutableImage       =   0x0001  
  
} CorFileMapping;  
```  
  
## <a name="members"></a><span data-ttu-id="07517-105">Membres</span><span class="sxs-lookup"><span data-stu-id="07517-105">Members</span></span>  
  
|<span data-ttu-id="07517-106">Membre</span><span class="sxs-lookup"><span data-stu-id="07517-106">Member</span></span>|<span data-ttu-id="07517-107">Description</span><span class="sxs-lookup"><span data-stu-id="07517-107">Description</span></span>|  
|------------|-----------------|  
|`fmFlat`|<span data-ttu-id="07517-108">Le fichier est mappé comme un fichier de données.</span><span class="sxs-lookup"><span data-stu-id="07517-108">The file is mapped as a data file.</span></span> <span data-ttu-id="07517-109">Autrement dit, le `SEC_IMAGE` indicateur n’a pas été transmis à Microsoft Win32 `CreateFileMapping` (fonction).</span><span class="sxs-lookup"><span data-stu-id="07517-109">That is, the `SEC_IMAGE` flag was not passed to the Microsoft Win32 `CreateFileMapping` function.</span></span>|  
|`fmExecutableImage`|<span data-ttu-id="07517-110">Le fichier est mappé pour l’exécution, en utilisant le `LoadLibrary` (fonction) ou le `CreateFileMapping` fonctionne avec le `SEC_IMAGE` indicateur.</span><span class="sxs-lookup"><span data-stu-id="07517-110">The file is mapped for execution, by using either the `LoadLibrary` function or the `CreateFileMapping` function with the `SEC_IMAGE` flag.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="07517-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07517-111">Requirements</span></span>  
 <span data-ttu-id="07517-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="07517-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="07517-113">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="07517-113">**Header:** CorHdr.h</span></span>  
  
 **<span data-ttu-id="07517-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="07517-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="07517-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07517-115">See also</span></span>

- [<span data-ttu-id="07517-116">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="07517-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
- [<span data-ttu-id="07517-117">GetFileMapping, méthode</span><span class="sxs-lookup"><span data-stu-id="07517-117">GetFileMapping Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatainfo-getfilemapping-method.md)
