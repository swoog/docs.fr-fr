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
ms.openlocfilehash: 65d6e929a0a6fb5e1933a6c9216dfc5b56342113
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560644"
---
# <a name="setassemblyprops-method"></a><span data-ttu-id="ccb8f-102">SetAssemblyProps, méthode</span><span class="sxs-lookup"><span data-stu-id="ccb8f-102">SetAssemblyProps Method</span></span>
<span data-ttu-id="ccb8f-103">Assigne des propriétés au niveau de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ccb8f-103">Assigns assembly-level properties.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ccb8f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccb8f-104">Syntax</span></span>  
  
```  
HRESULT SetAssemblyProps(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    AssemblyOptions Option,  
    VARIANT         Value  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ccb8f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccb8f-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="ccb8f-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="ccb8f-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="ccb8f-107">Fichier qui définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="ccb8f-107">File that defines the property.</span></span> <span data-ttu-id="ccb8f-108">Peut être NULL si `AssemblyID` n’indique pas un netmodule indépendant.</span><span class="sxs-lookup"><span data-stu-id="ccb8f-108">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `Option`  
 <span data-ttu-id="ccb8f-109">Indique l’option de modification.</span><span class="sxs-lookup"><span data-stu-id="ccb8f-109">Indicates the option to modify.</span></span>  
  
 `Value`  
 <span data-ttu-id="ccb8f-110">Nouvelle valeur de l’option.</span><span class="sxs-lookup"><span data-stu-id="ccb8f-110">New value of the option.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ccb8f-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ccb8f-111">Return Value</span></span>  
 <span data-ttu-id="ccb8f-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="ccb8f-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ccb8f-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ccb8f-113">Requirements</span></span>  
 <span data-ttu-id="ccb8f-114">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="ccb8f-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccb8f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccb8f-115">See also</span></span>
- [<span data-ttu-id="ccb8f-116">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="ccb8f-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="ccb8f-117">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="ccb8f-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="ccb8f-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="ccb8f-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
