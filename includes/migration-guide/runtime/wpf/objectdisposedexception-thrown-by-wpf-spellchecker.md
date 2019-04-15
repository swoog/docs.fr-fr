---
ms.openlocfilehash: a3f5f512fd17ab2b076f868be24e5c73d8698c49
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234139"
---
### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a><span data-ttu-id="d0968-101">ObjectDisposedException levée par le vérificateur orthographique de WPF</span><span class="sxs-lookup"><span data-stu-id="d0968-101">ObjectDisposedException thrown by WPF spellchecker</span></span>

|   |   |
|---|---|
|<span data-ttu-id="d0968-102">Détails</span><span class="sxs-lookup"><span data-stu-id="d0968-102">Details</span></span>|<span data-ttu-id="d0968-103">Les applications WPF plantent parfois lors de l’arrêt de l’application avec une <xref:System.ObjectDisposedException?displayProperty=name> levée par le vérificateur orthographique.</span><span class="sxs-lookup"><span data-stu-id="d0968-103">WPF applications occasionally crash during application shutdown with an <xref:System.ObjectDisposedException?displayProperty=name> thrown by the spellchecker.</span></span> <span data-ttu-id="d0968-104">Ce problème est résolu dans .NET Framework 4.7 WPF via une gestion différente de l’exception, qui permet aux applications de ne plus en être affectée de cette façon.</span><span class="sxs-lookup"><span data-stu-id="d0968-104">This is fixed in .NET Framework 4.7 WPF by handling the exception gracefully, and thus ensuring that applications are no longer adversely affected.</span></span> <span data-ttu-id="d0968-105">Notez que des exceptions occasionnelles continuent d’être observées dans les applications s’exécutant sous un débogueur.</span><span class="sxs-lookup"><span data-stu-id="d0968-105">It should be noted that occasional first-chance exceptions would continue to be observed in applications running under a debugger.</span></span>|
|<span data-ttu-id="d0968-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="d0968-106">Suggestion</span></span>|<span data-ttu-id="d0968-107">Mettre à niveau vers .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="d0968-107">Upgrade to .NET Framework 4.7</span></span>|
|<span data-ttu-id="d0968-108">Portée</span><span class="sxs-lookup"><span data-stu-id="d0968-108">Scope</span></span>|<span data-ttu-id="d0968-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="d0968-109">Edge</span></span>|
|<span data-ttu-id="d0968-110">Version</span><span class="sxs-lookup"><span data-stu-id="d0968-110">Version</span></span>|<span data-ttu-id="d0968-111">4.6.1</span><span class="sxs-lookup"><span data-stu-id="d0968-111">4.6.1</span></span>|
|<span data-ttu-id="d0968-112">Type</span><span class="sxs-lookup"><span data-stu-id="d0968-112">Type</span></span>|<span data-ttu-id="d0968-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="d0968-113">Runtime</span></span>|
