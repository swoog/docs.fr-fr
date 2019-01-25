---
title: 'Procédure : Utiliser EdmGen.exe pour valider les fichiers de modèle et mappage'
ms.date: 03/30/2017
ms.assetid: 2641906a-971a-4d0b-8aee-13fabc02a1cc
ms.openlocfilehash: 87150aee8eac6a594b18b77230889c1208003dde
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54566357"
---
# <a name="how-to-use-edmgenexe-to-validate-model-and-mapping-files"></a>Procédure : Utiliser EdmGen.exe pour valider les fichiers de modèle et mappage
Cette rubrique montre comment utiliser le [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) outil pour valider le modèle et les fichiers de mappage. Pour plus d’informations, consultez [Entity Data Model](../../../../../docs/framework/data/adonet/entity-data-model.md).  
  
### <a name="to-validate-the-school-model-using-edmgenexe"></a>Pour valider le modèle School à l'aide d'EdmGen.exe  
  
1.  Créez la base de données School. Pour plus d’informations, consultez [création de la base de données School](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).  
  
2.  Générez le modèle School. Pour plus d'informations, voir [Procédure : Utiliser EdmGen.exe pour générer des fichiers de modèle et mappage](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).  
  
3.  À l'invite de commandes, exécutez la commande suivante sans saut de ligne :  
  
    ```console
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:ValidateArtifacts /inssdl:.\School.ssdl /inmsl:.\School.msl /incsdl:.\School.csdl  
    ```  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Configurer manuellement un projet Entity Framework](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e)
- [Outils ADO.NET Entity Data Model](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)
- [Guide pratique pour Prégénérer des vues pour améliorer les performances de requête](https://msdn.microsoft.com/library/b18a9d16-e10b-4043-ba91-b632f85a2579)
- [Guide pratique pour Utiliser EdmGen.exe pour générer le Code de couche objet](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-object-layer-code.md)
