---
ms.openlocfilehash: 318609c15d2e0b9a7ee59b38463735b33ef87974
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59236191"
---
### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a><span data-ttu-id="5de80-101">PipeConnection.GetHashAlgorithm dans WCF utilise maintenant SHA256</span><span class="sxs-lookup"><span data-stu-id="5de80-101">WCF PipeConnection.GetHashAlgorithm now uses SHA256</span></span>

|   |   |
|---|---|
|<span data-ttu-id="5de80-102">Détails</span><span class="sxs-lookup"><span data-stu-id="5de80-102">Details</span></span>|<span data-ttu-id="5de80-103">À compter de .NET Framework 4.7.1, Windows Communication Foundation utilise un hachage SHA256 pour générer des noms aléatoires pour les canaux nommés.</span><span class="sxs-lookup"><span data-stu-id="5de80-103">Starting with the .NET Framework 4.7.1, Windows Communication Foundation uses a SHA256 hash to generate random names for named pipes.</span></span> <span data-ttu-id="5de80-104">Dans .NET Framework 4.7 et versions antérieures, il utilisait un hachage SHA1.</span><span class="sxs-lookup"><span data-stu-id="5de80-104">In the .NET Framework 4.7 and earlier versions, it used a SHA1 hash.</span></span>|
|<span data-ttu-id="5de80-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="5de80-105">Suggestion</span></span>|<span data-ttu-id="5de80-106">Si vous rencontrez des problèmes de compatibilité avec cette modification dans .NET Framework 4.7.1 ou version ultérieure, vous pouvez choisir de ne pas y adhérer en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> de votre fichier app.config :</span><span class="sxs-lookup"><span data-stu-id="5de80-106">If you run into compatibility issue with this change on the .NET Framework 4.7.1 or later, you can opt-out it by adding the following line to the <code>&lt;runtime&gt;</code> section of your app.config file:</span></span><pre><code class="lang-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="5de80-107">Portée</span><span class="sxs-lookup"><span data-stu-id="5de80-107">Scope</span></span>|<span data-ttu-id="5de80-108">Mineur</span><span class="sxs-lookup"><span data-stu-id="5de80-108">Minor</span></span>|
|<span data-ttu-id="5de80-109">Version</span><span class="sxs-lookup"><span data-stu-id="5de80-109">Version</span></span>|<span data-ttu-id="5de80-110">4.7.1</span><span class="sxs-lookup"><span data-stu-id="5de80-110">4.7.1</span></span>|
|<span data-ttu-id="5de80-111">Type</span><span class="sxs-lookup"><span data-stu-id="5de80-111">Type</span></span>|<span data-ttu-id="5de80-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="5de80-112">Runtime</span></span>|
