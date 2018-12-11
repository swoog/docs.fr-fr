---
title: 'Procédure : Définir la chaîne de connexion'
ms.date: 03/30/2017
ms.assetid: 6027335d-4e26-420d-9151-6523289b1989
ms.openlocfilehash: 7fb722acbb13b3502d004978581701cc70118ff8
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53129686"
---
# <a name="how-to-define-the-connection-string"></a><span data-ttu-id="90338-102">Procédure : Définir la chaîne de connexion</span><span class="sxs-lookup"><span data-stu-id="90338-102">How to: Define the Connection String</span></span>

<span data-ttu-id="90338-103">Cette rubrique montre comment définir la chaîne utilisée pour la connexion à un modèle conceptuel.</span><span class="sxs-lookup"><span data-stu-id="90338-103">This topic shows how to define the connection string that is used when connecting to a conceptual model.</span></span> <span data-ttu-id="90338-104">Cette rubrique est basée sur le [AdventureWorks Sales Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb387147(v=vs.100)) modèle conceptuel.</span><span class="sxs-lookup"><span data-stu-id="90338-104">This topic is based on the [AdventureWorks Sales](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb387147(v=vs.100)) conceptual model.</span></span> <span data-ttu-id="90338-105">Le modèle de vente AdventureWorks Sales Model est utilisé dans toutes les rubriques liées aux tâches de la documentation [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="90338-105">The AdventureWorks Sales Model is used throughout the task-related topics in the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] documentation.</span></span> <span data-ttu-id="90338-106">Cette rubrique suppose que vous avez déjà configuré le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] et défini le modèle AdventureWorks Sales Model.</span><span class="sxs-lookup"><span data-stu-id="90338-106">This topic assumes that you have already configured the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] and defined the AdventureWorks Sales Model.</span></span> <span data-ttu-id="90338-107">Pour plus d'informations, voir [Procédure : Définir le modèle manuellement et de fichiers de mappage](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399785(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="90338-107">For more information, see [How to: Manually Define the Model and Mapping Files](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399785(v=vs.100)).</span></span> <span data-ttu-id="90338-108">Les procédures décrites dans cette rubrique sont également incluses dans [Comment : Configurer manuellement un projet Entity Framework](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738546(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="90338-108">The procedures in this topic are also included in [How to: Manually Configure an Entity Framework Project](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738546(v=vs.100)).</span></span>

> [!NOTE]
> <span data-ttu-id="90338-109">Si vous utilisez le [!INCLUDE[adonet_edm](../../../../../includes/adonet-edm-md.md)] Assistant dans un projet Visual Studio, il génère automatiquement un fichier .edmx et configure le projet pour utiliser le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="90338-109">If you use the [!INCLUDE[adonet_edm](../../../../../includes/adonet-edm-md.md)] Wizard in a Visual Studio project, it automatically generates an .edmx file and configures the project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="90338-110">Pour plus d'informations, voir [Procédure : Utilisez l’Assistant Entity Data Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="90338-110">For more information, see [How to: Use the Entity Data Model Wizard](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738677(v=vs.100))</span></span>

## <a name="to-define-the-entity-framework-connection-string"></a><span data-ttu-id="90338-111">Pour définir la chaîne de connexion Entity Framework</span><span class="sxs-lookup"><span data-stu-id="90338-111">To define the Entity Framework connection string</span></span>

- <span data-ttu-id="90338-112">Ouvrez le fichier de configuration de l'application (app.config) du projet et ajoutez la chaîne de connexion suivante :</span><span class="sxs-lookup"><span data-stu-id="90338-112">Open the project's application configuration file (app.config) and add the following connection string:</span></span>

```xml
<connectionStrings>
    <add name="AdventureWorksEntities" 
         connectionString="metadata=.\AdventureWorks.csdl|.\AdventureWorks.ssdl|.\AdventureWorks.msl;
         provider=System.Data.SqlClient;provider connection string='Data Source=localhost;
         Initial Catalog=AdventureWorks;Integrated Security=True;Connection Timeout=60;
         multipleactiveresultsets=true'" providerName="System.Data.EntityClient" />
</connectionStrings>
```

<span data-ttu-id="90338-113">Si votre projet n’a pas d’un fichier de configuration d’application, vous pouvez en ajouter un en sélectionnant **ajouter un nouvel élément** à partir de la **projet** menu, en sélectionnant le **général** catégorie, en sélectionnant **fichier de Configuration d’Application**, puis en cliquant sur **ajouter**.</span><span class="sxs-lookup"><span data-stu-id="90338-113">If your project does not have an application configuration file, you can add one by selecting **Add New Item** from the **Project** menu, selecting the **General** category, selecting **Application Configuration File**, and then clicking **Add**.</span></span>

## <a name="see-also"></a><span data-ttu-id="90338-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90338-114">See also</span></span>

- <span data-ttu-id="90338-115">[Démarrage rapide](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399182(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="90338-115">[Quickstart](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399182(v=vs.100))</span></span>
- <span data-ttu-id="90338-116">[Comment : Créez un fichier .edmx](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716703(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="90338-116">[How to: Create a New .edmx File](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc716703(v=vs.100))</span></span>
- <span data-ttu-id="90338-117">[Outils ADO.NET Entity Data Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="90338-117">[ADO.NET Entity Data Model  Tools](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))</span></span>
