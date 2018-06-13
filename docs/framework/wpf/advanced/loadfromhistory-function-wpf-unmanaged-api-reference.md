---
title: LoadFromHistory (fonction) (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- LoadFromHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: d037c062-a911-4949-b251-ccd3e48b1d17
ms.openlocfilehash: 19674b45af84e1e6a6ca169f7b6654c6e3847416
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33544662"
---
# <a name="loadfromhistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="816fe-102">LoadFromHistory (fonction) (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="816fe-102">LoadFromHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="816fe-103">Cette API prend en charge l’infrastructure de Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="816fe-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="816fe-104">Utilisée par l’infrastructure de Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="816fe-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="816fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="816fe-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadFromHistory_export(  
        IStream* pHistoryStream,   
        IBindCtx* pBindCtx  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="816fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="816fe-106">Parameters</span></span>  
 <span data-ttu-id="816fe-107">pHistoryStream</span><span class="sxs-lookup"><span data-stu-id="816fe-107">pHistoryStream</span></span>  
 <span data-ttu-id="816fe-108">Pointeur vers un flux d’informations d’historique.</span><span class="sxs-lookup"><span data-stu-id="816fe-108">A pointer to a stream of history information.</span></span>  
  
 <span data-ttu-id="816fe-109">pBindCtx</span><span class="sxs-lookup"><span data-stu-id="816fe-109">pBindCtx</span></span>  
 <span data-ttu-id="816fe-110">Pointeur vers un contexte de liaison.</span><span class="sxs-lookup"><span data-stu-id="816fe-110">A pointer to a bind context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="816fe-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="816fe-111">Requirements</span></span>  
 <span data-ttu-id="816fe-112">**Plateformes :** consultez [configuration système requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="816fe-112">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="816fe-113">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="816fe-113">**DLL:**</span></span>  
  
 <span data-ttu-id="816fe-114">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="816fe-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="816fe-115">Dans le .NET Framework 4 et versions ultérieures : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="816fe-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="816fe-116">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="816fe-116">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="816fe-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="816fe-117">See Also</span></span>  
 [<span data-ttu-id="816fe-118">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="816fe-118">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
