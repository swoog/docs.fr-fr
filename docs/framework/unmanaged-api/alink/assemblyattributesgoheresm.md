---
title: AssemblyAttributesGoHereSM
ms.date: 03/30/2017
api_name:
- AssemblyAttributesGoHereSM
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyAttributesGoHereSM
helpviewer_keywords:
- AssemblyAttributesGoHereSM type
- Alink API, AssemblyAttributesGoHereSM type
ms.assetid: 4cf9bf39-1527-49e0-a0e9-55e7a018bf66
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6d47ca3a9134266d1c40447cea6eb8aaf2cc9eb9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706295"
---
# <a name="assemblyattributesgoheresm"></a><span data-ttu-id="3f8b6-102">AssemblyAttributesGoHereSM</span><span class="sxs-lookup"><span data-stu-id="3f8b6-102">AssemblyAttributesGoHereSM</span></span>
<span data-ttu-id="3f8b6-103">Utilisé par ALink en tant qu'espace réservé pour stocker des informations sur les attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-103">Used by ALink as a placeholder to store information about custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f8b6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f8b6-104">Syntax</span></span>  
  
```  
AssemblyAttributeGoHereSM  
```  
  
## <a name="remarks"></a><span data-ttu-id="3f8b6-105">Notes</span><span class="sxs-lookup"><span data-stu-id="3f8b6-105">Remarks</span></span>  
 <span data-ttu-id="3f8b6-106">Les références à ce type peuvent être incorporées dans les netmodules dont les sources contiennent des attributs personnalisés d'assembly.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-106">References to this type might be embedded inside netmodules whose sources contain assembly custom attributes.</span></span> <span data-ttu-id="3f8b6-107">Quand vous générez un manifeste d'assembly à partir d'un ou plusieurs netmodules qui contiennent des références à ces types, ALink utilise les informations associées à ces références pour émettre des attributs personnalisés réels.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-107">When building an assembly manifest from one or more netmodules that contain references to these types, ALink uses information attached to these references to emit real custom attributes.</span></span> <span data-ttu-id="3f8b6-108">Par conséquent, ce type n'est jamais instancié et ses références sont utilisées uniquement dans le cadre du processus de génération et n'ont aucune utilité dans l'assembly final.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-108">As such, this type is never instantiated, and references to it are used only as part of the build process and serve no purpose in the final assembly.</span></span>  
  
 <span data-ttu-id="3f8b6-109">Les références à ce type indiquent des attributs personnalisés qui sont liés à la sécurité et qui peuvent être utilisés plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-109">References to this type indicate custom attributes that are security related and multiple-use.</span></span>  
  
 <span data-ttu-id="3f8b6-110">Ces types sont marqués comme étant « internes » dans le .NET Framework et se trouvent dans <xref:System.Runtime.CompilerServices>.</span><span class="sxs-lookup"><span data-stu-id="3f8b6-110">These types are marked "internal" within the .NET Framework, and are located in <xref:System.Runtime.CompilerServices>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f8b6-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3f8b6-111">Requirements</span></span>  
 <span data-ttu-id="3f8b6-112">mscorlib.dll</span><span class="sxs-lookup"><span data-stu-id="3f8b6-112">mscorlib.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f8b6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f8b6-113">See also</span></span>
- [<span data-ttu-id="3f8b6-114">AssemblyAttributesGoHere</span><span class="sxs-lookup"><span data-stu-id="3f8b6-114">AssemblyAttributesGoHere</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgohere.md)
- [<span data-ttu-id="3f8b6-115">AssemblyAttributesGoHereM</span><span class="sxs-lookup"><span data-stu-id="3f8b6-115">AssemblyAttributesGoHereM</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoherem.md)
- [<span data-ttu-id="3f8b6-116">AssemblyAttributesGoHereS</span><span class="sxs-lookup"><span data-stu-id="3f8b6-116">AssemblyAttributesGoHereS</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoheres.md)
