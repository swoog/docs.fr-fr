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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61926449"
---
# <a name="createidispatchstaforwarder-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="1b83a-102">Fonction CreateIDispatchSTAForwarder (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="1b83a-102">CreateIDispatchSTAForwarder Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="1b83a-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="1b83a-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="1b83a-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de thread et de windows.</span><span class="sxs-lookup"><span data-stu-id="1b83a-104">Used by the Windows Presentation Foundation (WPF) infrastructure for thread and windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1b83a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b83a-105">Syntax</span></span>  
  
```cpp  
HRESULT CreateIDispatchSTAForwarder(  
   __in IDispatch *pDispatchDelegate,   
   __deref_out IDispatch **ppForwarder  
)  
```  
  
## <a name="parameters"></a><span data-ttu-id="1b83a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b83a-106">Parameters</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1b83a-107">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1b83a-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="1b83a-108">pDispatchDelegate</span><span class="sxs-lookup"><span data-stu-id="1b83a-108">pDispatchDelegate</span></span>  
 <span data-ttu-id="1b83a-109">Un pointeur vers un `IDispatch` interface.</span><span class="sxs-lookup"><span data-stu-id="1b83a-109">A pointer to an `IDispatch` interface.</span></span>  
  
 <span data-ttu-id="1b83a-110">ppForwarder</span><span class="sxs-lookup"><span data-stu-id="1b83a-110">ppForwarder</span></span>  
 <span data-ttu-id="1b83a-111">Un pointeur vers l’adresse d’un `IDispatch` interface.</span><span class="sxs-lookup"><span data-stu-id="1b83a-111">A pointer to the address of an `IDispatch` interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1b83a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b83a-112">Requirements</span></span>  
 <span data-ttu-id="1b83a-113">**Plateformes :** Consultez [requise du .NET Framework](../../get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1b83a-113">**Platforms:** See [.NET Framework System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1b83a-114">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="1b83a-114">**DLL:**</span></span>  
  
 <span data-ttu-id="1b83a-115">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="1b83a-115">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="1b83a-116">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="1b83a-116">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="1b83a-117">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1b83a-117">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b83a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b83a-118">See also</span></span>

- [<span data-ttu-id="1b83a-119">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="1b83a-119">WPF Unmanaged API Reference</span></span>](wpf-unmanaged-api-reference.md)
