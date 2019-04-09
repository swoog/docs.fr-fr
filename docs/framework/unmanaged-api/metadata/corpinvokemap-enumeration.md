---
title: CorPinvokeMap, énumération
ms.date: 03/30/2017
api_name:
- CorPinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorPinvokeMap
helpviewer_keywords:
- CorPinvokeMap enumeration [.NET Framework metadata]
ms.assetid: f14f986e-f6ce-42bc-aa23-18150c46d28c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 951941092f67f66c5b17c8ae592569c2a8e6a675
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59079628"
---
# <a name="corpinvokemap-enumeration"></a><span data-ttu-id="94ba4-102">CorPinvokeMap, énumération</span><span class="sxs-lookup"><span data-stu-id="94ba4-102">CorPinvokeMap Enumeration</span></span>
<span data-ttu-id="94ba4-103">Spécifie les options pour un appel PInvoke.</span><span class="sxs-lookup"><span data-stu-id="94ba4-103">Specifies options for a PInvoke call.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94ba4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94ba4-104">Syntax</span></span>  
  
```  
typedef enum  CorPinvokeMap {  
  
    pmNoMangle          = 0x0001,  
  
    pmCharSetMask       = 0x0006,  
    pmCharSetNotSpec    = 0x0000,  
    pmCharSetAnsi       = 0x0002,  
    pmCharSetUnicode    = 0x0004,  
    pmCharSetAuto       = 0x0006,  
  
    pmBestFitUseAssem   = 0x0000,  
    pmBestFitEnabled    = 0x0010,  
    pmBestFitDisabled   = 0x0020,  
    pmBestFitMask       = 0x0030,  
  
    pmThrowOnUnmappableCharUseAssem   = 0x0000,  
    pmThrowOnUnmappableCharEnabled    = 0x1000,  
    pmThrowOnUnmappableCharDisabled   = 0x2000,  
    pmThrowOnUnmappableCharMask       = 0x3000,  
  
    pmSupportsLastError = 0x0040,   
  
    pmCallConvMask      = 0x0700,  
    pmCallConvWinapi    = 0x0100,  
    pmCallConvCdecl     = 0x0200,  
    pmCallConvStdcall   = 0x0300,  
    pmCallConvThiscall  = 0x0400,  
    pmCallConvFastcall  = 0x0500,  
  
    pmMaxValue          = 0xFFFF  
  
} CorPinvokeMap;  
```  
  
## <a name="members"></a><span data-ttu-id="94ba4-105">Membres</span><span class="sxs-lookup"><span data-stu-id="94ba4-105">Members</span></span>  
  
|<span data-ttu-id="94ba4-106">Membre</span><span class="sxs-lookup"><span data-stu-id="94ba4-106">Member</span></span>|<span data-ttu-id="94ba4-107">Description</span><span class="sxs-lookup"><span data-stu-id="94ba4-107">Description</span></span>|  
|------------|-----------------|  
|`pmNoMangle`|<span data-ttu-id="94ba4-108">Utilisez chaque nom de membre spécifiés.</span><span class="sxs-lookup"><span data-stu-id="94ba4-108">Use each member name as specified.</span></span>|  
|`pmCharSetMask`|<span data-ttu-id="94ba4-109">Réservé.</span><span class="sxs-lookup"><span data-stu-id="94ba4-109">Reserved.</span></span>|  
|`pmCharSetNotSpec`|<span data-ttu-id="94ba4-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="94ba4-110">Reserved.</span></span>|  
|`pmCharSetAnsi`|<span data-ttu-id="94ba4-111">Les chaînes sont marshalées sous forme de chaînes de caractères multi-octets.</span><span class="sxs-lookup"><span data-stu-id="94ba4-111">Marshal strings as multiple-byte character strings.</span></span>|  
|`pmCharSetUnicode`|<span data-ttu-id="94ba4-112">Marshaler des chaînes comme des caractères Unicode sur 2 octets.</span><span class="sxs-lookup"><span data-stu-id="94ba4-112">Marshal strings as Unicode 2-byte characters.</span></span>|  
|`pmCharSetAuto`|<span data-ttu-id="94ba4-113">Chaînes sont automatiquement marshalées en conséquence pour le système d’exploitation cible.</span><span class="sxs-lookup"><span data-stu-id="94ba4-113">Automatically marshal strings appropriately for the target operating system.</span></span> <span data-ttu-id="94ba4-114">La valeur par défaut est Unicode sous Windows NT, Windows 2000, Windows XP et la famille Windows Server 2003 ; la valeur par défaut est ANSI sous Windows 98 et Windows Me.</span><span class="sxs-lookup"><span data-stu-id="94ba4-114">The default is Unicode on Windows NT, Windows 2000, Windows XP, and the Windows Server 2003 family; the default is ANSI on Windows 98 and Windows Me.</span></span>|  
|`pmBestFitUseAssem`|<span data-ttu-id="94ba4-115">Réservé.</span><span class="sxs-lookup"><span data-stu-id="94ba4-115">Reserved.</span></span>|  
|`pmBestFitEnabled`|<span data-ttu-id="94ba4-116">Effectuer le mappage ajusté des caractères Unicode qui ne disposent pas d’une correspondance exacte dans le jeu de caractères ANSI.</span><span class="sxs-lookup"><span data-stu-id="94ba4-116">Perform best-fit mapping of Unicode characters that lack an exact match in the ANSI character set.</span></span>|  
|`pmBestFitDisabled`|<span data-ttu-id="94ba4-117">N’effectuez pas de mappage ajusté des caractères Unicode.</span><span class="sxs-lookup"><span data-stu-id="94ba4-117">Do not perform best-fit mapping of Unicode characters.</span></span> <span data-ttu-id="94ba4-118">Dans ce cas, tous les caractères non mappables seront remplacés par un ' ?'.</span><span class="sxs-lookup"><span data-stu-id="94ba4-118">In this case, all unmappable characters will be replaced by a ‘?’.</span></span>|  
|`pmBestFitMask`|<span data-ttu-id="94ba4-119">Réservé.</span><span class="sxs-lookup"><span data-stu-id="94ba4-119">Reserved.</span></span>|  
|`pmThrowOnUnmappableCharUseAssem`|<span data-ttu-id="94ba4-120">Réservé.</span><span class="sxs-lookup"><span data-stu-id="94ba4-120">Reserved.</span></span>|  
|`pmThrowOnUnmappableCharEnabled`|<span data-ttu-id="94ba4-121">Lève une exception lorsque le marshaleur d’interopérabilité rencontre un caractère non mappable.</span><span class="sxs-lookup"><span data-stu-id="94ba4-121">Throw an exception when the interop marshaler encounters an unmappable character.</span></span>|  
|`pmThrowOnUnmappableCharDisabled`|<span data-ttu-id="94ba4-122">Ne levez pas d’exception lorsque le marshaleur d’interopérabilité rencontre un caractère non mappable.</span><span class="sxs-lookup"><span data-stu-id="94ba4-122">Do not throw an exception when the interop marshaler encounters an unmappable character.</span></span>|  
|`pmThrowOnUnmappableCharMask`|<span data-ttu-id="94ba4-123">Réservée</span><span class="sxs-lookup"><span data-stu-id="94ba4-123">Reserved</span></span>|  
|`pmSupportsLastError`|<span data-ttu-id="94ba4-124">Permet à l’appelé d’appeler Win32 `SetLastError` (fonction) avant le retour de la méthode avec attributs.</span><span class="sxs-lookup"><span data-stu-id="94ba4-124">Allow the callee to call the Win32 `SetLastError` function before returning from the attributed method.</span></span>|  
|`pmCallConvMask`|<span data-ttu-id="94ba4-125">Réservée</span><span class="sxs-lookup"><span data-stu-id="94ba4-125">Reserved</span></span>|  
|`pmCallConvWinapi`|<span data-ttu-id="94ba4-126">Utilisez la convention d’appel de plateforme par défaut.</span><span class="sxs-lookup"><span data-stu-id="94ba4-126">Use the default platform calling convention.</span></span> <span data-ttu-id="94ba4-127">Par exemple, sur Windows, la valeur par défaut est `StdCall` et sur Windows CE .NET, il est `Cdecl`.</span><span class="sxs-lookup"><span data-stu-id="94ba4-127">For example, on Windows the default is `StdCall` and on Windows CE .NET it is `Cdecl`.</span></span>|  
|`pmCallConvCdecl`|<span data-ttu-id="94ba4-128">Utilisez le `Cdecl` convention d’appel.</span><span class="sxs-lookup"><span data-stu-id="94ba4-128">Use the `Cdecl` calling convention.</span></span> <span data-ttu-id="94ba4-129">Dans ce cas, l’appelant nettoie la pile.</span><span class="sxs-lookup"><span data-stu-id="94ba4-129">In this case, the caller cleans the stack.</span></span> <span data-ttu-id="94ba4-130">Cela permet d’appeler des fonctions avec `varargs` (autrement dit, les fonctions qui acceptent un nombre variable de paramètres).</span><span class="sxs-lookup"><span data-stu-id="94ba4-130">This enables calling functions with `varargs` (that is, functions that accept a variable number of parameters).</span></span>|  
|`pmCallConvStdcall`|<span data-ttu-id="94ba4-131">Utilisez le `StdCall` convention d’appel.</span><span class="sxs-lookup"><span data-stu-id="94ba4-131">Use the `StdCall` calling convention.</span></span> <span data-ttu-id="94ba4-132">Dans ce cas, l’appelé nettoie la pile.</span><span class="sxs-lookup"><span data-stu-id="94ba4-132">In this case, the callee cleans the stack.</span></span> <span data-ttu-id="94ba4-133">Il s’agit de la convention par défaut pour appeler les fonctions non managées avec platform invoke.</span><span class="sxs-lookup"><span data-stu-id="94ba4-133">This is the default convention for calling unmanaged functions with platform invoke.</span></span>|  
|`pmCallConvThiscall`|<span data-ttu-id="94ba4-134">Utilisez le `ThisCall` convention d’appel.</span><span class="sxs-lookup"><span data-stu-id="94ba4-134">Use the `ThisCall` calling convention.</span></span> <span data-ttu-id="94ba4-135">Dans ce cas, le premier paramètre est le `this` pointeur et est stocké dans le Registre ECX.</span><span class="sxs-lookup"><span data-stu-id="94ba4-135">In this case, the first parameter is the `this` pointer and is stored in register ECX.</span></span> <span data-ttu-id="94ba4-136">Autres paramètres sont transmis sur la pile.</span><span class="sxs-lookup"><span data-stu-id="94ba4-136">Other parameters are pushed on the stack.</span></span> <span data-ttu-id="94ba4-137">Le `ThisCall` convention d’appel est utilisée pour appeler des méthodes sur des classes exportées à partir d’une DLL non managée.</span><span class="sxs-lookup"><span data-stu-id="94ba4-137">The `ThisCall` calling convention is used to call methods on classes exported from an unmanaged DLL.</span></span>|  
|`pmCallConvFastcall`|<span data-ttu-id="94ba4-138">Réservé.</span><span class="sxs-lookup"><span data-stu-id="94ba4-138">Reserved.</span></span>|  
|`pmMaxValue`|<span data-ttu-id="94ba4-139">Réservé.</span><span class="sxs-lookup"><span data-stu-id="94ba4-139">Reserved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="94ba4-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94ba4-140">Requirements</span></span>  
 <span data-ttu-id="94ba4-141">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="94ba4-141">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94ba4-142">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="94ba4-142">**Header:** CorHdr.h</span></span>  
  
 **<span data-ttu-id="94ba4-143">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="94ba4-143">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="94ba4-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94ba4-144">See also</span></span>

- [<span data-ttu-id="94ba4-145">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="94ba4-145">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
