---
title: Fonction LoadFromHistory (référence des API non managées WPF)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- LoadFromHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: d037c062-a911-4949-b251-ccd3e48b1d17
ms.openlocfilehash: 42be46d836a299139bded938237fe2a06e9794a5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54646930"
---
# <a name="loadfromhistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="3aa83-102">Fonction LoadFromHistory (référence des API non managées WPF)</span><span class="sxs-lookup"><span data-stu-id="3aa83-102">LoadFromHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="3aa83-103">Cette API prend en charge l’infrastructure Windows Presentation Foundation (WPF) et n’est pas destinée à être utilisée directement depuis votre code.</span><span class="sxs-lookup"><span data-stu-id="3aa83-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="3aa83-104">Utilisé par l’infrastructure Windows Presentation Foundation (WPF) pour la gestion de windows.</span><span class="sxs-lookup"><span data-stu-id="3aa83-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3aa83-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3aa83-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadFromHistory_export(  
        IStream* pHistoryStream,   
        IBindCtx* pBindCtx  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3aa83-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3aa83-106">Parameters</span></span>  
 <span data-ttu-id="3aa83-107">pHistoryStream</span><span class="sxs-lookup"><span data-stu-id="3aa83-107">pHistoryStream</span></span>  
 <span data-ttu-id="3aa83-108">Pointeur vers un flux d’informations d’historique.</span><span class="sxs-lookup"><span data-stu-id="3aa83-108">A pointer to a stream of history information.</span></span>  
  
 <span data-ttu-id="3aa83-109">pBindCtx</span><span class="sxs-lookup"><span data-stu-id="3aa83-109">pBindCtx</span></span>  
 <span data-ttu-id="3aa83-110">Pointeur vers un contexte de liaison.</span><span class="sxs-lookup"><span data-stu-id="3aa83-110">A pointer to a bind context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3aa83-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3aa83-111">Requirements</span></span>  
 <span data-ttu-id="3aa83-112">**Plateformes :** Consultez [requise du .NET Framework](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3aa83-112">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3aa83-113">**DLL :**</span><span class="sxs-lookup"><span data-stu-id="3aa83-113">**DLL:**</span></span>  
  
 <span data-ttu-id="3aa83-114">Dans le .NET Framework 3.0 et 3.5 : PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="3aa83-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="3aa83-115">Dans le .NET Framework 4 et versions ultérieur : PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="3aa83-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="3aa83-116">**Version du .NET framework :** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3aa83-116">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3aa83-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aa83-117">See also</span></span>
- [<span data-ttu-id="3aa83-118">Référence des API non managées WPF</span><span class="sxs-lookup"><span data-stu-id="3aa83-118">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
