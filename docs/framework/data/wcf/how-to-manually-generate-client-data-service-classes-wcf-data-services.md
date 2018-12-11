---
title: 'Procédure : Générer manuellement les Classes de Service de données Client (WCF Data Services)'
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, configuring
- WCF Data Services, client library
ms.assetid: b98cb1d6-956a-4e50-add6-67e4f2587346
ms.openlocfilehash: fbf3a3a2ee52df95780f715e1358a042eb7dd02c
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53128659"
---
# <a name="how-to-manually-generate-client-data-service-classes-wcf-data-services"></a>Procédure : Générer manuellement les Classes de Service de données Client (WCF Data Services)
WCF Data Services s’intègre à Visual Studio pour vous permettre de générer automatiquement des classes de service de données client lorsque vous utilisez le **ajouter une référence de Service** boîte de dialogue pour ajouter une référence à un service de données dans un projet Visual Studio. Pour plus d'informations, voir [Procédure : Ajouter une référence de Service de données](../../../../docs/framework/data/wcf/how-to-add-a-data-service-reference-wcf-data-services.md). Vous pouvez également générer manuellement les mêmes classes de service de données client en utilisant l'outil de génération de code, `DataSvcUtil.exe`. Cet outil, qui est inclus avec WCF Data Services, génère des classes .NET Framework à partir de la définition de service de données. Il peut également être utilisé pour générer des classes de service des données depuis le fichier de modèle conceptuel (.csdl) et depuis le fichier .edmx qui représente un modèle Entity Framework dans un projet Visual Studio.

 L'exemple dans cette rubrique crée des classes de service de données client basées sur l'exemple de service de données Northwind. Ce service est créé lorsque vous effectuez la [démarrage rapide WCF Data Services](../../../../docs/framework/data/wcf/quickstart-wcf-data-services.md). Certains exemples dans cette rubrique requièrent le fichier modèle conceptuel pour le modèle Northwind. Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md). Certains exemples dans cette rubrique requièrent le fichier .edmx pour le modèle Northwind. Pour plus d’informations, consultez [présentation d’un fichier .edmx](https://msdn.microsoft.com/library/f4c8e7ce-1db6-417e-9759-15f8b55155d4).

### <a name="to-generate-c-classes-that-support-data-binding"></a>Pour générer des classes C# qui prennent en charge la liaison de données

-   À l'invite de commandes, exécutez la commande suivante sans saut de ligne :

    ```console
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /dataservicecollection /version:2.0 /language:CSharp /out:Northwind.cs /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  Vous devez remplacer la valeur fournie au paramètre `/uri:` par l'URI de l'instance de votre exemple de service de données Northwind .

### <a name="to-generate-visual-basic-classes-that-support-data-binding"></a>Pour générer des classes Visual Basic qui prennent en charge la liaison de données

-   À l'invite de commandes, exécutez la commande suivante sans saut de ligne :

    ```console
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /dataservicecollection /version:2.0 /language:VB /out:Northwind.vb /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  Vous devez remplacer la valeur fournie au paramètre `/uri:` par l'URI de l'instance de votre exemple de service de données Northwind .

### <a name="to-generate-c-classes-based-on-the-service-uri"></a>Pour générer des classes C# basées sur l'URI de service

-   À l'invite de commandes, exécutez la commande suivante sans saut de ligne :

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\DataSvcUtil.exe" /language:CSharp /out:northwind.cs /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  Vous devez remplacer la valeur fournie au paramètre `/uri:` par l'URI de l'instance de votre exemple de service de données Northwind .

### <a name="to-generate-visual-basic-classes-based-on-the-service-uri"></a>Pour générer des classes Visual Basic basées sur l'URI de service

-   À l'invite de commandes, exécutez la commande suivante sans saut de ligne :

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /out:Northwind.vb /uri:http://localhost:12345/Northwind.svc
    ```

    > [!NOTE]
    >  Vous devez remplacer la valeur fournie au paramètre `/uri:` par l'URI de l'instance de votre exemple de service de données Northwind .

### <a name="to-generate-c-classes-based-on-the-conceptual-model-file-csdl"></a>Pour générer des classes C# basées sur le fichier de modèle conceptuel (CSDL)

-   À l'invite de commandes, exécutez la commande suivante sans saut de ligne :

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:CSharp /in:Northwind.csdl /out:Northwind.cs
    ```

### <a name="to-generate-visual-basic-classes-based-on-the-conceptual-model-file-csdl"></a>Pour générer des classes Visual Basic basées sur le fichier de modèle conceptuel (CSDL)

-   À l'invite de commandes, exécutez la commande suivante sans saut de ligne :

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /in:Northwind.csdl /out:Northwind.vb
    ```

### <a name="to-generate-c-classes-based-on-the-edmx-file"></a>Pour générer des classes C# basées sur le fichier .edmx

-   À l'invite de commandes, exécutez la commande suivante sans saut de ligne :

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:CSharp /in:Northwind.edmx /out:c:\northwind.cs
    ```

### <a name="to-generate-visual-basic-classes-based-on-the-edmx-file"></a>Pour générer des classes Visual Basic basées sur le fichier .edmx

-   À l'invite de commandes, exécutez la commande suivante sans saut de ligne :

    ```
    "%windir%\Microsoft.NET\Framework\v3.5\datasvcutil.exe" /language:VB /in:Northwind.edmx /out:c:\northwind.vb
    ```

## <a name="see-also"></a>Voir aussi

- [Génération de la bibliothèque cliente du service de données](../../../../docs/framework/data/wcf/generating-the-data-service-client-library-wcf-data-services.md)
- [Comment : Ajouter une référence de Service de données](../../../../docs/framework/data/wcf/how-to-add-a-data-service-reference-wcf-data-services.md)
- [Utilitaire client des services de données WCF (DataSvcUtil.exe)](../../../../docs/framework/data/wcf/wcf-data-service-client-utility-datasvcutil-exe.md)