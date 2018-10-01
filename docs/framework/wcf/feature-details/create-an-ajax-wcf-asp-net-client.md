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
# <a name="how-to-create-an-ajax-enabled-wcf-service-and-an-aspnet-client-that-accesses-the-service"></a>Comment : créer un service WCF compatible AJAX et un client ASP.NET qui accède à ce service

Cette rubrique montre comment utiliser Visual Studio pour créer un service compatible AJAX Windows Communication Foundation (WCF) et un client ASP.NET qui accède au service.

## <a name="create-an-aspnet-web-app"></a>Créer une application web ASP.NET

1. Ouvrez Visual Studio.

1. À partir de la **fichier** menu, sélectionnez **New** > **projet**

1. Dans le **nouveau projet** boîte de dialogue, développez le **installé** > **Visual C#** > **Web** catégorie, puis Sélectionnez **Application Web ASP.NET (.NET Framework)**.

1. Nommez le projet **SandwichServices** et cliquez sur **OK**.

1. Dans le **nouvelle Application Web ASP.NET** boîte de dialogue, sélectionnez **vide** , puis sélectionnez **OK**.

   ![ASP.NET web application type boîte de dialogue dans Visual Studio](media/create-an-ajax-wcf-asp-net-client/new-asp-net-web-app-type.png)

## <a name="add-a-web-form"></a>Ajoutez un formulaire web

1. Cliquez sur le projet SandwichServices dans **l’Explorateur de solutions** et sélectionnez **ajouter** > **un nouvel élément**.

1. Dans le **ajouter un nouvel élément** boîte de dialogue, développez le **installé** > **Visual C#** > **Web** catégorie, puis Sélectionnez le **Web Form** modèle.

1. Acceptez le nom par défaut (**WebForm1**), puis sélectionnez **ajouter**.

   *WebForm1.aspx* s’ouvre dans **Source** vue.

1. Ajoutez le balisage suivant à l’intérieur de la  **\<corps >** balises :

   ```html
   <input type="button" value="Price of 3 sandwiches" onclick="Calculate()"/>
   <br />
   <span id="additionResult"></span>
   ```

## <a name="create-an-ajax-enabled-wcf-service"></a>Créer un service WCF compatible AJAX

1. Cliquez sur le projet SandwichServices dans **l’Explorateur de solutions** et sélectionnez **ajouter** > **un nouvel élément**.

1. Dans le **ajouter un nouvel élément** boîte de dialogue, développez le **installé** > **Visual C#** > **Web** catégorie, puis Sélectionnez le **Service WCF (compatible AJAX)** modèle.

   ![Modèle d’élément (compatible AJAX) de Service WCF dans Visual Studio](media/create-an-ajax-wcf-asp-net-client/add-wcf-service.png)

1. Nommez le service **CostService** , puis sélectionnez **ajouter**.

   *CostService.svc.cs* s’ouvre dans l’éditeur.

1. Implémenter l’opération dans le service. Ajoutez la méthode suivante à la classe CostService pour calculer le coût d’une quantité de sandwichs :

    ```csharp
    [OperationContract]
    public double CostOfSandwiches(int quantity)
    {
        return 1.25 * quantity;
    }
    ```

## <a name="configure-the-client-to-access-the-service"></a>Configurer le client pour accéder au service

1. Ouvrez le *WebForm1.aspx* fichier et sélectionnez le **conception** vue.

2. À partir de la **vue** menu, sélectionnez **boîte à outils**.

3. Développez le **Extensions AJAX** nœud et glisser -déplacer un **ScriptManager** vers le formulaire.

4. Dans le **Source** afficher, ajoutez le code suivant entre les  **\<ScriptManager >** balises pour spécifier le chemin d’accès au service WCF :

    ```html
    <Services>
       <asp:ServiceReference Path="~/CostService.svc" />
    </Services>
    ```

1. Ajoutez le code pour la fonction Javascript `Calculate()`. Placez le code suivant dans le **head** section du formulaire web :

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

   Ce code appelle la méthode de CostService pour calculer le prix des trois sandwiches, puis affiche le résultat dans l’étendue appelée **additionResult**.

## <a name="run-the-program"></a>Exécuter le programme

Assurez-vous que l’option *WebForm1.aspx* a le focus, puis appuyez sur **Démarrer** bouton pour lancer le client web. Le bouton a un triangle vert et disant quelque chose comme **IIS Express (Microsoft Edge)**. Ou, vous pouvez appuyer sur **F5**. Cliquez sur le **prix de 3 sandwiches** bouton pour générer la sortie attendue de « 3.75 ».

## <a name="example-code"></a>exemple de code

Voici le code complet dans le *CostService.svc.cs* fichier :

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

Voici le contenu complet de la *WebForm1.aspx* page :

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
