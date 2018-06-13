---
title: EmitAssembly, méthode
ms.date: 03/30/2017
api_name:
- IALink2.EmitAssembly
- EmitAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitAssembly
helpviewer_keywords:
- EmitAssembly method
ms.assetid: 605ff39e-e5cc-4bff-8196-e8d68a9715b9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1cd1c077a8f2a5fe3b2b46c2e1da2e92b5a797a6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402055"
---
# <a name="emitassembly-method"></a><span data-ttu-id="08cd2-102">EmitAssembly, méthode</span><span class="sxs-lookup"><span data-stu-id="08cd2-102">EmitAssembly Method</span></span>
<span data-ttu-id="08cd2-103">Crée l’assembly.</span><span class="sxs-lookup"><span data-stu-id="08cd2-103">Creates the assembly.</span></span> <span data-ttu-id="08cd2-104">Appelez cette méthode après la fermeture de tous les autres fichiers à l’exception du fichier d’assembly.</span><span class="sxs-lookup"><span data-stu-id="08cd2-104">Call this method after all other files are closed except for the assembly file.</span></span> <span data-ttu-id="08cd2-105">N’appelez pas cette méthode lors de la production de modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="08cd2-105">Do not call this method when producing unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08cd2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08cd2-106">Syntax</span></span>  
  
```  
HRESULT EmitAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="08cd2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08cd2-107">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="08cd2-108">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="08cd2-108">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="08cd2-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="08cd2-109">Return Value</span></span>  
 <span data-ttu-id="08cd2-110">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="08cd2-110">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08cd2-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="08cd2-111">Requirements</span></span>  
 <span data-ttu-id="08cd2-112">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="08cd2-112">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08cd2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08cd2-113">See Also</span></span>  
 [<span data-ttu-id="08cd2-114">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="08cd2-114">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="08cd2-115">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="08cd2-115">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="08cd2-116">API ALink</span><span class="sxs-lookup"><span data-stu-id="08cd2-116">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
