---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset, méthode
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 923c85a9dff11753a338fcfd3673d3590fca607a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940125"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a><span data-ttu-id="b78b5-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="b78b5-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset Method</span></span>
<span data-ttu-id="b78b5-103">Définit le langage intermédiaire de décalage pour le gestionnaire catch généré par le compilateur qui encapsule une méthode async.</span><span class="sxs-lookup"><span data-stu-id="b78b5-103">Sets the IL offset for the compiler-generated catch handler that wraps an async method.</span></span>  
  
 <span data-ttu-id="b78b5-104">L’offset IL de la capture générée est utilisé par le débogueur pour gérer les captures comme s’il s’agissait d’un code non utilisateur même si elle peut se produire dans une méthode de code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b78b5-104">The IL offset of the generated catch is used by the debugger to handle the catch as if it were non-user code even though it might occur in a user code method.</span></span> <span data-ttu-id="b78b5-105">En particulier, il est utilisé en réponse à une **CatchHandlerFound** événement d’exception.</span><span class="sxs-lookup"><span data-stu-id="b78b5-105">In particular, it is used in response to a **CatchHandlerFound** exception event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b78b5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b78b5-106">Syntax</span></span>  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b78b5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b78b5-107">Parameters</span></span>  
  
|<span data-ttu-id="b78b5-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b78b5-108">Parameter</span></span>|<span data-ttu-id="b78b5-109">Description</span><span class="sxs-lookup"><span data-stu-id="b78b5-109">Description</span></span>|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a><span data-ttu-id="b78b5-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b78b5-110">Return Value</span></span>  
 <span data-ttu-id="b78b5-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="b78b5-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b78b5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b78b5-112">Requirements</span></span>  
 <span data-ttu-id="b78b5-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b78b5-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b78b5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b78b5-114">See also</span></span>

- [<span data-ttu-id="b78b5-115">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="b78b5-115">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
