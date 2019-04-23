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
ms.openlocfilehash: a89b29cd459060c93d5ca77bb2154e1a10b02d03
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59213647"
---
# <a name="createidispatchstaforwarder-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="887ba-102">Fonction CreateIDispatchSTAForwarder (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="887ba-102">CreateIDispatchSTAForwarder Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="887ba-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="887ba-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="887ba-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de thread et de windows.</span><span class="sxs-lookup"><span data-stu-id="887ba-104">Used by the Windows Presentation Foundation (WPF) infrastructure for thread and windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="887ba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="887ba-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateIDispatchSTAForwarder(  
   __in IDispatch *pDispatchDelegate,   
   __deref_out IDispatch **ppForwarder  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="887ba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="887ba-106">Parameters</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="887ba-107">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="887ba-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="887ba-108">pDispatchDelegate</span><span class="sxs-lookup"><span data-stu-id="887ba-108">pDispatchDelegate</span></span>  
 <span data-ttu-id="887ba-109">Un pointeur vers un `IDispatch` interface.</span><span class="sxs-lookup"><span data-stu-id="887ba-109">A pointer to an `IDispatch` interface.</span></span>  
  
 <span data-ttu-id="887ba-110">ppForwarder</span><span class="sxs-lookup"><span data-stu-id="887ba-110">ppForwarder</span></span>  
 <span data-ttu-id="887ba-111">Un pointeur vers l’adresse d’un `IDispatch` interface.</span><span class="sxs-lookup"><span data-stu-id="887ba-111">A pointer to the address of an `IDispatch` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="887ba-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="887ba-112">Requirements</span></span>  
 <span data-ttu-id="887ba-113">**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="887ba-113">**Platforms:** See [.NET Framework System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="887ba-114">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="887ba-114">**DLL:**</span></span>  
  
 <span data-ttu-id="887ba-115">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="887ba-115">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="887ba-116">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="887ba-116">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="887ba-117">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="887ba-117">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="887ba-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="887ba-118">See also</span></span>

- [<span data-ttu-id="887ba-119">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="887ba-119">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
