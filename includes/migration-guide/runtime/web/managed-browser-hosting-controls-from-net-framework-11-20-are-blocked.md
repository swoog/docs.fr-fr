---
ms.openlocfilehash: 38c35f3f6f2262d06409690d2326d9b982e1ec86
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59803818"
---
### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a><span data-ttu-id="338ba-101">Les navigateurs managés hébergeant des contrôles de .NET Framework 1.1 et 2.0 sont bloqués</span><span class="sxs-lookup"><span data-stu-id="338ba-101">Managed browser hosting controls from the .NET Framework 1.1 and 2.0 are blocked</span></span>

|   |   |
|---|---|
|<span data-ttu-id="338ba-102">Détails</span><span class="sxs-lookup"><span data-stu-id="338ba-102">Details</span></span>|<span data-ttu-id="338ba-103">L'hébergement de ces contrôles est bloqué dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="338ba-103">Hosting these controls is blocked in Internet Explorer.</span></span>|
|<span data-ttu-id="338ba-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="338ba-104">Suggestion</span></span>|<span data-ttu-id="338ba-105">Internet Explorer ne démarrera pas les applications qui utilisent des contrôles d'hébergement de navigateur géré.</span><span class="sxs-lookup"><span data-stu-id="338ba-105">Internet Explorer will fail to launch an application that uses managed browser hosting controls.</span></span> <span data-ttu-id="338ba-106">Le comportement précédent peut être restauré en définissant la valeur de EnableIEHosting de la sous-clé de Registre <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> sur <code>1</code> pour les systèmes x86 et pour les processus 32 bits sur les systèmes x64, et définissant la valeur <code>EnableIEHosting</code> de la sous-clé de Registre <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code> sur <code>1</code> pour les processus 64 bits sur les systèmes x64.</span><span class="sxs-lookup"><span data-stu-id="338ba-106">The previous behavior can be restored by setting the EnableIEHosting value of the registry subkey <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> to <code>1</code> for x86 systems and for 32-bit processes on x64 systems, and by setting the <code>EnableIEHosting</code> value of the registry subkey <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code> to <code>1</code> for 64-bit processes on x64 systems.</span></span>|
|<span data-ttu-id="338ba-107">Portée</span><span class="sxs-lookup"><span data-stu-id="338ba-107">Scope</span></span>|<span data-ttu-id="338ba-108">Mineur</span><span class="sxs-lookup"><span data-stu-id="338ba-108">Minor</span></span>|
|<span data-ttu-id="338ba-109">Version</span><span class="sxs-lookup"><span data-stu-id="338ba-109">Version</span></span>|<span data-ttu-id="338ba-110">4.5</span><span class="sxs-lookup"><span data-stu-id="338ba-110">4.5</span></span>|
|<span data-ttu-id="338ba-111">Type</span><span class="sxs-lookup"><span data-stu-id="338ba-111">Type</span></span>|<span data-ttu-id="338ba-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="338ba-112">Runtime</span></span>|
