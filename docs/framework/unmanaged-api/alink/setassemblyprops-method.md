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
ms.openlocfilehash: aed553a3a8d54b5229a122e76b61e3e58d4af3c1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401964"
---
# <a name="setassemblyprops-method"></a><span data-ttu-id="0af23-102">SetAssemblyProps, méthode</span><span class="sxs-lookup"><span data-stu-id="0af23-102">SetAssemblyProps Method</span></span>
<span data-ttu-id="0af23-103">Assigne des propriétés au niveau de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0af23-103">Assigns assembly-level properties.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0af23-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0af23-104">Syntax</span></span>  
  
```  
HRESULT SetAssemblyProps(  
    mdAssembly      AssemblyID,  
    mdToken         FileToken,  
    AssemblyOptions Option,  
    VARIANT         Value  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0af23-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0af23-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="0af23-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0af23-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="0af23-107">Fichier qui définit la propriété.</span><span class="sxs-lookup"><span data-stu-id="0af23-107">File that defines the property.</span></span> <span data-ttu-id="0af23-108">Peut être NULL si `AssemblyID` n’indique pas un netmodule indépendant.</span><span class="sxs-lookup"><span data-stu-id="0af23-108">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `Option`  
 <span data-ttu-id="0af23-109">Indique l’option de modification.</span><span class="sxs-lookup"><span data-stu-id="0af23-109">Indicates the option to modify.</span></span>  
  
 `Value`  
 <span data-ttu-id="0af23-110">Nouvelle valeur de l’option.</span><span class="sxs-lookup"><span data-stu-id="0af23-110">New value of the option.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0af23-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0af23-111">Return Value</span></span>  
 <span data-ttu-id="0af23-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="0af23-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0af23-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0af23-113">Requirements</span></span>  
 <span data-ttu-id="0af23-114">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="0af23-114">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0af23-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0af23-115">See Also</span></span>  
 [<span data-ttu-id="0af23-116">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="0af23-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="0af23-117">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="0af23-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="0af23-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="0af23-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
