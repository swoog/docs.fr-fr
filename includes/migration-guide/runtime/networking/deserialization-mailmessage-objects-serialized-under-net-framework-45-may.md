---
ms.openlocfilehash: a6f93bbdf39a1b525e2daeb12afc3a6392a66e30
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235383"
---
### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a><span data-ttu-id="51cf2-101">La désérialisation des objets MailMessage sérialisés sous .NET Framework 4.5 peut échouer</span><span class="sxs-lookup"><span data-stu-id="51cf2-101">Deserialization of MailMessage objects serialized under the .NET Framework 4.5 may fail</span></span>

|   |   |
|---|---|
|<span data-ttu-id="51cf2-102">Détails</span><span class="sxs-lookup"><span data-stu-id="51cf2-102">Details</span></span>|<span data-ttu-id="51cf2-103">À compter de .NET Framework 4.5, les objets <xref:System.Web.Mail.MailMessage> peuvent inclure des caractères non-ASCII.</span><span class="sxs-lookup"><span data-stu-id="51cf2-103">Starting with the .NET Framework 4.5, <xref:System.Web.Mail.MailMessage> objects can include non-ASCII characters.</span></span> <span data-ttu-id="51cf2-104">Dans le .NET Framework 4, seuls les caractères ASCII sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="51cf2-104">In the .NET Framework 4, only ASCII characters are supported.</span></span> <xref:System.Web.Mail.MailMessage> <span data-ttu-id="51cf2-105">Les objets contenant des caractères hors ASCII et sérialisés dans .NET Framework 4.5 ou une version ultérieure ne sont pas désérialisables dans .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="51cf2-105">objects that contain non-ASCII characters and that are serialized under the .NET Framework 4.5 or later cannot be deserialized under the .NET Framework 4.</span></span>|
|<span data-ttu-id="51cf2-106">Suggestion</span><span class="sxs-lookup"><span data-stu-id="51cf2-106">Suggestion</span></span>|<span data-ttu-id="51cf2-107">Vérifiez que votre code assure la gestion des exceptions lors de la désérialisation d’un objet <xref:System.Web.Mail.MailMessage>.</span><span class="sxs-lookup"><span data-stu-id="51cf2-107">Ensure that your code provides exception handling when deserializing a <xref:System.Web.Mail.MailMessage> object.</span></span>|
|<span data-ttu-id="51cf2-108">Portée</span><span class="sxs-lookup"><span data-stu-id="51cf2-108">Scope</span></span>|<span data-ttu-id="51cf2-109">Mineur</span><span class="sxs-lookup"><span data-stu-id="51cf2-109">Minor</span></span>|
|<span data-ttu-id="51cf2-110">Version</span><span class="sxs-lookup"><span data-stu-id="51cf2-110">Version</span></span>|<span data-ttu-id="51cf2-111">4.5</span><span class="sxs-lookup"><span data-stu-id="51cf2-111">4.5</span></span>|
|<span data-ttu-id="51cf2-112">Type</span><span class="sxs-lookup"><span data-stu-id="51cf2-112">Type</span></span>|<span data-ttu-id="51cf2-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="51cf2-113">Runtime</span></span>|
|<span data-ttu-id="51cf2-114">API affectées</span><span class="sxs-lookup"><span data-stu-id="51cf2-114">Affected APIs</span></span>|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|
