---
ms.openlocfilehash: a3f5f512fd17ab2b076f868be24e5c73d8698c49
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59774233"
---
### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a><span data-ttu-id="88c87-101">ObjectDisposedException levée par le vérificateur orthographique de WPF</span><span class="sxs-lookup"><span data-stu-id="88c87-101">ObjectDisposedException thrown by WPF spellchecker</span></span>

|   |   |
|---|---|
|<span data-ttu-id="88c87-102">Détails</span><span class="sxs-lookup"><span data-stu-id="88c87-102">Details</span></span>|<span data-ttu-id="88c87-103">Les applications WPF plantent parfois lors de l’arrêt de l’application avec une <xref:System.ObjectDisposedException?displayProperty=name> levée par le vérificateur orthographique.</span><span class="sxs-lookup"><span data-stu-id="88c87-103">WPF applications occasionally crash during application shutdown with an <xref:System.ObjectDisposedException?displayProperty=name> thrown by the spellchecker.</span></span> <span data-ttu-id="88c87-104">Ce problème est résolu dans .NET Framework 4.7 WPF via une gestion différente de l’exception, qui permet aux applications de ne plus en être affectée de cette façon.</span><span class="sxs-lookup"><span data-stu-id="88c87-104">This is fixed in .NET Framework 4.7 WPF by handling the exception gracefully, and thus ensuring that applications are no longer adversely affected.</span></span> <span data-ttu-id="88c87-105">Notez que des exceptions occasionnelles continuent d’être observées dans les applications s’exécutant sous un débogueur.</span><span class="sxs-lookup"><span data-stu-id="88c87-105">It should be noted that occasional first-chance exceptions would continue to be observed in applications running under a debugger.</span></span>|
|<span data-ttu-id="88c87-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="88c87-106">Suggestion</span></span>|<span data-ttu-id="88c87-107">Mettre à niveau vers .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="88c87-107">Upgrade to .NET Framework 4.7</span></span>|
|<span data-ttu-id="88c87-108">Portée</span><span class="sxs-lookup"><span data-stu-id="88c87-108">Scope</span></span>|<span data-ttu-id="88c87-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="88c87-109">Edge</span></span>|
|<span data-ttu-id="88c87-110">Version</span><span class="sxs-lookup"><span data-stu-id="88c87-110">Version</span></span>|<span data-ttu-id="88c87-111">4.6.1</span><span class="sxs-lookup"><span data-stu-id="88c87-111">4.6.1</span></span>|
|<span data-ttu-id="88c87-112">Type</span><span class="sxs-lookup"><span data-stu-id="88c87-112">Type</span></span>|<span data-ttu-id="88c87-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="88c87-113">Runtime</span></span>|
