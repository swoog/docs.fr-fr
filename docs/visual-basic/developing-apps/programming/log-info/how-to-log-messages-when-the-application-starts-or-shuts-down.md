---
title: 'Procédure : enregistrer des messages lorsque l’application démarre ou s’arrête (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- event logs, shutdown
- My.Application.Log object, logging
- Startup event [Visual Basic]
- event logs, startup
- Shutdown event [Visual Basic]
- My.Log object, logging
ms.assetid: 67624d05-cddf-48b7-8c36-5c99baa4c621
ms.openlocfilehash: 20eabd08db0763ec08bb28add41ff63fa3196dd6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585628"
---
# <a name="how-to-log-messages-when-the-application-starts-or-shuts-down-visual-basic"></a>Procédure : enregistrer des messages lorsque l’application démarre ou s’arrête (Visual Basic)
Vous pouvez utiliser les objets `My.Application.Log` et `My.Log` pour enregistrer des informations sur les événements qui se produisent dans votre application. Cet exemple montre comment utiliser la méthode `My.Application.Log.WriteEntry` avec les événements `Startup` et `Shutdown` pour enregistrer des informations de traçage.  
  
### <a name="to-access-the-applications-event-handler-code"></a>Pour accéder au code du gestionnaire d’événements de l’application  
  
1.  Sélectionnez un projet dans l' **Explorateur de solutions**. Dans le menu **Projet** , choisissez **Propriétés**.  
  
2.  Cliquez sur l’onglet **Application** .  
  
3.  Cliquez sur le bouton **Afficher les événements de l’application** pour ouvrir l’éditeur de code.  
  
     Le fichier ApplicationEvents.vb s’ouvre.  
  
### <a name="to-log-messages-when-the-application-starts"></a>Pour enregistrer des messages quand l’application démarre  
  
1.  Ouvrez le fichier ApplicationEvents.vb dans l’éditeur de code. Dans le menu **Général** , choisissez **Événements MyApplication**.  
  
2.  Dans le menu **Déclarations** , choisissez **Démarrage**.  
  
     L’application déclenche l’événement <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup> avant l’exécution de l’application principale.  
  
3.  Ajoutez la méthode `My.Application.Log.WriteEntry` au gestionnaire d’événements `Startup` .  
  
     [!code-vb[VbVbalrMyApplicationLog#1](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-messages-when-the-application-starts-or-shuts-down_1.vb)]  
  
### <a name="to-log-messages-when-the-application-shuts-down"></a>Pour enregistrer des messages quand l’application s’arrête  
  
1.  Ouvrez le fichier ApplicationEvents.vb dans l’éditeur de code. Dans le menu **Général** , choisissez **Événements MyApplication**.  
  
2.  Dans le menu **Déclarations** , choisissez **Arrêt**.  
  
     L’application déclenche l’événement <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown> après l’exécution de l’application principale, mais avant qu’elle s’arrête.  
  
3.  Ajoutez la méthode `My.Application.Log.WriteEntry` au gestionnaire d’événements `Shutdown` .  
  
     [!code-vb[VbVbalrMyApplicationLog#2](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-messages-when-the-application-starts-or-shuts-down_2.vb)]  
  
## <a name="example"></a>Exemple  
 Vous pouvez utiliser le **Concepteur de projets** pour accéder aux événements de l’application dans l’éditeur de code. Pour plus d’informations, consultez [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).  
  
 [!code-vb[VbVbalrMyApplicationLog#3](../../../../visual-basic/developing-apps/programming/log-info/codesnippet/VisualBasic/how-to-log-messages-when-the-application-starts-or-shuts-down_3.vb)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Logging.Log?displayProperty=nameWithType>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteEntry%2A>
- <xref:Microsoft.VisualBasic.Logging.Log.WriteException%2A>
- [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
- [Utilisation des journaux des applications](../../../../visual-basic/developing-apps/programming/log-info/working-with-application-logs.md)
