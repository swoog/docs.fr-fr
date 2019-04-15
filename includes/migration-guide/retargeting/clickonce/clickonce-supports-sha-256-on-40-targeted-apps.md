---
ms.openlocfilehash: 0358450024607a985f38564ec9743ba964949e8f
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234487"
---
### <a name="clickonce-supports-sha-256-on-40-targeted-apps"></a><span data-ttu-id="aef37-101">ClickOnce prend en charge SHA-256 sur les applications ciblées par la version 4.0</span><span class="sxs-lookup"><span data-stu-id="aef37-101">ClickOnce supports SHA-256 on 4.0-targeted apps</span></span>

|   |   |
|---|---|
|<span data-ttu-id="aef37-102">Détails</span><span class="sxs-lookup"><span data-stu-id="aef37-102">Details</span></span>|<span data-ttu-id="aef37-103">Avant, une application ClickOnce disposant d’un certificat signé avec SHA-256 nécessitait la présence de .NET Framework 4.5 ou ultérieur, même si l’application ciblait la version 4.0.</span><span class="sxs-lookup"><span data-stu-id="aef37-103">Previously, a ClickOnce app with a certificate signed with SHA-256 would require .NET Framework 4.5 or later to be present, even if the app targeted 4.0.</span></span> <span data-ttu-id="aef37-104">Désormais, les applications ClickOnce ciblées par .NET Framework 4.0 peuvent s’exécuter sur .NET Framework 4.0, même si elles sont signées avec SHA-256.</span><span class="sxs-lookup"><span data-stu-id="aef37-104">Now, .NET Framework 4.0-targeted ClickOnce apps can run on .NET Framework 4.0, even if signed with SHA-256.</span></span>|
|<span data-ttu-id="aef37-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="aef37-105">Suggestion</span></span>|<span data-ttu-id="aef37-106">Ce changement supprime cette dépendance et permet aux certificats SHA-256 d’être utilisés pour signer des applications ClickOnce qui ciblent .NET Framework 4 et les versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="aef37-106">This change removes that dependency and allows SHA-256 certificates to be used to sign ClickOnce apps that target .NET Framework 4 and earlier versions.</span></span>|
|<span data-ttu-id="aef37-107">Portée</span><span class="sxs-lookup"><span data-stu-id="aef37-107">Scope</span></span>|<span data-ttu-id="aef37-108">Mineur</span><span class="sxs-lookup"><span data-stu-id="aef37-108">Minor</span></span>|
|<span data-ttu-id="aef37-109">Version</span><span class="sxs-lookup"><span data-stu-id="aef37-109">Version</span></span>|<span data-ttu-id="aef37-110">4.6</span><span class="sxs-lookup"><span data-stu-id="aef37-110">4.6</span></span>|
|<span data-ttu-id="aef37-111">Type</span><span class="sxs-lookup"><span data-stu-id="aef37-111">Type</span></span>|<span data-ttu-id="aef37-112">Reciblage</span><span class="sxs-lookup"><span data-stu-id="aef37-112">Retargeting</span></span>|
