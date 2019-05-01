---
title: Créer des applications ASP.NET Core 2.1 déployées en tant que conteneurs Linux dans les clusters AKS/Kubernetes
description: Cycle de vie des applications Docker en conteneur avec la plateforme et les outils Microsoft
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 02/25/2019
ms.openlocfilehash: c6d778d345466b1b852d06bc01ce40ccfdebf964
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052759"
---
# <a name="build-aspnet-core-21-applications-deployed-as-linux-containers-into-an-akskubernetes-orchestrator"></a>Créer des applications ASP.NET Core 2.1 déployées comme conteneurs Linux dans un orchestrateur AKS/Kubernetes

Azure Kubernetes service (AKS) est Kubernetes orchestrations services gérés d’Azure qui simplifient la gestion et le déploiement de conteneur.

AKS les fonctionnalités principales sont :

- Un plan de contrôle hébergé sur Azure
- Mises à niveau automatisées
- Réparation automatique
- Mise à l’échelle de configurable utilisateur
- Une expérience utilisateur plus simple pour les développeurs et les opérateurs du cluster.

Les exemples suivants Explorer la création d’une application ASP.NET Core 2.1, s’exécute sur Linux et déploie vers un Cluster AKS dans Azure, tandis que le développement est effectué à l’aide de Visual Studio 2017.

## <a name="creating-the-aspnet-core-21-project-using-visual-studio-2017"></a>Création du projet ASP.NET Core 2.1 à l’aide de Visual Studio 2017

ASP.NET Core est une plateforme de développement à usage général gérée par Microsoft et la Communauté .NET sur GitHub. Il est multiplateforme, prenant en charge Windows, macOS et Linux et peut être utilisé dans l’appareil, de cloud et de systèmes embarqués/IOT.

Cet exemple utilise un projet simple qui repose sur un modèle API Web de Visual Studio, vous n’avez pas besoin d’autres bases de connaissances pour créer l’exemple. Vous devez uniquement créer le projet à l’aide d’un modèle standard qui inclut tous les éléments pour exécuter un petit projet avec une API REST, à l’aide de la technologie ASP.NET Core 2.1.

![Ajouter la fenêtre Nouveau projet dans Visual Studio, sélectionnez l’Application Web ASP.NET Core.](media/create-aspnet-core-application.png)

**Figure 4-36**. Création d’Application ASP.NET Core

Pour créer l’exemple de projet dans Visual Studio, sélectionnez **fichier** > **New** > **projet**, sélectionnez le **Web**types de projets dans le volet gauche, suivie de **Application Web ASP.NET Core**.

Répertorie les modèles pour les projets web Visual Studio. Dans notre exemple, sélectionnez **API** pour créer une Application de l’API Web ASP.NET.

Vérifiez que vous avez sélectionné ASP.NET Core 2.1 en tant que l’infrastructure. .NET core 2.1 est inclus dans la dernière version de Visual Studio 2017 et est automatiquement installé et configuré pour vous lorsque vous installez Visual Studio 2017.

![Visual Studio boîte de dialogue Choisir le type d’une Application Web ASP.NET Core avec l’option API sélectionnée.](media/create-web-api-application.png)

**Figure 4-37**. Type de projet en sélectionnant ASP.NET CORE 2.1 et l’API Web

Si vous avez des versions précédentes de .NET Core, vous pouvez télécharger et installer la version 2.1 à partir de <https://www.microsoft.com/net/download/core#/sdk>.

Vous pouvez ajouter la prise en charge Docker lors de la création du projet ou par la suite, par conséquent, vous pouvez « Dockerisez » votre projet à tout moment. Pour ajouter la prise en charge Docker après la création du projet, avec le bouton droit sur le nœud de projet dans l’Explorateur de solutions et sélectionnez **ajouter** > **prise en charge Docker** dans le menu contextuel.

![Option de menu contextuel pour ajouter la prise en charge Docker à un projet existant : Cliquez avec le bouton droit (sur le projet) > Ajouter > prise en charge Docker.](media/add-docker-support-to-project.png)

**Figure 4-38**. Ajout de prise en charge Docker à un projet existant

Pour effectuer un ajout prise en charge de Docker, vous pouvez choisir Windows ou Linux. Dans ce cas, sélectionnez **Linux**, car ACS ne prend pas en charge les conteneurs Windows (comme de fin 2018).

![Boîte de dialogue Options pour sélectionner le système d’exploitation cible pour le fichier Dockerfile.](media/select-linux-docker-support.png)

**Figure 4-39**. Sélection des conteneurs Linux.

Avec ces étapes simples, vous disposez de votre application ASP.NET Core 2.1 en cours d’exécution sur un conteneur Linux.

Comme vous pouvez le voir, l’intégration entre Visual Studio 2017 et Docker est entièrement orientée vers la productivité du développeur.

Vous pouvez maintenant exécuter votre application avec le **F5** clé ou en utilisant le **lire** bouton.

Après avoir exécuté le projet, vous pouvez répertorier les images à l’aide de la `docker images` commande. Vous devez voir le `mssampleapplication` image créée par le déploiement automatique de notre projet avec Visual Studio 2017.

```console
docker images
```

![La sortie de console à partir de la commande d’images docker, affiche une liste avec : Référentiel de balise, ID de l’Image, Created (date) et taille.](media/docker-images-command.png)

**Figure 4-40**. Affichage des images Docker

## <a name="register-the-solution-in-the-azure-container-registry"></a>Enregistrez la Solution dans le Registre de conteneurs Azure

Télécharger l’image à n’importe quel Registre Docker, comme [Azure Container Registry (ACR)](https://azure.microsoft.com/services/container-registry/) ou sur Docker Hub, afin des images peuvent être déployées sur le cluster AKS à partir de ce Registre. Dans ce cas, nous allons charger l’image dans Azure Container Registry.

### <a name="create-the-image-in-release-mode"></a>Créer l’image en mode de mise en production

Nous allons maintenant créer l’image dans **version** mode (prêt pour la production) en remplaçant par **version**, comme illustré dans la Figure 4-41 et exécution de l’application comme avant.

![Option de la barre d’outils dans Visual Studio pour générer en mode release.](media/select-release-mode.png)

**Figure 4-41**. Sélection du Mode de mise en production

Si vous exécutez le `docker image` commande, vous verrez les deux images créés, un pour `debug` et l’autre pour `release` mode.

### <a name="create-a-new-tag-for-the-image"></a>Créer une balise pour l’Image

Chaque image de conteneur doit être marquée avec le `loginServer` nom du Registre. Cette balise est utilisée pour le routage lors de l’envoi des images de conteneur à un registre d’image.

Vous pouvez afficher le `loginServer` nom à partir du portail Azure, en prenant les informations à partir du Registre de conteneur Azure

![Vue du navigateur du nom du Registre de conteneurs Azure, dans le coin supérieur droit.](media/loginServer-name.png)

**Figure 4-42**. Affichage du nom du Registre

Ou en exécutant la commande suivante :

```console
az acr list --resource-group MSSampleResourceGroup --query "[].{acrLoginServer:loginServer}" --output table
```

![Console de sortie à partir de la commande ci-dessus.](media/az-cli-loginServer-name.png)

**Figure 4-43**. Obtenir le nom du Registre à l’aide de PowerShell

Dans les deux cas, vous devez obtenir le nom. Dans notre exemple, `mssampleacr.azurecr.io`.

Maintenant vous pouvez marquer l’image, en prenant la dernière image (l’image de la mise en production), avec la commande :

```console
docker tag mssampleaksapplication:latest mssampleacr.azurecr.io/mssampleaksapplication:v1
```

Après l’exécution du `docker tag` de commande, de répertorier les images avec le `docker images` commande et vous devez voir l’image avec la nouvelle balise.

![Console de sortie à partir de la commande d’images docker.](media/tagged-docker-images-list.png)

**Figure 4-44**. Affichage d’images avec balises

### <a name="push-the-image-into-the-azure-acr"></a>Envoyez l’image dans l’ACR Azure

Envoyez l’image dans l’ACR Azure, à l’aide de la commande suivante :

```console
docker push mssampleacr.azurecr.io/mssampleaksapplication:v1
```

Cette commande prend un certain temps le téléchargement des images, mais vous donne des commentaires dans le processus.

![Sortie à partir de la commande push docker de la console : affiche une barre de progression basé sur des caractères pour chaque couche.](media/uploading-image-to-acr.png)

**Figure 4-45**. Chargement de l’image à l’ACR

Vous pouvez le voir ci-dessous le résultat que vous devez obtenir lorsque le processus est terminé :

![Sortie à partir de la commande push docker, terminée, affichant toutes les couches ou les nœuds de la console.](media/uploading-docker-images-complete.png)

**Figure 4-46**. Affichage de nœuds

L’étape suivante consiste à déployer votre conteneur dans votre cluster ACS Kubernetes. Pour ce faire, vous avez besoin d’un fichier (**.yml déployer le fichier**) qui contient les éléments suivants :

```yml
apiVersion: apps/v1beta1
kind: Deployment
metadata:
  name: mssamplesbook
spec:
  replicas: 1
  template:
    metadata:
      labels:
        app: mssample-kub-app
    spec:
      containers:
        - mane: mssample-services-app
          image: mssampleacr.azurecr.io/mssampleaksapplication:v1
          ports:
            - containerPort: 80
---
apiVersion: v1
kind: Service
metadata:
    name: mssample-kub-app
spec:
  ports:
    - name: http-port
      port: 80
      targetPort: 80
  selector:
    app: mssample-kub-app
  type: LoadBalancer
```

> [!NOTE]
> Pour plus d’informations sur le déploiement avec Kubernetes, consultez : <https://kubernetes.io/docs/reference/kubectl/cheatsheet/>

Maintenant vous êtes presque prêt à déployer à l’aide **Kubectl**, mais vous devez tout d’abord obtenir les informations d’identification pour le Cluster AKS avec cette commande :

```console
az aks get-credentials --resource-group MSSampleResourceGroupAKS --name mssampleclusterk801
```

![Console de sortie à partir de la commande ci-dessus : Fusionné MSSampleK8Cluster » en tant que contexte actuel dans /root/.kube/config](media/getting-aks-credentials.png)

**Figure 4-47**. obtention des informations d’identification

Ensuite, utilisez le `kubectl create` commande pour lancer le déploiement.

```console
kubectl create -f mssample-deploy.yml
```

![Console de sortie à partir de la commande ci-dessus : déploiement « mssamplesbook » créé. service « mssample-kub-app » créé.](media/kubectl-create-command.png)

**Figure 4-48**. Déployer sur Kubernetes

Lorsque le déploiement terminé, vous pouvez accéder à la console Kubernetes avec un proxy local auquel vous pouvez accéder temporellement avec cette commande :

```console
az aks browse --resource-group MSSampleResourceGroupAKS --name mssampleclusterk801
```

Et en accédant à l’url `http://127.0.0.1:8001`.

![Vue du navigateur du tableau de bord Kubernetes, montrant les déploiements, les Pods, les jeux de réplicas et les Services.](media/kubernetes-cluster-information.png)

**Figure 4-49**. Afficher les informations de cluster Kubernetes

Vous disposez maintenant de votre application déployée sur Azure, à l’aide d’un conteneur Linux et un Cluster de Kubernetes ACS. Vous pouvez accéder à votre application accédant à l’adresse IP publique de votre service, vous pouvez obtenir à partir du portail Azure.

> [!NOTE]
> Vous pouvez voir comment créer le Cluster AKS pour cet exemple dans la section [ **déployer vers Azure Kubernetes Service (AKS)** ](deploy-azure-kubernetes-service.md) sur ce guide.

>[!div class="step-by-step"]
>[Précédent](set-up-windows-containers-with-powershell.md)
>[Suivant](../docker-devops-workflow/index.md)
