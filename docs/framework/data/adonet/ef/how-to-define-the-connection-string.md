---
title: 'Comment : définir la chaîne de connexion'
ms.date: 03/30/2017
ms.assetid: 6027335d-4e26-420d-9151-6523289b1989
ms.openlocfilehash: f40b8bc68eda1cb4b64b34d12b2922da69929203
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43802159"
---
# <a name="how-to-define-the-connection-string"></a>Comment : définir la chaîne de connexion
Cette rubrique montre comment définir la chaîne utilisée pour la connexion à un modèle conceptuel. Cette rubrique est basée sur le [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) modèle conceptuel. Le modèle de vente AdventureWorks Sales Model est utilisé dans toutes les rubriques liées aux tâches de la documentation [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Cette rubrique suppose que vous avez déjà configuré le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] et défini le modèle AdventureWorks Sales Model. Pour plus d’informations, consultez [Comment : définir manuellement les fichiers de modèle et mappage](https://msdn.microsoft.com/library/d4fd6864-f2a1-48f0-aa32-1e318775a99a). Les procédures décrites dans cette rubrique sont également incluses dans [Comment : configurer manuellement un projet Entity Framework](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e).  
  
> [!NOTE]
>  Si vous utilisez le [!INCLUDE[adonet_edm](../../../../../includes/adonet-edm-md.md)] Assistant dans un projet Visual Studio, il génère automatiquement un fichier .edmx et configure le projet pour utiliser le [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]. Pour plus d’informations, consultez [Comment : utiliser l’Assistant Entity Data Model](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d)  
  
### <a name="to-define-the-entity-framework-connection-string"></a>Pour définir la chaîne de connexion Entity Framework  
  
-   Ouvrez le fichier de configuration de l'application (app.config) du projet et ajoutez la chaîne de connexion suivante :  
  
  
  
     Si votre projet n’a pas d’un fichier de configuration d’application, vous pouvez en ajouter un en sélectionnant **ajouter un nouvel élément** à partir de la **projet** menu, en sélectionnant le **général** catégorie, en sélectionnant **fichier de Configuration d’Application**, puis en cliquant sur **ajouter**.  
  
## <a name="see-also"></a>Voir aussi  
 [Démarrage rapide](https://msdn.microsoft.com/library/0bc534be-789f-4819-b9f6-76e51d961675)  
 [Comment : créer un fichier .edmx](https://msdn.microsoft.com/library/beb8189e-e51c-4051-839c-9902c224abf2)  
 [Outils ADO.NET Entity Data Model](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)
