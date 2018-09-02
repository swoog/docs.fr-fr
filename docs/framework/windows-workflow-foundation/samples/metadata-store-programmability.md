---
title: Programmabilité du magasin des métadonnées
ms.date: 03/30/2017
ms.assetid: 5b613661-f3f9-4e07-8e88-28c9ea2fd8f8
ms.openlocfilehash: 4ea6117686b985a9ea18ce4e5cc4ea2b5c25524c
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43423283"
---
# <a name="metadata-store-programmability"></a>Programmabilité du magasin des métadonnées
Le magasin des métadonnées est une fonctionnalité du [!INCLUDE[wfd1](../../../../includes/wfd1-md.md)] qui permet d'associer des métadonnées arbitraires, sous la forme d'attributs CLR, à des types au moment de l'exécution. Cela permet un couplage faible entre les composants runtime et leurs équivalents au moment du design, ainsi que la modification des composants au moment du design sans affecter le runtime. L'exemple montre comment d'écrire des programmes par rapport au magasin des métadonnées en appliquant des attributs à un type au moment de l'exécution, la source sur laquelle nous n'avons aucun contrôle. La terminologie généralement utilisée est qu'une application d'hébergement enregistre les métadonnées pour un ensemble de types.  
  
 Dans la sortie, vous pouvez remarquer un attribut supplémentaire inattendu, <!--zz <xref:System.Runtime.InteropServices.GUIDAttribute> --> `System.Runtime.InteropServices.GUIDAttribute`. Il est ajouté lorsque l'API des métadonnées est utilisée, et n'a aucun impact sur l'exécution de l'exemple.  
  
 Cet exemple illustre les opérations suivantes :  
  
## <a name="demonstrates"></a>Démonstrations  
  
-   Injection d'attributs à l'aide de l'API du magasin des métadonnées.  
  
-   Utilisation d'un mécanisme de rappel pour différer l'inscription des métadonnées.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1.  À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution ProgrammingMetadataStore.sln.  
  
2.  Pour générer la solution, appuyez sur Ctrl+Maj+B.  
  
3.  Pour exécuter la solution, appuyez sur F5.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\CustomActivityDesigners\MetadataStore`