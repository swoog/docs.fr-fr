---
title: ISymUnmanagedAsyncMethodPropertiesWriter, interface
ms.date: 03/30/2017
ms.assetid: caa71820-8058-4b6a-93a2-25ee757d92d3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d83270d0e7f5dabff8402f5f81dae20d4457d147
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604246"
---
# <a name="isymunmanagedasyncmethodpropertieswriter-interface"></a><span data-ttu-id="d3373-102">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="d3373-102">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>
<span data-ttu-id="d3373-103">Permet de vous permettent de définir des informations sur la méthode async facultatif pour chaque symbole de méthode.</span><span class="sxs-lookup"><span data-stu-id="d3373-103">Allows you to define optional async method information for each method symbol.</span></span> <span data-ttu-id="d3373-104">Toujours utiliser avec une méthode ouverte ; Autrement dit, entre les appels à la [OpenMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md) et [CloseMethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closemethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="d3373-104">Always use with an opened method; that is, between calls to the [OpenMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md) and the [CloseMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closemethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3373-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3373-105">Syntax</span></span>  
  
```idl  
[object,uuid(FC073774-1739-4232-BD56-A027294BEC15),pointer_default(unique)]interface ISymUnmanagedAsyncMethodPropertiesWriter : IUnknown  
```  
  
## <a name="methods"></a><span data-ttu-id="d3373-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d3373-106">Methods</span></span>  
 <span data-ttu-id="d3373-107">Cette interface contient les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d3373-107">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="d3373-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="d3373-108">Method</span></span>|<span data-ttu-id="d3373-109">Description</span><span class="sxs-lookup"><span data-stu-id="d3373-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d3373-110">DefineAsyncStepInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="d3373-110">DefineAsyncStepInfo Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md)|<span data-ttu-id="d3373-111">Définir un groupe d’async await des opérations dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="d3373-111">Define a group of async await operations in the current method.</span></span><br /><br /> <span data-ttu-id="d3373-112">Chaque décalage yield correspond à l’instruction de retour d’une expression await, identifiant un rendement potentiel.</span><span class="sxs-lookup"><span data-stu-id="d3373-112">Each yield offset matches an await's return instruction, identifying a potential yield.</span></span> <span data-ttu-id="d3373-113">Chaque `breakpointMethod` / `breakpointOffset` paire identifie où l’opération asynchrone reprendra ; il peut être dans une méthode différente.</span><span class="sxs-lookup"><span data-stu-id="d3373-113">Each `breakpointMethod`/`breakpointOffset` pair identifies where the asynchronous operation will resume; it may be in a different method.</span></span>|  
|[<span data-ttu-id="d3373-114">DefineCatchHandlerILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="d3373-114">DefineCatchHandlerILOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md)|<span data-ttu-id="d3373-115">Définit le langage intermédiaire de décalage pour le gestionnaire catch généré par le compilateur qui encapsule une méthode async.</span><span class="sxs-lookup"><span data-stu-id="d3373-115">Sets the IL offset for the compiler-generated catch handler that wraps an async method.</span></span><br /><br /> <span data-ttu-id="d3373-116">Offset IL de la capture générée est utilisé par le débogueur pour gérer les captures comme s’il s’agissait de code non-utilisateur, même si elle peut se produire dans une méthode de code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3373-116">The IL offset of the generated catch is used by the debugger to handle the catch as if it were non-user code, even though it may occur in a user code method.</span></span> <span data-ttu-id="d3373-117">En particulier, il est utilisé en réponse à une **CatchHandlerFound** événement d’exception.</span><span class="sxs-lookup"><span data-stu-id="d3373-117">In particular, it is used in response to a **CatchHandlerFound** exception event.</span></span>|  
|[<span data-ttu-id="d3373-118">DefineKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="d3373-118">DefineKickoffMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md)|<span data-ttu-id="d3373-119">Définit la méthode de départ qui lance l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="d3373-119">Sets the starting method that initiates the async operation.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d3373-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d3373-120">Requirements</span></span>  
 <span data-ttu-id="d3373-121">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d3373-121">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3373-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3373-122">See also</span></span>
- [<span data-ttu-id="d3373-123">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="d3373-123">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
