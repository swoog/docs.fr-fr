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
ms.openlocfilehash: 52c2f64bbb71e07dcab1fd7cd42662f9ed2c8445
ms.sourcegitcommit: 2b986afe4ce9e13bbeec929c9737757eb61de60e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56665028"
---
# <a name="walkthrough-create-a-windows-service-app"></a><span data-ttu-id="ae682-102">Procédure pas à pas : Créer une application de service Windows</span><span class="sxs-lookup"><span data-stu-id="ae682-102">Walkthrough: Create a Windows service app</span></span>

<span data-ttu-id="ae682-103">Cet article explique comment créer, dans Visual Studio, une application de service Windows simple qui écrit des messages dans un journal des événements.</span><span class="sxs-lookup"><span data-stu-id="ae682-103">This article demonstrates how to create a simple Windows service app in Visual Studio that writes messages to an event log.</span></span>

## <a name="create-a-service"></a><span data-ttu-id="ae682-104">Créer un service</span><span class="sxs-lookup"><span data-stu-id="ae682-104">Create a service</span></span>

<span data-ttu-id="ae682-105">Pour commencer, créez votre projet et définissez les valeurs nécessaires au fonctionnement correct du service.</span><span class="sxs-lookup"><span data-stu-id="ae682-105">To begin, create the project and set values that are required for the service to function correctly.</span></span>

1. <span data-ttu-id="ae682-106">Dans Visual Studio, dans la barre de menus, choisissez **Fichier** > **Nouveau** > **Projet** (ou appuyez sur **Ctrl**+**MAJ**+**N**) pour ouvrir la boîte de dialogue **Nouveau projet**.</span><span class="sxs-lookup"><span data-stu-id="ae682-106">In Visual Studio, on the menu bar, choose **File** > **New** > **Project** (or press **Ctrl**+**Shift**+**N**) to open the **New Project** dialog.</span></span>

2. <span data-ttu-id="ae682-107">Accédez au modèle de projet **Windows Service** et sélectionnez-le.</span><span class="sxs-lookup"><span data-stu-id="ae682-107">Navigate to and select the **Windows Service** project template.</span></span> <span data-ttu-id="ae682-108">Développez **Installé** > [**Visual C#** ou **Visual Basic**] > **Windows Desktop** ou tapez **Windows Service** dans la zone de recherche dans l’angle supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="ae682-108">Expand **Installed** > [**Visual C#** or **Visual Basic**] > **Windows Desktop**, or type **Windows Service** in the search box on the upper right.</span></span>

   ![Modèle Windows Service dans la boîte de dialogue Nouveau projet de Visual Studio](media/new-project-dialog.png)

   > [!NOTE]
   > <span data-ttu-id="ae682-110">Si le modèle **Windows Service** ne s’affiche pas, vous devrez peut-être installer la charge de travail **Développement bureau .NET**.</span><span class="sxs-lookup"><span data-stu-id="ae682-110">If you don't see the **Windows Service** template, you may need to install the **.NET desktop development** workload.</span></span> <span data-ttu-id="ae682-111">Dans la boîte de dialogue **Nouveau projet**, cliquez sur le lien **Ouvrir Visual Studio Installer** dans l’angle inférieur gauche.</span><span class="sxs-lookup"><span data-stu-id="ae682-111">In the **New Project** dialog, click the link that says **Open Visual Studio Installer** on the lower left.</span></span> <span data-ttu-id="ae682-112">Dans **Visual Studio Installer**, sélectionnez la charge de travail **Développement bureau .NET** et choisissez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="ae682-112">In **Visual Studio Installer**, select the **.NET desktop development** workload and then choose **Modify**.</span></span>

3. <span data-ttu-id="ae682-113">Nommez le projet **MyNewService**, puis choisissez **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae682-113">Name the project **MyNewService**, and then choose **OK**.</span></span>

   <span data-ttu-id="ae682-114">Le modèle de projet inclut une classe Component appelée `Service1` qui hérite de <xref:System.ServiceProcess.ServiceBase?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="ae682-114">The project template includes a component class named `Service1` that inherits from <xref:System.ServiceProcess.ServiceBase?displayProperty=nameWithType>.</span></span> <span data-ttu-id="ae682-115">Elle contient une grande partie du code de service de base, comme le code pour démarrer le service.</span><span class="sxs-lookup"><span data-stu-id="ae682-115">It includes much of the basic service code, such as the code to start the service.</span></span>

## <a name="rename-the-service"></a><span data-ttu-id="ae682-116">Renommer le service</span><span class="sxs-lookup"><span data-stu-id="ae682-116">Rename the service</span></span>

<span data-ttu-id="ae682-117">Renommez le service **Service1** en **MyNewService**.</span><span class="sxs-lookup"><span data-stu-id="ae682-117">Rename the service from **Service1** to **MyNewService**.</span></span>

1. <span data-ttu-id="ae682-118">Dans le mode **Création** pour Service1.cs (ou Service1.vb), cliquez sur le lien pour **passer en mode Code**.</span><span class="sxs-lookup"><span data-stu-id="ae682-118">In the **Design** view for Service1.cs (or Service1.vb), click the link to **switch to code view**.</span></span> <span data-ttu-id="ae682-119">Cliquez avec le bouton droit sur **Service1** et sélectionnez **Renommer** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ae682-119">Right-click on **Service1** and select **Rename** from the context menu.</span></span> <span data-ttu-id="ae682-120">Entrez **MyNewService**, puis appuyez sur **Entrée** ou cliquez sur **Appliquer**.</span><span class="sxs-lookup"><span data-stu-id="ae682-120">Enter **MyNewService** and then press **Enter** or click **Apply**.</span></span>

2. <span data-ttu-id="ae682-121">Dans la fenêtre **Propriétés** pour **Service1.cs [Design]** ou **Service1.vb [Design]**, remplacez la valeur **ServiceName** par **MyNewService**.</span><span class="sxs-lookup"><span data-stu-id="ae682-121">In the **Properties** window for **Service1.cs [Design]** or **Service1.vb [Design]**, change the **ServiceName** value to **MyNewService**.</span></span>

3. <span data-ttu-id="ae682-122">Dans **l’Explorateur de solutions**, renommez **Service1.cs** en **MyNewService.cs**, ou renommez **Service1.vb** en **MyNewService.vb**.</span><span class="sxs-lookup"><span data-stu-id="ae682-122">In **Solution Explorer**, rename **Service1.cs** to **MyNewService.cs**, or rename **Service1.vb** to **MyNewService.vb**.</span></span>

## <a name="add-features-to-the-service"></a><span data-ttu-id="ae682-123">Ajouter des fonctionnalités au service</span><span class="sxs-lookup"><span data-stu-id="ae682-123">Add features to the service</span></span>

<span data-ttu-id="ae682-124">Dans cette section, vous ajoutez un journal des événements personnalisé au service Windows.</span><span class="sxs-lookup"><span data-stu-id="ae682-124">In this section, you add a custom event log to the Windows service.</span></span> <span data-ttu-id="ae682-125">Les journaux des événements ne sont en aucune façon associés aux services Windows.</span><span class="sxs-lookup"><span data-stu-id="ae682-125">Event logs are not associated in any way with Windows services.</span></span> <span data-ttu-id="ae682-126">Ici, le composant <xref:System.Diagnostics.EventLog> est utilisé comme un exemple du type de composants que vous pouvez ajouter à un service Windows.</span><span class="sxs-lookup"><span data-stu-id="ae682-126">The <xref:System.Diagnostics.EventLog> component is used here as an example of the type of component you can add to a Windows service.</span></span>

### <a name="add-custom-event-log-functionality"></a><span data-ttu-id="ae682-127">Ajouter une fonctionnalité de journal des événements personnalisé</span><span class="sxs-lookup"><span data-stu-id="ae682-127">Add custom event log functionality</span></span>

1. <span data-ttu-id="ae682-128">Dans l' **Explorateur de solutions**, ouvrez le menu contextuel pour **MyNewService.cs** ou **MyNewService.vb**, puis choisissez **Concepteur de vues**.</span><span class="sxs-lookup"><span data-stu-id="ae682-128">In **Solution Explorer**, open the context menu for **MyNewService.cs** or **MyNewService.vb**, and then choose **View Designer**.</span></span>

2. <span data-ttu-id="ae682-129">À partir de la section **Composants** de la **boîte à outils**, faites glisser un composant <xref:System.Diagnostics.EventLog> jusqu'au concepteur.</span><span class="sxs-lookup"><span data-stu-id="ae682-129">From the **Components** section of the **Toolbox**, drag an <xref:System.Diagnostics.EventLog> component to the designer.</span></span>

3. <span data-ttu-id="ae682-130">Dans l' **Explorateur de solutions**, ouvrez le menu contextuel pour **MyNewService.cs** ou **MyNewService.vb**, puis choisissez **Afficher le code**.</span><span class="sxs-lookup"><span data-stu-id="ae682-130">In **Solution Explorer**, open the context menu for **MyNewService.cs** or **MyNewService.vb**, and then choose **View Code**.</span></span>

4. <span data-ttu-id="ae682-131">Modifiez le constructeur pour définir un journal des événements personnalisé :</span><span class="sxs-lookup"><span data-stu-id="ae682-131">Edit the constructor to define a custom event log:</span></span>

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

### <a name="define-what-occurs-when-the-service-starts"></a><span data-ttu-id="ae682-132">Définir les actions à effectuer lors du démarrage du service</span><span class="sxs-lookup"><span data-stu-id="ae682-132">Define what occurs when the service starts</span></span>

<span data-ttu-id="ae682-133">Dans l’éditeur de code, localisez la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> qui a été automatiquement substituée lorsque vous avez créé le projet.</span><span class="sxs-lookup"><span data-stu-id="ae682-133">In the code editor, locate the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method that was automatically overridden when you created the project.</span></span> <span data-ttu-id="ae682-134">Ajoutez une ligne de code qui écrit une entrée dans le journal des événements lorsque le service démarre :</span><span class="sxs-lookup"><span data-stu-id="ae682-134">Add a line of code that writes an entry to the event log when the service starts:</span></span>

[!code-csharp[VbRadconService#3](../../../samples/snippets/csharp/VS_Snippets_VBCSharp/VbRadconService/CS/MyNewService.cs#3)]
[!code-vb[VbRadconService#3](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#3)]

<span data-ttu-id="ae682-135">Une application de service est conçue pour s'exécuter sur une longue durée, et elle interroge ou surveille généralement quelque chose dans le système.</span><span class="sxs-lookup"><span data-stu-id="ae682-135">A service application is designed to be long-running, so it usually polls or monitors something in the system.</span></span> <span data-ttu-id="ae682-136">La surveillance est configurée dans la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> .</span><span class="sxs-lookup"><span data-stu-id="ae682-136">The monitoring is set up in the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method.</span></span> <span data-ttu-id="ae682-137">Toutefois, la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> n'effectue pas elle-même la surveillance.</span><span class="sxs-lookup"><span data-stu-id="ae682-137">However, <xref:System.ServiceProcess.ServiceBase.OnStart%2A> doesn’t actually do the monitoring.</span></span> <span data-ttu-id="ae682-138">La méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> doit retourner au système d'exploitation dès que le service est en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="ae682-138">The <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method must return to the operating system after the service's operation has begun.</span></span> <span data-ttu-id="ae682-139">Elle ne doit pas s'exécuter indéfiniment en boucle ni se bloquer.</span><span class="sxs-lookup"><span data-stu-id="ae682-139">It must not loop forever or block.</span></span> <span data-ttu-id="ae682-140">Pour définir un mécanisme d'interrogation simple, vous pouvez utiliser le composant <xref:System.Timers.Timer?displayProperty=nameWithType>, comme suit : Dans la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A>, définissez des paramètres sur le composant, puis attribuez à la propriété <xref:System.Timers.Timer.Enabled%2A> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="ae682-140">To set up a simple polling mechanism, you can use the <xref:System.Timers.Timer?displayProperty=nameWithType> component as follows: In the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method, set parameters on the component, and then set the <xref:System.Timers.Timer.Enabled%2A> property to `true`.</span></span> <span data-ttu-id="ae682-141">La minuterie déclenche périodiquement des événements dans votre code, lesquels indiquent au service qu'il peut effectuer son analyse.</span><span class="sxs-lookup"><span data-stu-id="ae682-141">The timer raises events in your code periodically, at which time your service could do its monitoring.</span></span> <span data-ttu-id="ae682-142">Pour cela, vous pouvez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="ae682-142">You can use the following code to do this:</span></span>

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

<span data-ttu-id="ae682-143">Ajoutez une variable membre à la classe.</span><span class="sxs-lookup"><span data-stu-id="ae682-143">Add a member variable to the class.</span></span> <span data-ttu-id="ae682-144">Elle contient l’identificateur de l’événement suivant à écrire dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="ae682-144">It contains the identifier of the next event to write into the event log.</span></span>

```csharp
private int eventId = 1;
```

```vb
Private eventId As Integer = 1
```

<span data-ttu-id="ae682-145">Ajoutez une nouvelle méthode pour gérer l'événement du minuteur :</span><span class="sxs-lookup"><span data-stu-id="ae682-145">Add a new method to handle the timer event:</span></span>

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

<span data-ttu-id="ae682-146">Vous pouvez effectuer des tâches à l'aide de threads de travail en arrière-plan au lieu d'exécuter l'ensemble de votre travail sur le thread principal.</span><span class="sxs-lookup"><span data-stu-id="ae682-146">You might want to perform tasks by using background worker threads instead of running all your work on the main thread.</span></span> <span data-ttu-id="ae682-147">Pour plus d'informations, consultez <xref:System.ComponentModel.BackgroundWorker?displayProperty=fullName>.</span><span class="sxs-lookup"><span data-stu-id="ae682-147">For more information, see <xref:System.ComponentModel.BackgroundWorker?displayProperty=fullName>.</span></span>

### <a name="define-what-occurs-when-the-service-is-stopped"></a><span data-ttu-id="ae682-148">Définir les actions à effectuer lors de l'arrêt du service</span><span class="sxs-lookup"><span data-stu-id="ae682-148">Define what occurs when the service is stopped</span></span>

<span data-ttu-id="ae682-149">Ajoutez une ligne de code à la méthode <xref:System.ServiceProcess.ServiceBase.OnStop%2A> qui ajoute une entrée dans le journal des événements lorsque le service est arrêté :</span><span class="sxs-lookup"><span data-stu-id="ae682-149">Add a line of code to the <xref:System.ServiceProcess.ServiceBase.OnStop%2A> method that adds an entry to the event log when the service is stopped:</span></span>

```csharp
eventLog1.WriteEntry("In OnStop.");
```

[!code-vb[VbRadconService#4](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#4)]

### <a name="define-other-actions-for-the-service"></a><span data-ttu-id="ae682-150">Définir d'autres actions du service</span><span class="sxs-lookup"><span data-stu-id="ae682-150">Define other actions for the service</span></span>

<span data-ttu-id="ae682-151">Vous pouvez substituer les méthodes <xref:System.ServiceProcess.ServiceBase.OnPause%2A>, <xref:System.ServiceProcess.ServiceBase.OnContinue%2A> et <xref:System.ServiceProcess.ServiceBase.OnShutdown%2A> afin de définir d'autres types de traitement pour votre composant.</span><span class="sxs-lookup"><span data-stu-id="ae682-151">You can override the <xref:System.ServiceProcess.ServiceBase.OnPause%2A>, <xref:System.ServiceProcess.ServiceBase.OnContinue%2A>, and <xref:System.ServiceProcess.ServiceBase.OnShutdown%2A> methods to define additional processing for your component.</span></span> <span data-ttu-id="ae682-152">Le code suivant montre comment substituer la méthode <xref:System.ServiceProcess.ServiceBase.OnContinue%2A> :</span><span class="sxs-lookup"><span data-stu-id="ae682-152">The following code shows how you can override the <xref:System.ServiceProcess.ServiceBase.OnContinue%2A> method:</span></span>

[!code-csharp[VbRadconService#5](../../../samples/snippets/csharp/VS_Snippets_VBCSharp/VbRadconService/CS/MyNewService.cs#5)]
[!code-vb[VbRadconService#5](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#5)]

<span data-ttu-id="ae682-153">Certaines actions personnalisées doivent se produire lorsqu'un service Windows est installé par la classe <xref:System.Configuration.Install.Installer> .</span><span class="sxs-lookup"><span data-stu-id="ae682-153">Some custom actions have to occur when a Windows service is installed by the <xref:System.Configuration.Install.Installer> class.</span></span> <span data-ttu-id="ae682-154">Visual Studio peut créer ces programmes d'installation spécialement pour un service Windows et les ajouter à votre projet.</span><span class="sxs-lookup"><span data-stu-id="ae682-154">Visual Studio can create these installers specifically for a Windows service and add them to your project.</span></span>

## <a name="set-service-status"></a><span data-ttu-id="ae682-155">Définir l’état du service</span><span class="sxs-lookup"><span data-stu-id="ae682-155">Set service status</span></span>

<span data-ttu-id="ae682-156">Les services indiquent leur état au Gestionnaire de contrôle des services. Les utilisateurs peuvent ainsi déterminer si un service fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="ae682-156">Services report their status to the Service Control Manager, so that users can tell whether a service is functioning correctly.</span></span> <span data-ttu-id="ae682-157">Par défaut, les services qui héritent de <xref:System.ServiceProcess.ServiceBase> indiquent un ensemble limité de paramètres d'état, notamment Arrêté, Suspendu et En cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="ae682-157">By default, services that inherit from <xref:System.ServiceProcess.ServiceBase> report a limited set of status settings, including Stopped, Paused, and Running.</span></span> <span data-ttu-id="ae682-158">Si le démarrage d'un service prend un peu de temps, il peut être utile de signaler un état Démarrer Suspendre.</span><span class="sxs-lookup"><span data-stu-id="ae682-158">If a service takes a little while to start up, it might be helpful to report a Start Pending status.</span></span> <span data-ttu-id="ae682-159">Vous pouvez également implémenter les paramètres d’état Démarrer Suspendre et Arrêter Suspendre en ajoutant du code qui appelle la [fonction SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) Windows.</span><span class="sxs-lookup"><span data-stu-id="ae682-159">You can also implement the Start Pending and Stop Pending status settings by adding code that calls into the Windows [SetServiceStatus function](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus).</span></span>

<span data-ttu-id="ae682-160">Pour implémenter l'état de service suspendu :</span><span class="sxs-lookup"><span data-stu-id="ae682-160">To implement service pending status:</span></span>

1. <span data-ttu-id="ae682-161">Ajoutez une instruction `using` ou une déclaration `Imports` à l’espace de noms <xref:System.Runtime.InteropServices?displayProperty=nameWithType> dans le fichier MyNewService.cs ou MyNewService.vb :</span><span class="sxs-lookup"><span data-stu-id="ae682-161">Add a `using` statement or `Imports` declaration for the <xref:System.Runtime.InteropServices?displayProperty=nameWithType> namespace in the MyNewService.cs or MyNewService.vb file:</span></span>

    ```csharp
    using System.Runtime.InteropServices;
    ```

    ```vb
    Imports System.Runtime.InteropServices
    ```

2. <span data-ttu-id="ae682-162">Ajoutez le code suivant dans MyNewService.cs pour déclarer les valeurs `ServiceState` et ajouter une structure pour l'état. Vous utiliserez cette structure dans un appel de code non managé :</span><span class="sxs-lookup"><span data-stu-id="ae682-162">Add the following code to MyNewService.cs to declare the `ServiceState` values and to add a structure for the status, which you'll use in a platform invoke call:</span></span>

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

3. <span data-ttu-id="ae682-163">Maintenant, dans la classe `MyNewService`, déclarez la [fonction SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) à l’aide d’un [appel de code non managé](../interop/consuming-unmanaged-dll-functions.md) :</span><span class="sxs-lookup"><span data-stu-id="ae682-163">Now, in the `MyNewService` class, declare the [SetServiceStatus function](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) by using [platform invoke](../interop/consuming-unmanaged-dll-functions.md):</span></span>

    ```csharp
    [DllImport("advapi32.dll", SetLastError = true)]
    private static extern bool SetServiceStatus(System.IntPtr handle, ref ServiceStatus serviceStatus);
    ```

    ```vb
    Declare Auto Function SetServiceStatus Lib "advapi32.dll" (ByVal handle As IntPtr, ByRef serviceStatus As ServiceStatus) As Boolean
    ```

4. <span data-ttu-id="ae682-164">Pour implémenter l'état Démarrer Suspendre, ajoutez le code suivant au début de la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> :</span><span class="sxs-lookup"><span data-stu-id="ae682-164">To implement the Start Pending status, add the following code to the beginning of the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method:</span></span>

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

5. <span data-ttu-id="ae682-165">Ajoutez du code pour définir l'état En cours d'exécution à la fin de la méthode <xref:System.ServiceProcess.ServiceBase.OnStart%2A> .</span><span class="sxs-lookup"><span data-stu-id="ae682-165">Add code to set the status to Running at the end of the <xref:System.ServiceProcess.ServiceBase.OnStart%2A> method.</span></span>

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

6. <span data-ttu-id="ae682-166">(Facultatif) Répétez cette procédure pour la méthode <xref:System.ServiceProcess.ServiceBase.OnStop%2A> .</span><span class="sxs-lookup"><span data-stu-id="ae682-166">(Optional) Repeat this procedure for the <xref:System.ServiceProcess.ServiceBase.OnStop%2A> method.</span></span>

> [!NOTE]
> <span data-ttu-id="ae682-167">La boîte de dialogue [Gestionnaire de contrôle des services](/windows/desktop/Services/service-control-manager) utilise les membres `dwWaitHint` et `dwCheckpoint` de la [structure SERVICE_STATUS](/windows/desktop/api/winsvc/ns-winsvc-_service_status) pour déterminer le délai d’attente avant le démarrage ou l’arrêt d’un service Windows.</span><span class="sxs-lookup"><span data-stu-id="ae682-167">The [Service Control Manager](/windows/desktop/Services/service-control-manager) uses the `dwWaitHint` and `dwCheckpoint` members of the [SERVICE_STATUS structure](/windows/desktop/api/winsvc/ns-winsvc-_service_status) to determine how much time to wait for a Windows service to start or shut down.</span></span> <span data-ttu-id="ae682-168">Si l’exécution de vos méthodes <xref:System.ServiceProcess.ServiceBase.OnStart%2A> et <xref:System.ServiceProcess.ServiceBase.OnStop%2A> est longue, votre service peut demander plus de temps en appelant à nouveau [SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) avec une valeur `dwCheckPoint` incrémentée.</span><span class="sxs-lookup"><span data-stu-id="ae682-168">If your <xref:System.ServiceProcess.ServiceBase.OnStart%2A> and <xref:System.ServiceProcess.ServiceBase.OnStop%2A> methods run long, your service can request more time by calling [SetServiceStatus](/windows/desktop/api/winsvc/nf-winsvc-setservicestatus) again with an incremented `dwCheckPoint` value.</span></span>

## <a name="add-installers-to-the-service"></a><span data-ttu-id="ae682-169">Ajouter des programmes d'installation pour le service</span><span class="sxs-lookup"><span data-stu-id="ae682-169">Add installers to the service</span></span>

<span data-ttu-id="ae682-170">Avant de pouvoir exécuter un service Windows, vous devez l'installer, ce qui l'inscrit auprès du Gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="ae682-170">Before you can run a Windows service, you need to install it, which registers it with the Service Control Manager.</span></span> <span data-ttu-id="ae682-171">Vous pouvez ajouter à votre projet des programmes d'installation qui gèrent les détails de l'inscription.</span><span class="sxs-lookup"><span data-stu-id="ae682-171">You can add installers to your project that handle the registration details.</span></span>

1. <span data-ttu-id="ae682-172">Dans l' **Explorateur de solutions**, ouvrez le menu contextuel pour **MyNewService.cs** ou **MyNewService.vb**, puis choisissez **Concepteur de vues**.</span><span class="sxs-lookup"><span data-stu-id="ae682-172">In **Solution Explorer**, open the context menu for **MyNewService.cs** or **MyNewService.vb**, and then choose **View Designer**.</span></span>

2. <span data-ttu-id="ae682-173">Cliquez sur l'arrière-plan du concepteur pour sélectionner le service lui-même plutôt que son contenu.</span><span class="sxs-lookup"><span data-stu-id="ae682-173">Click the background of the designer to select the service itself, instead of any of its contents.</span></span>

3. <span data-ttu-id="ae682-174">Ouvrez le menu contextuel de la fenêtre du concepteur (si vous utilisez un dispositif de pointage, cliquez avec le bouton droit à l'intérieur de la fenêtre), puis choisissez **Ajouter le programme d'installation**.</span><span class="sxs-lookup"><span data-stu-id="ae682-174">Open the context menu for the designer window (if you’re using a pointing device, right-click inside the window), and then choose **Add Installer**.</span></span>

   <span data-ttu-id="ae682-175">Par défaut, une classe Component comprenant deux programmes d'installation est ajoutée à votre projet.</span><span class="sxs-lookup"><span data-stu-id="ae682-175">By default, a component class that contains two installers is added to your project.</span></span> <span data-ttu-id="ae682-176">Le composant est appelé **ProjectInstaller**et contient le programme d'installation de votre service ainsi que le programme d'installation du processus associé au service.</span><span class="sxs-lookup"><span data-stu-id="ae682-176">The component is named **ProjectInstaller**, and the installers it contains are the installer for your service and the installer for the service's associated process.</span></span>

4. <span data-ttu-id="ae682-177">En mode **Design** pour **ProjectInstaller**, choisissez **serviceInstaller1** pour un projet Visual C# ou **ServiceInstaller1** pour un projet Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ae682-177">In **Design** view for **ProjectInstaller**, choose **serviceInstaller1** for a Visual C# project, or **ServiceInstaller1** for a Visual Basic project.</span></span>

5. <span data-ttu-id="ae682-178">Dans la fenêtre **Propriétés** , vérifiez que la propriété <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> a la valeur **MyNewService**.</span><span class="sxs-lookup"><span data-stu-id="ae682-178">In the **Properties** window, make sure the <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> property is set to **MyNewService**.</span></span>

6. <span data-ttu-id="ae682-179">Affectez à la propriété **Description** du texte, par exemple « Un exemple de service ».</span><span class="sxs-lookup"><span data-stu-id="ae682-179">Set the **Description** property to some text, such as "A sample service".</span></span> <span data-ttu-id="ae682-180">Ce texte, qui s'affiche dans la fenêtre Services, permet à l'utilisateur d'identifier le service et de comprendre son utilité.</span><span class="sxs-lookup"><span data-stu-id="ae682-180">This text appears in the Services window and helps the user identify the service and understand what it’s used for.</span></span>

7. <span data-ttu-id="ae682-181">Affectez à la propriété <xref:System.ServiceProcess.ServiceInstaller.DisplayName%2A> le texte à afficher dans la colonne **Nom** de la fenêtre Services.</span><span class="sxs-lookup"><span data-stu-id="ae682-181">Set the <xref:System.ServiceProcess.ServiceInstaller.DisplayName%2A> property to the text that you want to appear in the Services window in the **Name** column.</span></span> <span data-ttu-id="ae682-182">Par exemple, vous pouvez entrer « Nom complet de MyNewService ».</span><span class="sxs-lookup"><span data-stu-id="ae682-182">For example, you can enter "MyNewService Display Name".</span></span> <span data-ttu-id="ae682-183">Ce nom peut être différent de la propriété <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> , qui est le nom utilisé par le système (par exemple, lorsque vous utilisez la commande `net start` pour démarrer votre service).</span><span class="sxs-lookup"><span data-stu-id="ae682-183">This name can be different from the <xref:System.ServiceProcess.ServiceInstaller.ServiceName%2A> property, which is the name used by the system (for example, when you use the `net start` command to start your service).</span></span>

8. <span data-ttu-id="ae682-184">Affectez à la propriété <xref:System.ServiceProcess.ServiceInstaller.StartType%2A> la valeur <xref:System.ServiceProcess.ServiceStartMode.Automatic>.</span><span class="sxs-lookup"><span data-stu-id="ae682-184">Set the <xref:System.ServiceProcess.ServiceInstaller.StartType%2A> property to <xref:System.ServiceProcess.ServiceStartMode.Automatic>.</span></span>

     <span data-ttu-id="ae682-185">![Propriétés du programme d’installation d’un service Windows](../../../docs/framework/windows-services/media/windowsservice-installerproperties.PNG "WindowsService_InstallerProperties")</span><span class="sxs-lookup"><span data-stu-id="ae682-185">![Installer Properties for a Windows service](../../../docs/framework/windows-services/media/windowsservice-installerproperties.PNG "WindowsService_InstallerProperties")</span></span>

9. <span data-ttu-id="ae682-186">Dans le concepteur, choisissez **serviceProcessInstaller1** pour un projet Visual C# ou **ServiceProcessInstaller1** pour un projet Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ae682-186">In the designer, choose **serviceProcessInstaller1** for a Visual C# project, or **ServiceProcessInstaller1** for a Visual Basic project.</span></span> <span data-ttu-id="ae682-187">Affectez à la propriété <xref:System.ServiceProcess.ServiceProcessInstaller.Account%2A> la valeur <xref:System.ServiceProcess.ServiceAccount.LocalSystem>.</span><span class="sxs-lookup"><span data-stu-id="ae682-187">Set the <xref:System.ServiceProcess.ServiceProcessInstaller.Account%2A> property to <xref:System.ServiceProcess.ServiceAccount.LocalSystem>.</span></span> <span data-ttu-id="ae682-188">Ainsi, le service est installé et exécuté à l’aide du compte système local.</span><span class="sxs-lookup"><span data-stu-id="ae682-188">This causes the service to be installed and to run using the local system account.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="ae682-189">Le compte <xref:System.ServiceProcess.ServiceAccount.LocalSystem> dispose d'autorisations générales, y compris la possibilité d'écrire dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="ae682-189">The <xref:System.ServiceProcess.ServiceAccount.LocalSystem> account has broad permissions, including the ability to write to the event log.</span></span> <span data-ttu-id="ae682-190">Utilisez ce compte avec précaution car il peut augmenter le risque d'attaques par des logiciels malveillants.</span><span class="sxs-lookup"><span data-stu-id="ae682-190">Use this account with caution, because it might increase your risk of attacks from malicious software.</span></span> <span data-ttu-id="ae682-191">Pour les autres tâches, utilisez le compte <xref:System.ServiceProcess.ServiceAccount.LocalService> , qui se comporte comme un utilisateur non privilégié de l'ordinateur local et présente des informations d'identification anonymes à tout serveur distant.</span><span class="sxs-lookup"><span data-stu-id="ae682-191">For other tasks, consider using the <xref:System.ServiceProcess.ServiceAccount.LocalService> account, which acts as a non-privileged user on the local computer and presents anonymous credentials to any remote server.</span></span> <span data-ttu-id="ae682-192">Cet exemple échoue si vous essayez d'utiliser le compte <xref:System.ServiceProcess.ServiceAccount.LocalService> , car il doit disposer d'une autorisation pour écrire dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="ae682-192">This example fails if you try to use the <xref:System.ServiceProcess.ServiceAccount.LocalService> account, because it needs permission to write to the event log.</span></span>

<span data-ttu-id="ae682-193">Pour plus d’informations sur les programmes d’installation, consultez [Guide pratique pour ajouter des programmes d’installation à votre application de service](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md).</span><span class="sxs-lookup"><span data-stu-id="ae682-193">For more information about installers, see [How to: Add Installers to Your service Application](../../../docs/framework/windows-services/how-to-add-installers-to-your-service-application.md).</span></span>

## <a name="optional-set-startup-parameters"></a><span data-ttu-id="ae682-194">(Facultatif) Définition de paramètres de démarrage</span><span class="sxs-lookup"><span data-stu-id="ae682-194">(Optional) Set startup parameters</span></span>

<span data-ttu-id="ae682-195">Un service Windows, comme tout autre fichier exécutable, peut accepter des arguments de ligne de commande ou des paramètres de démarrage.</span><span class="sxs-lookup"><span data-stu-id="ae682-195">A Windows service, like any other executable, can accept command-line arguments, or startup parameters.</span></span> <span data-ttu-id="ae682-196">Lorsque vous ajoutez du code pour traiter les paramètres de démarrage, les utilisateurs peuvent démarrer votre service avec leurs propres paramètres de démarrage personnalisés à l'aide de la fenêtre Services du panneau de configuration Windows.</span><span class="sxs-lookup"><span data-stu-id="ae682-196">When you add code to process startup parameters, users can start your service with their own custom startup parameters by using the Services window in the Windows Control Panel.</span></span> <span data-ttu-id="ae682-197">Toutefois, ces paramètres de démarrage ne sont pas persistants lors du prochain démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="ae682-197">However, these startup parameters are not persisted the next time the service starts.</span></span> <span data-ttu-id="ae682-198">Pour définir les paramètres de démarrage de façon permanente, vous pouvez les définir dans le Registre, comme indiqué dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="ae682-198">To set startup parameters permanently, you can set them in the registry, as shown in this procedure.</span></span>

> [!NOTE]
> <span data-ttu-id="ae682-199">Avant de décider d'ajouter des paramètres de démarrage, vous devez déterminer si c'est le meilleur moyen de passer des informations à votre service.</span><span class="sxs-lookup"><span data-stu-id="ae682-199">Before you decide to add startup parameters, consider whether that is the best way to pass information to your service.</span></span> <span data-ttu-id="ae682-200">Les paramètres de démarrage sont faciles à utiliser et à analyser, et les utilisateurs peuvent facilement les substituer. Il peut toutefois être plus difficile pour les utilisateurs de les détecter et de les utiliser sans documentation.</span><span class="sxs-lookup"><span data-stu-id="ae682-200">Although startup parameters are easy to use and to parse, and users can easily override them, they might be harder for users to discover and use without documentation.</span></span> <span data-ttu-id="ae682-201">En général, si votre service nécessite seulement quelques paramètres de démarrage, vous devez envisager d'utiliser plutôt le Registre ou un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="ae682-201">Generally, if your service requires more than just a few startup parameters, you should consider using the registry or a configuration file instead.</span></span> <span data-ttu-id="ae682-202">Tous les services Windows ont une entrée dans le Registre, sous **HKLM\System\CurrentControlSet\services**.</span><span class="sxs-lookup"><span data-stu-id="ae682-202">Every Windows service has an entry in the registry under **HKLM\System\CurrentControlSet\services**.</span></span> <span data-ttu-id="ae682-203">Sous la clé du service, vous pouvez utiliser la sous-clé **Parameters** pour stocker les informations auxquelles votre service peut accéder.</span><span class="sxs-lookup"><span data-stu-id="ae682-203">Under the service's key, you can use the **Parameters** subkey to store information that your service can access.</span></span> <span data-ttu-id="ae682-204">Vous pouvez utiliser des fichiers de configuration d'application pour un service Windows de la même façon que vous le faites pour les autres types de programmes.</span><span class="sxs-lookup"><span data-stu-id="ae682-204">You can use application configuration files for a Windows service the same way you do for other types of programs.</span></span> <span data-ttu-id="ae682-205">Pour obtenir un exemple de code, consultez <xref:System.Configuration.ConfigurationManager.AppSettings%2A>.</span><span class="sxs-lookup"><span data-stu-id="ae682-205">For example code, see <xref:System.Configuration.ConfigurationManager.AppSettings%2A>.</span></span>

<span data-ttu-id="ae682-206">Pour ajouter des paramètres de démarrage :</span><span class="sxs-lookup"><span data-stu-id="ae682-206">To add startup parameters:</span></span>

1. <span data-ttu-id="ae682-207">Dans la méthode `Main` dans le fichier Program.cs ou MyNewService.Designer.vb, ajoutez un paramètre d’entrée à passer au constructeur de service :</span><span class="sxs-lookup"><span data-stu-id="ae682-207">In the `Main` method in Program.cs or in MyNewService.Designer.vb, add an input parameter to pass to the service constructor:</span></span>

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

2. <span data-ttu-id="ae682-208">Modifiez le constructeur `MyNewService` comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae682-208">Change the `MyNewService` constructor as follows:</span></span>

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

   <span data-ttu-id="ae682-209">Ce code définit la source d'événement et le nom du journal en fonction des paramètres de démarrage fournis, ou utilise les valeurs par défaut si aucun argument n'est fourni.</span><span class="sxs-lookup"><span data-stu-id="ae682-209">This code sets the event source and log name according to the supplied startup parameters, or uses default values if no arguments are supplied.</span></span>

3. <span data-ttu-id="ae682-210">Pour spécifier les arguments de ligne de commande, ajoutez le code suivant à la classe `ProjectInstaller` dans ProjectInstaller.cs ou ProjectInstaller.vb :</span><span class="sxs-lookup"><span data-stu-id="ae682-210">To specify the command-line arguments, add the following code to the `ProjectInstaller` class in ProjectInstaller.cs or ProjectInstaller.vb:</span></span>

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

   <span data-ttu-id="ae682-211">Ce code modifie la clé de Registre **ImagePath** qui contient généralement le chemin d'accès complet au fichier exécutable du service Windows, en ajoutant les valeurs de paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="ae682-211">This code modifies the **ImagePath** registry key, which typically contains the full path to the executable for the Windows service, by adding the default parameter values.</span></span> <span data-ttu-id="ae682-212">Les guillemets autour du chemin d'accès (et autour de chaque paramètre individuel) sont nécessaires pour que le service démarre correctement.</span><span class="sxs-lookup"><span data-stu-id="ae682-212">The quotation marks around the path (and around each individual parameter) are required for the service to start up correctly.</span></span> <span data-ttu-id="ae682-213">Pour modifier les paramètres de démarrage de ce service Windows, les utilisateurs peuvent modifier les paramètres indiqués dans la clé de Registre **ImagePath** . La meilleure méthode consiste toutefois à la modifier par programmation et à exposer les fonctionnalités aux utilisateurs d'une manière conviviale (par exemple dans un utilitaire de gestion ou de configuration).</span><span class="sxs-lookup"><span data-stu-id="ae682-213">To change the startup parameters for this Windows service, users can change the parameters given in the **ImagePath** registry key, although the better way is to change it programmatically and expose the functionality to users in a friendly way (for example, in a management or configuration utility).</span></span>

## <a name="build-the-service"></a><span data-ttu-id="ae682-214">Générer le service</span><span class="sxs-lookup"><span data-stu-id="ae682-214">Build the service</span></span>

1. <span data-ttu-id="ae682-215">Dans l' **Explorateur de solutions**, ouvrez le menu contextuel de votre projet, puis choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="ae682-215">In **Solution Explorer**, open the context menu for your project, and then choose **Properties**.</span></span>

   <span data-ttu-id="ae682-216">Les pages de propriétés de votre projet s'affichent.</span><span class="sxs-lookup"><span data-stu-id="ae682-216">The property pages for your project appear.</span></span>

2. <span data-ttu-id="ae682-217">Dans la liste **Objet de démarrage** de l'onglet **Application**, choisissez **MyNewService.Program**.</span><span class="sxs-lookup"><span data-stu-id="ae682-217">On the **Application** tab, in the **Startup object** list, choose **MyNewService.Program**.</span></span>

3. <span data-ttu-id="ae682-218">Dans **l’Explorateur de solutions**, ouvrez le menu contextuel de votre projet, puis choisissez **Générer** pour générer le projet (ou appuyez sur **Ctrl**+**Maj**+**B**).</span><span class="sxs-lookup"><span data-stu-id="ae682-218">In **Solution Explorer**, open the context menu for your project, and then choose **Build** to build the project (or press **Ctrl**+**Shift**+**B**).</span></span>

## <a name="install-the-service"></a><span data-ttu-id="ae682-219">Installer le service</span><span class="sxs-lookup"><span data-stu-id="ae682-219">Install the service</span></span>

<span data-ttu-id="ae682-220">Maintenant que vous avez généré le service Windows, vous pouvez l'installer.</span><span class="sxs-lookup"><span data-stu-id="ae682-220">Now that you've built the Windows service, you can install it.</span></span> <span data-ttu-id="ae682-221">Pour installer un service Windows, vous devez disposer d'informations d'identification d'administrateur sur l'ordinateur sur lequel vous l'installez.</span><span class="sxs-lookup"><span data-stu-id="ae682-221">To install a Windows service, you must have administrator credentials on the computer on which you're installing it.</span></span>

1. <span data-ttu-id="ae682-222">Ouvrez **Invite de commandes développeur pour Visual Studio** avec des informations d'identification administratives.</span><span class="sxs-lookup"><span data-stu-id="ae682-222">Open **Developer Command Prompt for Visual Studio** with administrative credentials.</span></span> <span data-ttu-id="ae682-223">Si vous utilisez une souris, cliquez avec le bouton droit sur **Invite de commandes développeur pour VS 2017** dans le menu Démarrer de Windows, puis choisissez **Plus** > **Exécuter en tant qu'administrateur**.</span><span class="sxs-lookup"><span data-stu-id="ae682-223">If you’re using a mouse, right-click on **Developer Command Prompt for VS 2017** in the Windows Start menu, and then choose **More** > **Run as Administrator**.</span></span>

2. <span data-ttu-id="ae682-224">Dans la fenêtre **Invite de commandes développeur**, accédez au dossier qui contient la sortie de votre projet (par défaut, il s’agit du sous-répertoire *\bin\Debug* de votre projet).</span><span class="sxs-lookup"><span data-stu-id="ae682-224">In the **Developer Command Prompt** window, navigate to the folder that contains your project's output (by default, it's the *\bin\Debug* subdirectory of your project).</span></span>

3. <span data-ttu-id="ae682-225">Entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ae682-225">Enter the following command:</span></span>

    ```shell
    installutil.exe MyNewService.exe
    ```

    <span data-ttu-id="ae682-226">Si le service est installé correctement, le fichier **installutil.exe** le signale.</span><span class="sxs-lookup"><span data-stu-id="ae682-226">If the service installs successfully, **installutil.exe** reports success.</span></span> <span data-ttu-id="ae682-227">Si le système n'a pas trouvé **InstallUtil.exe**, vérifiez qu'il existe sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ae682-227">If the system could not find **InstallUtil.exe**, make sure that it exists on your computer.</span></span> <span data-ttu-id="ae682-228">Cet outil est installé avec le .NET Framework dans le dossier *%windir%\Microsoft.NET\Framework[64]\\[version du framework]*.</span><span class="sxs-lookup"><span data-stu-id="ae682-228">This tool is installed with the .NET Framework to the folder *%windir%\Microsoft.NET\Framework[64]\\[framework version]*.</span></span> <span data-ttu-id="ae682-229">Par exemple, le chemin d’accès par défaut pour la version 32 bits est *%windir%\Microsoft.NET\Framework\v4.0.30319\InstallUtil.exe*.</span><span class="sxs-lookup"><span data-stu-id="ae682-229">For example, the default path for the 32-bit version is *%windir%\Microsoft.NET\Framework\v4.0.30319\InstallUtil.exe*.</span></span>

    <span data-ttu-id="ae682-230">Si le processus **installutil.exe** signale un échec, examinez le journal d’installation pour en connaître la raison.</span><span class="sxs-lookup"><span data-stu-id="ae682-230">If the **installutil.exe** process reports failure, check the install log to find out why.</span></span> <span data-ttu-id="ae682-231">Par défaut, le journal se trouve dans le même dossier que l’exécutable du service.</span><span class="sxs-lookup"><span data-stu-id="ae682-231">By default the log is in the same folder as the service executable.</span></span> <span data-ttu-id="ae682-232">L’installation peut échouer si la classe <xref:System.ComponentModel.RunInstallerAttribute> n’est pas présente sur la classe `ProjectInstaller`, si l’attribut n’a pas la valeur **true** ou si la classe `ProjectInstaller` n’est pas **publique**.</span><span class="sxs-lookup"><span data-stu-id="ae682-232">The installation can fail if  the <xref:System.ComponentModel.RunInstallerAttribute> Class is not present on the `ProjectInstaller` class, if the attribute is not set to **true**, or if the `ProjectInstaller` class is not marked **public**.</span></span>

<span data-ttu-id="ae682-233">Pour plus d'informations, voir [Procédure : Installer et désinstaller des services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).</span><span class="sxs-lookup"><span data-stu-id="ae682-233">For more information, see [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).</span></span>

## <a name="start-and-run-the-service"></a><span data-ttu-id="ae682-234">Démarrer et exécuter le service</span><span class="sxs-lookup"><span data-stu-id="ae682-234">Start and run the service</span></span>

1. <span data-ttu-id="ae682-235">Dans Windows, ouvrez l’application de bureau **Services**.</span><span class="sxs-lookup"><span data-stu-id="ae682-235">In Windows, open the **Services** desktop app.</span></span> <span data-ttu-id="ae682-236">Appuyez sur **Windows**+**R** pour ouvrir la zone **Exécuter**, puis entrez **services.msc** et appuyez sur **Entrée** ou cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae682-236">Press **Windows**+**R** to open the **Run** box, and then enter **services.msc** and press **Enter** or click **OK**.</span></span>

     <span data-ttu-id="ae682-237">Votre service doit être répertorié dans **Services**, affiché par ordre alphabétique du nom d’affichage que vous lui avez donné.</span><span class="sxs-lookup"><span data-stu-id="ae682-237">You should see your service listed in **Services**, displayed alphabetically by the display name that you set for it.</span></span>

     ![MyNewService dans la fenêtre Services.](../../../docs/framework/windows-services/media/windowsservices-serviceswindow.PNG)

2. <span data-ttu-id="ae682-239">Dans **Services**, ouvrez le menu contextuel de votre service, puis choisissez **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="ae682-239">In **Services**, open the shortcut menu for your service, and then choose **Start**.</span></span>

3. <span data-ttu-id="ae682-240">Pour arrêter le service, ouvrez le menu contextuel de votre service, puis choisissez **Arrêter**.</span><span class="sxs-lookup"><span data-stu-id="ae682-240">To stop the service, open the shortcut menu for the service, and then choose **Stop**.</span></span>

4. <span data-ttu-id="ae682-241">(Facultatif) À partir de la ligne de commande, vous pouvez utiliser les commandes `net start ServiceName` et `net stop ServiceName` pour démarrer et arrêter votre service.</span><span class="sxs-lookup"><span data-stu-id="ae682-241">(Optional) From the command line, you can use the commands `net start ServiceName` and `net stop ServiceName` to start and stop your service.</span></span>

### <a name="verify-the-event-log-output-of-your-service"></a><span data-ttu-id="ae682-242">Vérifier la sortie du journal des événements de votre service</span><span class="sxs-lookup"><span data-stu-id="ae682-242">Verify the event log output of your service</span></span>

1. <span data-ttu-id="ae682-243">Ouvrez **l’Observateur d’événements** en commençant à taper **Observateur d’événements** dans la zone de recherche de la barre des tâches Windows, puis en sélectionnant **Observateur d’événements** dans les résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="ae682-243">Open **Event Viewer** by starting to type **Event Viewer** in the search box on the Windows task bar, and then selecting **Event Viewer** from the search results.</span></span>

   > [!TIP]
   > <span data-ttu-id="ae682-244">Dans Visual Studio, vous pouvez accéder aux journaux des événements en ouvrant **Explorateur de serveurs** (clavier : **Ctrl**+**Alt**+**S**) et en développant le nœud **Journaux des événements** pour l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="ae682-244">In Visual Studio, you can access event logs by opening **Server Explorer** (Keyboard: **Ctrl**+**Alt**+**S**) and expanding the **Event Logs** node for the local computer.</span></span>

2. <span data-ttu-id="ae682-245">Dans **l’Observateur d’événements**, développez **Journaux des applications et services**.</span><span class="sxs-lookup"><span data-stu-id="ae682-245">In **Event Viewer**, expand **Applications and Services Logs**.</span></span>

3. <span data-ttu-id="ae682-246">Recherchez le nom **MyNewLog** (ou **MyLogFile1**, si vous avez utilisé la procédure facultative pour ajouter des arguments de ligne de commande) dans la liste, puis développez-le.</span><span class="sxs-lookup"><span data-stu-id="ae682-246">Locate the listing for **MyNewLog** (or **MyLogFile1**, if you followed the optional procedure to add command-line arguments) and expand it.</span></span> <span data-ttu-id="ae682-247">Vous devez voir des entrées relatives aux deux actions (démarrage et arrêt) que votre service a effectuées.</span><span class="sxs-lookup"><span data-stu-id="ae682-247">You should see entries for the two actions (start and stop) that your service performed.</span></span>

     ![Utiliser l'Observateur d'événements pour visualiser les entrées du journal des événements](../../../docs/framework/windows-services/media/windows-service-event-viewer.png)

## <a name="uninstall-the-service"></a><span data-ttu-id="ae682-249">Désinstaller le service</span><span class="sxs-lookup"><span data-stu-id="ae682-249">Uninstall the service</span></span>

1. <span data-ttu-id="ae682-250">Ouvrez **Invite de commandes développeur pour Visual Studio** avec des informations d'identification administratives.</span><span class="sxs-lookup"><span data-stu-id="ae682-250">Open **Developer Command Prompt for Visual Studio** with administrative credentials.</span></span>

2. <span data-ttu-id="ae682-251">Dans la fenêtre d'invite de commandes, accédez au dossier qui contient la sortie de votre projet.</span><span class="sxs-lookup"><span data-stu-id="ae682-251">In the command prompt window, navigate to the folder that contains your project's output.</span></span>

3. <span data-ttu-id="ae682-252">Entrez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="ae682-252">Enter the following command:</span></span>

    ```shell
    installutil.exe /u MyNewService.exe
    ```

   <span data-ttu-id="ae682-253">Si le service est désinstallé avec succès, **installutil.exe** le signale.</span><span class="sxs-lookup"><span data-stu-id="ae682-253">If the service uninstalls successfully, **installutil.exe** reports that your service was successfully removed.</span></span> <span data-ttu-id="ae682-254">Pour plus d'informations, voir [Procédure : Installer et désinstaller des services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).</span><span class="sxs-lookup"><span data-stu-id="ae682-254">For more information, see [How to: Install and Uninstall Services](../../../docs/framework/windows-services/how-to-install-and-uninstall-services.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="ae682-255">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ae682-255">Next steps</span></span>

<span data-ttu-id="ae682-256">Maintenant que vous avez créé le service, vous pouvez créer un programme d'installation autonome que d'autres peuvent utiliser pour installer votre service Windows.</span><span class="sxs-lookup"><span data-stu-id="ae682-256">Now that you've created the service, you might want to create a standalone setup program that others can use to install your Windows service.</span></span> <span data-ttu-id="ae682-257">ClickOnce ne prend pas en charge les services Windows, mais vous pouvez utiliser [WiX Toolset](http://wixtoolset.org/) pour créer un programme d’installation pour un service Windows.</span><span class="sxs-lookup"><span data-stu-id="ae682-257">ClickOnce doesn't support Windows services, but you can use the [WiX Toolset](http://wixtoolset.org/) to create an installer for a Windows service.</span></span> <span data-ttu-id="ae682-258">Pour d’autres idées, consultez [Créer un package de programme d’installation](/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-desktop).</span><span class="sxs-lookup"><span data-stu-id="ae682-258">For other ideas, see [Create an installer package](/visualstudio/deployment/deploying-applications-services-and-components#create-an-installer-package-windows-desktop).</span></span>

<span data-ttu-id="ae682-259">Vous pouvez également opter pour l'utilisation d'un composant <xref:System.ServiceProcess.ServiceController>, ce qui vous permet d'envoyer des commandes au service que vous avez installé.</span><span class="sxs-lookup"><span data-stu-id="ae682-259">You might explore the use of a <xref:System.ServiceProcess.ServiceController> component, which enables you to send commands to the service you've installed.</span></span>

<span data-ttu-id="ae682-260">Vous pouvez utiliser un programme d'installation pour créer un journal des événements lors de l'installation de l'application plutôt que lors de son exécution.</span><span class="sxs-lookup"><span data-stu-id="ae682-260">You can use an installer to create an event log when the application is installed instead of creating the event log when the application runs.</span></span> <span data-ttu-id="ae682-261">En outre, le journal des événements sera supprimé par le programme d'installation lors de la désinstallation de l'application.</span><span class="sxs-lookup"><span data-stu-id="ae682-261">Additionally, the event log will be deleted by the installer when the application is uninstalled.</span></span> <span data-ttu-id="ae682-262">Pour plus d'informations, consultez la page de référence relative à <xref:System.Diagnostics.EventLogInstaller> .</span><span class="sxs-lookup"><span data-stu-id="ae682-262">For more information, see the <xref:System.Diagnostics.EventLogInstaller> reference page.</span></span>

## <a name="see-also"></a><span data-ttu-id="ae682-263">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae682-263">See also</span></span>

- [<span data-ttu-id="ae682-264">Applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="ae682-264">Windows service applications</span></span>](../../../docs/framework/windows-services/index.md)
- [<span data-ttu-id="ae682-265">Introduction aux applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="ae682-265">Introduction to Windows service applications</span></span>](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
- [<span data-ttu-id="ae682-266">Guide pratique pour déboguer les applications de service Windows</span><span class="sxs-lookup"><span data-stu-id="ae682-266">How to: Debug Windows service applications</span></span>](../../../docs/framework/windows-services/how-to-debug-windows-service-applications.md)
- [<span data-ttu-id="ae682-267">Services (Windows)</span><span class="sxs-lookup"><span data-stu-id="ae682-267">Services (Windows)</span></span>](/windows/desktop/Services/services)
