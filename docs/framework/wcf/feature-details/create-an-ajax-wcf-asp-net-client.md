---
title: Créer un Service WCF compatible AJAX et un Client ASP.NET dans Visual Studio
ms.date: 08/17/2018
ms.assetid: 95012df8-2a66-420d-944a-8afab261013e
ms.openlocfilehash: 954ee0409f370c3fa28814a70d51334fd75f7b79
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/29/2018
ms.locfileid: "47454313"
---
# <a name="how-to-create-an-ajax-enabled-wcf-service-and-an-aspnet-client-that-accesses-the-service"></a><span data-ttu-id="8b994-102">Comment : créer un service WCF compatible AJAX et un client ASP.NET qui accède à ce service</span><span class="sxs-lookup"><span data-stu-id="8b994-102">How to: Create an AJAX-Enabled WCF Service and an ASP.NET Client that Accesses the Service</span></span>

<span data-ttu-id="8b994-103">Cette rubrique montre comment utiliser Visual Studio pour créer un service compatible AJAX Windows Communication Foundation (WCF) et un client ASP.NET qui accède au service.</span><span class="sxs-lookup"><span data-stu-id="8b994-103">This topic shows how to use Visual Studio to create an AJAX-enabled Windows Communication Foundation (WCF) service and an ASP.NET client that accesses the service.</span></span>

## <a name="create-an-aspnet-web-app"></a><span data-ttu-id="8b994-104">Créer une application web ASP.NET</span><span class="sxs-lookup"><span data-stu-id="8b994-104">Create an ASP.NET web app</span></span>

1. <span data-ttu-id="8b994-105">Ouvrez Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8b994-105">Open Visual Studio.</span></span>

1. <span data-ttu-id="8b994-106">À partir de la **fichier** menu, sélectionnez **New** > **projet**</span><span class="sxs-lookup"><span data-stu-id="8b994-106">From the **File** menu, select **New** > **Project**</span></span>

1. <span data-ttu-id="8b994-107">Dans le **nouveau projet** boîte de dialogue, développez le **installé** > **Visual C#** > **Web** catégorie, puis Sélectionnez **Application Web ASP.NET (.NET Framework)**.</span><span class="sxs-lookup"><span data-stu-id="8b994-107">In the **New Project** dialog, expand the **Installed** > **Visual C#** > **Web** category, and then select **ASP.NET Web Application (.NET Framework)**.</span></span>

1. <span data-ttu-id="8b994-108">Nommez le projet **SandwichServices** et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b994-108">Name the Project **SandwichServices** and click **OK**.</span></span>

1. <span data-ttu-id="8b994-109">Dans le **nouvelle Application Web ASP.NET** boîte de dialogue, sélectionnez **vide** , puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b994-109">In the **New ASP.NET Web Application** dialog, select **Empty** and then select **OK**.</span></span>

   ![ASP.NET web application type boîte de dialogue dans Visual Studio](media/create-an-ajax-wcf-asp-net-client/new-asp-net-web-app-type.png)

## <a name="add-a-web-form"></a><span data-ttu-id="8b994-111">Ajoutez un formulaire web</span><span class="sxs-lookup"><span data-stu-id="8b994-111">Add a web form</span></span>

1. <span data-ttu-id="8b994-112">Cliquez sur le projet SandwichServices dans **l’Explorateur de solutions** et sélectionnez **ajouter** > **un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="8b994-112">Right-click the SandwichServices project in **Solution Explorer** and select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="8b994-113">Dans le **ajouter un nouvel élément** boîte de dialogue, développez le **installé** > **Visual C#** > **Web** catégorie, puis Sélectionnez le **Web Form** modèle.</span><span class="sxs-lookup"><span data-stu-id="8b994-113">In the **Add New Item** dialog, expand the **Installed** > **Visual C#** > **Web** category, and then select the **Web Form** template.</span></span>

1. <span data-ttu-id="8b994-114">Acceptez le nom par défaut (**WebForm1**), puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="8b994-114">Accept the default name (**WebForm1**), and then select **Add**.</span></span>

   <span data-ttu-id="8b994-115">*WebForm1.aspx* s’ouvre dans **Source** vue.</span><span class="sxs-lookup"><span data-stu-id="8b994-115">*WebForm1.aspx* opens in **Source** view.</span></span>

1. <span data-ttu-id="8b994-116">Ajoutez le balisage suivant à l’intérieur de la  **\<corps >** balises :</span><span class="sxs-lookup"><span data-stu-id="8b994-116">Add the following markup inside the **\<body>** tags:</span></span>

   ```html
   <input type="button" value="Price of 3 sandwiches" onclick="Calculate()"/>
   <br />
   <span id="additionResult"></span>
   ```

## <a name="create-an-ajax-enabled-wcf-service"></a><span data-ttu-id="8b994-117">Créer un service WCF compatible AJAX</span><span class="sxs-lookup"><span data-stu-id="8b994-117">Create an AJAX-enabled WCF service</span></span>

1. <span data-ttu-id="8b994-118">Cliquez sur le projet SandwichServices dans **l’Explorateur de solutions** et sélectionnez **ajouter** > **un nouvel élément**.</span><span class="sxs-lookup"><span data-stu-id="8b994-118">Right-click the SandwichServices project in **Solution Explorer** and select **Add** > **New Item**.</span></span>

1. <span data-ttu-id="8b994-119">Dans le **ajouter un nouvel élément** boîte de dialogue, développez le **installé** > **Visual C#** > **Web** catégorie, puis Sélectionnez le **Service WCF (compatible AJAX)** modèle.</span><span class="sxs-lookup"><span data-stu-id="8b994-119">In the **Add New Item** dialog, expand the **Installed** > **Visual C#** > **Web** category, and then select the **WCF Service (AJAX-enabled)** template.</span></span>

   ![Modèle d’élément (compatible AJAX) de Service WCF dans Visual Studio](media/create-an-ajax-wcf-asp-net-client/add-wcf-service.png)

1. <span data-ttu-id="8b994-121">Nommez le service **CostService** , puis sélectionnez **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="8b994-121">Name the service **CostService** and then select **Add**.</span></span>

   <span data-ttu-id="8b994-122">*CostService.svc.cs* s’ouvre dans l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="8b994-122">*CostService.svc.cs* opens in the editor.</span></span>

1. <span data-ttu-id="8b994-123">Implémenter l’opération dans le service.</span><span class="sxs-lookup"><span data-stu-id="8b994-123">Implement the operation in the service.</span></span> <span data-ttu-id="8b994-124">Ajoutez la méthode suivante à la classe CostService pour calculer le coût d’une quantité de sandwichs :</span><span class="sxs-lookup"><span data-stu-id="8b994-124">Add the following method to the CostService class to calculate the cost of a quantity of sandwiches:</span></span>

    ```csharp
    [OperationContract]
    public double CostOfSandwiches(int quantity)
    {
        return 1.25 * quantity;
    }
    ```

## <a name="configure-the-client-to-access-the-service"></a><span data-ttu-id="8b994-125">Configurer le client pour accéder au service</span><span class="sxs-lookup"><span data-stu-id="8b994-125">Configure the client to access the service</span></span>

1. <span data-ttu-id="8b994-126">Ouvrez le *WebForm1.aspx* fichier et sélectionnez le **conception** vue.</span><span class="sxs-lookup"><span data-stu-id="8b994-126">Open the *WebForm1.aspx* file and select the **Design** view.</span></span>

2. <span data-ttu-id="8b994-127">À partir de la **vue** menu, sélectionnez **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="8b994-127">From the **View** menu, select **Toolbox**.</span></span>

3. <span data-ttu-id="8b994-128">Développez le **Extensions AJAX** nœud et glisser -déplacer un **ScriptManager** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="8b994-128">Expand the **AJAX Extensions** node and drag and drop a **ScriptManager** onto the form.</span></span>

4. <span data-ttu-id="8b994-129">Dans le **Source** afficher, ajoutez le code suivant entre les  **\<ScriptManager >** balises pour spécifier le chemin d’accès au service WCF :</span><span class="sxs-lookup"><span data-stu-id="8b994-129">Back in the **Source** view, add the following code between the **\<ScriptManager>** tags to specify the path to the WCF service:</span></span>

    ```html
    <Services>
       <asp:ServiceReference Path="~/CostService.svc" />
    </Services>
    ```

1. <span data-ttu-id="8b994-130">Ajoutez le code pour la fonction Javascript `Calculate()`.</span><span class="sxs-lookup"><span data-stu-id="8b994-130">Add the code for the Javascript function `Calculate()`.</span></span> <span data-ttu-id="8b994-131">Placez le code suivant dans le **head** section du formulaire web :</span><span class="sxs-lookup"><span data-stu-id="8b994-131">Place the following code in the **head** section of the web form:</span></span>

    ```javascript
    <script type="text/javascript">

        function Calculate() {
            CostService.CostOfSandwiches(3, onSuccess);
        }

        function onSuccess(result) {
            var myres = $get("additionResult");
            myres.innerHTML = result;
        }

    </script>
    ```

   <span data-ttu-id="8b994-132">Ce code appelle la méthode de CostService pour calculer le prix des trois sandwiches, puis affiche le résultat dans l’étendue appelée **additionResult**.</span><span class="sxs-lookup"><span data-stu-id="8b994-132">This code calls the method of CostService to calculate the price for three sandwiches, and then displays the result in the span called **additionResult**.</span></span>

## <a name="run-the-program"></a><span data-ttu-id="8b994-133">Exécuter le programme</span><span class="sxs-lookup"><span data-stu-id="8b994-133">Run the program</span></span>

<span data-ttu-id="8b994-134">Assurez-vous que l’option *WebForm1.aspx* a le focus, puis appuyez sur **Démarrer** bouton pour lancer le client web.</span><span class="sxs-lookup"><span data-stu-id="8b994-134">Make sure that *WebForm1.aspx* has focus, and then press **Start** button to launch the web client.</span></span> <span data-ttu-id="8b994-135">Le bouton a un triangle vert et disant quelque chose comme **IIS Express (Microsoft Edge)**.</span><span class="sxs-lookup"><span data-stu-id="8b994-135">The button has a green triangle and says something like **IIS Express (Microsoft Edge)**.</span></span> <span data-ttu-id="8b994-136">Ou, vous pouvez appuyer sur **F5**.</span><span class="sxs-lookup"><span data-stu-id="8b994-136">Or, you can press **F5**.</span></span> <span data-ttu-id="8b994-137">Cliquez sur le **prix de 3 sandwiches** bouton pour générer la sortie attendue de « 3.75 ».</span><span class="sxs-lookup"><span data-stu-id="8b994-137">Click the **Price of 3 sandwiches** button to generate the expected output of "3.75".</span></span>

## <a name="example-code"></a><span data-ttu-id="8b994-138">exemple de code</span><span class="sxs-lookup"><span data-stu-id="8b994-138">Example code</span></span>

<span data-ttu-id="8b994-139">Voici le code complet dans le *CostService.svc.cs* fichier :</span><span class="sxs-lookup"><span data-stu-id="8b994-139">Following is the full code in the *CostService.svc.cs* file :</span></span>

```csharp
using System.ServiceModel;
using System.ServiceModel.Activation;

namespace SandwichServices
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class CostService
    {
        [OperationContract]
        public double CostOfSandwiches(int quantity)
        {
            return 1.25 * quantity;
        }
    }
}
```

<span data-ttu-id="8b994-140">Voici le contenu complet de la *WebForm1.aspx* page :</span><span class="sxs-lookup"><span data-stu-id="8b994-140">Following is the full contents of the *WebForm1.aspx* page:</span></span>

```aspx-csharp
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs" Inherits="SandwichServices.WebForm1" %>

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
    <title></title>
    <script type="text/javascript">

        function Calculate() {
            CostService.CostOfSandwiches(3, onSuccess);
        }

        function onSuccess(result) {
            var myres = $get("additionResult");
            myres.innerHTML = result;
        }

    </script>
</head>
<body>
    <form id="form1" runat="server">
        <div>
        </div>
        <asp:ScriptManager ID="ScriptManager1" runat="server">
            <Services>
                <asp:ServiceReference Path="~/CostService.svc" />
            </Services>
        </asp:ScriptManager>

        <input type="button" value="Price of 3 sandwiches" onclick="Calculate()" />
        <br />
        <span id="additionResult"></span>
    </form>
</body>
</html>
```
