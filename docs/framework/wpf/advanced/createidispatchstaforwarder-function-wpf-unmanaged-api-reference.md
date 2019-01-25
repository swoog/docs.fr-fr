---
title: Fonction CreateIDispatchSTAForwarder (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CreateIDispatchSTAForwarder
api_location:
- PresentationHost_v0400.dll
ms.assetid: 57a02dfa-f091-4ace-9c06-1f4ab52b3527
ms.openlocfilehash: 215f6ff727b814e7e7d7c708c29a8c5221f5797f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54575980"
---
# <a name="createidispatchstaforwarder-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="c9623-102">Fonction CreateIDispatchSTAForwarder (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="c9623-102">CreateIDispatchSTAForwarder Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="c9623-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="c9623-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="c9623-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de thread et de windows.</span><span class="sxs-lookup"><span data-stu-id="c9623-104">Used by the Windows Presentation Foundation (WPF) infrastructure for thread and windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9623-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9623-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateIDispatchSTAForwarder(  
   __in IDispatch *pDispatchDelegate,   
   __deref_out IDispatch **ppForwarder  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c9623-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9623-106">Parameters</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c9623-107">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c9623-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="c9623-108">pDispatchDelegate</span><span class="sxs-lookup"><span data-stu-id="c9623-108">pDispatchDelegate</span></span>  
 <span data-ttu-id="c9623-109">Un pointeur vers un `IDispatch` interface.</span><span class="sxs-lookup"><span data-stu-id="c9623-109">A pointer to an `IDispatch` interface.</span></span>  
  
 <span data-ttu-id="c9623-110">ppForwarder</span><span class="sxs-lookup"><span data-stu-id="c9623-110">ppForwarder</span></span>  
 <span data-ttu-id="c9623-111">Un pointeur vers l’adresse d’un `IDispatch` interface.</span><span class="sxs-lookup"><span data-stu-id="c9623-111">A pointer to the address of an `IDispatch` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9623-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c9623-112">Requirements</span></span>  
 <span data-ttu-id="c9623-113">**Plateformes :** Consultez [requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c9623-113">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9623-114">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="c9623-114">**DLL:**</span></span>  
  
 <span data-ttu-id="c9623-115">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="c9623-115">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="c9623-116">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="c9623-116">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="c9623-117">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c9623-117">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9623-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9623-118">See also</span></span>
- [<span data-ttu-id="c9623-119">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="c9623-119">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
