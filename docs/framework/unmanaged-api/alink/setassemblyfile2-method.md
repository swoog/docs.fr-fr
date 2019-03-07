---
title: SetAssemblyFile2, méthode
ms.date: 03/30/2017
api_name:
- IALink2.SetAssemblyFile2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetAssemblyFile2
helpviewer_keywords:
- SetAssemblyFile2 method
ms.assetid: eedb9125-1ef1-4000-abfc-7de86e5a1f17
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 41e10855a7254da4124ac0bf9aa247b90311632b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57479076"
---
# <a name="setassemblyfile2-method"></a><span data-ttu-id="fae74-102">SetAssemblyFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="fae74-102">SetAssemblyFile2 Method</span></span>
<span data-ttu-id="fae74-103">Définit le nom et les options pour un nouvel assembly.</span><span class="sxs-lookup"><span data-stu-id="fae74-103">Sets the name of and options for a new assembly.</span></span> <span data-ttu-id="fae74-104">N’appelez pas cette méthode lorsque vous générez des modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="fae74-104">Do not call this method when you produce unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fae74-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fae74-105">Syntax</span></span>  
  
```  
HRESULT SetAssemblyFile2(  
    LPCWSTR pszFilename,  
    IMetaDataEmit2* pEmitter,  
    AssemblyFlags   afFlags,  
    mdAssembly* pAssemblyID  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="fae74-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fae74-106">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="fae74-107">Nom du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="fae74-107">Name of manifest file.</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="fae74-108">[IMetaDataEmit2, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface pour ce fichier.</span><span class="sxs-lookup"><span data-stu-id="fae74-108">[IMetaDataEmit2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface for this file.</span></span>  
  
 `afFlags`  
 <span data-ttu-id="fae74-109">Les options représentées par [AssemblyFlags, énumération](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="fae74-109">Options represented by [AssemblyFlags Enumeration](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span></span>  
  
 `pAssemblyID`  
 <span data-ttu-id="fae74-110">Reçoit l’ID unique pour l’assembly en cours de construction.</span><span class="sxs-lookup"><span data-stu-id="fae74-110">Receives unique ID for the assembly being constructed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fae74-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fae74-111">Return Value</span></span>  
 <span data-ttu-id="fae74-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="fae74-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fae74-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fae74-113">Requirements</span></span>  
 <span data-ttu-id="fae74-114">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="fae74-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fae74-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fae74-115">See also</span></span>
- [<span data-ttu-id="fae74-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="fae74-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="fae74-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="fae74-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="fae74-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="fae74-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
