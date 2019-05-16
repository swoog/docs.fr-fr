---
title: Téléchargement du package du Gestionnaire de jetons Web JSON
ms.date: 10/10/2018
ms.assetid: d12b3f5b-f1f1-4a9d-a159-0c13e5976c90
ms.openlocfilehash: a8685a71d46778d932595965f32c0041b176bd83
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633524"
---
# <a name="download-the-json-web-token-handler-package"></a><span data-ttu-id="e808b-102">Télécharger le Package du Gestionnaire de jetons Web JSON</span><span class="sxs-lookup"><span data-stu-id="e808b-102">Download the JSON Web Token Handler Package</span></span>

<span data-ttu-id="e808b-103">Cette rubrique explique comment télécharger et utiliser le Gestionnaire de jetons Web JSON dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="e808b-103">This topic discusses how to download and use the JSON Web Token Handler in your project.</span></span>

<span data-ttu-id="e808b-104">L’extension du Gestionnaire de jetons Web JSON est disponible sous forme de package NuGet, qui ajoute les assemblys et les références nécessaires à votre projet.</span><span class="sxs-lookup"><span data-stu-id="e808b-104">The JSON Web Token Handler extension is available as a NuGet package, which adds the necessary assemblies and references to your project.</span></span> <span data-ttu-id="e808b-105">Si vous n’avez pas encore installé NuGet, accédez à [nuget.org](https://nuget.org) pour l’installer.</span><span class="sxs-lookup"><span data-stu-id="e808b-105">If you do not already have NuGet installed, go to [nuget.org](https://nuget.org) to install it.</span></span> <span data-ttu-id="e808b-106">Vous pouvez consulter l’historique de contrôle de version pour l’extension en visitant sa page sur NuGet : [Gestionnaire de jetons Web JSON sur NuGet](https://www.nuget.org/packages/System.IdentityModel.Tokens.Jwt/)</span><span class="sxs-lookup"><span data-stu-id="e808b-106">You can see the versioning history for the extension by visiting its page on NuGet: [JSON Web Token Handler on NuGet](https://www.nuget.org/packages/System.IdentityModel.Tokens.Jwt/)</span></span>

## <a name="use-the-package-manager-gui"></a><span data-ttu-id="e808b-107">Utiliser l’interface utilisateur graphique du Gestionnaire de Package</span><span class="sxs-lookup"><span data-stu-id="e808b-107">Use the Package Manager GUI</span></span>

1. <span data-ttu-id="e808b-108">Dans Visual Studio, cliquez sur votre projet dans l’**Explorateur de solutions**, puis sélectionnez **Gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="e808b-108">In Visual Studio, right-click your project in **Solution Explorer**, and then select **Manage NuGet Packages**.</span></span>

2. <span data-ttu-id="e808b-109">Dans la fenêtre **Gérer les packages NuGet**, cliquez sur la zone de recherche et tapez `JWT Token Handler`, puis appuyez sur **Entrée**.</span><span class="sxs-lookup"><span data-stu-id="e808b-109">In the **Manage NuGet Packages** window, click the search box and enter `JWT Token Handler` and press **Enter**.</span></span>

3. <span data-ttu-id="e808b-110">Dans le volet de résultats, cliquez sur le bouton **Installer** pour le premier résultat.</span><span class="sxs-lookup"><span data-stu-id="e808b-110">From the results pane, click the **Install** button for the first result.</span></span>

4. <span data-ttu-id="e808b-111">Le téléchargement du package commence.</span><span class="sxs-lookup"><span data-stu-id="e808b-111">The package will begin downloading.</span></span> <span data-ttu-id="e808b-112">Avant l’ajout du package à votre projet, la boîte de dialogue d’acceptation de licence s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e808b-112">Before it is added to your project, the License Acceptance dialog will appear.</span></span> <span data-ttu-id="e808b-113">Si vous êtes d’accord avec les termes du contrat de licence, cliquez sur **Accepter**.</span><span class="sxs-lookup"><span data-stu-id="e808b-113">If you agree to the license terms, click **I Accept**.</span></span>

5. <span data-ttu-id="e808b-114">Les assemblys du Gestionnaire de jetons Web JSON les plus récents seront téléchargés et ajoutés à votre projet.</span><span class="sxs-lookup"><span data-stu-id="e808b-114">The latest JSON Web Token Handler assemblies will be downloaded and added to your project.</span></span>

## <a name="use-the-package-manager-console"></a><span data-ttu-id="e808b-115">Utilisez la Console du Gestionnaire de Package</span><span class="sxs-lookup"><span data-stu-id="e808b-115">Use the Package Manager Console</span></span>

1. <span data-ttu-id="e808b-116">Dans Visual Studio, cliquez sur **outils** > **Gestionnaire de Package NuGet** > **Console du Gestionnaire de Package**.</span><span class="sxs-lookup"><span data-stu-id="e808b-116">In Visual Studio, click **Tools** > **NuGet Package Manager** > **Package Manager Console**.</span></span>

2. <span data-ttu-id="e808b-117">La **Console du Gestionnaire de package** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e808b-117">The **Package Manager Console** appears.</span></span> <span data-ttu-id="e808b-118">Tapez le texte suivant et appuyez sur **Entrée** :</span><span class="sxs-lookup"><span data-stu-id="e808b-118">Enter the following text and press **Enter**:</span></span>

    ```powershell
    Install-Package System.IdentityModel.Tokens.Jwt
    ```

3. <span data-ttu-id="e808b-119">Les assemblys du Gestionnaire de jetons Web JSON les plus récents seront téléchargés et ajoutés à votre projet.</span><span class="sxs-lookup"><span data-stu-id="e808b-119">The latest JSON Web Token Handler assemblies will be downloaded and added to your project.</span></span>
