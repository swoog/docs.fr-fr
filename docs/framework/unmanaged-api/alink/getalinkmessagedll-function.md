---
title: GetALinkMessageDll, fonction
ms.date: 03/30/2017
api_name:
- GetALinkMessageDll
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- GetALinkMessageDll
helpviewer_keywords:
- Alink API, GetALinkMessageDll function
- GetALinkMessageDll function
ms.assetid: 67985a22-88a2-4c54-8d99-4bcde9d6213e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 395dc85ad638e8a790962a4aa38019612c360ce1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402215"
---
# <a name="getalinkmessagedll-function"></a><span data-ttu-id="47077-102">GetALinkMessageDll, fonction</span><span class="sxs-lookup"><span data-stu-id="47077-102">GetALinkMessageDll Function</span></span>
<span data-ttu-id="47077-103">Recherche et charge la DLL de message.</span><span class="sxs-lookup"><span data-stu-id="47077-103">Finds and loads the message DLL.</span></span> <span data-ttu-id="47077-104">Retourne 0 si Impossible de trouver ou de charger la DLL de message.</span><span class="sxs-lookup"><span data-stu-id="47077-104">Returns 0 if the message DLL could not be located or loaded.</span></span> <span data-ttu-id="47077-105">La DLL de message doit être dans un sous-répertoire dont le nom est un ID de langue, ou dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="47077-105">The message DLL should be either in a subdirectory whose name is a language ID, or in the current directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47077-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47077-106">Syntax</span></span>  
  
```  
HINSTANCE WINAPI GetALinkMessageDll();  
```  
  
## <a name="requirements"></a><span data-ttu-id="47077-107">Spécifications</span><span class="sxs-lookup"><span data-stu-id="47077-107">Requirements</span></span>  
 <span data-ttu-id="47077-108">**En-tête :** alink.h</span><span class="sxs-lookup"><span data-stu-id="47077-108">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="47077-109">**Bibliothèque**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="47077-109">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47077-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47077-110">See Also</span></span>  
 [<span data-ttu-id="47077-111">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="47077-111">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
