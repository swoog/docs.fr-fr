---
title: CorSymVarFlag, énumération
ms.date: 03/30/2017
api_name:
- CorSymVarFlag
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSymVarFlag
helpviewer_keywords:
- CorSymVarFlag enumeration [.NET Framework debugging]
ms.assetid: c3f7d307-4047-4f9a-be8c-f152fca42fd0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0c797378f5e13f39c1c786237a3a7b9cf577fccc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59198853"
---
# <a name="corsymvarflag-enumeration"></a><span data-ttu-id="3082d-102">CorSymVarFlag, énumération</span><span class="sxs-lookup"><span data-stu-id="3082d-102">CorSymVarFlag Enumeration</span></span>
<span data-ttu-id="3082d-103">Indique si une variable est générée par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="3082d-103">Indicates whether a variable is compiler-generated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3082d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3082d-104">Syntax</span></span>  
  
```  
typedef enum CorSymVarFlag   
{  
    VAR_IS_COMP_GEN = 1  
} CorSymVarFlag;  
```  
  
## <a name="members"></a><span data-ttu-id="3082d-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3082d-105">Members</span></span>  
  
|<span data-ttu-id="3082d-106">Membre</span><span class="sxs-lookup"><span data-stu-id="3082d-106">Member</span></span>|<span data-ttu-id="3082d-107">Description</span><span class="sxs-lookup"><span data-stu-id="3082d-107">Description</span></span>|  
|------------|-----------------|  
|`VAR_IS_COMP_GEN`|<span data-ttu-id="3082d-108">Indique que la variable donnée est généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="3082d-108">Indicates that the given variable is compiler-generated.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3082d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3082d-109">Requirements</span></span>  
 <span data-ttu-id="3082d-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="3082d-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3082d-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3082d-111">See also</span></span>

- [<span data-ttu-id="3082d-112">Énumérations du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="3082d-112">Diagnostics Symbol Store Enumerations</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-enumerations.md)
