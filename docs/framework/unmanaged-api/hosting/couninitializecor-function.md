---
title: CoUninitializeCor, fonction
ms.date: 03/30/2017
api_name:
- CoUninitializeCor
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CoUninitializeCor
helpviewer_keywords:
- CoUninitializeCor function [.NET Framework hosting]
ms.assetid: 50a95b8b-9766-470e-bb29-2c7ecddfd4a1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 305a8d7b5a800c46ed814b1e654947859dc9bd03
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427809"
---
# <a name="couninitializecor-function"></a><span data-ttu-id="92455-102">CoUninitializeCor, fonction</span><span class="sxs-lookup"><span data-stu-id="92455-102">CoUninitializeCor Function</span></span>
<span data-ttu-id="92455-103">`CoUninitializeCor` est obsolète.</span><span class="sxs-lookup"><span data-stu-id="92455-103">`CoUninitializeCor` is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="92455-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92455-104">Syntax</span></span>  
  
```  
STDAPI_(void) CoUninitializeCor(void);  
```  
  
## <a name="remarks"></a><span data-ttu-id="92455-105">Notes</span><span class="sxs-lookup"><span data-stu-id="92455-105">Remarks</span></span>  
 <span data-ttu-id="92455-106">Le common language runtime ne peut pas être déchargé d’un processus.</span><span class="sxs-lookup"><span data-stu-id="92455-106">The common language runtime cannot be unloaded from a process.</span></span> <span data-ttu-id="92455-107">Pour supprimer complètement le runtime d’un processus en cours d’exécution, vous devez arrêter ce processus.</span><span class="sxs-lookup"><span data-stu-id="92455-107">To completely remove the runtime from a running process, you must shut down that process.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92455-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92455-108">See Also</span></span>  
 [<span data-ttu-id="92455-109">Fonctions statiques globales des métadonnées</span><span class="sxs-lookup"><span data-stu-id="92455-109">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
