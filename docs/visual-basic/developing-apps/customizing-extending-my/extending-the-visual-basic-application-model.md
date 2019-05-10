---
title: Extension du modèle d'application Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic Application Model, extending
ms.assetid: e91d3bed-4c27-40e3-871d-2be17467c72c
ms.openlocfilehash: bb87879fdf584a439e09839bf4321b85e7dd6a43
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64602445"
---
# <a name="extending-the-visual-basic-application-model"></a>Extension du modèle d'application Visual Basic
Vous pouvez ajouter des fonctionnalités pour le modèle d’application en substituant le `Overridable` membres de la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase> classe. Cette technique vous permet de personnaliser le comportement du modèle d’application et ajouter des appels à vos propres méthodes lorsque l’application démarre et s’arrête.  
  
## <a name="visual-overview-of-the-application-model"></a>Aperçu visuel du modèle d’Application  
 Cette section présente visuellement la séquence d’appels de fonction dans le modèle d’Application Visual Basic. La section suivante décrit l’objectif de chaque fonction en détail.  
  
 Le graphique suivant montre la séquence d’appel application modèle dans une application Visual Basic Windows Forms normale. La séquence commence lorsque le `Sub Main` les appels de procédure le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Run%2A> (méthode).  
  
 ![Diagramme montrant la séquence d’appel de modèle d’Application.](./media/extending-the-visual-basic-application-model/application-model-call-sequence.gif)  
  
 Le modèle d’Application Visual Basic fournit également la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.StartupNextInstance> et <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException> événements. Les graphiques suivants illustrent le mécanisme de déclenchement de ces événements.  
  
 ![Diagramme montrant la méthode OnStartupNextInstance qui déclenche l’événement StartupNextInstance.](./media/extending-the-visual-basic-application-model/raise-startupnextinstance-event.gif)  
  
 ![Diagramme montrant la méthode OnUnhandledException qui déclenche l’événement UnhandledException.](./media/extending-the-visual-basic-application-model/raise-unhandledexception-event.gif)  
  
## <a name="overriding-the-base-methods"></a>Substitution des méthodes de Base  
 Le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Run%2A> méthode définit l’ordre dans lequel le `Application` exécuter des méthodes. Par défaut, le `Sub Main` procédure pour une application Windows Forms appelle le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Run%2A> (méthode).  
  
 Si l’application est une application normale (plusieurs instances d’application) ou la première instance d’une application à instance unique, la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Run%2A> méthode s’exécute le `Overridable` méthodes dans l’ordre suivant :  
  
1. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnInitialize%2A>. Par défaut, cette méthode définit les styles visuels, les styles d’affichage de texte et les principal actuel pour le thread d’application principal (si l’application utilise l’authentification Windows) et les appels `ShowSplashScreen` si ni `/nosplash` ni `-nosplash` est utilisé comme un argument de ligne de commande.  
  
     La séquence de démarrage d’application est annulée si cette fonction retourne `False`. Cela peut être utile si les circonstances dans lesquelles l’application ne doit pas exécutée.  
  
     Le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnInitialize%2A> méthode appelle les méthodes suivantes :  
  
    1. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.ShowSplashScreen%2A>. Détermine si l’application a un écran de démarrage défini et le cas échéant, affiche l’écran de démarrage sur un thread distinct.  
  
         Le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.ShowSplashScreen%2A> méthode contient le code qui affiche l’écran d’accueil de l’écran au moins le nombre de millisecondes spécifié par le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MinimumSplashScreenDisplayTime%2A> propriété. Pour utiliser cette fonctionnalité, vous devez ajouter l’écran de démarrage à votre application à l’aide la **Concepteur de projets** (qui affecte le `My.Application.MinimumSplashScreenDisplayTime` propriété à deux secondes), ou définir le `My.Application.MinimumSplashScreenDisplayTime` propriété dans une méthode qui substitue la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnInitialize%2A> ou <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateSplashScreen%2A> (méthode). Pour plus d'informations, consultez <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MinimumSplashScreenDisplayTime%2A>.  
  
    2. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateSplashScreen%2A>. Permet à un concepteur d’émettre du code qui initialise l’écran de démarrage.  
  
         Par défaut, cette méthode ne fait rien. Si vous sélectionnez un écran de démarrage pour votre application dans Visual Basic **Concepteur de projets**, le concepteur substitue le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateSplashScreen%2A> méthode avec une méthode qui définit le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.SplashScreen%2A> propriété à une nouvelle instance de la forme d’écran de démarrage .  
  
2. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnStartup%2A>. Fournit un point d’extensibilité pour déclencher le `Startup` événement. La séquence de démarrage d’application s’arrête si cette fonction retourne `False`.  
  
     Par défaut, cette méthode déclenche la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup> événement. Si le Gestionnaire d’événements définit la <xref:System.ComponentModel.CancelEventArgs.Cancel> propriété de l’argument d’événement à `True`, la méthode retourne `False` pour annuler le démarrage de l’application.  
  
3. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnRun%2A>. Fournit le point de départ lorsque l’application principale est prête à commencer son exécution, une fois que l’initialisation est terminée.  
  
     Par défaut, avant d’entrer dans la boucle de message Windows Forms, cette méthode appelle la `OnCreateMainForm` (pour créer le formulaire principal de l’application) et `HideSplashScreen` (pour fermer l’écran de démarrage) méthodes :  
  
    1. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A>. Fournit un moyen pour un concepteur d’émettre du code qui initialise le formulaire principal.  
  
         Par défaut, cette méthode ne fait rien. Toutefois, lorsque vous sélectionnez un formulaire principal pour votre application dans Visual Basic **Concepteur de projets**, le concepteur substitue le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A> méthode avec une méthode qui définit la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A> propriété vers une nouvelle instance du formulaire principal.  
  
    2. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.HideSplashScreen%2A>. Si l’application a un écran de démarrage défini, et il est ouvert, cette méthode ferme l’écran de démarrage.  
  
         Par défaut, cette méthode ferme l’écran de démarrage.  
  
4. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnStartupNextInstance%2A>. Fournit un moyen de personnaliser le comportement d’une application à instance unique lorsqu’une autre instance de l’application démarre.  
  
     Par défaut, cette méthode déclenche la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.StartupNextInstance> événement.  
  
5. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnShutdown%2A>. Fournit un point d’extensibilité pour déclencher le `Shutdown` événement. Cette méthode n’exécute pas si une exception non gérée se produit dans l’application principale.  
  
     Par défaut, cette méthode déclenche la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown> événement.  
  
6. <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnUnhandledException%2A>. Exécuté si une exception non gérée se produit dans une des méthodes répertoriées ci-dessus.  
  
     Par défaut, cette méthode déclenche la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException> événement tant qu’un débogueur n’est pas attaché et que l’application gère le `UnhandledException` événement.  
  
 Si l’application est une application à instance unique, et que l’application est déjà en cours d’exécution, l’instance suivante de l’application appelle la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnStartupNextInstance%2A> méthode sur l’instance d’origine de l’application, puis se ferme.  
 
 Le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnStartupNextInstance(Microsoft.VisualBasic.ApplicationServices.StartupNextInstanceEventArgs)> constructeur appelle la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UseCompatibleTextRendering%2A> propriété afin de déterminer le moteur de rendu de texte à utiliser pour les formulaires de l’application. Par défaut, le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UseCompatibleTextRendering%2A> retourne de la propriété `False`, indiquant que le moteur de rendu de texte GDI être utilisé, qui est la valeur par défaut dans [!INCLUDE[vbprvblong](~/includes/vbprvblong-md.md)]. Vous pouvez remplacer le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UseCompatibleTextRendering%2A> propriété à retourner `True`, ce qui indique que le moteur de rendu de texte GDI + servir, qui est la valeur par défaut dans Visual Basic .NET 2002 et Visual Basic .NET 2003.  
  
## <a name="configuring-the-application"></a>Configuration de l’Application  
 Dans le cadre du modèle d’Application Visual Basic, le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UseCompatibleTextRendering> classe fournit des propriétés protégées qui configurent l’application. Ces propriétés doivent être définies dans le constructeur de la classe d’implémentation.  
  
 Dans un projet Windows Forms par défaut, le **Concepteur de projets** crée du code pour définir les propriétés avec les paramètres du concepteur. Les propriétés sont utilisées uniquement lors du démarrage de l’application ; leur définition après le démarrage de l’application n’a aucun effet.  
  
|Propriété|Détermine|Paramètre dans le volet Application du Concepteur de projets|  
|---|---|---|  
|<xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.IsSingleInstance%2A>|Indique si l’application s’exécute comme une application à instance unique ou plusieurs instances.|**Application à instance unique** case à cocher|  
|<xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.EnableVisualStyles%2A>|Si l’application utilise des styles visuels qui correspondent à Windows XP.|**Activer des styles visuels XP** case à cocher|  
|<xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.SaveMySettingsOnExit%2A>|Si l’application enregistre automatiquement les modifications des paramètres utilisateur de l’application lorsque l’application se ferme.|**Enregistrer My.Settings lors de l’arrêt** case à cocher|  
|<xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.ShutdownStyle%2A>|Ce qui entraîne l’application de terminer, par exemple lorsque le formulaire de démarrage ferme ou lorsque le dernier formulaire.|**Mode d’arrêt** liste|  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.StartupNextInstance>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.UnhandledException>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.NetworkAvailabilityChanged>
- [Vue d’ensemble du modèle d’application Visual Basic](../../../visual-basic/developing-apps/development-with-my/overview-of-the-visual-basic-application-model.md)
- [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
