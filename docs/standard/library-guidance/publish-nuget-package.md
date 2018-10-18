---
title: Publication d’un package NuGet
description: Meilleures pratiques recommandées pour la publication des bibliothèques .NET sur NuGet.
author: jamesnk
ms.author: mairaw
ms.date: 10/02/2018
ms.openlocfilehash: 0602712311411ef3d59825bec8c5e550bc8d8265
ms.sourcegitcommit: d88024e6d6d8b242feae5f4007a709379355aa24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2018
ms.locfileid: "49370049"
---
# <a name="publishing-a-nuget-package"></a><span data-ttu-id="d7181-103">Publication d’un package NuGet</span><span class="sxs-lookup"><span data-stu-id="d7181-103">Publishing a NuGet package</span></span>

<span data-ttu-id="d7181-104">Les packages NuGet sont publiés et consommés à partir de référentiels de packages.</span><span class="sxs-lookup"><span data-stu-id="d7181-104">NuGet packages are published and consumed from package repositories.</span></span> <span data-ttu-id="d7181-105">Tandis que NuGet.org est le plus largement connue et utilisée, il existe de nombreux endroits pour publier les packages NuGet :</span><span class="sxs-lookup"><span data-stu-id="d7181-105">While NuGet.org is the most widely known and used repository, there are many places to publish NuGet packages:</span></span>

* <span data-ttu-id="d7181-106">**[NuGet.org](https://www.nuget.org/)**  est le référentiel principal en ligne pour les packages NuGet.</span><span class="sxs-lookup"><span data-stu-id="d7181-106">**[NuGet.org](https://www.nuget.org/)** is the primary online repository for NuGet packages.</span></span> <span data-ttu-id="d7181-107">Tous les packages sur NuGet.org sont accessibles à tout le monde.</span><span class="sxs-lookup"><span data-stu-id="d7181-107">All packages on NuGet.org are publicly available to everyone.</span></span> <span data-ttu-id="d7181-108">Par défaut, Visual Studio a NuGet.org comme source de package et pour de nombreux développeurs NuGet.org est le seul référentiel de package qu’ils allez interagir avec.</span><span class="sxs-lookup"><span data-stu-id="d7181-108">By default, Visual Studio has NuGet.org as a package source and for many developers NuGet.org is the only package repository they'll interact with.</span></span> <span data-ttu-id="d7181-109">NuGet.org est le meilleur endroit pour publier des packages stables et préliminaires les packages que vous voulez les commentaires de la Communauté sur.</span><span class="sxs-lookup"><span data-stu-id="d7181-109">NuGet.org is the best place to publish stable packages and pre-release packages that you want community feedback on.</span></span>

* <span data-ttu-id="d7181-110">**[MyGet](https://myget.org/)**  prend en charge du service de référentiel [de flux de package personnalisé gratuit pour les projets open source](https://www.myget.org/opensource).</span><span class="sxs-lookup"><span data-stu-id="d7181-110">**[MyGet](https://myget.org/)** repository service supports [free custom package feeds for open-source projects](https://www.myget.org/opensource).</span></span> <span data-ttu-id="d7181-111">Un flux personnalisé public MyGet est un endroit idéal pour publier des packages en préversion créés par votre service d’intégration continue.</span><span class="sxs-lookup"><span data-stu-id="d7181-111">A MyGet public custom feed is an ideal place to publish pre-release packages created by your CI service.</span></span> <span data-ttu-id="d7181-112">MyGet fournit également les flux privés dans le commerce.</span><span class="sxs-lookup"><span data-stu-id="d7181-112">MyGet also provides private feeds commercially.</span></span>

* <span data-ttu-id="d7181-113">Un **[flux local](/nuget/hosting-packages/local-feeds)** vous permet de traiter un dossier comme un référentiel de packages et rend le `*.nupkg` fichiers dans le dossier accessible par NuGet.</span><span class="sxs-lookup"><span data-stu-id="d7181-113">A **[local feed](/nuget/hosting-packages/local-feeds)** allows you to treat a folder like a package repository and makes the `*.nupkg` files in the folder accessible by NuGet.</span></span> <span data-ttu-id="d7181-114">Un flux local est utile pour tester un package NuGet avant sa publication sur NuGet.org.</span><span class="sxs-lookup"><span data-stu-id="d7181-114">A local feed is useful for testing a NuGet package before publishing it to NuGet.org.</span></span>

> [!NOTE]
> <span data-ttu-id="d7181-115">NuGet.org [n’autorise pas un package à supprimer](/nuget/policies/deleting-packages) une fois qu’il est chargé.</span><span class="sxs-lookup"><span data-stu-id="d7181-115">NuGet.org [does not allow a package to be deleted](/nuget/policies/deleting-packages) once it is uploaded.</span></span> <span data-ttu-id="d7181-116">Un package peut être retirée de la liste afin qu’il ne soit pas publiquement visible dans l’interface utilisateur, mais le `*.nupkg` peut toujours être téléchargé sur la restauration.</span><span class="sxs-lookup"><span data-stu-id="d7181-116">A package can be unlisted so that it is not publicly visible in the UI but the `*.nupkg` can still be downloaded on restore.</span></span> <span data-ttu-id="d7181-117">En outre, nuget.org n’autorise pas les versions de package en double.</span><span class="sxs-lookup"><span data-stu-id="d7181-117">Also, nuget.org does not allow duplicate package versions.</span></span> <span data-ttu-id="d7181-118">Pour corriger un package NuGet avec une erreur d’avoir au retirer de la liste le package incorrect, incrémenter le numéro de version et publier une nouvelle version du package.</span><span class="sxs-lookup"><span data-stu-id="d7181-118">To correct a NuGet package with an error you have to unlist the incorrect package, increment the version number and publish a new version of the package.</span></span>

<span data-ttu-id="d7181-119">**FAIRE ✔️** [publier des packages stables et préliminaires](/nuget/create-packages/publish-a-package) vous souhaitez que les commentaires de la Communauté sur NuGet.org.</span><span class="sxs-lookup"><span data-stu-id="d7181-119">**✔️ DO** [publish stable packages and pre-release packages](/nuget/create-packages/publish-a-package) you want community feedback on to NuGet.org.</span></span>

<span data-ttu-id="d7181-120">**ENVISAGEZ de ✔️** packages de préversion de publication pour un MyGet flux à partir d’une build d’intégration continue.</span><span class="sxs-lookup"><span data-stu-id="d7181-120">**✔️ CONSIDER** publishing pre-release packages to a MyGet feed from a continuous integration build.</span></span>

<span data-ttu-id="d7181-121">**ENVISAGEZ de ✔️** test des packages dans votre environnement de développement à l’aide d’un flux local ou un MyGet.</span><span class="sxs-lookup"><span data-stu-id="d7181-121">**✔️ CONSIDER** testing packages in your development environment using a local feed or MyGet.</span></span> <span data-ttu-id="d7181-122">Vérifier le fonctionnement du package, puis publiez-le sur NuGet.org.</span><span class="sxs-lookup"><span data-stu-id="d7181-122">Check the package works then publish it to NuGet.org.</span></span>

## <a name="nugetorg-security"></a><span data-ttu-id="d7181-123">Sécurité de NuGet.org</span><span class="sxs-lookup"><span data-stu-id="d7181-123">NuGet.org security</span></span>

<span data-ttu-id="d7181-124">Il est important que les mauvais acteurs ne peut pas accéder à votre compte de NuGet et charger une version malveillante de votre bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d7181-124">It's important that bad actors can't access your NuGet account and upload a malicious version of your library.</span></span> <span data-ttu-id="d7181-125">NuGet.org offre deux facteurs d’authentification et les notifications électroniques lors de la publication d’un package.</span><span class="sxs-lookup"><span data-stu-id="d7181-125">NuGet.org offers two-factor authentication and email notifications when a package is published.</span></span> <span data-ttu-id="d7181-126">Activer ces fonctionnalités une fois connecté à NuGet.org sur le **paramètres du compte** page.</span><span class="sxs-lookup"><span data-stu-id="d7181-126">Enable these features after logging into NuGet.org on the **Account settings** page.</span></span>

<span data-ttu-id="d7181-127">![texte de remplacement](./media/publish-nuget-package/nuget-2fa.png "sécurité du compte NuGet")</span><span class="sxs-lookup"><span data-stu-id="d7181-127">![alt text](./media/publish-nuget-package/nuget-2fa.png "NuGet Account Security")</span></span>

<span data-ttu-id="d7181-128">**FAIRE ✔️** utiliser un compte Microsoft pour vous connecter à NuGet.</span><span class="sxs-lookup"><span data-stu-id="d7181-128">**✔️ DO** use a Microsoft account to sign in to NuGet.</span></span>

<span data-ttu-id="d7181-129">**FAIRE ✔️** activer l’authentification à deux facteurs pour accéder à NuGet.</span><span class="sxs-lookup"><span data-stu-id="d7181-129">**✔️ DO** enable two-factor authentication for accessing NuGet.</span></span>

<span data-ttu-id="d7181-130">**FAIRE ✔️** activer la notification par courrier électronique lorsqu’un package est publié.</span><span class="sxs-lookup"><span data-stu-id="d7181-130">**✔️ DO** enable email notification when a package is published.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="d7181-131">[Précédent](./sourcelink.md)
[Suivant](./versioning.md)</span><span class="sxs-lookup"><span data-stu-id="d7181-131">[Previous](./sourcelink.md)
[Next](./versioning.md)</span></span>
