---
title: 'Procédure : Générer manuellement les Classes de Service de données Client (WCF Data Services)'
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, configuring
- WCF Data Services, client library
ms.assetid: b98cb1d6-956a-4e50-add6-67e4f2587346
ms.openlocfilehash: d197088f94614aac007c0adc310500ae4609f757
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61788711"
---
# <a name="how-to-manually-generate-client-data-service-classes-wcf-data-services"></a><span data-ttu-id="38566-102">Procédure : Générer manuellement les Classes de Service de données Client (WCF Data Services)</span><span class="sxs-lookup"><span data-stu-id="38566-102">How to: Manually Generate Client Data Service Classes (WCF Data Services)</span></span>
<span data-ttu-id="38566-103">WCF Data Services s’intègre à Visual Studio pour vous permettre de générer automatiquement des classes de service de données client lorsque vous utilisez le **ajouter une référence de Service** boîte de dialogue pour ajouter une référence à un service de données dans un projet Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="38566-103">WCF Data Services integrates with Visual Studio to enable you to automatically generate client data service classes when you use the **Add Service Reference** dialog box to add a reference to a data service in a Visual Studio project.</span></span> <span data-ttu-id="38566-104">Pour plus d'informations, voir [Procédure : Ajouter une référence de Service de données](../../../../docs/framework/data/wcf/how-to-add-a-data-service-reference-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="38566-104">For more information, see [How to: Add a Data Service Reference](../../../../docs/framework/data/wcf/how-to-add-a-data-service-reference-wcf-data-services.md).</span></span> <span data-ttu-id="38566-105">Vous pouvez également générer manuellement les mêmes classes de service de données client en utilisant l'outil de génération de code, `DataSvcUtil.exe`.</span><span class="sxs-lookup"><span data-stu-id="38566-105">You can also manually generate the same client data service classes by using the code-generation tool, `DataSvcUtil.exe`.</span></span> <span data-ttu-id="38566-106">Cet outil, qui est inclus avec WCF Data Services, génère des classes .NET Framework à partir de la définition de service de données.</span><span class="sxs-lookup"><span data-stu-id="38566-106">This tool, which is included with WCF Data Services, generates .NET Framework classes from the data service definition.</span></span> <span data-ttu-id="38566-107">Il peut également être utilisé pour générer des classes de service des données depuis le fichier de modèle conceptuel (.csdl) et depuis le fichier .edmx qui représente un modèle Entity Framework dans un projet Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="38566-107">It can also be used to generate data service classes from the conceptual model (.csdl) file and from the .edmx file that represents an Entity Framework model in a Visual Studio project.</span></span>

 <span data-ttu-id="38566-108">L'exemple dans cette rubrique crée des classes de service de données client basées sur l'exemple de service de données Northwind.</span><span class="sxs-lookup"><span data-stu-id="38566-108">The example in this topic creates client data service classes based on the Northwind sample data service.</span></span> <span data-ttu-id="38566-109">Ce service est créé lorsque vous effectuez la [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).</span><span class="sxs-lookup"><span data-stu-id="38566-109">This service is created when you complete the [WCF Data Services quickstart](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md).</span></span> <span data-ttu-id="38566-110">Certains exemples dans cette rubrique requièrent le fichier modèle conceptuel pour le modèle Northwind.</span><span class="sxs-lookup"><span data-stu-id="38566-110">Some examples in this topic require the conceptual model file for the Northwind model.</span></span> <span data-ttu-id="38566-111">Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span><span class="sxs-lookup"><span data-stu-id="38566-111">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span> <span data-ttu-id="38566-112">Certains exemples dans cette rubrique requièrent le fichier .edmx pour le modèle Northwind.</span><span class="sxs-lookup"><span data-stu-id="38566-112">Some examples in this topic require the .edmx file for the Northwind model.</span></span> <span data-ttu-id="38566-113">Pour plus d’informations, consultez [présentation d’un fichier .edmx](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="38566-113">For more information, see [.edmx File Overview](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/cc982042(v=vs.100)).</span></span>

### <a name="to-generate-c-classes-that-support-data-binding"></a><span data-ttu-id="38566-114">Pour générer des classes C# qui prennent en charge la liaison de données</span><span class="sxs-lookup"><span data-stu-id="38566-114">To generate C# classes that support data binding</span></span>

- <span data-ttu-id="38566-115">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="38566-115">At the command prompt, execute the following command without line breaks:</span></span>

    ```console
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /dataservicecollection /version:2.0 /language:CSharp /out:Northwind.cs /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  <span data-ttu-id="38566-116">Vous devez remplacer la valeur fournie au paramètre `/uri:` par l'URI de l'instance de votre exemple de service de données Northwind .</span><span class="sxs-lookup"><span data-stu-id="38566-116">You must replace the value supplied to the `/uri:` parameter with the URI of your instance of the Northwind sample data service.</span></span>

### <a name="to-generate-visual-basic-classes-that-support-data-binding"></a><span data-ttu-id="38566-117">Pour générer des classes Visual Basic qui prennent en charge la liaison de données</span><span class="sxs-lookup"><span data-stu-id="38566-117">To generate Visual Basic classes that support data binding</span></span>

- <span data-ttu-id="38566-118">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="38566-118">At the command prompt, execute the following command without line breaks:</span></span>

    ```console
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /dataservicecollection /version:2.0 /language:VB /out:Northwind.vb /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  <span data-ttu-id="38566-119">Vous devez remplacer la valeur fournie au paramètre `/uri:` par l'URI de l'instance de votre exemple de service de données Northwind .</span><span class="sxs-lookup"><span data-stu-id="38566-119">You must replace value supplied to the `/uri:` parameter with the URI of your instance of the Northwind sample data service.</span></span>

### <a name="to-generate-c-classes-based-on-the-service-uri"></a><span data-ttu-id="38566-120">Pour générer des classes C# basées sur l'URI de service</span><span class="sxs-lookup"><span data-stu-id="38566-120">To generate C# classes based on the service URI</span></span>

- <span data-ttu-id="38566-121">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="38566-121">At the command prompt, execute the following command without line breaks:</span></span>

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /language:CSharp /out:northwind.cs /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  <span data-ttu-id="38566-122">Vous devez remplacer la valeur fournie au paramètre `/uri:` par l'URI de l'instance de votre exemple de service de données Northwind .</span><span class="sxs-lookup"><span data-stu-id="38566-122">You must replace the value supplied to the `/uri:` parameter with the URI of your instance of the Northwind sample data service.</span></span>

### <a name="to-generate-visual-basic-classes-based-on-the-service-uri"></a><span data-ttu-id="38566-123">Pour générer des classes Visual Basic basées sur l'URI de service</span><span class="sxs-lookup"><span data-stu-id="38566-123">To generate Visual Basic classes based on the service URI</span></span>

- <span data-ttu-id="38566-124">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="38566-124">At the command prompt, execute the following command without line breaks:</span></span>

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /out:Northwind.vb /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  <span data-ttu-id="38566-125">Vous devez remplacer la valeur fournie au paramètre `/uri:` par l'URI de l'instance de votre exemple de service de données Northwind .</span><span class="sxs-lookup"><span data-stu-id="38566-125">You must replace value supplied to the `/uri:` parameter with the URI of your instance of the Northwind sample data service.</span></span>

### <a name="to-generate-c-classes-based-on-the-conceptual-model-file-csdl"></a><span data-ttu-id="38566-126">Pour générer des classes C# basées sur le fichier de modèle conceptuel (CSDL)</span><span class="sxs-lookup"><span data-stu-id="38566-126">To generate C# classes based on the conceptual model file (CSDL)</span></span>

- <span data-ttu-id="38566-127">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="38566-127">At the command prompt, execute the following command without line breaks:</span></span>

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:CSharp /in:Northwind.csdl /out:Northwind.cs
    ```

### <a name="to-generate-visual-basic-classes-based-on-the-conceptual-model-file-csdl"></a><span data-ttu-id="38566-128">Pour générer des classes Visual Basic basées sur le fichier de modèle conceptuel (CSDL)</span><span class="sxs-lookup"><span data-stu-id="38566-128">To generate Visual Basic classes based on the conceptual model file (CSDL)</span></span>

- <span data-ttu-id="38566-129">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="38566-129">At the command prompt, execute the following command without line breaks:</span></span>

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /in:Northwind.csdl /out:Northwind.vb
    ```

### <a name="to-generate-c-classes-based-on-the-edmx-file"></a><span data-ttu-id="38566-130">Pour générer des classes C# basées sur le fichier .edmx</span><span class="sxs-lookup"><span data-stu-id="38566-130">To generate C# classes based on the .edmx file</span></span>

- <span data-ttu-id="38566-131">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="38566-131">At the command prompt, execute the following command without line breaks:</span></span>

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:CSharp /in:Northwind.edmx /out:c:\northwind.cs
    ```

### <a name="to-generate-visual-basic-classes-based-on-the-edmx-file"></a><span data-ttu-id="38566-132">Pour générer des classes Visual Basic basées sur le fichier .edmx</span><span class="sxs-lookup"><span data-stu-id="38566-132">To generate Visual Basic classes based on the .edmx file</span></span>

- <span data-ttu-id="38566-133">À l'invite de commandes, exécutez la commande suivante sans saut de ligne :</span><span class="sxs-lookup"><span data-stu-id="38566-133">At the command prompt, execute the following command without line breaks:</span></span>

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /in:Northwind.edmx /out:c:\northwind.vb
    ```

## <a name="see-also"></a><span data-ttu-id="38566-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38566-134">See also</span></span>

- [<span data-ttu-id="38566-135">Génération de la bibliothèque cliente du service de données</span><span class="sxs-lookup"><span data-stu-id="38566-135">Generating the Data Service Client Library</span></span>](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md)
- [<span data-ttu-id="38566-136">Guide pratique pour Ajouter une référence de Service de données</span><span class="sxs-lookup"><span data-stu-id="38566-136">How to: Add a Data Service Reference</span></span>](../../../../docs/framework/data/wcf/how-to-add-a-data-service-reference-wcf-data-services.md)
- [<span data-ttu-id="38566-137">Utilitaire client des services de données WCF (DataSvcUtil.exe)</span><span class="sxs-lookup"><span data-stu-id="38566-137">WCF Data Service Client Utility (DataSvcUtil.exe)</span></span>](../../../../docs/framework/data/wcf/wcf-data-service-client-utility-datasvcutil-exe.md)