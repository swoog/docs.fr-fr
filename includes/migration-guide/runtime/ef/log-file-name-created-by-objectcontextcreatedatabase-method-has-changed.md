---
ms.openlocfilehash: cf1a8169351e29c18d85303fb32d4394877448f4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235392"
---
### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a><span data-ttu-id="86001-101">Le nom du fichier journal créé par la méthode ObjectContext.CreateDatabase a été changé pour répondre aux spécifications SQL Server</span><span class="sxs-lookup"><span data-stu-id="86001-101">Log file name created by the ObjectContext.CreateDatabase method has changed to match SQL Server specifications</span></span>

|   |   |
|---|---|
|<span data-ttu-id="86001-102">Détails</span><span class="sxs-lookup"><span data-stu-id="86001-102">Details</span></span>|<span data-ttu-id="86001-103">Quand la méthode <xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name> est appelée directement ou en utilisant Code First avec le fournisseur SqlClient et une valeur AttachDBFilename dans la chaîne de connexion, elle crée un fichier journal nommé nom_fichier_log.ldf au lieu de nom_fichier.ldf (où « nom_fichier » correspond au nom du fichier spécifié par la valeur AttachDBFilename).</span><span class="sxs-lookup"><span data-stu-id="86001-103">When the <xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name> method is called either directly or by using Code First with the SqlClient provider and an AttachDBFilename value in the connection string, it creates a log file named filename_log.ldf instead of filename.ldf (where filename is the name of the file specified by the AttachDBFilename value).</span></span> <span data-ttu-id="86001-104">Cette modification améliore le débogage en fournissant un fichier journal dont le nom répond aux spécifications SQL Server.</span><span class="sxs-lookup"><span data-stu-id="86001-104">This change improves debugging by providing a log file named according to SQL Server specifications.</span></span>|
|<span data-ttu-id="86001-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="86001-105">Suggestion</span></span>|<span data-ttu-id="86001-106">Si le nom du fichier journal est important pour une application, celle-ci doit être mise à jour pour attendre le format de nom de fichier standard « _log.ldf ».</span><span class="sxs-lookup"><span data-stu-id="86001-106">If the log file name is important for an app, the app should be updated to expect the standard _log.ldf file name format.</span></span>|
|<span data-ttu-id="86001-107">Portée</span><span class="sxs-lookup"><span data-stu-id="86001-107">Scope</span></span>|<span data-ttu-id="86001-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="86001-108">Edge</span></span>|
|<span data-ttu-id="86001-109">Version</span><span class="sxs-lookup"><span data-stu-id="86001-109">Version</span></span>|<span data-ttu-id="86001-110">4.5</span><span class="sxs-lookup"><span data-stu-id="86001-110">4.5</span></span>|
|<span data-ttu-id="86001-111">Type</span><span class="sxs-lookup"><span data-stu-id="86001-111">Type</span></span>|<span data-ttu-id="86001-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="86001-112">Runtime</span></span>|
|<span data-ttu-id="86001-113">API affectées</span><span class="sxs-lookup"><span data-stu-id="86001-113">Affected APIs</span></span>|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|
