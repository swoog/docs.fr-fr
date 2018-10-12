---
title: Créer une application de service Windows dans Visual Studio
ms.date: 09/10/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows service applications, walkthroughs
- Windows service applications, creating
ms.assetid: e24d8a3d-edc6-485c-b6e0-5672d91fb607
author: ghogen
manager: douge
ms.openlocfilehash: 27acdac5d34b96dd04fec1bb763edec9077ff928
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2018
ms.locfileid: "46493605"
---
# <a name="walkthrough-create-a-windows-service-app"></a>Procédure pas à pas : Créer une application de service Windows

Cet article explique comment créer, dans Visual Studio, une application de service Windows simple qui écrit des messages dans un journal des événements.

## <a name="create-a-service"></a>Créer un service

Pour commencer, créez votre projet et définissez les valeurs nécessaires au fonctionnement correct du service.

1. Dans Visual Studio, dans la barre de menus, choisissez **Fichier** > **Nouveau** > **Projet** (ou appuyez sur **Ctrl**+**MAJ**+**N**) pour ouvrir la boîte de dialogue **Nouveau projet**.

2. Accédez au modèle de projet **Windows Service** et sélectionnez-le. Développez **Installé** > [**Visual C#** ou **Visual Basic**] > **Windows Desktop** ou tapez **Windows Service** dans la zone de recherche dans l’angle supérieur droit.

   ![Modèle Windows Service dans la boîte de dialogue Nouveau projet de Visual Studio](media/new-project-dialog.png)

   > [!NOTE]
   > Si le modèle **Windows Service** ne s’affiche pas, vous devrez peut-être installer la charge de travail **Développement bureau .NET**. Dans la boîte de dialogue **Nouveau projet**, cliquez sur le lien **Ouvrir Visual Studio Installer** dans l’angle inférieur gauche. Dans **Visual Studio Installer**, sélectionnez la charge de travail **Développement bureau .NET** et choisissez **Modifier**.

3. Nommez le projet **MyNewService**, puis choisissez **OK**.

   Le modèle de projet inclut une classe Component appelée `Service1` qui hérite de <xref:System.ServiceProcess.ServiceBase?displayProperty=nameWithType>. Elle contient une grande partie du code de service de base, comme le code pour démarrer le service.

## <a name="rename-the-service"></a>Renommer le service

Renommez le service **Service1** en **MyNewService**.

1. Dans le mode **Création** pour Service1.cs (ou Service1.vb), cliquez sur le lien pour **passer en mode Code**. Cliquez avec le bouton droit sur **Service1** et sélectionnez **Renommer** dans le menu contextuel. Entrez **MyNewService**, puis appuyez sur **Entrée** ou cliquez sur **Appliquer**.

2. Dans la fenêtre **Propriétés** pour **Service1.cs [Design]** ou **Service1.vb [Design]**, remplacez la valeur **ServiceName** par **MyNewService**.

3. Dans **l’Explorateur de solutions**, renommez **Service1.cs** en **MyNewService.cs**, ou renommez **Service1.vb** en **MyNewService.vb**.

## <a name="add-features-to-the-service"></a>Ajouter des fonctionnalités au service

Dans cette section, vous ajoutez un journal des événements personnalisé au service Windows. Les journaux des événements ne sont en aucune façon associés aux services Windows. Ici, le composant <xref:System.Diagnostics.EventLog> est utilisé comme un exemple du type de composants que vous pouvez ajouter à un service Windows.

### <a name="add-custom-event-log-functionality"></a>Ajouter une fonctionnalité de journal des événements personnalisé

1. Dans l' **Explorateur de solutions**, ouvrez le menu contextuel pour **MyNewService.cs** ou **MyNewService.vb**, puis choisissez **Concepteur de vues**.

2. À partir de la section **Composants** de la **boîte à outils**, faites glisser un composant <xref:System.Diagnostics.EventLog> jusqu'au concepteur.

3. Dans l' **Explorateur de solutions**, ouvrez le menu contextuel pour **MyNewService.cs** ou **MyNewService.vb**, puis choisissez **Afficher le code**.

4. Modifiez le constructeur pour définir un journal des événements personnalisé :

   ```csharp
   public MyNewService()
   {
        InitializeComponent();

        eventLog1 = new System.Diagnostics.EventLog();
        if (!System.Diagnostics.EventLog.SourceExists("MySource"))
        {
            System.Diagnostics.EventLog.CreateEventSource(
                "MySource", "MyNewLog");
        }
        eventLog1.Source = "MySource";
        eventLog1.Log = "MyNewLog";
    }
   ```

   [!code-vb[VbRadconService#2](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#2)]

### <a name="define-what-occurs-when-the-service-starts"></a>Définir les actions à effectuer lors du démarrage du service

Dans l’éditeur de code, localisez la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> qui a été automatiquement substituée lorsque vous avez créé le projet. Ajoutez une ligne de code qui écrit une entrée dans le journal des événements lorsque le service démarre :

[!code-csharp[VbRadconService#3](../../../samples/snippets/csharp/VS_Snippets_VBCSharp/VbRadconService/CS/MyNewService.cs#3)]
[!code-vb[VbRadconService#3](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#3)]

Une application de service est conçue pour s'exécuter sur une longue durée, et elle interroge ou surveille généralement quelque chose dans le système. La surveillance est configurée dans la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> . Toutefois, la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> n'effectue pas elle-même la surveillance. La méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> doit retourner au système d'exploitation dès que le service est en cours d'exécution. Elle ne doit pas s'exécuter indéfiniment en boucle ni se bloquer. Pour définir un mécanisme d'interrogation simple, vous pouvez utiliser le composant <xref:System.Timers.Timer?displayProperty=nameWithType> comme suit : dans la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A>, définissez des paramètres sur le composant, puis affectez à la propriété <xref:System.Timers.Timer.Enabled%2A> la valeur `true`. La minuterie déclenche périodiquement des événements dans votre code, lesquels indiquent au service qu'il peut effectuer son analyse. Pour cela, vous pouvez utiliser le code suivant :

```csharp
// Set up a timer that triggers every minute.
System.Timers.Timer timer = new System.Timers.Timer();
timer.Interval = 60000; // 60 seconds
timer.Elapsed += new System.Timers.ElapsedEventHandler(this.OnTimer);
timer.Start();
```

```vb
' Set up a timer that triggers every minute.
Dim timer As System.Timers.Timer = New System.Timers.Timer()
timer.Interval = 60000 ' 60 seconds
AddHandler timer.Elapsed, AddressOf Me.OnTimer
timer.Start()
```

Ajoutez une variable membre à la classe. Elle contient l’identificateur de l’événement suivant à écrire dans le journal des événements.

```csharp
private int eventId = 1;
```

```vb
Private eventId As Integer = 1
```

Ajoutez une nouvelle méthode pour gérer l'événement du minuteur :

```csharp
public void OnTimer(object sender, System.Timers.ElapsedEventArgs args)
{
    // TODO: Insert monitoring activities here.
    eventLog1.WriteEntry("Monitoring the System", EventLogEntryType.Information, eventId++);
}
```

```vb
Private Sub OnTimer(sender As Object, e As Timers.ElapsedEventArgs)
    ' TODO: Insert monitoring activities here.
    eventLog1.WriteEntry("Monitoring the System", EventLogEntryType.Information, eventId)
    eventId = eventId + 1
End Sub
```

Vous pouvez effectuer des tâches à l'aide de threads de travail en arrière-plan au lieu d'exécuter l'ensemble de votre travail sur le thread principal. Pour plus d'informations, consultez <xref:System.ComponentModel.BackgroundWorker?displayProperty=fullName>.

### <a name="define-what-occurs-when-the-service-is-stopped"></a>Définir les actions à effectuer lors de l'arrêt du service

Ajoutez une ligne de code à la méthode <xref:System.ServiceProcess.ServiceBase.OnStop%2A> qui ajoute une entrée dans le journal des événements lorsque le service est arrêté :

```csharp
eventLog1.WriteEntry("In OnStop.");
```

[!code-vb[VbRadconService#4](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#4)]

### <a name="define-other-actions-for-the-service"></a>Définir d'autres actions du service

Vous pouvez substituer les méthodes <xref:System.ServiceProcess.ServiceBase.OnPause%2A>, <xref:System.ServiceProcess.ServiceBase.OnContinue%2A> et <xref:System.ServiceProcess.ServiceBase.OnShutdown%2A> afin de définir d'autres types de traitement pour votre composant. Le code suivant montre comment substituer la méthode <xref:System.ServiceProcess.ServiceBase.OnContinue%2A> :

[!code-csharp[VbRadconService#5](../../../samples/snippets/csharp/VS_Snippets_VBCSharp/VbRadconService/CS/MyNewService.cs#5)]
[!code-vb[VbRadconService#5](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#5)]

Certaines actions personnalisées doivent se produire lorsqu'un service Windows est installé par la classe <xref:System.Configuration.Install.Installer> . Visual Studio peut créer ces programmes d'installation spécialement pour un service Windows et les ajouter à votre projet.

## <a name="set-service-status"></a>Définir l’état du service

Les services indiquent leur état au Gestionnaire de contrôle des services. Les utilisateurs peuvent ainsi déterminer si un service fonctionne correctement. Par défaut, les services qui héritent de <xref:System.ServiceProcess.ServiceBase> indiquent un ensemble limité de paramètres d'état, notamment Arrêté, Suspendu et En cours d'exécution. Si le démarrage d'un service prend un peu de temps, il peut être utile de signaler un état Démarrer Suspendre. Vous pouvez également implémenter les paramètres d’état Démarrer Suspendre et Arrêter Suspendre en ajoutant du code qui appelle la [fonction SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) Windows.

Pour implémenter l'état de service suspendu :

1. Ajoutez une instruction `using` ou une déclaration `Imports` à l’espace de noms <xref:System.Runtime.InteropServices?displayProperty=nameWithType> dans le fichier MyNewService.cs ou MyNewService.vb :

    ```csharp
    using System.Runtime.InteropServices;
    ```

    ```vb
    Imports System.Runtime.InteropServices
    ```

2. Ajoutez le code suivant dans MyNewService.cs pour déclarer les valeurs `ServiceState` et ajouter une structure pour l'état. Vous utiliserez cette structure dans un appel de code non managé :

    ```csharp
    public enum ServiceState
    {
        SERVICE_STOPPED = 0x00000001,
        SERVICE_START_PENDING = 0x00000002,
        SERVICE_STOP_PENDING = 0x00000003,
        SERVICE_RUNNING = 0x00000004,
        SERVICE_CONTINUE_PENDING = 0x00000005,
        SERVICE_PAUSE_PENDING = 0x00000006,
        SERVICE_PAUSED = 0x00000007,
    }

    [StructLayout(LayoutKind.Sequential)]
    public struct ServiceStatus
    {
        public int dwServiceType;
        public ServiceState dwCurrentState;
        public int dwControlsAccepted;
        public int dwWin32ExitCode;
        public int dwServiceSpecificExitCode;
        public int dwCheckPoint;
        public int dwWaitHint;
    };
    ```

    ```vb
    Public Enum ServiceState
        SERVICE_STOPPED = 1
        SERVICE_START_PENDING = 2
        SERVICE_STOP_PENDING = 3
        SERVICE_RUNNING = 4
        SERVICE_CONTINUE_PENDING = 5
        SERVICE_PAUSE_PENDING = 6
        SERVICE_PAUSED = 7
    End Enum

    <StructLayout(LayoutKind.Sequential)>
    Public Structure ServiceStatus
        Public dwServiceType As Long
        Public dwCurrentState As ServiceState
        Public dwControlsAccepted As Long
        Public dwWin32ExitCode As Long
        Public dwServiceSpecificExitCode As Long
        Public dwCheckPoint As Long
        Public dwWaitHint As Long
    End Structure
    ```

3. Maintenant, dans la classe `MyNewService`, déclarez la [fonction SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) à l’aide d’un [appel de code non managé](../interop/consuming-unmanaged-dll-functions.md) :

    ```csharp
    [DllImport("advapi32.dll", SetLastError = true)]
    private static extern bool SetServiceStatus(System.IntPtr handle, ref ServiceStatus serviceStatus);
    ```

    ```vb
    Declare Auto Function SetServiceStatus Lib "advapi32.dll" (ByVal handle As IntPtr, ByRef serviceStatus As ServiceStatus) As Boolean
    ```

4. Pour implémenter l'état Démarrer Suspendre, ajoutez le code suivant au début de la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> :

    ```csharp
    // Update the service state to Start Pending.
    ServiceStatus serviceStatus = new ServiceStatus();
    serviceStatus.dwCurrentState = ServiceState.SERVICE_START_PENDING;
    serviceStatus.dwWaitHint = 100000;
    SetServiceStatus(this.ServiceHandle, ref serviceStatus);
    ```

    ```vb
    ' Update the service state to Start Pending.
    Dim serviceStatus As ServiceStatus = New ServiceStatus()
    serviceStatus.dwCurrentState = ServiceState.SERVICE_START_PENDING
    serviceStatus.dwWaitHint = 100000
    SetServiceStatus(Me.ServiceHandle, serviceStatus)
    ```

5. Ajoutez du code pour définir l'état En cours d'exécution à la fin de la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> .

    ```csharp
    // Update the service state to Running.
    serviceStatus.dwCurrentState = ServiceState.SERVICE_RUNNING;
    SetServiceStatus(this.ServiceHandle, ref serviceStatus);
    ```

    ```vb
    ' Update the service state to Running.
    serviceStatus.dwCurrentState = ServiceState.SERVICE_RUNNING
    SetServiceStatus(Me.ServiceHandle, serviceStatus)
    ```

6. (Facultatif) Répétez cette procédure pour la méthode <xref:System.ServiceProcess.ServiceBase.OnStop%2A> .

> [!NOTE]
> La boîte de dialogue [Gestionnaire de contrôle des services](/windows/desktop/Services/service-control-manager) utilise les membres `dwWaitHint` et `dwCheckpoint` de la [structure SERVICE_STATUS](/windows/desktop/api/winsvc/ns-winsvc-_service_status) pour déterminer le délai d’attente avant le démarrage ou l’arrêt d’un service Windows. Si l’exécution de vos méthodes <xref:System.ServiceProcess.ServiceBase.OnStart%2A> et <xref:System.ServiceProcess.ServiceBase.OnStop%2A> est longue, votre service peut demander plus de temps en appelant à nouveau [SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) avec une valeur `dwCheckPoint` incrémentée.

## <a name="add-installers-to-the-service"></a>Ajouter des programmes d'installation pour le service

Avant de pouvoir exécuter un service Windows, vous devez l'installer, ce qui l'inscrit auprès du Gestionnaire de contrôle des services. Vous pouvez ajouter à votre projet des programmes d'installation qui gèrent les détails de l'inscription.

1. Dans l' **Explorateur de solutions**, ouvrez le menu contextuel pour **MyNewService.cs** ou **MyNewService.vb**, puis choisissez **Concepteur de vues**.

2. Cliquez sur l'arrière-plan du concepteur pour sélectionner le service lui-même plutôt que son contenu.

3. Ouvrez le menu contextuel de la fenêtre du concepteur (si vous utilisez un dispositif de pointage, cliquez avec le bouton droit à l'intérieur de la fenêtre), puis choisissez **Ajouter le programme d'installation**.

   Par défaut, une classe Component comprenant deux programmes d'installation est ajoutée à votre projet. Le composant est appelé **ProjectInstaller**et contient le programme d'installation de votre service ainsi que le programme d'installation du processus associé au service.

4. En mode **Design** pour **ProjectInstaller**, choisissez **serviceInstaller1** pour un projet Visual C# ou **ServiceInstaller1** pour un projet Visual Basic.

5. Dans la fenêtre **Propriétés** , vérifiez que la propriété <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> a la valeur **MyNewService**.

6. Affectez à la propriété **Description** du texte, par exemple « Un exemple de service ». Ce texte, qui s'affiche dans la fenêtre Services, permet à l'utilisateur d'identifier le service et de comprendre son utilité.

7. Affectez à la propriété <xref:System.ServiceProcess.ServiceInstaller.DisplayName%2A> le texte à afficher dans la colonne **Nom** de la fenêtre Services. Par exemple, vous pouvez entrer « Nom complet de MyNewService ». Ce nom peut être différent de la propriété <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> , qui est le nom utilisé par le système (par exemple, lorsque vous utilisez la commande `net start` pour démarrer votre service).

8. Affectez à la propriété <xref:System.ServiceProcess.ServiceInstaller.StartType%2A> la valeur <xref:System.ServiceProcess.ServiceStartMode.Automatic>.

     ![Propriétés du programme d’installation d’un service Windows](../../../docs/framework/windows-services/media/windowsservice-installerproperties.PNG "WindowsService_InstallerProperties")

9. Dans le concepteur, choisissez **serviceProcessInstaller1** pour un projet Visual C# ou **ServiceProcessInstaller1** pour un projet Visual Basic. Affectez à la propriété <xref:System.ServiceProcess.ServiceProcessInstaller.Account%2A> la valeur <xref:System.ServiceProcess.ServiceAccount.LocalSystem>. Ainsi, le service est installé et exécuté à l’aide du compte système local.

    > [!IMPORTANT]
    > Le compte <xref:System.ServiceProcess.ServiceAccount.LocalSystem> dispose d'autorisations générales, y compris la possibilité d'écrire dans le journal des événements. Utilisez ce compte avec précaution car il peut augmenter le risque d'attaques par des logiciels malveillants. Pour les autres tâches, utilisez le compte <xref:System.ServiceProcess.ServiceAccount.LocalService>, qui se comporte comme un utilisateur non privilégié de l'ordinateur local et présente des informations d'identification anonymes à tout serveur distant. Cet exemple échoue si vous essayez d'utiliser le compte <xref:System.ServiceProcess.ServiceAccount.LocalService>, car il doit disposer d'une autorisation pour écrire dans le journal des événements.

Pour plus d’informations sur les programmes d’installation, consultez [Guide pratique pour ajouter des programmes d’installation à votre application de service](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md).

## <a name="optional-set-startup-parameters"></a>(Facultatif) Définition de paramètres de démarrage

Un service Windows, comme tout autre fichier exécutable, peut accepter des arguments de ligne de commande ou des paramètres de démarrage. Lorsque vous ajoutez du code pour traiter les paramètres de démarrage, les utilisateurs peuvent démarrer votre service avec leurs propres paramètres de démarrage personnalisés à l'aide de la fenêtre Services du panneau de configuration Windows. Toutefois, ces paramètres de démarrage ne sont pas persistants lors du prochain démarrage du service. Pour définir les paramètres de démarrage de façon permanente, vous pouvez les définir dans le Registre, comme indiqué dans la procédure suivante.

> [!NOTE]
> Avant de décider d'ajouter des paramètres de démarrage, vous devez déterminer si c'est le meilleur moyen de passer des informations à votre service. Les paramètres de démarrage sont faciles à utiliser et à analyser, et les utilisateurs peuvent facilement les substituer. Il peut toutefois être plus difficile pour les utilisateurs de les détecter et de les utiliser sans documentation. En général, si votre service nécessite seulement quelques paramètres de démarrage, vous devez envisager d'utiliser plutôt le Registre ou un fichier de configuration. Tous les services Windows ont une entrée dans le Registre, sous **HKLM\System\CurrentControlSet\services**. Sous la clé du service, vous pouvez utiliser la sous-clé **Parameters** pour stocker les informations auxquelles votre service peut accéder. Vous pouvez utiliser des fichiers de configuration d'application pour un service Windows de la même façon que vous le faites pour les autres types de programmes. Pour obtenir un exemple de code, consultez <xref:System.Configuration.ConfigurationManager.AppSettings%2A>.

Pour ajouter des paramètres de démarrage :

1. Dans la méthode `Main` dans le fichier Program.cs ou MyNewService.Designer.vb, ajoutez un paramètre d’entrée à passer au constructeur de service :

   ```csharp
   static void Main(string[] args)
   {
       ServiceBase[] ServicesToRun;
       ServicesToRun = new ServiceBase[]
       {
           new MyNewService(args)
       };
       ServiceBase.Run(ServicesToRun);
   }
   ```

   ```vb
   Shared Sub Main(ByVal cmdArgs() As String)
       Dim ServicesToRun() As System.ServiceProcess.ServiceBase = New System.ServiceProcess.ServiceBase() {New MyNewServiceVB(cmdArgs)}
       System.ServiceProcess.ServiceBase.Run(ServicesToRun)
   End Sub
   ```

2. Modifiez le constructeur `MyNewService` comme suit :

   ```csharp
   public MyNewService(string[] args)
   {
       InitializeComponent();

        string eventSourceName = "MySource";
        string logName = "MyNewLog";

        if (args.Length > 0)
        {
            eventSourceName = args[0];
        }

        if (args.Length > 1)
        {
            logName = args[1];
        }

        eventLog1 = new System.Diagnostics.EventLog();

        if (!System.Diagnostics.EventLog.SourceExists(eventSourceName))
        {
            System.Diagnostics.EventLog.CreateEventSource(eventSourceName, logName);
        }

        eventLog1.Source = eventSourceName;
        eventLog1.Log = logName;
   }
   ```

   ```vb
   Public Sub New(ByVal cmdArgs() As String)
       InitializeComponent()
       Dim eventSourceName As String = "MySource"
       Dim logName As String = "MyNewLog"
       If (cmdArgs.Count() > 0) Then
           eventSourceName = cmdArgs(0)
       End If
       If (cmdArgs.Count() > 1) Then
           logName = cmdArgs(1)
       End If
       eventLog1 = New System.Diagnostics.EventLog()
       If (Not System.Diagnostics.EventLog.SourceExists(eventSourceName)) Then
           System.Diagnostics.EventLog.CreateEventSource(eventSourceName, logName)
       End If
       eventLog1.Source = eventSourceName
       eventLog1.Log = logName
   End Sub
   ```

   Ce code définit la source d'événement et le nom du journal en fonction des paramètres de démarrage fournis, ou utilise les valeurs par défaut si aucun argument n'est fourni.

3. Pour spécifier les arguments de ligne de commande, ajoutez le code suivant à la classe `ProjectInstaller` dans ProjectInstaller.cs ou ProjectInstaller.vb :

   ```csharp
   protected override void OnBeforeInstall(IDictionary savedState)
   {
       string parameter = "MySource1\" \"MyLogFile1";
       Context.Parameters["assemblypath"] = "\"" + Context.Parameters["assemblypath"] + "\" \"" + parameter + "\"";
       base.OnBeforeInstall(savedState);
   }
   ```

   ```vb
   Protected Overrides Sub OnBeforeInstall(ByVal savedState As IDictionary)
       Dim parameter As String = "MySource1"" ""MyLogFile1"
       Context.Parameters("assemblypath") = """" + Context.Parameters("assemblypath") + """ """ + parameter + """"
       MyBase.OnBeforeInstall(savedState)
   End Sub
   ```

   Ce code modifie la clé de Registre **ImagePath** qui contient généralement le chemin d'accès complet au fichier exécutable du service Windows, en ajoutant les valeurs de paramètres par défaut. Les guillemets autour du chemin d'accès (et autour de chaque paramètre individuel) sont nécessaires pour que le service démarre correctement. Pour modifier les paramètres de démarrage de ce service Windows, les utilisateurs peuvent modifier les paramètres indiqués dans la clé de Registre **ImagePath** . La meilleure méthode consiste toutefois à la modifier par programmation et à exposer les fonctionnalités aux utilisateurs d'une manière conviviale (par exemple dans un utilitaire de gestion ou de configuration).

## <a name="build-the-service"></a>Générer le service

1. Dans l' **Explorateur de solutions**, ouvrez le menu contextuel de votre projet, puis choisissez **Propriétés**.

   Les pages de propriétés de votre projet s'affichent.

2. Dans la liste **Objet de démarrage** de l'onglet **Application**, choisissez **MyNewService.Program**.

3. Dans **l’Explorateur de solutions**, ouvrez le menu contextuel de votre projet, puis choisissez **Générer** pour générer le projet (ou appuyez sur **Ctrl**+**Maj**+**B**).

## <a name="install-the-service"></a>Installer le service

Maintenant que vous avez généré le service Windows, vous pouvez l'installer. Pour installer un service Windows, vous devez disposer d'informations d'identification d'administrateur sur l'ordinateur sur lequel vous l'installez.

1. Ouvrez **Invite de commandes développeur pour Visual Studio** avec des informations d'identification administratives. Si vous utilisez une souris, cliquez avec le bouton droit sur **Invite de commandes développeur pour VS 2017** dans le menu Démarrer de Windows, puis choisissez **Plus** > **Exécuter en tant qu'administrateur**.

2. Dans la fenêtre **Invite de commandes développeur**, accédez au dossier qui contient la sortie de votre projet (par défaut, il s’agit du sous-répertoire *\bin\Debug* de votre projet).

3. Entrez la commande suivante :

    ```shell
    installutil.exe MyNewService.exe
    ```

    Si le service est installé correctement, le fichier **installutil.exe** le signale. Si le système n'a pas trouvé **InstallUtil.exe**, vérifiez qu'il existe sur votre ordinateur. Cet outil est installé avec le .NET Framework dans le dossier *%windir%\Microsoft.NET\Framework[64]\\[version du framework]*. Par exemple, le chemin d’accès par défaut pour la version 32 bits est *%windir%\Microsoft.NET\Framework\v4.0.30319\InstallUtil.exe*.

    Si le processus **installutil.exe** signale un échec, examinez le journal d’installation pour en connaître la raison. Par défaut, le journal se trouve dans le même dossier que l’exécutable du service. L’installation peut échouer si la classe <xref:System.ComponentModel.RunInstallerAttribute> n’est pas présente sur la classe `ProjectInstaller`, si l’attribut n’a pas la valeur **true** ou si la classe `ProjectInstaller` n’est pas **publique**.

Pour plus d'informations, consultez [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).

## <a name="start-and-run-the-service"></a>Démarrer et exécuter le service

1. Dans Windows, ouvrez l’application de bureau **Services**. Appuyez sur **Windows**+**R** pour ouvrir la zone **Exécuter**, puis entrez **services.msc** et appuyez sur **Entrée** ou cliquez sur **OK**.

     Votre service doit être répertorié dans **Services**, affiché par ordre alphabétique du nom d’affichage que vous lui avez donné.

     ![MyNewService dans la fenêtre Services.](../../../docs/framework/windows-services/media/windowsservices-serviceswindow.PNG)

2. Dans **Services**, ouvrez le menu contextuel de votre service, puis choisissez **Démarrer**.

3. Pour arrêter le service, ouvrez le menu contextuel de votre service, puis choisissez **Arrêter**.

4. (Facultatif) À partir de la ligne de commande, vous pouvez utiliser les commandes `net start ServiceName` et `net stop ServiceName` pour démarrer et arrêter votre service.

### <a name="verify-the-event-log-output-of-your-service"></a>Vérifier la sortie du journal des événements de votre service

1. Ouvrez **l’Observateur d’événements** en commençant à taper **Observateur d’événements** dans la zone de recherche de la barre des tâches Windows, puis en sélectionnant **Observateur d’événements** dans les résultats de recherche.

   > [!TIP]
   > Dans Visual Studio, vous pouvez accéder aux journaux des événements en ouvrant **l’Explorateur de serveurs** (clavier : **Ctrl**+**Alt**+**S**) et en développant le nœud **Journaux des événements** pour l’ordinateur local.

2. Dans **l’Observateur d’événements**, développez **Journaux des applications et services**.

3. Recherchez le nom **MyNewLog** (ou **MyLogFile1**, si vous avez utilisé la procédure facultative pour ajouter des arguments de ligne de commande) dans la liste, puis développez-le. Vous devez voir des entrées relatives aux deux actions (démarrage et arrêt) que votre service a effectuées.

     ![Utiliser l'Observateur d'événements pour visualiser les entrées du journal des événements](../../../docs/framework/windows-services/media/windows-service-event-viewer.png)

## <a name="uninstall-the-service"></a>Désinstaller le service

1. Ouvrez **Invite de commandes développeur pour Visual Studio** avec des informations d'identification administratives.

2. Dans la fenêtre d'invite de commandes, accédez au dossier qui contient la sortie de votre projet.

3. Entrez la commande suivante :

    ```shell
    installutil.exe /u MyNewService.exe
    ```

   Si le service est désinstallé avec succès, **installutil.exe** le signale. Pour plus d'informations, consultez [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).

## <a name="next-steps"></a>Étapes suivantes

Maintenant que vous avez créé le service, vous pouvez créer un programme d'installation autonome que d'autres peuvent utiliser pour installer votre service Windows. ClickOnce ne prend pas en charge les services Windows, mais vous pouvez utiliser [WiX Toolset](http://wixtoolset.org/) pour créer un programme d’installation pour un service Windows. Pour d’autres idées, consultez [Créer un package de programme d’installation](/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-client).

Vous pouvez également opter pour l'utilisation d'un composant <xref:System.ServiceProcess.ServiceController>, ce qui vous permet d'envoyer des commandes au service que vous avez installé.

Vous pouvez utiliser un programme d'installation pour créer un journal des événements lors de l'installation de l'application plutôt que lors de son exécution. En outre, le journal des événements sera supprimé par le programme d'installation lors de la désinstallation de l'application. Pour plus d'informations, consultez la page de référence relative à <xref:System.Diagnostics.EventLogInstaller> .

## <a name="see-also"></a>Voir aussi

- [Applications de service Windows](../../../docs/framework/windows-services/index.md)
- [Introduction aux applications de service Windows](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
- [Guide pratique pour déboguer les applications de service Windows](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md)
- [Services (Windows)](https://msdn.microsoft.com/library/windows/desktop/ms685141.aspx)
