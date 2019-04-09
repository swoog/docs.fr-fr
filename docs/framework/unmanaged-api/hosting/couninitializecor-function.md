---
title: CoUninitializeCor, fonction
ms.date: 03/30/2017
api_name:
- CoUninitializeCor
api_location:
- mscoree.dll
- mscorsvr.dll
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
ms.openlocfilehash: 0845c4d493cb3c750931a0ae2ad92b628a255c0c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59202714"
---
# <a name="couninitializecor-function"></a><span data-ttu-id="18b92-102">CoUninitializeCor, fonction</span><span class="sxs-lookup"><span data-stu-id="18b92-102">CoUninitializeCor Function</span></span>
`CoUninitializeCor` <span data-ttu-id="18b92-103">est obsolète.</span><span class="sxs-lookup"><span data-stu-id="18b92-103">is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18b92-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18b92-104">Syntax</span></span>  
  
```  
STDAPI_(void) CoUninitializeCor(void);  
```  
  
## <a name="remarks"></a><span data-ttu-id="18b92-105">Notes</span><span class="sxs-lookup"><span data-stu-id="18b92-105">Remarks</span></span>  
 <span data-ttu-id="18b92-106">Le common language runtime ne peut pas être déchargé d’un processus.</span><span class="sxs-lookup"><span data-stu-id="18b92-106">The common language runtime cannot be unloaded from a process.</span></span> <span data-ttu-id="18b92-107">Pour supprimer complètement le runtime d’un processus en cours d’exécution, vous devez arrêter ce processus.</span><span class="sxs-lookup"><span data-stu-id="18b92-107">To completely remove the runtime from a running process, you must shut down that process.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18b92-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18b92-108">See also</span></span>

- [<span data-ttu-id="18b92-109">Fonctions statiques globales des métadonnées</span><span class="sxs-lookup"><span data-stu-id="18b92-109">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
