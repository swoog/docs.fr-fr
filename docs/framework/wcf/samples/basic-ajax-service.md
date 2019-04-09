---
title: Basic AJAX Service
ms.date: 03/30/2017
ms.assetid: d66d0c91-0109-45a0-a901-f3e4667c2465
ms.openlocfilehash: 8bcfb9a751670d3d1c32de6d8e6f7dc1b84ea30d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59146993"
---
# <a name="basic-ajax-service"></a><span data-ttu-id="b3803-102">Basic AJAX Service</span><span class="sxs-lookup"><span data-stu-id="b3803-102">Basic AJAX Service</span></span>
<span data-ttu-id="b3803-103">Cet exemple montre comment utiliser Windows Communication Foundation (WCF) pour créer un service ASP.NET Asynchronous JavaScript and XML (AJAX) base (service que vous pouvez accéder à l’aide de code JavaScript à partir d’un client de navigateur Web).</span><span class="sxs-lookup"><span data-stu-id="b3803-103">This sample demonstrates how to use Windows Communication Foundation (WCF) to create a basic ASP.NET Asynchronous JavaScript and XML (AJAX) service (a service that you can access using JavaScript code from a Web browser client).</span></span> <span data-ttu-id="b3803-104">L'attribut <xref:System.ServiceModel.Web.WebGetAttribute> est utilisé afin de garantir que le service répond aux requêtes HTTP GET et que ce service utilise le format de données JSON (JavaScript Object Notation) pour les réponses.</span><span class="sxs-lookup"><span data-stu-id="b3803-104">The service uses the <xref:System.ServiceModel.Web.WebGetAttribute> attribute to ensure that the service responds to HTTP GET requests and is configured to use the JavaScript Object Notation (JSON) data format for responses.</span></span>  
  
 <span data-ttu-id="b3803-105">Prise en charge d’AJAX dans WCF est optimisé pour une utilisation avec ASP.NET AJAX via le `ScriptManager` contrôle.</span><span class="sxs-lookup"><span data-stu-id="b3803-105">AJAX support in WCF is optimized for use with ASP.NET AJAX through the `ScriptManager` control.</span></span> <span data-ttu-id="b3803-106">Pour obtenir un exemple d’utilisation de WCF avec ASP.NET AJAX, consultez le [exemples AJAX](ajax.md).</span><span class="sxs-lookup"><span data-stu-id="b3803-106">For an example of using WCF with ASP.NET AJAX, see the [AJAX Samples](ajax.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b3803-107">La procédure d'installation ainsi que les instructions de génération correspondant à cet exemple figurent en fin de rubrique.</span><span class="sxs-lookup"><span data-stu-id="b3803-107">The set-up procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="b3803-108">Dans le code suivant, l'attribut <xref:System.ServiceModel.Web.WebGetAttribute> est appliqué à l'opération `Add` afin de garantir que le service répond aux requêtes HTTP GET.</span><span class="sxs-lookup"><span data-stu-id="b3803-108">In the following code, the <xref:System.ServiceModel.Web.WebGetAttribute> attribute is applied to the `Add` operation to ensure that the service responds to HTTP GET requests.</span></span> <span data-ttu-id="b3803-109">Le code utilise la méthode GET pour des raisons pratiques (vous pouvez construire une requête HTTP GET à partir de tout navigateur Web).</span><span class="sxs-lookup"><span data-stu-id="b3803-109">The code uses GET for simplicity (you can construct an HTTP GET request from any Web browser).</span></span> <span data-ttu-id="b3803-110">Vous pouvez également utiliser la méthode GET pour activer la mise en cache.</span><span class="sxs-lookup"><span data-stu-id="b3803-110">You can also use GET to enable caching.</span></span> <span data-ttu-id="b3803-111">HTTP POST est la valeur par défaut en l'absence d'attribut `WebGetAttribute`.</span><span class="sxs-lookup"><span data-stu-id="b3803-111">HTTP POST is the default in the absence of the `WebGetAttribute` attribute.</span></span>  

```csharp
[ServiceContract(Namespace = "SimpleAjaxService")]
public interface ICalculator
{
    [WebGet]
    double Add(double n1, double n2);
    //Other operations omitted…
}
```

 <span data-ttu-id="b3803-112">Le fichier d'exemple .svc utilise <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory>, qui ajoute un point de terminaison standard <xref:System.ServiceModel.Description.WebScriptEndpoint> au service.</span><span class="sxs-lookup"><span data-stu-id="b3803-112">The sample .svc file uses <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory>, which adds a <xref:System.ServiceModel.Description.WebScriptEndpoint> standard endpoint to the service.</span></span> <span data-ttu-id="b3803-113">Ce point de terminaison est configuré à une adresse vide relative au fichier .svc.</span><span class="sxs-lookup"><span data-stu-id="b3803-113">The endpoint is configured at an empty address relative to the .svc file.</span></span> <span data-ttu-id="b3803-114">Cela signifie que l’adresse du service est `http://localhost/ServiceModelSamples/service.svc`, sans autre suffixe autres que le nom de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b3803-114">This means that the address of the service is `http://localhost/ServiceModelSamples/service.svc`, with no additional suffixes other than the operation name.</span></span>  

```svc
<%@ServiceHost language="C#" Debug="true" Service="Microsoft.Samples.SimpleAjaxService.CalculatorService" Factory="System.ServiceModel.Activation.WebScriptServiceHostFactory" %>
```

 <span data-ttu-id="b3803-115">Le <xref:System.ServiceModel.Description.WebScriptEndpoint> est préconfiguré pour rendre le service accessible à partir d'une page cliente ASP.NET AJAX.</span><span class="sxs-lookup"><span data-stu-id="b3803-115">The <xref:System.ServiceModel.Description.WebScriptEndpoint> is pre-configured to make the service accessible from an ASP.NET AJAX client page.</span></span> <span data-ttu-id="b3803-116">La section suivante dans Web.config peut être utilisée pour apporter des modifications de configuration supplémentaires au point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b3803-116">The following section in Web.config can be used to make additional configuration changes to the endpoint.</span></span> <span data-ttu-id="b3803-117">Elle peut être supprimée si aucune modification supplémentaire n'est requise.</span><span class="sxs-lookup"><span data-stu-id="b3803-117">It can be removed if no extra changes are required.</span></span>  
  
```xml  
<system.serviceModel>  
  <standardEndpoints>  
    <webScriptEndpoint>  
      <!-- Use this element to configure the endpoint -->  
      <standardEndpoint name=""  />  
    </webScriptEndpoint>  
  </standardEndpoints>  
</system.serviceModel>  
```  
  
 <span data-ttu-id="b3803-118">Le <xref:System.ServiceModel.Description.WebScriptEndpoint> affecte au format de données par défaut du service la valeur JSON au lieu de XML.</span><span class="sxs-lookup"><span data-stu-id="b3803-118">The <xref:System.ServiceModel.Description.WebScriptEndpoint> sets the default data format for the service to JSON instead of XML.</span></span> <span data-ttu-id="b3803-119">Pour appeler le service, accédez à `http://localhost/ServiceModelSamples/service.svc/Add?n1=100&n2=200` après la fin de l’ensemble des étapes et de génération indiqués plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="b3803-119">To invoke the service, navigate to `http://localhost/ServiceModelSamples/service.svc/Add?n1=100&n2=200` after completing the set up and build steps shown later in this topic.</span></span> <span data-ttu-id="b3803-120">L'utilisation d'une requête HTTP GET active cette fonctionnalité de test.</span><span class="sxs-lookup"><span data-stu-id="b3803-120">This testing functionality is enabled by the use of a HTTP GET request.</span></span>  
  
 <span data-ttu-id="b3803-121">La page web PostAjaxClientPage.aspx du client contient le code ASP.NET permettant d’appeler le service à chaque fois que l’utilisateur clique sur l’un des boutons d’opération de cette page.</span><span class="sxs-lookup"><span data-stu-id="b3803-121">The client Web page SimpleAjaxClientPage.aspx contains ASP.NET code to invoke the service whenever the user clicks one of the operation buttons on the page.</span></span> <span data-ttu-id="b3803-122">Le contrôle `ScriptManager` est utilisé pour permettre l'accès à un proxy du service via JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b3803-122">The `ScriptManager` control is used to make a proxy to the service accessible through JavaScript.</span></span>  

```aspx-csharp
<asp:ScriptManager ID="ScriptManager" runat="server">  
    <Services>  
        <asp:ServiceReference Path="service.svc" />  
    </Services>  
</asp:ScriptManager>  
```

 <span data-ttu-id="b3803-123">Le proxy local est instancié et les opérations sont appelées à l'aide du code Javascript suivant.</span><span class="sxs-lookup"><span data-stu-id="b3803-123">The local proxy is instantiated and operations are invoked using the following JavaScript code.</span></span>  

```javascript
// Code for extracting arguments n1 and n2 omitted…  
// Instantiate a service proxy  
var proxy = new SimpleAjaxService.ICalculator();  
// Code for selecting operation omitted…  
proxy.Add(parseFloat(n1), parseFloat(n2), onSuccess, onFail, null);  
```

 <span data-ttu-id="b3803-124">Si l'appel du service réussit, le code appelle le gestionnaire `onSuccess` et le résultat de l'opération s'affiche dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="b3803-124">If the service call succeeds, the code invokes the `onSuccess` handler and the result of the operation is displayed in a text box.</span></span>  

```javascript
function onSuccess(mathResult){  
     document.getElementById("result").value = mathResult;  
}
```

> [!IMPORTANT]
>  <span data-ttu-id="b3803-125">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b3803-125">The samples may already be installed on your machine.</span></span> <span data-ttu-id="b3803-126">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="b3803-126">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="b3803-127">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="b3803-127">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="b3803-128">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="b3803-128">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Ajax\SimpleAjaxService`  
