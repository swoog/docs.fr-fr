---
title: SetAssemblyFile, méthode
ms.date: 03/30/2017
api_name:
- IALink.SetAssemblyFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetAssemblyFile
helpviewer_keywords:
- SetAssemblyFile method
ms.assetid: 3a912787-f139-43ca-a841-8bbda3107ecf
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 006360203518f74adb964634af52505a71d51473
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54587097"
---
# <a name="setassemblyfile-method"></a><span data-ttu-id="3f372-102">SetAssemblyFile, méthode</span><span class="sxs-lookup"><span data-stu-id="3f372-102">SetAssemblyFile Method</span></span>
<span data-ttu-id="3f372-103">Attribue le nom de l’assembly à générer.</span><span class="sxs-lookup"><span data-stu-id="3f372-103">Assigns the name of the assembly to be built.</span></span> <span data-ttu-id="3f372-104">Non pour être utilisés lors de la production de modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="3f372-104">Not for use when producing unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f372-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f372-105">Syntax</span></span>  
  
```  
HRESULT SetAssemblyFile(  
    LPCWSTR pszFilename,  
    IMetaDataEmit* pEmitter,  
    AssemblyFlags afFlags,  
    mdAssembly* pAssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3f372-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f372-106">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="3f372-107">Nom qualifié complet du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="3f372-107">Fully qualified name of the manifest file.</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="3f372-108">Pointeur vers [IMetaDataEmit (Interface)](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="3f372-108">Pointer to [IMetaDataEmit Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface.</span></span>  
  
 `afFlags`  
 <span data-ttu-id="3f372-109">Indicateurs tel que défini dans [AssemblyFlags, énumération](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="3f372-109">Flags as defined in [AssemblyFlags Enumeration](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span></span>  
  
 `pAssemblyID`  
 <span data-ttu-id="3f372-110">Pointeur vers l’ID de l’assembly résultant.</span><span class="sxs-lookup"><span data-stu-id="3f372-110">Pointer to ID of resulting assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3f372-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3f372-111">Return Value</span></span>  
 <span data-ttu-id="3f372-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="3f372-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f372-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f372-113">Requirements</span></span>  
 <span data-ttu-id="3f372-114">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="3f372-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f372-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f372-115">See also</span></span>
- [<span data-ttu-id="3f372-116">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="3f372-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="3f372-117">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="3f372-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="3f372-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="3f372-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
