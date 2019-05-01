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
# <a name="deploy-to-azure-kubernetes-service-aks"></a>Déployer sur Azure Kubernetes Service (AKS)

Vous pouvez interagir avec AKS à l’aide de votre système d’exploitation de client préférée, nous montrons ici comment procéder avec Microsoft Windows et une version incorporée de Ubuntu Linux dans Windows, à l’aide de commandes Bash.

Conditions préalables pour avoir avant d’utiliser ACS sont :

- Ordinateur de développement Linux ou Mac
- Ordinateur de développement Windows
  - Mode développeur est activé sur Windows
  - Sous-système Windows pour Linux
- Azure-CLI est installée sur [Windows, Mac ou Linux](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest)

> [!NOTE]
> Pour trouver des informations complètes sur :
>
> Azure-CLI : <https://docs.microsoft.com/cli/azure/index?view=azure-cli-latest>
>
> Sous-système Windows pour Linux : <https://docs.microsoft.com/windows/wsl/about>

## <a name="create-the-aks-environment-in-azure"></a>Créez l’environnement d’ACS dans Azure

Il existe plusieurs façons de créer l’environnement AKS. Il est possible à l’aide des commandes Azure CLI ou à l’aide du portail Azure.

Ici, vous pouvez explorer des exemples à l’aide de l’interface CLI Azure pour créer le cluster et le portail Azure pour passer en revue les résultats. Vous devez également avoir Kubectl et Docker sur votre ordinateur de développement.  

## <a name="create-the-aks-cluster"></a>Créer le cluster AKS

Créez le cluster AKS à l’aide de cette commande :

```console
az aks create --resource-group MSSampleResourceGroup --name MSSampleClusterK801 --agent-count 1 --generate-ssh-keys --location westus2
```

Une fois la tâche de création terminée, vous pouvez voir le AKS créé dans le portail Azure :

Le groupe de ressources :

![Vue du navigateur du groupe de ressources Azure ACS.](media/aks-resource-group-view.png)

**Figure 4-17**. Affichage du groupe de ressources AKS à partir d’Azure.

Le cluster AKS :

![Vue du navigateur d’un groupe de ressources AKS.](media/aks-cluster-view.png)

**Figure 4-18**. Vue d’AKS à partir d’Azure.

Vous pouvez également afficher le nœud créé à l’aide `Azure-CLI` et `Kubectl`.

Tout d’abord, obtenir les informations d’identification :

```console
az aks get-credentials --resource-group MSSampleK8ClusterRG --name MSSampleK8Cluster
```

![Console de sortie à partir de la commande ci-dessus : Fusionné « MsSampleK8Cluster comme contexte actuel dans /root/.kube/config.](media/get-credentials-command-result.png)

**Figure 4-19**. `aks get-credentials` résultat de la commande.

Puis, l’obtention de nœuds à partir de Kubectl :

```console
kubectl get nodes
```

![Sortie mentionnée plus haut la commande de la console : Liste de nœuds avec état, l’âge (temps en cours d’exécution) et version](media/kubectl-get-nodes-command-result.png)

**Figure 4-20**. `kubectl get nodes` résultat de la commande.

>[!div class="step-by-step"]
>[Précédent](orchestrate-high-scalability-availability.md)
>[Suivant](docker-apps-development-environment.md)
