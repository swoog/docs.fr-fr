---
title: 'Procédure : modifier la valeur d’un paramètre entre des sessions d’application'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], changing
- application settings [Windows Forms], between application sessions
ms.assetid: 1a85911f-97b2-476c-930b-83379edd890c
ms.openlocfilehash: 95e613cb280813cd75d887d3cf147d7c897bc2e6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59318887"
---
# <a name="how-to-change-the-value-of-a-setting-between-application-sessions"></a>Procédure : modifier la valeur d’un paramètre entre des sessions d’application
Dans certains cas, vous souhaiterez modifier la valeur d’un paramètre entre des sessions d’application une fois que l’application a été compilée et déployée. Par exemple, vous souhaiterez peut-être modifier une chaîne de connexion pour pointer vers l’emplacement de la base de données correcte. Dans la mesure où les outils de conception ne sont pas disponibles une fois que l’application a été compilée et déployée, vous devez modifier la valeur du paramètre manuellement dans le fichier.  
  
### <a name="to-change-the-value-of-a-setting-between-application-sessions"></a>Pour modifier la valeur d’un paramètre entre des Sessions d’Application  
  
1. À l’aide de Microsoft Notepad ou un autre texte ou éditeur XML, ouvrez le fichier .config associé à votre application.  
  
2. Recherchez l’entrée pour le paramètre que vous souhaitez modifier. Il doit ressembler à l’exemple présenté ci-dessous.  
  
    ```xml  
    <setting name="Setting1" serializeAs="String" >  
       <value>My Setting Value</value>  
    </setting>  
    ```  
  
3. Tapez une nouvelle valeur pour votre paramètre et enregistrez le fichier.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de paramètres d'application et de paramètres utilisateur](using-application-settings-and-user-settings.md)
- [Vue d'ensemble des paramètres d'application](application-settings-overview.md)
