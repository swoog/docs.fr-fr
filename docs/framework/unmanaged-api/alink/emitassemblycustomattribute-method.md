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
ms.openlocfilehash: 67073f04cfe981dd383369029d9a4b436929a0a6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59117843"
---
# <a name="emitassemblycustomattribute-method"></a><span data-ttu-id="0e890-102">EmitAssemblyCustomAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="0e890-102">EmitAssemblyCustomAttribute Method</span></span>
<span data-ttu-id="0e890-103">Appel permettant de définir les attributs personnalisés de niveau assembly.</span><span class="sxs-lookup"><span data-stu-id="0e890-103">Call to set assembly-level custom attributes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0e890-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e890-104">Syntax</span></span>  
  
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
  
## <a name="parameters"></a><span data-ttu-id="0e890-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e890-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="0e890-106">ID de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0e890-106">ID of the assembly.</span></span>  
  
 `FileToken`  
 <span data-ttu-id="0e890-107">Fichier qui définit l’attribut.</span><span class="sxs-lookup"><span data-stu-id="0e890-107">File that defiles the attribute.</span></span> <span data-ttu-id="0e890-108">Peut être NULL si `AssemblyID` n’indique pas un netmodule indépendant.</span><span class="sxs-lookup"><span data-stu-id="0e890-108">Can be NULL if `AssemblyID` does not indicate an unbound netmodule.</span></span>  
  
 `tkType`  
 <span data-ttu-id="0e890-109">Type de l’attribut personnalisé.</span><span class="sxs-lookup"><span data-stu-id="0e890-109">Type of the custom attribute.</span></span>  
  
 `pCustomValue`  
 <span data-ttu-id="0e890-110">Valeur des données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="0e890-110">Custom value data.</span></span>  
  
 `cbCustomValue`  
 <span data-ttu-id="0e890-111">Longueur des données de valeur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="0e890-111">Length of custom value data.</span></span>  
  
 `bSecurity`  
 <span data-ttu-id="0e890-112">TRUE si l’attribut personnalisé est associé à la signature de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="0e890-112">TRUE if the custom attribute is related to assembly signing.</span></span>  
  
 `bAllowMulti`  
 <span data-ttu-id="0e890-113">TRUE si plusieurs attributs doivent être émis.</span><span class="sxs-lookup"><span data-stu-id="0e890-113">TRUE if multiple attributes are to be emitted.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0e890-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0e890-114">Return Value</span></span>  
 <span data-ttu-id="0e890-115">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="0e890-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0e890-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e890-116">Requirements</span></span>  
 <span data-ttu-id="0e890-117">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="0e890-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0e890-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e890-118">See also</span></span>

- [<span data-ttu-id="0e890-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="0e890-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="0e890-120">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="0e890-120">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="0e890-121">API ALink</span><span class="sxs-lookup"><span data-stu-id="0e890-121">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
