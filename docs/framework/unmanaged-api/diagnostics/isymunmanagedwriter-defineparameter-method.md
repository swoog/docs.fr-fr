---
title: ISymUnmanagedWriter::DefineParameter, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineParameter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineParameter
helpviewer_keywords:
- DefineParameter method [.NET Framework debugging]
- ISymUnmanagedWriter::DefineParameter method [.NET Framework debugging]
ms.assetid: a8e3dd32-6a44-4371-9a74-f417b11998c8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b6b01abc16334dbe091e7586efcce1c3e390a64e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426973"
---
# <a name="isymunmanagedwriterdefineparameter-method"></a><span data-ttu-id="ad15b-102">ISymUnmanagedWriter::DefineParameter, méthode</span><span class="sxs-lookup"><span data-stu-id="ad15b-102">ISymUnmanagedWriter::DefineParameter Method</span></span>
<span data-ttu-id="ad15b-103">Définit un paramètre unique dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="ad15b-103">Defines a single parameter in the current method.</span></span> <span data-ttu-id="ad15b-104">Le type de paramètre provient de la position du paramètre (séquence) dans la signature de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ad15b-104">The parameter type is taken from the parameter's position (sequence) within the method's signature.</span></span>  
  
 <span data-ttu-id="ad15b-105">Si les paramètres sont définis dans les métadonnées pour une méthode donnée, vous n’avez pas à les définir à nouveau à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ad15b-105">If parameters are defined in the metadata for a given method, you do not have to define them again by using this method.</span></span> <span data-ttu-id="ad15b-106">Les lecteurs de symbole doivent vérifier les métadonnées normales pour les paramètres avant de vérifier le magasin de symboles.</span><span class="sxs-lookup"><span data-stu-id="ad15b-106">The symbol readers must check the normal metadata for the parameters before checking the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad15b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad15b-107">Syntax</span></span>  
  
```  
HRESULT DefineParameter(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      sequence,  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ad15b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad15b-108">Parameters</span></span>  
 `name`  
 <span data-ttu-id="ad15b-109">[in] Le nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad15b-109">[in] The parameter name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="ad15b-110">[in] Les attributs de paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad15b-110">[in] The parameter attributes.</span></span>  
  
 `sequence`  
 <span data-ttu-id="ad15b-111">[in] La signature de paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad15b-111">[in] The parameter signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="ad15b-112">[in] Le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="ad15b-112">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="ad15b-113">[in] La première adresse de la spécification du paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad15b-113">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="ad15b-114">[in] La deuxième adresse de la spécification du paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad15b-114">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="ad15b-115">[in] Troisième adresse de la spécification du paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad15b-115">[in] The third address for the parameter specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ad15b-116">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ad15b-116">Return Value</span></span>  
 <span data-ttu-id="ad15b-117">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ad15b-117">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad15b-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ad15b-118">Requirements</span></span>  
 <span data-ttu-id="ad15b-119">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ad15b-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad15b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad15b-120">See Also</span></span>  
 [<span data-ttu-id="ad15b-121">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="ad15b-121">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
