---
title: Orchestration des microservices et des applications à plusieurs conteneurs pour une grande scalabilité et une haute disponibilité
description: Découvrez comment déployer une application à l’aide d’Azure Kubernetes Service.
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/15/2019
ms.openlocfilehash: 82a1cf7f3cc367bfb8b8f67a130600815f2a21c4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62006548"
---
# <a name="deploy-to-azure-kubernetes-service-aks"></a><span data-ttu-id="4159e-103">Déployer sur Azure Kubernetes Service (AKS)</span><span class="sxs-lookup"><span data-stu-id="4159e-103">Deploy to Azure Kubernetes Service (AKS)</span></span>

<span data-ttu-id="4159e-104">Vous pouvez interagir avec AKS à l’aide de votre système d’exploitation de client préférée, nous montrons ici comment procéder avec Microsoft Windows et une version incorporée de Ubuntu Linux dans Windows, à l’aide de commandes Bash.</span><span class="sxs-lookup"><span data-stu-id="4159e-104">You can interact with AKS using your preferred client operating system, here we show how to do it with Microsoft Windows and an embedded version of Ubuntu Linux in Windows, using Bash commands.</span></span>

<span data-ttu-id="4159e-105">Conditions préalables pour avoir avant d’utiliser ACS sont :</span><span class="sxs-lookup"><span data-stu-id="4159e-105">Prerequisites to have before using AKS are:</span></span>

- <span data-ttu-id="4159e-106">Ordinateur de développement Linux ou Mac</span><span class="sxs-lookup"><span data-stu-id="4159e-106">Linux or Mac development machine</span></span>
- <span data-ttu-id="4159e-107">Ordinateur de développement Windows</span><span class="sxs-lookup"><span data-stu-id="4159e-107">Windows development machine</span></span>
  - <span data-ttu-id="4159e-108">Mode développeur est activé sur Windows</span><span class="sxs-lookup"><span data-stu-id="4159e-108">Developer Mode enabled on Windows</span></span>
  - <span data-ttu-id="4159e-109">Sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="4159e-109">Windows Subsystem for Linux</span></span>
- <span data-ttu-id="4159e-110">Azure-CLI est installée sur [Windows, Mac ou Linux](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest)</span><span class="sxs-lookup"><span data-stu-id="4159e-110">Azure-CLI installed on [Windows, Mac or Linux](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest)</span></span>

> [!NOTE]
> <span data-ttu-id="4159e-111">Pour trouver des informations complètes sur :</span><span class="sxs-lookup"><span data-stu-id="4159e-111">To find complete information about:</span></span>
>
> <span data-ttu-id="4159e-112">Azure-CLI : <https://docs.microsoft.com/cli/azure/index?view=azure-cli-latest></span><span class="sxs-lookup"><span data-stu-id="4159e-112">Azure-CLI: <https://docs.microsoft.com/cli/azure/index?view=azure-cli-latest></span></span>
>
> <span data-ttu-id="4159e-113">Sous-système Windows pour Linux : <https://docs.microsoft.com/windows/wsl/about></span><span class="sxs-lookup"><span data-stu-id="4159e-113">Windows Subsystem for Linux: <https://docs.microsoft.com/windows/wsl/about></span></span>

## <a name="create-the-aks-environment-in-azure"></a><span data-ttu-id="4159e-114">Créez l’environnement d’ACS dans Azure</span><span class="sxs-lookup"><span data-stu-id="4159e-114">Create the AKS environment in Azure</span></span>

<span data-ttu-id="4159e-115">Il existe plusieurs façons de créer l’environnement AKS.</span><span class="sxs-lookup"><span data-stu-id="4159e-115">There are several ways to create the AKS Environment.</span></span> <span data-ttu-id="4159e-116">Il est possible à l’aide des commandes Azure CLI ou à l’aide du portail Azure.</span><span class="sxs-lookup"><span data-stu-id="4159e-116">It can be done by using Azure-CLI commands or by using the Azure portal.</span></span>

<span data-ttu-id="4159e-117">Ici, vous pouvez explorer des exemples à l’aide de l’interface CLI Azure pour créer le cluster et le portail Azure pour passer en revue les résultats.</span><span class="sxs-lookup"><span data-stu-id="4159e-117">Here you can explore some examples using the Azure-CLI to create the cluster and the Azure portal to review the results.</span></span> <span data-ttu-id="4159e-118">Vous devez également avoir Kubectl et Docker sur votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="4159e-118">You also need to have Kubectl and Docker in your development machine.</span></span>  

## <a name="create-the-aks-cluster"></a><span data-ttu-id="4159e-119">Créer le cluster AKS</span><span class="sxs-lookup"><span data-stu-id="4159e-119">Create the AKS cluster</span></span>

<span data-ttu-id="4159e-120">Créez le cluster AKS à l’aide de cette commande :</span><span class="sxs-lookup"><span data-stu-id="4159e-120">Create the AKS cluster using this command:</span></span>

```console
az aks create --resource-group MSSampleResourceGroup --name MSSampleClusterK801 --agent-count 1 --generate-ssh-keys --location westus2
```

<span data-ttu-id="4159e-121">Une fois la tâche de création terminée, vous pouvez voir le AKS créé dans le portail Azure :</span><span class="sxs-lookup"><span data-stu-id="4159e-121">After the creation job finishes, you can see the AKS created in the Azure portal:</span></span>

<span data-ttu-id="4159e-122">Le groupe de ressources :</span><span class="sxs-lookup"><span data-stu-id="4159e-122">The resource group:</span></span>

![Vue du navigateur du groupe de ressources Azure ACS.](media/aks-resource-group-view.png)

<span data-ttu-id="4159e-124">**Figure 4-17**.</span><span class="sxs-lookup"><span data-stu-id="4159e-124">**Figure 4-17**.</span></span> <span data-ttu-id="4159e-125">Affichage du groupe de ressources AKS à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="4159e-125">AKS Resource Group view from Azure.</span></span>

<span data-ttu-id="4159e-126">Le cluster AKS :</span><span class="sxs-lookup"><span data-stu-id="4159e-126">The AKS cluster:</span></span>

![Vue du navigateur d’un groupe de ressources AKS.](media/aks-cluster-view.png)

<span data-ttu-id="4159e-128">**Figure 4-18**.</span><span class="sxs-lookup"><span data-stu-id="4159e-128">**Figure 4-18**.</span></span> <span data-ttu-id="4159e-129">Vue d’AKS à partir d’Azure.</span><span class="sxs-lookup"><span data-stu-id="4159e-129">AKS view from Azure.</span></span>

<span data-ttu-id="4159e-130">Vous pouvez également afficher le nœud créé à l’aide `Azure-CLI` et `Kubectl`.</span><span class="sxs-lookup"><span data-stu-id="4159e-130">You can also view the node created using `Azure-CLI` and `Kubectl`.</span></span>

<span data-ttu-id="4159e-131">Tout d’abord, obtenir les informations d’identification :</span><span class="sxs-lookup"><span data-stu-id="4159e-131">First, getting the credentials:</span></span>

```console
az aks get-credentials --resource-group MSSampleK8ClusterRG --name MSSampleK8Cluster
```

![Console de sortie à partir de la commande ci-dessus : Fusionné « MsSampleK8Cluster comme contexte actuel dans /root/.kube/config.](media/get-credentials-command-result.png)

<span data-ttu-id="4159e-133">**Figure 4-19**.</span><span class="sxs-lookup"><span data-stu-id="4159e-133">**Figure 4-19**.</span></span> <span data-ttu-id="4159e-134">`aks get-credentials` résultat de la commande.</span><span class="sxs-lookup"><span data-stu-id="4159e-134">`aks get-credentials` command result.</span></span>

<span data-ttu-id="4159e-135">Puis, l’obtention de nœuds à partir de Kubectl :</span><span class="sxs-lookup"><span data-stu-id="4159e-135">And then, getting nodes from Kubectl:</span></span>

```console
kubectl get nodes
```

![Sortie mentionnée plus haut la commande de la console : Liste de nœuds avec état, l’âge (temps en cours d’exécution) et version](media/kubectl-get-nodes-command-result.png)

<span data-ttu-id="4159e-137">**Figure 4-20**.</span><span class="sxs-lookup"><span data-stu-id="4159e-137">**Figure 4-20**.</span></span> <span data-ttu-id="4159e-138">`kubectl get nodes` résultat de la commande.</span><span class="sxs-lookup"><span data-stu-id="4159e-138">`kubectl get nodes` command result.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="4159e-139">[Précédent](orchestrate-high-scalability-availability.md)
>[Suivant](docker-apps-development-environment.md)</span><span class="sxs-lookup"><span data-stu-id="4159e-139">[Previous](orchestrate-high-scalability-availability.md)
[Next](docker-apps-development-environment.md)</span></span>
