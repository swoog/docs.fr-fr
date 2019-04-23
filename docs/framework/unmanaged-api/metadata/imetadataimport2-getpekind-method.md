---
title: IMetaDataImport2::GetPEKind, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetPEKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetPEKind
helpviewer_keywords:
- GetPEKind method [.NET Framework metadata]
- IMetaDataImport2::GetPEKind method [.NET Framework metadata]
ms.assetid: d91c3d89-8022-4a4c-a2a2-a8af2c387507
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d9dda1fb38546138d52b5fe61754d5497e676c37
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59113478"
---
# <a name="imetadataimport2getpekind-method"></a><span data-ttu-id="87fa9-102">IMetaDataImport2::GetPEKind, méthode</span><span class="sxs-lookup"><span data-stu-id="87fa9-102">IMetaDataImport2::GetPEKind Method</span></span>
<span data-ttu-id="87fa9-103">Obtient une valeur qui identifie la nature du code dans le fichier exécutable portable (PE) de fichiers, en général, un fichier DLL ou EXE, qui est défini dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="87fa9-103">Gets a value identifying the nature of the code in the portable executable (PE) file, typically a DLL or EXE file, that is defined in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87fa9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87fa9-104">Syntax</span></span>  
  
```  
HRESULT GetPEKind (  
   [out] DWORD *pdwPEKind,  
   [out] DWORD *pdwMachine  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="87fa9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87fa9-105">Parameters</span></span>  
 `pdwPEKind`  
 <span data-ttu-id="87fa9-106">[out] Un pointeur vers une valeur de la [CorPEKind](../../../../docs/framework/unmanaged-api/metadata/corpekind-enumeration.md) énumération qui décrit le fichier PE.</span><span class="sxs-lookup"><span data-stu-id="87fa9-106">[out] A pointer to a value of the [CorPEKind](../../../../docs/framework/unmanaged-api/metadata/corpekind-enumeration.md) enumeration that describes the PE file.</span></span>  
  
 `pdwMachine`  
 <span data-ttu-id="87fa9-107">[out] Pointeur vers une valeur qui identifie l’architecture de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="87fa9-107">[out] A pointer to a value that identifies the architecture of the machine.</span></span> <span data-ttu-id="87fa9-108">Consultez la section suivante pour les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="87fa9-108">See the next section for possible values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="87fa9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="87fa9-109">Remarks</span></span>  
 <span data-ttu-id="87fa9-110">La valeur référencée par le `pdwMachine` paramètre peut prendre l’une des opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="87fa9-110">The value referenced by the `pdwMachine` parameter can be one of the following.</span></span>  
  
|<span data-ttu-id="87fa9-111">Value</span><span class="sxs-lookup"><span data-stu-id="87fa9-111">Value</span></span>|<span data-ttu-id="87fa9-112">Architecture de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="87fa9-112">Machine architecture</span></span>|  
|-----------|--------------------------|  
|<span data-ttu-id="87fa9-113">IMAGE_FILE_MACHINE_I386</span><span class="sxs-lookup"><span data-stu-id="87fa9-113">IMAGE_FILE_MACHINE_I386</span></span><br /><br /> <span data-ttu-id="87fa9-114">0x014C</span><span class="sxs-lookup"><span data-stu-id="87fa9-114">0x014C</span></span>|<span data-ttu-id="87fa9-115">x86</span><span class="sxs-lookup"><span data-stu-id="87fa9-115">x86</span></span>|  
|<span data-ttu-id="87fa9-116">IMAGE_FILE_MACHINE_IA64</span><span class="sxs-lookup"><span data-stu-id="87fa9-116">IMAGE_FILE_MACHINE_IA64</span></span><br /><br /> <span data-ttu-id="87fa9-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="87fa9-117">0x0200</span></span>|<span data-ttu-id="87fa9-118">Intel IPF</span><span class="sxs-lookup"><span data-stu-id="87fa9-118">Intel IPF</span></span>|  
|<span data-ttu-id="87fa9-119">IMAGE_FILE_MACHINE_AMD64</span><span class="sxs-lookup"><span data-stu-id="87fa9-119">IMAGE_FILE_MACHINE_AMD64</span></span><br /><br /> <span data-ttu-id="87fa9-120">0x8664</span><span class="sxs-lookup"><span data-stu-id="87fa9-120">0x8664</span></span>|<span data-ttu-id="87fa9-121">X64</span><span class="sxs-lookup"><span data-stu-id="87fa9-121">x64</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="87fa9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87fa9-122">Requirements</span></span>  
 <span data-ttu-id="87fa9-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="87fa9-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="87fa9-124">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="87fa9-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="87fa9-125">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="87fa9-125">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="87fa9-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="87fa9-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87fa9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87fa9-127">See also</span></span>

- [<span data-ttu-id="87fa9-128">IMetaDataImport2, interface</span><span class="sxs-lookup"><span data-stu-id="87fa9-128">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
- [<span data-ttu-id="87fa9-129">IMetaDataImport, interface</span><span class="sxs-lookup"><span data-stu-id="87fa9-129">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [<span data-ttu-id="87fa9-130">CorPEKind, énumération</span><span class="sxs-lookup"><span data-stu-id="87fa9-130">CorPEKind Enumeration</span></span>](../../../../docs/framework/unmanaged-api/metadata/corpekind-enumeration.md)
