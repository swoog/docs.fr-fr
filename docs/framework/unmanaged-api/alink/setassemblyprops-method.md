---
title: SetAssemblyProps, méthode
ms.date: 03/30/2017
api_name:
- IALink.SetAssemblyProps
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetAssemblyProps
helpviewer_keywords:
- SetAssemblyProps method
ms.assetid: a3d7cf29-1414-49e6-8aae-9b3283c4f5f0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 589bd7b2132693c89dc10ae1a5c8d0bf52ed481e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59218990"
---
# <a name="setassemblyprops-method"></a><span data-ttu-id="a69d6-102">SetAssemblyProps, méthode</span><span class="sxs-lookup"><span data-stu-id="a69d6-102">SetAssemblyProps Method</span></span>
<span data-ttu-id="a69d6-103">Assigne des propriétés au niveau de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a69d6-103">Assigns assembly-level properties.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a69d6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a69d6-104">Syntax</span></span>  
  
```  
HRESULT SetAssemblyProps(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    AssemblyOptions Option,  
    VARIANT         Value  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="a69d6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a69d6-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="a69d6-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a69d6-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="a69d6-107">Fichier qui définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="a69d6-107">File that defines the property.</span></span> <span data-ttu-id="a69d6-108">Peut être NULL si `AssemblyID` n’indique pas un netmodule indépendant.</span><span class="sxs-lookup"><span data-stu-id="a69d6-108">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `Option`  
 <span data-ttu-id="a69d6-109">Indique l’option de modification.</span><span class="sxs-lookup"><span data-stu-id="a69d6-109">Indicates the option to modify.</span></span>  
  
 `Value`  
 <span data-ttu-id="a69d6-110">Nouvelle valeur de l’option.</span><span class="sxs-lookup"><span data-stu-id="a69d6-110">New value of the option.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a69d6-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a69d6-111">Return Value</span></span>  
 <span data-ttu-id="a69d6-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="a69d6-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a69d6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a69d6-113">Requirements</span></span>  
 <span data-ttu-id="a69d6-114">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="a69d6-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a69d6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a69d6-115">See also</span></span>

- [<span data-ttu-id="a69d6-116">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="a69d6-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="a69d6-117">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="a69d6-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="a69d6-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="a69d6-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
