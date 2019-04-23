---
title: SqlDependency dans une application ASP.NET
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ff226ce3-f6b5-47a1-8d22-dc78b67e07f5
ms.openlocfilehash: 67c1307bb18b3e86e05b56f4853a39f6831ab9cc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59313591"
---
# <a name="sqldependency-in-an-aspnet-application"></a><span data-ttu-id="a6b22-102">SqlDependency dans une application ASP.NET</span><span class="sxs-lookup"><span data-stu-id="a6b22-102">SqlDependency in an ASP.NET Application</span></span>
<span data-ttu-id="a6b22-103">L'exemple de cette section montre comment utiliser <xref:System.Data.SqlClient.SqlDependency> indirectement en tirant parti de l'objet <xref:System.Web.Caching.SqlCacheDependency> ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="a6b22-103">The example in this section shows how to use <xref:System.Data.SqlClient.SqlDependency> indirectly by leveraging the ASP.NET <xref:System.Web.Caching.SqlCacheDependency> object.</span></span> <span data-ttu-id="a6b22-104">L'objet <xref:System.Web.Caching.SqlCacheDependency> utilise un objet <xref:System.Data.SqlClient.SqlDependency> pour écouter les notifications et mettre correctement à jour le cache.</span><span class="sxs-lookup"><span data-stu-id="a6b22-104">The <xref:System.Web.Caching.SqlCacheDependency> object uses a <xref:System.Data.SqlClient.SqlDependency> to listen for notifications and correctly update the cache.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a6b22-105">L’exemple de code suppose que vous avez activé les notifications de requête en exécutant les scripts dans [l’activation des Notifications de requête](../../../../../docs/framework/data/adonet/sql/enabling-query-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a6b22-105">The sample code assumes that you have enabled query notifications by executing the scripts in [Enabling Query Notifications](../../../../../docs/framework/data/adonet/sql/enabling-query-notifications.md).</span></span>  
  
## <a name="about-the-sample-application"></a><span data-ttu-id="a6b22-106">À propose de l'exemple d'application</span><span class="sxs-lookup"><span data-stu-id="a6b22-106">About the Sample Application</span></span>  
 <span data-ttu-id="a6b22-107">L’exemple d’application utilise une seule page Web ASP.NET pour afficher des informations de produit à partir de la **AdventureWorks** base de données SQL Server dans un <xref:System.Web.UI.WebControls.GridView> contrôle.</span><span class="sxs-lookup"><span data-stu-id="a6b22-107">The sample application uses a single ASP.NET Web page to display product information from the **AdventureWorks** SQL Server database in a <xref:System.Web.UI.WebControls.GridView> control.</span></span> <span data-ttu-id="a6b22-108">Lorsque la page se charge, le code écrit l'heure actuelle dans un contrôle <xref:System.Web.UI.WebControls.Label>.</span><span class="sxs-lookup"><span data-stu-id="a6b22-108">When the page loads, the code writes the current time to a <xref:System.Web.UI.WebControls.Label> control.</span></span> <span data-ttu-id="a6b22-109">Ensuite, elle définit un objet <xref:System.Web.Caching.SqlCacheDependency> et les propriétés de l'objet <xref:System.Web.Caching.Cache> pour stocker les données du cache pendant trois minutes au maximum.</span><span class="sxs-lookup"><span data-stu-id="a6b22-109">It then defines a <xref:System.Web.Caching.SqlCacheDependency> object and sets properties on the <xref:System.Web.Caching.Cache> object to store the cache data for up to three minutes.</span></span> <span data-ttu-id="a6b22-110">Le code se connecte ensuite à la base de données et récupère les données.</span><span class="sxs-lookup"><span data-stu-id="a6b22-110">The code then connects to the database and retrieves the data.</span></span> <span data-ttu-id="a6b22-111">Une fois que la page est chargée et que l'application s'exécute, ASP.NET récupère les données dans le cache, ce que vous pouvez vérifier en notant que l'heure indiquée sur la page ne change pas.</span><span class="sxs-lookup"><span data-stu-id="a6b22-111">When the page is loaded and the application is running ASP.NET will retrieve data from the cache, which you can verify by noting that the time on the page does not change.</span></span> <span data-ttu-id="a6b22-112">Si les données surveillées sont modifiées, ASP.NET invalide le cache et remplit de nouveau le contrôle `GridView` avec les données actualisées, ce qui met à jour l'heure affichée dans le contrôle `Label`.</span><span class="sxs-lookup"><span data-stu-id="a6b22-112">If the data being monitored changes, ASP.NET invalidates the cache and repopulate the `GridView` control with fresh data, updating the time displayed in the `Label` control.</span></span>  
  
## <a name="creating-the-sample-application"></a><span data-ttu-id="a6b22-113">Création de l'exemple d'application</span><span class="sxs-lookup"><span data-stu-id="a6b22-113">Creating the Sample Application</span></span>  
 <span data-ttu-id="a6b22-114">Procédez comme suit pour créer et exécuter l'exemple d'application :</span><span class="sxs-lookup"><span data-stu-id="a6b22-114">Follow these steps to create and run the sample application:</span></span>  
  
1. <span data-ttu-id="a6b22-115">Créez un site Web ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="a6b22-115">Create a new ASP.NET Web site.</span></span>  
  
2. <span data-ttu-id="a6b22-116">Ajoutez un contrôle <xref:System.Web.UI.WebControls.Label> et un contrôle <xref:System.Web.UI.WebControls.GridView> à la page Default.aspx.</span><span class="sxs-lookup"><span data-stu-id="a6b22-116">Add a <xref:System.Web.UI.WebControls.Label> and a <xref:System.Web.UI.WebControls.GridView> control to the Default.aspx page.</span></span>  
  
3. <span data-ttu-id="a6b22-117">Ouvrez le module de classe de la page et ajoutez les directives suivantes :</span><span class="sxs-lookup"><span data-stu-id="a6b22-117">Open the page's class module and add the following directives:</span></span>  
  
    ```vb  
    Option Strict On  
    Option Explicit On  
  
    Imports System.Data.SqlClient  
    ```  
  
    ```csharp  
    using System.Data.SqlClient;  
    using System.Web.Caching;  
    ```  
  
4. <span data-ttu-id="a6b22-118">Ajoutez le code suivant dans l'événement `Page_Load` de la page :</span><span class="sxs-lookup"><span data-stu-id="a6b22-118">Add the following code in the page's `Page_Load` event:</span></span>  
  
     [!code-csharp[DataWorks SqlDependency.AspNet#1](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlDependency.AspNet/CS/Default.aspx.cs#1)]
     [!code-vb[DataWorks SqlDependency.AspNet#1](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlDependency.AspNet/VB/Default.aspx.vb#1)]  
  
5. <span data-ttu-id="a6b22-119">Ajoutez deux méthodes d'assistance, `GetConnectionString` et `GetSQL`.</span><span class="sxs-lookup"><span data-stu-id="a6b22-119">Add two helper methods, `GetConnectionString` and `GetSQL`.</span></span> <span data-ttu-id="a6b22-120">La chaîne de connexion définie utilise une sécurité intégrée.</span><span class="sxs-lookup"><span data-stu-id="a6b22-120">The connection string defined uses integrated security.</span></span> <span data-ttu-id="a6b22-121">Vous devez vérifier que le compte que vous utilisez dispose les autorisations de base de données nécessaires et que la base de données exemple **AdventureWorks**, notifications sont activées.</span><span class="sxs-lookup"><span data-stu-id="a6b22-121">You will need to verify that the account you are using has the necessary database permissions and that the sample database, **AdventureWorks**, has notifications enabled.</span></span>
  
     [!code-csharp[DataWorks SqlDependency.AspNet#2](../../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlDependency.AspNet/CS/Default.aspx.cs#2)]
     [!code-vb[DataWorks SqlDependency.AspNet#2](../../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlDependency.AspNet/VB/Default.aspx.vb#2)]  
  
### <a name="testing-the-application"></a><span data-ttu-id="a6b22-122">Test de l'application</span><span class="sxs-lookup"><span data-stu-id="a6b22-122">Testing the Application</span></span>  
 <span data-ttu-id="a6b22-123">L'application met en cache les données affichées sur le formulaire Web et l'actualise toutes les trois minutes en cas d'inactivité.</span><span class="sxs-lookup"><span data-stu-id="a6b22-123">The application caches the data displayed on the Web form and refreshes it every three minutes if there is no activity.</span></span> <span data-ttu-id="a6b22-124">En cas de modification de la base de données, le cache est immédiatement actualisé.</span><span class="sxs-lookup"><span data-stu-id="a6b22-124">If a change occurs to the database, the cache is refreshed immediately.</span></span> <span data-ttu-id="a6b22-125">Exécutez l'application à partir de Visual Studio, ce qui charge la page dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="a6b22-125">Run the application from Visual Studio, which loads the page into the browser.</span></span> <span data-ttu-id="a6b22-126">L'heure d'actualisation du cache affichée indique la dernière actualisation du cache.</span><span class="sxs-lookup"><span data-stu-id="a6b22-126">The cache refresh time displayed indicates when the cache was last refreshed.</span></span> <span data-ttu-id="a6b22-127">Attendez trois minutes, puis actualisez la page. Un événement de publication se produit alors.</span><span class="sxs-lookup"><span data-stu-id="a6b22-127">Wait three minutes, and then refresh the page, causing a postback event to occur.</span></span> <span data-ttu-id="a6b22-128">Notez que l'heure affichée sur la page a changé.</span><span class="sxs-lookup"><span data-stu-id="a6b22-128">Note that the time displayed on the page has changed.</span></span> <span data-ttu-id="a6b22-129">Si vous actualisez la page avant trois minutes, l'heure affichée sur la page restera la même.</span><span class="sxs-lookup"><span data-stu-id="a6b22-129">If you refresh the page in less than three minutes, the time displayed on the page will remain the same.</span></span>  
  
 <span data-ttu-id="a6b22-130">Mettez à jour les données dans la base de données en utilisant une commande Transact-SQL UPDATE, puis actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="a6b22-130">Now update the data in the database, using a Transact-SQL UPDATE command and refresh the page.</span></span> <span data-ttu-id="a6b22-131">L'heure affichée indique maintenant que le cache a été actualisé avec les nouvelles données de la base de données.</span><span class="sxs-lookup"><span data-stu-id="a6b22-131">The time displayed now indicates that the cache was refreshed with the new data from the database.</span></span> <span data-ttu-id="a6b22-132">Notez que même si le cache est mis à jour, l'heure affichée sur le page n'est pas modifiée tant qu'un événement de publication ne s'est pas produit.</span><span class="sxs-lookup"><span data-stu-id="a6b22-132">Note that although the cache is updated, the time displayed on the page does not change until a postback event occurs.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6b22-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6b22-133">See also</span></span>

- [<span data-ttu-id="a6b22-134">Notifications de requête dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="a6b22-134">Query Notifications in SQL Server</span></span>](../../../../../docs/framework/data/adonet/sql/query-notifications-in-sql-server.md)
- [<span data-ttu-id="a6b22-135">Fournisseurs managés ADO.NET et centre de développement DataSet</span><span class="sxs-lookup"><span data-stu-id="a6b22-135">ADO.NET Managed Providers and DataSet Developer Center</span></span>](https://go.microsoft.com/fwlink/?LinkId=217917)
