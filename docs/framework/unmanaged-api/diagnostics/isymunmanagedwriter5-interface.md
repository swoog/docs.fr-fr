---
title: ISymUnmanagedWriter5, interface
ms.date: 03/30/2017
ms.assetid: 15b8526e-4f5d-475c-a1e3-d8b2d145c879
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a6ed8c6e61c558a4bc9e3f92d559615ac93ecff8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61962337"
---
# <a name="isymunmanagedwriter5-interface"></a><span data-ttu-id="5fdef-102">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="5fdef-102">ISymUnmanagedWriter5 Interface</span></span>
<span data-ttu-id="5fdef-103">Isymunmanagedwriter5, interface.</span><span class="sxs-lookup"><span data-stu-id="5fdef-103">ISymUnmanagedWriter5 interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5fdef-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fdef-104">Syntax</span></span>  
  
```idl  
[object,uuid(DCF7780D-BDE9-45DF-ACFE-21731A32000C),pointer_default(unique)]interface ISymUnmanagedWriter5 : ISymUnmanagedWriter4  
```  
  
## <a name="methods"></a><span data-ttu-id="5fdef-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5fdef-105">Methods</span></span>  
 <span data-ttu-id="5fdef-106">Cette interface contient les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fdef-106">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="5fdef-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="5fdef-107">Method</span></span>|<span data-ttu-id="5fdef-108">Description</span><span class="sxs-lookup"><span data-stu-id="5fdef-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5fdef-109">CloseMapTokensToSourceSpans, méthode</span><span class="sxs-lookup"><span data-stu-id="5fdef-109">CloseMapTokensToSourceSpans Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md)|<span data-ttu-id="5fdef-110">Fermez la section de données personnalisé spécial pour l’étendue de jeton pour source des informations de mappage.</span><span class="sxs-lookup"><span data-stu-id="5fdef-110">Close the special custom data section for token-to- source span mapping information.</span></span> <span data-ttu-id="5fdef-111">Après sa fermeture, aucune information de mappage plus ne peut être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="5fdef-111">After it is closed, no more mapping information can be added.</span></span>|  
|[<span data-ttu-id="5fdef-112">MapTokenToSourceSpan, méthode</span><span class="sxs-lookup"><span data-stu-id="5fdef-112">MapTokenToSourceSpan Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-maptokentosourcespan-method.md)|<span data-ttu-id="5fdef-113">Cartes s’étendent sur le jeton de métadonnées donné à la ligne source donné dans le fichier source spécifié.</span><span class="sxs-lookup"><span data-stu-id="5fdef-113">Maps the given metadata token to the given source line span in the specified source file.</span></span><br /><br /> <span data-ttu-id="5fdef-114">Doit être appelée entre les appels à [openmaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) et [closemaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span><span class="sxs-lookup"><span data-stu-id="5fdef-114">Must be called between calls to [OpenMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) and [CloseMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span></span>|  
|[<span data-ttu-id="5fdef-115">OpenMapTokensToSourceSpans, méthode</span><span class="sxs-lookup"><span data-stu-id="5fdef-115">OpenMapTokensToSourceSpans Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md)|<span data-ttu-id="5fdef-116">Ouvrez une section spéciale de données personnalisées pour émettre des informations de mappage de l’étendue de source de jeton dans.</span><span class="sxs-lookup"><span data-stu-id="5fdef-116">Open a special custom data section to emit token-to- source span mapping information into.</span></span> <span data-ttu-id="5fdef-117">Ouverture de cette section quand une méthode est déjà ouverte, ou vice versa, est une erreur.</span><span class="sxs-lookup"><span data-stu-id="5fdef-117">Opening this section when a method is already open, or vice versa, is an error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5fdef-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fdef-118">Requirements</span></span>  
 <span data-ttu-id="5fdef-119">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5fdef-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5fdef-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fdef-120">See also</span></span>

- [<span data-ttu-id="5fdef-121">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="5fdef-121">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="5fdef-122">ISymUnmanagedWriter4, interface</span><span class="sxs-lookup"><span data-stu-id="5fdef-122">ISymUnmanagedWriter4 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter4-interface.md)
