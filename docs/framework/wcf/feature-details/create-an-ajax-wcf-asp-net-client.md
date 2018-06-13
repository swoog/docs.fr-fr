---
title: 'Comment : créer un service WCF compatible AJAX et un client ASP.NET qui accède à ce service'
ms.date: 03/30/2017
ms.assetid: 95012df8-2a66-420d-944a-8afab261013e
ms.openlocfilehash: 58971d11ab76112627dd81d53381236932268e25
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33490628"
---
# <a name="how-to-create-an-ajax-enabled-wcf-service-and-an-aspnet-client-that-accesses-the-service"></a><span data-ttu-id="82797-102">Comment : créer un service WCF compatible AJAX et un client ASP.NET qui accède à ce service</span><span class="sxs-lookup"><span data-stu-id="82797-102">How to: Create an AJAX-Enabled WCF Service and an ASP.NET Client that Accesses the Service</span></span>
<span data-ttu-id="82797-103">Cette rubrique montre comment utiliser Visual Studio 2008 pour créer un service compatible AJAX Windows Communication Foundation (WCF) et un client ASP.NET qui accède au service.</span><span class="sxs-lookup"><span data-stu-id="82797-103">This topic shows how to use Visual Studio 2008 to create an AJAX-enabled Windows Communication Foundation (WCF) service and an ASP.NET client that accesses the service.</span></span> <span data-ttu-id="82797-104">Le code pour le service et pour le client est fourni dans la section Exemple après les étapes de création décrites dans la section Procédures.</span><span class="sxs-lookup"><span data-stu-id="82797-104">The code for the service and for the client are provided in the Example section after the steps for creating them are described in the Procedures section.</span></span>  
  
### <a name="to-create-the-aspnet-client-application"></a><span data-ttu-id="82797-105">Pour créer l'application cliente ASP.NET</span><span class="sxs-lookup"><span data-stu-id="82797-105">To create the ASP.NET client application</span></span>  
  
1.  <span data-ttu-id="82797-106">Ouvrez [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="82797-106">Open [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)].</span></span>  
  
2.  <span data-ttu-id="82797-107">À partir de la **fichier** menu, sélectionnez **nouveau**, puis **projet**, puis **Web**, puis sélectionnez **ASP.NET Web Application**.</span><span class="sxs-lookup"><span data-stu-id="82797-107">From the **File** menu, select **New**, then **Project**, then **Web**, and then select **ASP.NET Web Application**.</span></span>  
  
3.  <span data-ttu-id="82797-108">Nommez le projet `SandwichServices` et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="82797-108">Name the Project `SandwichServices` and click **OK**.</span></span>  
  
### <a name="to-create-the-wcf-ajax-enabled-service"></a><span data-ttu-id="82797-109">Pour créer le service WCF compatible AJAX</span><span class="sxs-lookup"><span data-stu-id="82797-109">To create the WCF AJAX-enabled service</span></span>  
  
1.  <span data-ttu-id="82797-110">Avec le bouton droit le `SandwichServices` de projet dans le **l’Explorateur de solutions** et sélectionnez **ajouter**, puis **un nouvel élément**, puis **Service WCF compatible AJAX** .</span><span class="sxs-lookup"><span data-stu-id="82797-110">Right-click the `SandwichServices` project in the **Solution Explorer** window and select **Add**, then **New Item**, and then **AJAX-enabled WCF Service**.</span></span>  
  
2.  <span data-ttu-id="82797-111">Nom de service `CostService` dans les **nom** , puis cliquez sur **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="82797-111">Name the service `CostService` in the **Name** box and click **Add**.</span></span>  
  
3.  <span data-ttu-id="82797-112">Ouvrez le fichier CostService.svc.cs.</span><span class="sxs-lookup"><span data-stu-id="82797-112">Open the CostService.svc.cs file.</span></span>  
  
4.  <span data-ttu-id="82797-113">Spécifiez le `Namespace` pour <xref:System.ServiceModel.ServiceContractAttribute> comme `SandwichService`:</span><span class="sxs-lookup"><span data-stu-id="82797-113">Specify the `Namespace` for <xref:System.ServiceModel.ServiceContractAttribute> as `SandwichService`:</span></span>  
  
    ```  
    namespace SandwichServices  
    {  
      [ServiceContract(Namespace = "SandwichServices")]  
      [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]  
       public class CostService  
       {  
         …  
       }  
     }  
    ```  
  
5.  <span data-ttu-id="82797-114">Implémentez les opérations dans le service.</span><span class="sxs-lookup"><span data-stu-id="82797-114">Implement the operations in the service.</span></span> <span data-ttu-id="82797-115">Ajoutez <xref:System.ServiceModel.OperationContractAttribute> à chacune des opérations pour indiquer qu'elles font partie du contrat.</span><span class="sxs-lookup"><span data-stu-id="82797-115">Add the <xref:System.ServiceModel.OperationContractAttribute> to each of the operations to indicate that they are part of the contract.</span></span> <span data-ttu-id="82797-116">L'exemple suivant implémente une méthode qui retourne le coût d'une quantité donnée de sandwichs.</span><span class="sxs-lookup"><span data-stu-id="82797-116">The following example implements a method that returns the cost of a given quantity of sandwiches.</span></span>  
  
    ```  
    public class CostService  
    {  
        [OperationContract]  
        public double CostOfSandwiches(int quantity)  
        {  
            return 1.25 * quantity;  
        }  
  
    // Add more operations here and mark them with [OperationContract]  
    }  
    ```  
  
### <a name="to-configure-the-client-to-access-the-service"></a><span data-ttu-id="82797-117">Pour configurer le client pour accéder au service</span><span class="sxs-lookup"><span data-stu-id="82797-117">To configure the client to access the service</span></span>  
  
1.  <span data-ttu-id="82797-118">Ouvrez la page Default.aspx, puis sélectionnez le **conception** vue.</span><span class="sxs-lookup"><span data-stu-id="82797-118">Open the Default.aspx page and select the **Design** view.</span></span>  
  
2.  <span data-ttu-id="82797-119">À partir de la **vue** menu, sélectionnez **boîte à outils**.</span><span class="sxs-lookup"><span data-stu-id="82797-119">From the **View** menu, select **Toolbox**.</span></span>  
  
3.  <span data-ttu-id="82797-120">Développez le **Extensions AJAX** nœud et glisser-déplacer un **ScriptManager** sur la page Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="82797-120">Expand the **AJAX Extensions** node and drag and drop a **ScriptManager** on to the Default.aspx page.</span></span>  
  
4.  <span data-ttu-id="82797-121">Cliquez sur le **ScriptManager** et sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="82797-121">Right-click the **ScriptManager** and select **Properties**.</span></span>  
  
5.  <span data-ttu-id="82797-122">Développez le **Services** collection dans le **propriétés** fenêtre pour ouvrir la **éditeur de collections ServiceReference** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="82797-122">Expand the **Services** collection in the **Properties** window to open up the **ServiceReference Collection Editor** window.</span></span>  
  
6.  <span data-ttu-id="82797-123">Cliquez sur **ajouter**, spécifiez `CostService.svc` comme le **chemin d’accès** référencé, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="82797-123">Click **Add**, specify `CostService.svc` as the **Path** referenced, and click **OK**.</span></span>  
  
7.  <span data-ttu-id="82797-124">Développez le **HTML** nœud dans le **boîte à outils** et faites glisser et déposez une **entrée (bouton)** sur la page Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="82797-124">Expand the **HTML** node in the **Toolbox** and drag and drop an **Input (Button)** on to the Default.aspx page.</span></span>  
  
8.  <span data-ttu-id="82797-125">Cliquez sur le **bouton** et sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="82797-125">Right-click the **Button** and select **Properties**.</span></span>  
  
9. <span data-ttu-id="82797-126">Modifier la **valeur** au champ `Price for 3 Sandwiches`.</span><span class="sxs-lookup"><span data-stu-id="82797-126">Change the **Value** field to `Price for 3 Sandwiches`.</span></span>  
  
10. <span data-ttu-id="82797-127">Double-cliquez sur le **bouton** pour accéder au code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="82797-127">Double-click the **Button** to access the JavaScript code.</span></span>  
  
11. <span data-ttu-id="82797-128">Passez dans le code JavaScript suivant dans le <`script`> élément.</span><span class="sxs-lookup"><span data-stu-id="82797-128">Pass in the following JavaScript code within the <`script`> element.</span></span>  
  
    ```  
    function Button1_onclick() {  
    var service = new SandwichServices.CostService();  
    service.CostOfSandwiches(3, onSuccess, null, null);  
    }  
  
    function onSuccess(result){  
    alert(result);  
    }  
    ```  
  
### <a name="to-access-the-service-from-the-client"></a><span data-ttu-id="82797-129">Pour accéder au service depuis le client</span><span class="sxs-lookup"><span data-stu-id="82797-129">To access the service from the client</span></span>  
  
1.  <span data-ttu-id="82797-130">Utilisez Ctrl + F5 pour lancer le service et le client Web.</span><span class="sxs-lookup"><span data-stu-id="82797-130">Use Ctrl +F5 to launch the service and the Web client.</span></span> <span data-ttu-id="82797-131">Cliquez sur le **prix de 3 Sandwiches grillé** bouton pour générer la sortie attendue de « 3.75 ».</span><span class="sxs-lookup"><span data-stu-id="82797-131">Click the **Price for 3 Grilled Sandwiches** button to generate the expected output of "3.75".</span></span>  
  
## <a name="example"></a><span data-ttu-id="82797-132">Exemple</span><span class="sxs-lookup"><span data-stu-id="82797-132">Example</span></span>  
 <span data-ttu-id="82797-133">Cet exemple contient le code de service contenu dans le fichier WCFService.svc.cs et le code client contenu dans le fichier Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="82797-133">This example contains the service code contained in the WCFService.svc.cs file and the client code contained in the Default.aspx file.</span></span>  
  
```  
//The service code contained in the CostService.svc.cs file.  
  
using System;  
using System.Linq;  
using System.Runtime.Serialization;  
using System.ServiceModel;  
using System.ServiceModel.Activation;  
using System.ServiceModel.Web;  
  
namespace SandwichServices  
{  
    [ServiceContract(Namespace="SandwichServices")]  
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]  
    public class CostService  
    {  
        // Add [WebGet] attribute to use HTTP GET  
        [OperationContract]  
        public double CostOfSandwiches(int quantity)  
        {  
            return 1.25 * quantity;  
        }  
  
        // Add more operations here and mark them with [OperationContract]  
    }  
}  
//The code for hosting the service is contained in the CostService.svc file.  
  
<%@ ServiceHost Language="C#" Debug="true" Service="SandwichServices.CostService" CodeBehind="CostService.svc.cs" %>  
  
//The client code contained in the Default.aspx file.  
  
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Default.aspx.cs" Inherits="SandwichServices._Default" %>  
  
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">  
  
<html >  
<head runat="server">  
    <title>Untitled Page</title>  
<script language="javascript" type="text/javascript">  
// <!CDATA[  
  
function Button1_onclick() {  
var service = new SandwichServices.CostService();  
service.CostOfSandwiches(3, onSuccess, null, null);  
}  
  
function onSuccess(result){  
alert(result);  
}  
  
// ]]>  
</script>  
</head>  
<body>  
    <form id="form1" runat="server">  
    <div>  
  
    </div>  
    <asp:ScriptManager ID="ScriptManager1" runat="server">  
        <services>  
            <asp:servicereference Path="CostService.svc" />  
        </services>  
    </asp:ScriptManager>  
    </form>  
    <p>  
        <input id="Button1" type="button" value="Price for 3 Sandwiches" onclick="return Button1_onclick()" /></p>  
</body>  
</html>  
```     
