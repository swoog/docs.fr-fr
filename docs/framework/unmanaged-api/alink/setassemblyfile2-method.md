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
ms.openlocfilehash: 3882998d3155b49251fbe091b72ef11022ebfd2b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54540206"
---
# <a name="setassemblyfile2-method"></a><span data-ttu-id="f79ed-102">SetAssemblyFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="f79ed-102">SetAssemblyFile2 Method</span></span>
<span data-ttu-id="f79ed-103">Définit le nom et les options pour un nouvel assembly.</span><span class="sxs-lookup"><span data-stu-id="f79ed-103">Sets the name of and options for a new assembly.</span></span> <span data-ttu-id="f79ed-104">N’appelez pas cette méthode lorsque vous générez des modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="f79ed-104">Do not call this method when you produce unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f79ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f79ed-105">Syntax</span></span>  
  
```  
HRESULT SetAssemblyFile2(  
    LPCWSTR pszFilename,  
    IMetaDataEmit2* pEmitter,  
    AssemblyFlags   afFlags,  
    mdAssembly* pAssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f79ed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f79ed-106">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="f79ed-107">Nom du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="f79ed-107">Name of manifest file.</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="f79ed-108">[IMetaDataEmit2, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface pour ce fichier.</span><span class="sxs-lookup"><span data-stu-id="f79ed-108">[IMetaDataEmit2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface for this file.</span></span>  
  
 `afFlags`  
 <span data-ttu-id="f79ed-109">Les options représentées par [AssemblyFlags, énumération](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f79ed-109">Options represented by [AssemblyFlags Enumeration](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span></span>  
  
 `pAssemblyID`  
 <span data-ttu-id="f79ed-110">Reçoit l’ID unique pour l’assembly en cours de construction.</span><span class="sxs-lookup"><span data-stu-id="f79ed-110">Receives unique ID for the assembly being constructed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f79ed-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f79ed-111">Return Value</span></span>  
 <span data-ttu-id="f79ed-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="f79ed-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f79ed-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f79ed-113">Requirements</span></span>  
 <span data-ttu-id="f79ed-114">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="f79ed-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f79ed-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f79ed-115">See also</span></span>
- [<span data-ttu-id="f79ed-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="f79ed-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="f79ed-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="f79ed-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="f79ed-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="f79ed-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
