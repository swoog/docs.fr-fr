---
title: SYMLINEDELTA, structure
ms.date: 03/30/2017
api_name:
- SYMLINEDELTA
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SYMLINEDELTA
helpviewer_keywords:
- SYMLINEDELTA structure [.NET Framework debugging]
ms.assetid: 9634e995-d46d-4397-ab66-cc5781d11e4e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: fabc8f77b12865d0d971b5934d7de27b52f3e813
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59159482"
---
# <a name="symlinedelta-structure"></a><span data-ttu-id="e3101-102">SYMLINEDELTA, structure</span><span class="sxs-lookup"><span data-stu-id="e3101-102">SYMLINEDELTA Structure</span></span>
<span data-ttu-id="e3101-103">Fournit des informations pour le Gestionnaire de symboles sur les méthodes qui ont été déplacées à la suite de modifications.</span><span class="sxs-lookup"><span data-stu-id="e3101-103">Provides information to the symbol handler about methods that were moved as a result of edits.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3101-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3101-104">Syntax</span></span>  
  
```  
typedef struct _SYMLINEDELTA  
    {  
        mdMethodDef  mdMethod;  
        INT32        delta;  
    } SYMLINEDELTA;  
```  
  
## <a name="members"></a><span data-ttu-id="e3101-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e3101-105">Members</span></span>  
  
|<span data-ttu-id="e3101-106">Membre</span><span class="sxs-lookup"><span data-stu-id="e3101-106">Member</span></span>|<span data-ttu-id="e3101-107">Description</span><span class="sxs-lookup"><span data-stu-id="e3101-107">Description</span></span>|  
|------------|-----------------|  
|`mdMethod`|<span data-ttu-id="e3101-108">Jeton de métadonnées de la méthode.</span><span class="sxs-lookup"><span data-stu-id="e3101-108">The method's metadata token.</span></span>|  
|`delta`|<span data-ttu-id="e3101-109">Le nombre de lignes de que la méthode a été déplacée.</span><span class="sxs-lookup"><span data-stu-id="e3101-109">The number of lines the method was moved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e3101-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3101-110">Requirements</span></span>  
 <span data-ttu-id="e3101-111">**En-tête :** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="e3101-111">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3101-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3101-112">See also</span></span>

- [<span data-ttu-id="e3101-113">Structures du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="e3101-113">Diagnostics Symbol Store Structures</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-structures.md)
