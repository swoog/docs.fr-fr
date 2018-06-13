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
ms.openlocfilehash: ade568889d1c0203115f160d855de8c598798196
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33403355"
---
# <a name="setassemblyfile2-method"></a><span data-ttu-id="d41fc-102">SetAssemblyFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="d41fc-102">SetAssemblyFile2 Method</span></span>
<span data-ttu-id="d41fc-103">Définit le nom et les options pour un nouvel assembly.</span><span class="sxs-lookup"><span data-stu-id="d41fc-103">Sets the name of and options for a new assembly.</span></span> <span data-ttu-id="d41fc-104">N’appelez pas cette méthode lorsque vous générez des modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="d41fc-104">Do not call this method when you produce unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d41fc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d41fc-105">Syntax</span></span>  
  
```  
HRESULT SetAssemblyFile2(  
    LPCWSTR pszFilename,  
    IMetaDataEmit2* pEmitter,  
    AssemblyFlags   afFlags,  
    mdAssembly* pAssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d41fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d41fc-106">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="d41fc-107">Nom du fichier manifeste.</span><span class="sxs-lookup"><span data-stu-id="d41fc-107">Name of manifest file.</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="d41fc-108">[IMetaDataEmit2 (Interface)](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface pour ce fichier.</span><span class="sxs-lookup"><span data-stu-id="d41fc-108">[IMetaDataEmit2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface for this file.</span></span>  
  
 `afFlags`  
 <span data-ttu-id="d41fc-109">Les options sont représentées par [énumération AssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="d41fc-109">Options represented by [AssemblyFlags Enumeration](../../../../docs/framework/unmanaged-api/metadata/assemblyflags-enumeration.md).</span></span>  
  
 `pAssemblyID`  
 <span data-ttu-id="d41fc-110">Reçoit l’ID unique de l’assembly en cours de construction.</span><span class="sxs-lookup"><span data-stu-id="d41fc-110">Receives unique ID for the assembly being constructed.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d41fc-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d41fc-111">Return Value</span></span>  
 <span data-ttu-id="d41fc-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="d41fc-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d41fc-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d41fc-113">Requirements</span></span>  
 <span data-ttu-id="d41fc-114">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="d41fc-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d41fc-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d41fc-115">See Also</span></span>  
 [<span data-ttu-id="d41fc-116">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="d41fc-116">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="d41fc-117">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="d41fc-117">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="d41fc-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="d41fc-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
