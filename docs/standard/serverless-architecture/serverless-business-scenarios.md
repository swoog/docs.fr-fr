---
title: Exemples de scénarios d’entreprise et en cas d’utilisation pour les applications sans serveur
description: Découvrez sans serveur avec une approche pratique en accédant à des exemples qui vont du traitement d’image pour mobiles back-ends et les pipelines ETL.
author: JEREMYLIKNESS
ms.author: jeliknes
ms.date: 06/26/2018
ms.openlocfilehash: 177fb1d7f79a0067ab185e520778b593d4b8eaf6
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62017223"
---
# <a name="serverless-business-scenarios-and-use-cases"></a>Scénarios métier et cas d’usage serverless

Il existe de nombreux cas d’usage et scénarios pour les applications sans serveur. Ce chapitre inclut des exemples qui illustrent les différents scénarios. Les scénarios incluent des liens vers la documentation connexe et les référentiels de code source publics. Les exemples de ce chapitre permettent de prendre en main votre propre création et d’implémentation de solutions sans serveur.

## <a name="analyze-and-archive-images"></a>Analyser et archiver des images

Cet exemple montre les événements sans serveur (Event Grid), des flux de travail (application logique) et le code (Azure Functions). Il montre également comment intégrer à une autre ressource, dans ce cas Cognitive Services pour l’analyse de l’image.

Une application de console vous permet de transmettre un lien vers une URL sur le web. L’application publie l’URL en tant qu’un message de la grille d’événement. En parallèle, une application de fonction sans serveur et une application logique s’abonner au message. L’application de fonction sans serveur sérialise l’image vers le stockage blob. Il stocke également des informations dans le stockage Table Azure. Les métadonnées stockent l’URL d’image d’origine et le nom de l’image de l’objet blob. L’application logique interagit avec l’API de Vision personnalisée pour analyser l’image et de créer une légende générées par l’ordinateur. La légende est stockée dans la table de métadonnées.

![Analyser et archiver l’architecture d’images](./media/image-processing-example.png)

Une application distincte monopage (SPA) appelle une fonction sans serveur pour obtenir la liste des images et des métadonnées. Pour chaque image, il appelle une autre fonction qui fournit les données d’image à partir de l’archive. Le résultat final est une galerie avec des sous-titres codés automatiques.

![Galerie d’images automatisée](./media/automated-image-gallery.png)

Le référentiel complet et des instructions pour générer l’application logique sont disponibles ici : [Collage de grille d’événement](https://github.com/JeremyLikness/Event-Grid-Glue).

## <a name="cross-platform-mobile-client-using-xamarinforms-and-functions"></a>Client mobile multiplateforme à l’aide de Xamarin.Forms et fonctions

Découvrez comment implémenter une fonction Azure sans serveur simple dans le portail Web Azure ou dans Visual Studio. Générer un client avec Xamarin.Forms qui s’exécute sur Android, iOS et Windows. L’application est ensuite affinée pour utiliser JavaScript Objet Notation (JSON) comme un moyen de communication entre le serveur et les clients mobiles avec un backend sans serveur.

Pour plus d’informations, consultez [implémentation d’une fonction Azure simple avec un client Xamarin.Forms](https://azure.microsoft.com/resources/samples/functions-xamarin-getting-started/)

## <a name="generate-a-photo-mosaic-with-serverless-image-recognition"></a>Générer une mosaïque de photo avec reconnaissance d’images sans serveur

L’exemple utilise les fonctions Azure et Microsoft Cognitive Services Custom Vision Service pour générer une mosaïque de photos à partir d’une image d’entrée. Le modèle est formé de reconnaître les images. Lorsqu’une image est chargée, il reconnaît l’image et la recherche avec Bing. L’image d’origine est recomposée en utilisant les résultats de recherche.

![Mosaïque et photo de œil à Orlando](./media/orlando-eye-both.png)

Par exemple, vous pouvez former votre modèle avec des points d’intérêt à Orlando, telles que le œil Orlando. Vision personnalisée reconnaît une image de le œil d’Orlando, et la fonction créera une mosaïque de photos composée Bing image des résultats de recherche pour « Yeux Orlando. »

Pour plus d’informations, consultez [Générateur de mosaic photo Azure Functions](https://azure.microsoft.com/resources/samples/functions-dotnet-photo-mosaic/).

## <a name="migrate-an-existing-application-to-the-cloud"></a>Migrer une application existante vers le cloud

Comme indiqué dans les chapitres précédents, il est courant d’adopter une architecture multiniveau pour héberger votre application en local. Bien que la migration de ressources « tel quel » à l’aide de machines virtuelles est le chemin d’accès moins risquée dans le cloud, de nombreuses sociétés choisissent d’utiliser la possibilité de refactoriser leurs applications. Heureusement, la refactorisation ne doit être un effort « tout ou rien ». En fait, il est possible de migrer votre application puis remplacez fragmentaire des composants par équivalents natifs du cloud.

L’application utilise la fonctionnalité de proxys d’Azure Functions pour permettre la refactorisation d’un point de terminaison à partir du code hérité en local à un point de terminaison sans serveur.

![Architecture de la migration](./media/migration-architecture.png)

Le proxy fournit un point de terminaison d’API unique qui est mis à jour pour rediriger les demandes individuelles pendant leur déplacement dans les fonctions sans serveur.

Vous pouvez afficher une vidéo qui vous guide à travers toute la migration : [Lift- and -shift avec Azure functions sans serveur](https://channel9.msdn.com/Events/Connect/2017/E102). Accéder à l’exemple de code : [Apportez votre propre application](https://github.com/JeremyLikness/bring-own-app-connect-17).

## <a name="parse-a-csv-file-and-insert-into-a-database"></a>Analyser un fichier CSV et les insérer dans une base de données

Extraire, transformer et chargement (ETL) est une fonction métier courants qui s’intègre différents systèmes. Les approches traditionnelles impliquent souvent la configuration des serveurs dédiés de FTP, puis déployer des tâches planifiées pour analyser des fichiers et de les traduire pour une utilisation professionnelle. Architecture sans serveur facilite le travail, car un déclencheur peut être activé lorsque le fichier est téléchargé. Tâches de s’attaque de fonctions Azure telles que ETL via sa composition idéal de petits morceaux de code qui se concentrent sur un problème spécifique.

![Capture d’écran montrant le processus d’analyse du csv.](./media/serverless-business-scenarios/csv-parse-database-import.png)

Pour le code source et des exercices pratiques, consultez [CSV importer lab](https://github.com/JeremyLikness/azure-fn-file-process-hol).

## <a name="shorten-links-and-track-metrics"></a>Raccourcissez les liens et suivre les mesures

Outils de réduction de lien à l’origine a permis à encoder en bref les URL twitter billets pour prendre en compte la limite de 140 caractères. Ils se sont pour englober plusieurs utilisations, plus souvent pour effectuer le suivi des clics pour l’analytique. Le scénario de réducteur de lien est une application entièrement sans serveur qui gère les liens et signale les mesures.

Azure Functions est utilisé pour répondre à une Application à Page unique (SPA) qui vous permet de coller l’URL longue et générer des URL courtes. Les URL sont marqués pour effectuer le suivi des éléments tels que les campagnes (rubriques) et des supports (par exemple, les réseaux sociaux qui les liens sont publiés sur). Le code court est stocké dans le stockage Table Azure en tant que la clé, avec l’URL en tant que la valeur longue. Lorsque vous cliquez sur le lien court, une autre fonction recherche l’URL longue, envoie une redirection et place des informations sur l’événement dans une file d’attente. Une autre fonction Azure traite la file d’attente et place les informations dans Azure Cosmos DB.

![Lien raccourcisseur architecture](./media/link-shortener-architecture.png)

Vous pouvez ensuite créer un tableau de bord Power BI pour rassembler des informations sur les données collectées. Sur le serveur principal, Application Insights fournit des métriques importantes. Données de télémétrie incluent le temps nécessaire pour l’utilisateur moyen rediriger et le temps nécessaire pour accéder au stockage de Table Azure.

![Exemple de Power BI](./media/power-bi-example.png)

Le référentiel de raccourcisseur de liens complète en cours avec des instructions est disponible ici : [Sans serveur raccourcisseur d’URL](https://github.com/jeremylikness/serverless-url-shortener). Vous trouverez ici une version simplifiée : [Stockage Azure pour les applications .NET sans serveur en quelques minutes](https://blogs.msdn.microsoft.com/webdev/2018/01/25/azure-storage-for-serverless-net-apps-in-minutes/).

## <a name="verify-device-connectivity-using-a-ping"></a>Vérifier la connectivité d’appareil à l’aide d’une commande ping

L’exemple se compose d’un Azure IoT Hub et une fonction Azure. Un nouveau message sur le IoT Hub déclenche la fonction Azure. Le code sans serveur envoie le message même contenu vers l’appareil qui l’a envoyée. Le projet possède toute la configuration de déploiement et le code nécessaire pour la solution.

Pour plus d’informations, consultez [ping d’Azure IoT Hub](https://azure.microsoft.com/resources/samples/iot-hub-node-ping/).

## <a name="recommended-resources"></a>Ressources recommandées

* [Générateur de mosaic Azure fonctions photo](https://azure.microsoft.com/resources/samples/functions-dotnet-photo-mosaic/)
* [Ping de IoT Hub Azure](https://azure.microsoft.com/resources/samples/iot-hub-node-ping/)
* [Stockage Azure pour les applications .NET sans serveur en quelques minutes](https://blogs.msdn.microsoft.com/webdev/2018/01/25/azure-storage-for-serverless-net-apps-in-minutes/)
* [Apportez votre propre application](https://github.com/JeremyLikness/bring-own-app-connect-17)
* [Laboratoire d’importation CSV](https://github.com/JeremyLikness/azure-fn-file-process-hol)
* [Collage de grille d’événement](https://github.com/JeremyLikness/Event-Grid-Glue)
* [Implémentation d’une fonction Azure simple avec un client Xamarin.Forms](https://azure.microsoft.com/resources/samples/functions-xamarin-getting-started/)
* [Lift- and -shift avec Azure functions sans serveur](https://channel9.msdn.com/Events/Connect/2017/E102)
* [Sans serveur raccourcisseur d’URL](https://github.com/jeremylikness/serverless-url-shortener)

>[!div class="step-by-step"]
>[Précédent](orchestration-patterns.md)
>[Suivant](serverless-conclusion.md)