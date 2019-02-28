---
title: Classe AssemblyAttributesGoHere (System.Runtime.CompilerServices)
ms.date: 03/30/2017
api_name:
- System.Runtime.CompilerServices.AssemblyAttributesGoHere
api_location:
- mscorlib.dll
api_type:
- Assembly
f1_keywords:
- AssemblyAttributesGoHere
helpviewer_keywords:
- AssemblyAttributesGoHere type
- Alink API, AssemblyAttributesGoHere type
ms.assetid: 7b26fcb6-94f4-4f09-933e-b33efe451f4f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 571c2f6723e827a1b385f77724c33703ae970ae3
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56968112"
---
# <a name="assemblyattributesgohere-class"></a><span data-ttu-id="22006-102">Classe de AssemblyAttributesGoHere</span><span class="sxs-lookup"><span data-stu-id="22006-102">AssemblyAttributesGoHere Class</span></span>

<span data-ttu-id="22006-103">Utilisé par ALink en tant qu'espace réservé pour stocker des informations sur les attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="22006-103">Used by ALink as a placeholder to store information about custom attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="22006-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22006-104">Syntax</span></span>

```csharp
internal sealed class AssemblyAttributesGoHere
```

## <a name="remarks"></a><span data-ttu-id="22006-105">Notes</span><span class="sxs-lookup"><span data-stu-id="22006-105">Remarks</span></span>

<span data-ttu-id="22006-106">Les références à ce type peuvent être incorporées dans les netmodules dont les sources contiennent des attributs personnalisés d'assembly.</span><span class="sxs-lookup"><span data-stu-id="22006-106">References to this type might be embedded inside netmodules whose sources contain assembly custom attributes.</span></span> <span data-ttu-id="22006-107">Quand vous générez un manifeste d'assembly à partir d'un ou plusieurs netmodules qui contiennent des références à ces types, ALink utilise les informations associées à ces références pour émettre des attributs personnalisés réels.</span><span class="sxs-lookup"><span data-stu-id="22006-107">When building an assembly manifest from one or more netmodules that contain references to these types, ALink uses information attached to these references to emit real custom attributes.</span></span> <span data-ttu-id="22006-108">Par conséquent, ce type n'est jamais instancié et ses références sont utilisées uniquement dans le cadre du processus de génération et n'ont aucune utilité dans l'assembly final.</span><span class="sxs-lookup"><span data-stu-id="22006-108">As such, this type is never instantiated, and references to it are used only as part of the build process and serve no purpose in the final assembly.</span></span>

<span data-ttu-id="22006-109">Les références à ce type indiquent des attributs personnalisés qui ne sont pas liés à la sécurité et ne peuvent pas être utilisés plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="22006-109">References to this type indicate custom attributes that are not security related and are not multiple-use.</span></span>

<span data-ttu-id="22006-110">Ces types sont marqués « internes » dans le .NET Framework et se trouvent dans le <xref:System.Runtime.CompilerServices> espace de noms.</span><span class="sxs-lookup"><span data-stu-id="22006-110">These types are marked "internal" within the .NET Framework and are located in the <xref:System.Runtime.CompilerServices> namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="22006-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="22006-111">Requirements</span></span>

<span data-ttu-id="22006-112">mscorlib.dll</span><span class="sxs-lookup"><span data-stu-id="22006-112">mscorlib.dll</span></span>

## <a name="see-also"></a><span data-ttu-id="22006-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22006-113">See also</span></span>

- [<span data-ttu-id="22006-114">AssemblyAttributesGoHereM</span><span class="sxs-lookup"><span data-stu-id="22006-114">AssemblyAttributesGoHereM</span></span>](assemblyattributesgoherem.md)
- [<span data-ttu-id="22006-115">AssemblyAttributesGoHereS</span><span class="sxs-lookup"><span data-stu-id="22006-115">AssemblyAttributesGoHereS</span></span>](assemblyattributesgoheres.md)
- [<span data-ttu-id="22006-116">AssemblyAttributesGoHereSM</span><span class="sxs-lookup"><span data-stu-id="22006-116">AssemblyAttributesGoHereSM</span></span>](assemblyattributesgoheresm.md)
