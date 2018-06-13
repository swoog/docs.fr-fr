---
title: EmitAssemblyCustomAttribute, méthode
ms.date: 03/30/2017
api_name:
- IALink.EmitAssemblyCustomAttribute
- EmitAssemblyCustomAttribute
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitAssemblyCustomAttribute
helpviewer_keywords:
- EmitAssemblyCustomAttribute method
ms.assetid: b72f5409-79af-4fa7-90a7-7630eec170f1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: daf2c3dcaf16e949f8770121d8324cbfe6c7d05b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404077"
---
# <a name="emitassemblycustomattribute-method"></a><span data-ttu-id="48fe9-102">EmitAssemblyCustomAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="48fe9-102">EmitAssemblyCustomAttribute Method</span></span>
<span data-ttu-id="48fe9-103">L’appel à définir les attributs de niveau assembly.</span><span class="sxs-lookup"><span data-stu-id="48fe9-103">Call to set assembly-level custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48fe9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48fe9-104">Syntax</span></span>  
  
```  
HRESULT EmitAssemblyCustomAttribute(  
    mdAssembly   AssemblyID,  
    mdToken      FileToken,  
    mdToken      tkType,  
    void const*  pCustomValue,  
    DWORD        cbCustomValue,  
    BOOL         bSecurity,  
    BOOL         bAllowMulti  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="48fe9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48fe9-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="48fe9-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="48fe9-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="48fe9-107">Fichier qui définit l’attribut.</span><span class="sxs-lookup"><span data-stu-id="48fe9-107">File that defiles the attribute.</span></span> <span data-ttu-id="48fe9-108">Peut être NULL si `AssemblyID` n’indique pas un netmodule indépendant.</span><span class="sxs-lookup"><span data-stu-id="48fe9-108">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `tkType`  
 <span data-ttu-id="48fe9-109">Type de l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="48fe9-109">Type of the custom attribute.</span></span>  
  
 `pCustomValue`  
 <span data-ttu-id="48fe9-110">Valeur des données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="48fe9-110">Custom value data.</span></span>  
  
 `cbCustomValue`  
 <span data-ttu-id="48fe9-111">Longueur des données de valeur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="48fe9-111">Length of custom value data.</span></span>  
  
 `bSecurity`  
 <span data-ttu-id="48fe9-112">TRUE si l’attribut personnalisé est associée à la signature de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="48fe9-112">TRUE if the custom attribute is related to assembly signing.</span></span>  
  
 `bAllowMulti`  
 <span data-ttu-id="48fe9-113">TRUE si plusieurs attributs doivent être émises.</span><span class="sxs-lookup"><span data-stu-id="48fe9-113">TRUE if multiple attributes are to be emitted.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="48fe9-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="48fe9-114">Return Value</span></span>  
 <span data-ttu-id="48fe9-115">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="48fe9-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48fe9-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="48fe9-116">Requirements</span></span>  
 <span data-ttu-id="48fe9-117">Requiert alink.h</span><span class="sxs-lookup"><span data-stu-id="48fe9-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48fe9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48fe9-118">See Also</span></span>  
 [<span data-ttu-id="48fe9-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="48fe9-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="48fe9-120">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="48fe9-120">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="48fe9-121">API ALink</span><span class="sxs-lookup"><span data-stu-id="48fe9-121">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
