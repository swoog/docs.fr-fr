---
title: Suivi de workflow
ms.date: 03/30/2017
ms.assetid: 18737989-0502-4367-b5f6-617ebfb77c96
ms.openlocfilehash: 92497768e7e8d720cdcc7c8f2c7c04b4dfcc47b4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59224934"
---
# <a name="workflow-tracing"></a><span data-ttu-id="cc196-102">Suivi de workflow</span><span class="sxs-lookup"><span data-stu-id="cc196-102">Workflow Tracing</span></span>
<span data-ttu-id="cc196-103">Le suivi de workflow offre une méthode de capture des informations de diagnostic à l'aide d'écouteurs de suivi .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="cc196-103">Workflow tracing offers a way to capture diagnostic information using .NET Framework trace listeners.</span></span> <span data-ttu-id="cc196-104">Le suivi peut être activé si un problème a été détecté dans l'application, puis désactivé de nouveau une fois le problème résolu.</span><span class="sxs-lookup"><span data-stu-id="cc196-104">Tracing can be enabled if a problem is detected with the application and then disabled again once the problem is resolved.</span></span> <span data-ttu-id="cc196-105">Deux méthodes s'offrent à vous pour activer le suivi de débogage pour les flux de travail.</span><span class="sxs-lookup"><span data-stu-id="cc196-105">There are two ways you could enable debug tracing for workflows.</span></span> <span data-ttu-id="cc196-106">Vous pouvez le configurer à l'aide de la visionneuse de suivi d'événements ou bien utiliser l'objet <xref:System.Diagnostics> pour envoyer des événements de suivi à un fichier.</span><span class="sxs-lookup"><span data-stu-id="cc196-106">You can configure it using the Event Trace viewer or you can use <xref:System.Diagnostics> to send trace events to a file.</span></span>  
  
## <a name="enabling-debug-tracing-in-etw"></a><span data-ttu-id="cc196-107">Activation du suivi de débogage dans ETW</span><span class="sxs-lookup"><span data-stu-id="cc196-107">Enabling Debug Tracing in ETW</span></span>  
 <span data-ttu-id="cc196-108">Pour activer le suivi à l'aide d'ETW, activez le canal de débogage dans l'Observateur d'événements :</span><span class="sxs-lookup"><span data-stu-id="cc196-108">To enable tracing using ETW, enable the Debug channel in Event Viewer:</span></span>  
  
1.  <span data-ttu-id="cc196-109">Dans l'Observateur d'événements, naviguez vers le nœud des journaux d'analyse et de débogage.</span><span class="sxs-lookup"><span data-stu-id="cc196-109">Navigate to analytic and debug logs node in Event Viewer.</span></span>  
  
2.  <span data-ttu-id="cc196-110">Dans l’arborescence de commandes dans l’Observateur d’événements, accédez à **Observateur d’événements -> Applications et journaux des Services -> Microsoft -> Windows -> serveur d’applications-Applications**.</span><span class="sxs-lookup"><span data-stu-id="cc196-110">In the tree view in Event Viewer, navigate to **Event Viewer->Applications and Services Logs->Microsoft->Windows->Application Server-Applications**.</span></span> <span data-ttu-id="cc196-111">Avec le bouton droit **serveur d’applications-Applications** et sélectionnez **Affichage -> Afficher les journaux d’analyse et de débogage**.</span><span class="sxs-lookup"><span data-stu-id="cc196-111">Right-click **Application Server-Applications** and select **View->Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="cc196-112">Avec le bouton droit **déboguer** et sélectionnez **activer le journal**.</span><span class="sxs-lookup"><span data-stu-id="cc196-112">Right-click **Debug** and select **Enable Log**.</span></span>  
  
3.  <span data-ttu-id="cc196-113">Lorsqu'un flux de travail exécute le débogage et qu'un suivi est émis vers le canal de débogage ETW, le suivi peut être affiché dans l'Observateur d'événements.</span><span class="sxs-lookup"><span data-stu-id="cc196-113">When a workflow runs the debug and traces are emitted to ETW debug channel, they can be viewed in the Event Viewer.</span></span> <span data-ttu-id="cc196-114">Accédez à **Observateur d’événements -> Applications et journaux des Services -> Microsoft -> Windows -> serveur d’applications-Applications**.</span><span class="sxs-lookup"><span data-stu-id="cc196-114">Navigate to **Event Viewer->Applications and Services Logs->Microsoft->Windows->Application Server-Applications**.</span></span> <span data-ttu-id="cc196-115">Avec le bouton droit **déboguer** et sélectionnez **Actualiser**.</span><span class="sxs-lookup"><span data-stu-id="cc196-115">Right-click **Debug** and select **Refresh**.</span></span>  
  
4.  <span data-ttu-id="cc196-116">La taille de la mémoire tampon de trace analytique par défaut est de 4 kilo-octet (Ko) seulement. Il est recommandé d'augmenter la taille à 32 Ko.</span><span class="sxs-lookup"><span data-stu-id="cc196-116">The default analytic trace buffer size is only 4 kilobytes (KB); it is recommended to increase the size to 32 KB.</span></span> <span data-ttu-id="cc196-117">Pour ce faire, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc196-117">To do this, perform the following steps.</span></span>  
  
    1.  <span data-ttu-id="cc196-118">Exécutez la commande suivante dans le répertoire framework actuel (par exemple, C:\Windows\Microsoft.NET\Framework\v4.0.21203) :</span><span class="sxs-lookup"><span data-stu-id="cc196-118">Execute the following command in the current framework directory (for example, C:\Windows\Microsoft.NET\Framework\v4.0.21203):</span></span> `wevtutil um Microsoft.Windows.ApplicationServer.Applications.man`  
  
    2.  <span data-ttu-id="cc196-119">Modifier le \<bufferSize > valeur dans le fichier Windows.ApplicationServer.applications.man par 32.</span><span class="sxs-lookup"><span data-stu-id="cc196-119">Change the \<bufferSize> value in the Windows.ApplicationServer.Applications.man file to 32.</span></span>  
  
        ```xml  
        <channel name="Microsoft-Windows-Application Server-Applications/Analytic" chid="ANALYTIC_CHANNEL" symbol="ANALYTIC_CHANNEL" type="Analytic" enabled="false" isolation="Application" message="$(string.MICROSOFT_WINDOWS_APPLICATIONSERVER_APPLICATIONS.channel.ANALYTIC_CHANNEL.message)" >  
                    <publishing>  
                      <bufferSize>32</bufferSize>  
                    </publishing>  
                  </channel>  
        ```  
  
    3.  <span data-ttu-id="cc196-120">Exécutez la commande suivante dans le répertoire framework actuel (par exemple, C:\Windows\Microsoft.NET\Framework\v4.0.21203) :</span><span class="sxs-lookup"><span data-stu-id="cc196-120">Execute the following command in the current framework directory (for example, C:\Windows\Microsoft.NET\Framework\v4.0.21203):</span></span> `wevtutil im Microsoft.Windows.ApplicationServer.Applications.man`  
  
> [!NOTE]
>  <span data-ttu-id="cc196-121">Si vous utilisez .NET Framework 4 Client Profile, vous devez tout d’abord enregistrer le manifeste ETW en exécutant la commande suivante à partir du répertoire .NET Framework 4 :</span><span class="sxs-lookup"><span data-stu-id="cc196-121">If you are using the .NET Framework 4 Client Profile, you must first register the ETW manifest by running the following command from the .NET Framework 4 directory:</span></span> `ServiceModelReg.exe –i –c:etw`  
  
## <a name="enabling-debug-tracing-using-systemdiagnostics"></a><span data-ttu-id="cc196-122">Activation du suivi de débogage à l'aide de System.Diagnostics</span><span class="sxs-lookup"><span data-stu-id="cc196-122">Enabling Debug Tracing using System.Diagnostics</span></span>  
 <span data-ttu-id="cc196-123">Ces écouteurs peuvent être configurés dans le fichier App.config de l'application de workflow ou le fichier Web.config pour un service de workflow.</span><span class="sxs-lookup"><span data-stu-id="cc196-123">These listeners can be configured in the App.config file of the workflow application, or the Web.config for a workflow service.</span></span> <span data-ttu-id="cc196-124">Dans cet exemple, un [TextWriterTraceListener](https://go.microsoft.com/fwlink/?LinkId=165424) est configuré pour enregistrer les informations de traçage dans le fichier MyTraceLog.txt du répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="cc196-124">In this example, a [TextWriterTraceListener](https://go.microsoft.com/fwlink/?LinkId=165424) is configured to save tracing information to the MyTraceLog.txt file in the current directory.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
      <source name="System.Activities" switchValue="Information">  
        <listeners>  
          <add name="textListener" />  
          <remove name="Default" />  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="textListener"  
           type="System.Diagnostics.TextWriterTraceListener"  
           initializeData="MyTraceLog.txt"  
           traceOutputOptions="ProcessId, DateTime" />  
    </sharedListeners>  
    <trace autoflush="true" indentsize="4">  
      <listeners>  
        <add name="textListener" />  
      </listeners>  
    </trace>  
  </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="cc196-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc196-125">See also</span></span>

- [<span data-ttu-id="cc196-126">Surveillance de Windows Server App Fabric</span><span class="sxs-lookup"><span data-stu-id="cc196-126">Windows Server App Fabric Monitoring</span></span>](https://go.microsoft.com/fwlink/?LinkId=201273)
- [<span data-ttu-id="cc196-127">Surveillance des Applications avec App Fabric</span><span class="sxs-lookup"><span data-stu-id="cc196-127">Monitoring Applications with App Fabric</span></span>](https://go.microsoft.com/fwlink/?LinkId=201275)
