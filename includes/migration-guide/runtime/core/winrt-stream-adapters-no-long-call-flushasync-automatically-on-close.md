---
ms.openlocfilehash: 60759e3d03137bb5983703cbf04719ba4946cb6e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235308"
---
### <a name="winrt-stream-adapters-no-long-call-flushasync-automatically-on-close"></a><span data-ttu-id="1c0d4-101">Les adaptateurs de flux WinRT n’appellent plus FlushAsync automatiquement lors de la fermeture</span><span class="sxs-lookup"><span data-stu-id="1c0d4-101">WinRT stream adapters no long call FlushAsync automatically on close</span></span>

|   |   |
|---|---|
|<span data-ttu-id="1c0d4-102">Détails</span><span class="sxs-lookup"><span data-stu-id="1c0d4-102">Details</span></span>|<span data-ttu-id="1c0d4-103">Dans les applications du Windows Store, les adaptateurs de flux Windows Runtime n’appellent plus la méthode FlushAsync à partir de la méthode Dispose.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-103">In Windows Store apps, Windows Runtime stream adapters no longer call the FlushAsync method from the Dispose method.</span></span>|
|<span data-ttu-id="1c0d4-104">Suggestion</span><span class="sxs-lookup"><span data-stu-id="1c0d4-104">Suggestion</span></span>|<span data-ttu-id="1c0d4-105">Cette modification devrait être transparente.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-105">This change should be transparent.</span></span> <span data-ttu-id="1c0d4-106">Les développeurs peuvent rétablir le comportement précédent en écrivant du code comme le suivant :</span><span class="sxs-lookup"><span data-stu-id="1c0d4-106">Developers can restore the previous behavior by writing code like this:</span></span><pre><code class="lang-csharp">using (var stream = GetWindowsRuntimeStream() as Stream)&#13;&#10;{&#13;&#10;// do something&#13;&#10;await stream.FlushAsync();&#13;&#10;}&#13;&#10;</code></pre>|
|<span data-ttu-id="1c0d4-107">Portée</span><span class="sxs-lookup"><span data-stu-id="1c0d4-107">Scope</span></span>|<span data-ttu-id="1c0d4-108">Transparent</span><span class="sxs-lookup"><span data-stu-id="1c0d4-108">Transparent</span></span>|
|<span data-ttu-id="1c0d4-109">Version</span><span class="sxs-lookup"><span data-stu-id="1c0d4-109">Version</span></span>|<span data-ttu-id="1c0d4-110">4.5.1</span><span class="sxs-lookup"><span data-stu-id="1c0d4-110">4.5.1</span></span>|
|<span data-ttu-id="1c0d4-111">Type</span><span class="sxs-lookup"><span data-stu-id="1c0d4-111">Type</span></span>|<span data-ttu-id="1c0d4-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="1c0d4-112">Runtime</span></span>|
