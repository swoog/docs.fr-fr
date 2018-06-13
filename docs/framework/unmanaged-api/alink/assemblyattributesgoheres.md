---
title: AssemblyAttributesGoHereS
ms.date: 03/30/2017
api_name:
- AssemblyAttributesGoHereS
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyAttributesGoHereS
helpviewer_keywords:
- AssemblyAttributesGoHereS type
- Alink API, AssemblyAttributesGoHereS type
ms.assetid: 4e817f35-a2bc-4403-9e6f-f731e6b9fe23
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d68450d05f667851404a009c0984f8722253e71e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402908"
---
# <a name="assemblyattributesgoheres"></a><span data-ttu-id="6b1bd-102">AssemblyAttributesGoHereS</span><span class="sxs-lookup"><span data-stu-id="6b1bd-102">AssemblyAttributesGoHereS</span></span>
<span data-ttu-id="6b1bd-103">Utilisé par ALink en tant qu'espace réservé pour stocker des informations sur les attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-103">Used by ALink as a placeholder to store information about custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6b1bd-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b1bd-104">Syntax</span></span>  
  
```  
AssemblyAttributesGoHereS  
```  
  
## <a name="remarks"></a><span data-ttu-id="6b1bd-105">Notes</span><span class="sxs-lookup"><span data-stu-id="6b1bd-105">Remarks</span></span>  
 <span data-ttu-id="6b1bd-106">Les références à ce type peuvent être incorporées dans les netmodules dont les sources contiennent des attributs personnalisés d'assembly.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-106">References to this type might be embedded inside netmodules whose sources contain assembly custom attributes.</span></span> <span data-ttu-id="6b1bd-107">Quand vous générez un manifeste d'assembly à partir d'un ou plusieurs netmodules qui contiennent des références à ces types, ALink utilise les informations associées à ces références pour émettre des attributs personnalisés réels.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-107">When building an assembly manifest from one or more netmodules that contain references to these types, ALink uses information attached to these references to emit real custom attributes.</span></span> <span data-ttu-id="6b1bd-108">Par conséquent, ce type n'est jamais instancié et ses références sont utilisées uniquement dans le cadre du processus de génération et n'ont aucune utilité dans l'assembly final.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-108">As such, this type is never instantiated, and references to it are used only as part of the build process and serve no purpose in the final assembly.</span></span>  
  
 <span data-ttu-id="6b1bd-109">Les références à ce type indiquent des attributs personnalisés qui sont liés à la sécurité et ne peuvent pas être utilisés plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-109">References to this type indicate custom attributes that are security related and are not multiple-use.</span></span>  
  
 <span data-ttu-id="6b1bd-110">Ces types sont marqués comme étant « internes » dans le .NET Framework et se trouvent dans <xref:System.Runtime.CompilerServices>.</span><span class="sxs-lookup"><span data-stu-id="6b1bd-110">These types are marked "internal" within the .NET Framework, and are located in <xref:System.Runtime.CompilerServices>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6b1bd-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6b1bd-111">Requirements</span></span>  
 <span data-ttu-id="6b1bd-112">mscorlib.dll</span><span class="sxs-lookup"><span data-stu-id="6b1bd-112">mscorlib.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6b1bd-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b1bd-113">See Also</span></span>  
 [<span data-ttu-id="6b1bd-114">AssemblyAttributesGoHere</span><span class="sxs-lookup"><span data-stu-id="6b1bd-114">AssemblyAttributesGoHere</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgohere.md)  
 [<span data-ttu-id="6b1bd-115">AssemblyAttributesGoHereM</span><span class="sxs-lookup"><span data-stu-id="6b1bd-115">AssemblyAttributesGoHereM</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoherem.md)  
 [<span data-ttu-id="6b1bd-116">AssemblyAttributesGoHereSM</span><span class="sxs-lookup"><span data-stu-id="6b1bd-116">AssemblyAttributesGoHereSM</span></span>](../../../../docs/framework/unmanaged-api/alink/assemblyattributesgoheresm.md)
