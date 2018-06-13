---
title: Vue d'ensemble du modèle d'application Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- My.Application object [Visual Basic], Visual Basic application model
- Visual Basic application model
ms.assetid: 17538984-84fe-43c9-82c8-724c9529fe8b
ms.openlocfilehash: 5194810574f594e2c117fef8d8998b7ecebbc981
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33591597"
---
# <a name="overview-of-the-visual-basic-application-model"></a>Vue d'ensemble du modèle d'application Visual Basic
Visual Basic fournit un modèle précis pour contrôler le comportement des applications Windows Forms : le modèle d’Application Visual Basic. Ce modèle inclut des événements pour gérer de l’application démarrage et arrêt, ainsi que les événements pour l’interception des exceptions non gérées. Il prend également en charge pour le développement d’applications à instance unique. Le modèle d’application est extensible, afin que les développeurs nécessitant davantage de contrôle peuvent personnaliser ses méthodes substituables.  
  
## <a name="uses-for-the-application-model"></a>Utilise le modèle d’Application  
 Une application classique doit effectuer des tâches lorsqu’il démarre et s’arrête. Par exemple, lors de son démarrage, l’application peut afficher un écran de démarrage, établir des connexions de base de données, charger un état enregistré et ainsi de suite. Lorsque l’application s’arrête, il peut fermer les connexions de base de données, enregistrer l’état actuel et ainsi de suite. En outre, l’application peut exécuter du code spécifique lors de la fermeture de l’application vers le bas de façon inattendue, tels que lors d’une exception non gérée.  
  
 Le modèle d’Application Visual Basic permet de créer facilement un *uniques* application. Une application à instance unique diffère d’une application normale dans ce qu’une seule instance de l’application peut être en cours d’exécution à la fois. Entraîne une tentative de lancement d’une autre instance d’une application à instance unique l’instance d’origine de la notification, à l’aide de la `StartupNextInstance` événement — qu’une autre tentative de lancement a été faite. La notification inclut les arguments de ligne de commande de l’instance suivante. L’instance suivante de l’application est ensuite fermée avant toute initialisation peut se produire.  
  
 Une application à instance unique démarre et vérifie s’il s’agit de la première instance ou une instance suivante de l’application :  
  
-   Si elle est la première instance, elle démarre comme d’habitude.  
  
-   Toute tentative ultérieure de démarrer l’application, alors que la première instance s’exécute, entraîne un comportement très différent. La tentative suivante notifie la première instance sur les arguments de ligne de commande, puis quitte immédiatement. La première instance gère la `StartupNextInstance` événement pour déterminer les arguments de ligne de commande de l’instance suivantes ont été et continue de s’exécuter.  
  
     Ce diagramme illustre comment une instance suivante signale la première instance.  
  
     ![Une seule Image Application à Instance](../../../visual-basic/developing-apps/development-with-my/media/singleinstance.gif "SingleInstance")  
  
 En gérant la `StartupNextInstance` événement, vous pouvez contrôler le comportement de votre application à instance unique. Par exemple, Microsoft Outlook s’exécute généralement en tant qu’une application à instance unique ; Quand Outlook est en cours d’exécution et que vous essayez de démarrer Outlook là encore, la sélection se déplace vers l’instance d’origine mais une autre instance ne s’ouvre pas.  
  
## <a name="events-in-the-application-model"></a>Événements dans le modèle d’Application  
 Les événements suivants sont trouvent dans le modèle d’application :  
  
-   **Démarrage de l’application**. L’application déclenche le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup> événement lorsqu’il démarre. En gérant cet événement, vous pouvez ajouter du code qui initialise l’application avant de charger le formulaire principal. Le `Startup` événement prévoit également l’annulation de l’exécution de l’application pendant cette phase du processus de démarrage, si vous le souhaitez.  
  
     Vous pouvez configurer l’application pour afficher un écran de démarrage pendant l’exécution de code de démarrage de l’application. Par défaut, le modèle d’application supprime le démarrage de l’écran lorsque soit la `/nosplash` ou `-nosplash` argument de ligne de commande est utilisé.  
  
-   **Applications à instance unique**. Le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.StartupNextInstance> événement est déclenché lorsqu’une instance suivante d’une application à instance unique démarre. L’événement passe les arguments de ligne de commande de l’instance suivante.  
  
-   **Les exceptions non gérées**. Si l’application rencontre une exception non gérée, elle déclenche le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException> événement. Votre gestionnaire pour cet événement peut examiner l’exception et déterminer s’il faut continuer l’exécution.  
  
     Le `UnhandledException` événement n’est pas déclenché dans certains cas. Pour plus d'informations, consultez <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException>.  
  
-   **Modifications de la connectivité réseau**. Si la disponibilité du réseau de l’ordinateur change, l’application déclenche le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.NetworkAvailabilityChanged> événement.  
  
     Le `NetworkAvailabilityChanged` événement n’est pas déclenché dans certains cas. Pour plus d'informations, consultez <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.NetworkAvailabilityChanged>.  
  
-   **Application arrête**. L’application fournit le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown> événement pour signaler quand il est sur le point d’arrêt. Dans ce cas gestionnaire, vous pouvez vous assurer que les opérations de votre application doit effectuer, fermeture et l’enregistrement, par exemple, sont terminées. Vous pouvez configurer votre application s’arrête lorsque le formulaire principal, ou pour l’arrêter lorsque tous les formulaires ferment uniquement.  
  
## <a name="availability"></a>Disponibilité  
 Par défaut, le modèle d’Application Visual Basic est disponible pour les projets Windows Forms. Si vous configurez l’application pour utiliser un objet de démarrage différentes, ou le code d’application avec une personnalisée `Sub Main`, cet objet ou classe devra éventuellement fournir une implémentation de la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase> classe à utiliser le modèle d’application. Pour plus d’informations sur la modification de l’objet de démarrage, consultez [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.StartupNextInstance>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.NetworkAvailabilityChanged>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase>  
 [Extension du modèle d’application Visual Basic](../../../visual-basic/developing-apps/customizing-extending-my/extending-the-visual-basic-application-model.md)
