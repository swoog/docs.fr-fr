---
title: 'Procédure : accéder à un service à partir d’une application de workflow'
ms.date: 03/30/2017
ms.assetid: 925ef8ea-5550-4c9d-bb7b-209e20c280ad
ms.openlocfilehash: 178fb04244cb3e5075722877fdd3e2b5a92b8502
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61779642"
---
# <a name="how-to-access-a-service-from-a-workflow-application"></a>Procédure : accéder à un service à partir d’une application de workflow
Cette rubrique décrit comment appeler un service de workflow à partir d'une application console de workflow. Cela dépend à la fin de la [Comment : Créer un Service de flux de travail avec les activités de messagerie](../../../../docs/framework/wcf/feature-details/how-to-create-a-workflow-service-with-messaging-activities.md) rubrique. Bien que cette rubrique décrit comment appeler un service de workflow à partir d’une application de workflow, les mêmes méthodes peuvent servir à appeler n’importe quel service Windows Communication Foundation (WCF) à partir d’une application de workflow.

### <a name="create-a-workflow-console-application-project"></a>Créer un projet d'application console de workflow.

1. Démarrez Visual Studio 2012.

2. Charger le projet mywfservice que vous avez créé dans le [Comment : Créer un Service de flux de travail avec les activités de messagerie](../../../../docs/framework/wcf/feature-details/how-to-create-a-workflow-service-with-messaging-activities.md) rubrique.

3. Bouton droit sur le **MyWFService** solution dans le **l’Explorateur de solutions** et sélectionnez **ajouter**, **nouveau projet**. Sélectionnez **Workflow** dans le **modèles installés** et **Application Console de Workflow** dans la liste des types de projets. Nommez le projet MyWFClient et utilisez l'emplacement par défaut, comme indiqué dans l'illustration suivante.

     ![Ajouter une nouvelle boîte de dialogue Nouveau projet](./media/how-to-access-a-service-from-a-workflow-application/add-new-project-dialog.jpg)

     Cliquez sur le **OK** bouton pour fermer la **nouveau projet boîte de dialogue Ajouter**.

4. Après avoir créé le projet, le fichier Workflow1.xaml s'ouvre dans le concepteur. Cliquez sur le **boîte à outils** onglet pour ouvrir la boîte à outils si elle n’est pas déjà ouvert puis cliquez sur la punaise pour garder la fenêtre Boîte à outils ouverte.

5. Appuyez sur **Ctrl**+**F5** pour générer et lancer le service. Comme auparavant, le Serveur de développement ASP.NET se lance et Internet Explorer affiche la page d'aide WCF. Notez l'URI de cette page, car vous devez l'utiliser dans l'étape suivante.

     ![IE affichant la page d’aide WCF et URI](./media/how-to-access-a-service-from-a-workflow-application/ie-wcf-help-page-uri.jpg)

6. Bouton droit sur le **MyWFClient** de projet dans le **l’Explorateur de solutions** et sélectionnez **ajouter** > **une référence de Service**. Cliquez sur le **Discover** bouton pour rechercher la solution actuelle pour tous les services. Cliquez sur le triangle à côté de Service1.xamlx dans la liste des services. Cliquez sur le triangle à côté de Service1 pour répertorier les contrats implémentés par le service Service1. Développez le **Service1** nœud dans le **Services** liste. L’opération Echo est affichée dans le **opérations** liste comme indiqué dans l’illustration suivante.

     ![Boîte de dialogue Ajouter une référence de service](./media/how-to-access-a-service-from-a-workflow-application/add-service-reference.jpg)

     Conservez l’espace de noms par défaut et cliquez sur **OK** pour faire disparaître le **ajouter une référence de Service** boîte de dialogue. La boîte de dialogue suivante s'affiche.

     ![Ajouter la boîte de dialogue de Notification de référence de Service](./media/how-to-access-a-service-from-a-workflow-application/add-service-reference-dialog.jpg)

     Cliquez sur **OK** pour faire disparaître la boîte de dialogue. Appuyez ensuite sur Ctrl+Maj+B pour générer la solution. Notez que dans la boîte à outils a été ajoutée une nouvelle section appelée **MyWFClient.ServiceReference1.Activities**. Développez cette section ; l’activité Echo a été ajoutée comme indiqué dans l’illustration suivante.

     ![Activité Echo dans la boîte à outils](./media/how-to-access-a-service-from-a-workflow-application/echo-activity-toolbox.jpg)

7. Faites glisser une activité <xref:System.Activities.Statements.Sequence> sur l'aire du concepteur. Il se trouve sous le **flux de contrôle** section de la boîte à outils.

8. Avec le <xref:System.Activities.Statements.Sequence> activité en mode focus, cliquez sur le **Variables** lier et ajoutez une variable de chaîne nommée `inString`. Affectez la valeur par défaut à la variable `"Hello, world"` ainsi que d’une variable chaîne nommée `outString` comme indiqué dans le diagramme suivant.

     ![Ajout d’une variable inString](./media/how-to-access-a-service-from-a-workflow-application/add-instring-variable.jpg)

9. Faites glisser et déposez une **Echo** l’activité dans le <xref:System.Activities.Statements.Sequence>. Dans la fenêtre Propriétés lier le `inMsg` l’argument de la `inString` variable et la `outMsg` l’argument de la `outString` variable, comme indiqué dans l’illustration suivante. Cela transmet la valeur de la variable `inString` à l'opération, puis prend la valeur de retour et la place dans la variable `outString`.

     ![Lier les arguments à des variables](./media/how-to-access-a-service-from-a-workflow-application/bind-arguments-variables.jpg)

10. Faites glisser et déposez un **WriteLine** activité ci-dessous le **Echo** activité pour afficher la chaîne retournée par l’appel de service. Le **WriteLine** activité se trouve dans le **Primitives** nœud dans la boîte à outils. Lier le **texte** argument de la **WriteLine** activité à la `outString` variable en tapant `outString` dans la zone de texte sur le **WriteLine** activité. Le workflow doit maintenant ressembler à l'illustration suivante.

     ![Flux de travail client complet](./media/how-to-access-a-service-from-a-workflow-application/complete-client-workflow.jpg)

11. Avec le bouton droit de la solution MyWFService et sélectionnez **définir les projets de démarrage...** . Sélectionnez le **plusieurs projets de démarrage** case d’option et sélectionnez **Démarrer** pour chaque projet dans le **Action** colonne comme indiqué dans l’illustration suivante.

     ![Options des projets de démarrage](./media/how-to-access-a-service-from-a-workflow-application/startup-project-options.jpg)

12. Appuyez sur Ctrl + F5 pour lancer à la fois le service et le client. Le serveur de développement ASP.NET héberge le service, Internet Explorer affiche la page d’aide WCF et l’application de flux de travail cliente est lancée dans une fenêtre de console et affiche la chaîne retournée à partir du service (« Hello, world »).

## <a name="see-also"></a>Voir aussi

- [Services de workflow](../../../../docs/framework/wcf/feature-details/workflow-services.md)
- [Guide pratique pour Créer un Service de flux de travail avec les activités de messagerie](../../../../docs/framework/wcf/feature-details/how-to-create-a-workflow-service-with-messaging-activities.md)
- [Utilisation d’un Service WCF à partir d’un flux de travail dans un projet Web](https://go.microsoft.com/fwlink/?LinkId=207725)
