---
title: 'Procédure : Utiliser EdmGen.exe pour générer le code de couche objet'
ms.date: 03/30/2017
ms.assetid: c44d2ebe-f66f-42cb-9741-4a3f0c2dcffb
ms.openlocfilehash: 8a39027ee6a5647bbd645f5a38e35d61f7ebbd8e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61605767"
---
# <a name="how-to-use-edmgenexe-to-generate-object-layer-code"></a>Procédure : Utiliser EdmGen.exe pour générer le code de couche objet
Cette rubrique montre comment utiliser le [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) outil pour générer le code de couche objet basée sur le fichier .csdl.  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-visual-basic-project-using-edmgenexe"></a>Pour générer le code de couche objet pour le modèle School à l'aide d'EdmGen.exe dans le cadre d'un projet Visual Basic  
  
1. Créez la base de données School. Pour plus d’informations, consultez [création de la base de données School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).  
  
2. Générez le modèle School ou obtenez le fichier School.csdl. Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).  
  
3. À l'invite de commandes, exécutez la commande suivante sans saut de ligne :  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.vb /language:VB  
    ```  
  
### <a name="to-generate-object-layer-code-for-the-school-model-for-a-c-project-using-edmgenexe"></a>Pour générer le code de couche objet pour le modèle School à l'aide d'EdmGen.exe dans le cadre d'un projet C#  
  
1. Créez la base de données School. Pour plus d’informations, consultez [création de la base de données School](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399731(v=vs.100)).  
  
2. Générez le modèle School ou obtenez le fichier School.csdl. Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).  
  
3. À l'invite de commandes, exécutez la commande suivante sans saut de ligne :  
  
    ```  
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:EntityClassGeneration   
    /incsdl:.\School.csdl /outobjectlayer:.\School.Objects.cs /language:CSharp  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Modélisation et mappage](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md)
- [Guide pratique pour Configurer manuellement un projet Entity Framework](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb738546(v=vs.100))
- [Outils ADO.NET Entity Data Model](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb399249(v=vs.100))
- [Guide pratique pour Prégénérer des vues pour améliorer les performances de requête](https://docs.microsoft.com/previous-versions/dotnet/netframework-4.0/bb896240(v=vs.100))
- [Guide pratique pour Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md)
