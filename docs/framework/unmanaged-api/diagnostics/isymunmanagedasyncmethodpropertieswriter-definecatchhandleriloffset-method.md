---
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset, méthode
ms.date: 03/30/2017
ms.assetid: 92af7896-2201-408d-8b1b-23e28001eeac
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ce462c4e7e9c8fb11ee74a91f3ece2465a44a834
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425429"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefinecatchhandleriloffset-method"></a><span data-ttu-id="19c1f-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="19c1f-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineCatchHandlerILOffset Method</span></span>
<span data-ttu-id="19c1f-103">Définit le langage intermédiaire de décalage pour le gestionnaire catch de généré par le compilateur qui encapsule une méthode async.</span><span class="sxs-lookup"><span data-stu-id="19c1f-103">Sets the IL offset for the compiler-generated catch handler that wraps an async method.</span></span>  
  
 <span data-ttu-id="19c1f-104">Par le débogueur, l’offset IL de la capture générée permet de gérer la capture comme s’il était code non-utilisateur, même si elle peut se produire dans une méthode de code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="19c1f-104">The IL offset of the generated catch is used by the debugger to handle the catch as if it were non-user code even though it might occur in a user code method.</span></span> <span data-ttu-id="19c1f-105">En particulier, il est utilisé en réponse à une **CatchHandlerFound** événement d’exception.</span><span class="sxs-lookup"><span data-stu-id="19c1f-105">In particular, it is used in response to a **CatchHandlerFound** exception event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19c1f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19c1f-106">Syntax</span></span>  
  
```idl  
HRESULT DefineCatchHandlerILOffset(    [in] ULONG32 catchHandlerOffset);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="19c1f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19c1f-107">Parameters</span></span>  
  
|<span data-ttu-id="19c1f-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="19c1f-108">Parameter</span></span>|<span data-ttu-id="19c1f-109">Description</span><span class="sxs-lookup"><span data-stu-id="19c1f-109">Description</span></span>|  
|---------------|-----------------|  
|`catchHandlerOffset`||  
  
## <a name="return-value"></a><span data-ttu-id="19c1f-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="19c1f-110">Return Value</span></span>  
 <span data-ttu-id="19c1f-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="19c1f-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="19c1f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="19c1f-112">Requirements</span></span>  
 <span data-ttu-id="19c1f-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="19c1f-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19c1f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19c1f-114">See Also</span></span>  
 [<span data-ttu-id="19c1f-115">ISymUnmanagedAsyncMethodPropertiesWriter, interface</span><span class="sxs-lookup"><span data-stu-id="19c1f-115">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
