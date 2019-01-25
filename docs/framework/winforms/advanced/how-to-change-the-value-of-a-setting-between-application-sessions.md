---
title: 'Procédure : Modifiez la valeur d’un paramètre entre des Sessions d’Application'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], changing
- application settings [Windows Forms], between application sessions
ms.assetid: 1a85911f-97b2-476c-930b-83379edd890c
ms.openlocfilehash: 475e57e8bfdd5f3296c6af0fb20a472c729ea75c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54540713"
---
# <a name="how-to-change-the-value-of-a-setting-between-application-sessions"></a><span data-ttu-id="75ca1-102">Procédure : Modifiez la valeur d’un paramètre entre des Sessions d’Application</span><span class="sxs-lookup"><span data-stu-id="75ca1-102">How To: Change the Value of a Setting Between Application Sessions</span></span>
<span data-ttu-id="75ca1-103">Dans certains cas, vous souhaiterez modifier la valeur d’un paramètre entre des sessions d’application une fois que l’application a été compilée et déployée.</span><span class="sxs-lookup"><span data-stu-id="75ca1-103">At times, you might want to change the value of a setting between application sessions after the application has been compiled and deployed.</span></span> <span data-ttu-id="75ca1-104">Par exemple, vous souhaiterez peut-être modifier une chaîne de connexion pour pointer vers l’emplacement de la base de données correcte.</span><span class="sxs-lookup"><span data-stu-id="75ca1-104">For example, you might want to change a connection string to point to the correct database location.</span></span> <span data-ttu-id="75ca1-105">Dans la mesure où les outils de conception ne sont pas disponibles une fois que l’application a été compilée et déployée, vous devez modifier la valeur du paramètre manuellement dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="75ca1-105">Since design-time tools are not available after the application has been compiled and deployed, you must change the setting value manually in the file.</span></span>  
  
### <a name="to-change-the-value-of-a-setting-between-application-sessions"></a><span data-ttu-id="75ca1-106">Pour modifier la valeur d’un paramètre entre des Sessions d’Application</span><span class="sxs-lookup"><span data-stu-id="75ca1-106">To Change the Value of a Setting Between Application Sessions</span></span>  
  
1.  <span data-ttu-id="75ca1-107">À l’aide de Microsoft Notepad ou un autre texte ou éditeur XML, ouvrez le fichier .config associé à votre application.</span><span class="sxs-lookup"><span data-stu-id="75ca1-107">Using Microsoft Notepad or some other text or XML editor, open the .config file associated with your application.</span></span>  
  
2.  <span data-ttu-id="75ca1-108">Recherchez l’entrée pour le paramètre que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="75ca1-108">Locate the entry for the setting you want to change.</span></span> <span data-ttu-id="75ca1-109">Il doit ressembler à l’exemple présenté ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="75ca1-109">It should look similar to the example presented below.</span></span>  
  
    ```xml  
    <setting name="Setting1" serializeAs="String" >  
       <value>My Setting Value</value>  
    </setting>  
    ```  
  
3.  <span data-ttu-id="75ca1-110">Tapez une nouvelle valeur pour votre paramètre et enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="75ca1-110">Type a new value for your setting and save the file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75ca1-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75ca1-111">See also</span></span>
- [<span data-ttu-id="75ca1-112">Utilisation de paramètres d'application et de paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="75ca1-112">Using Application Settings and User Settings</span></span>](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)
- [<span data-ttu-id="75ca1-113">Vue d'ensemble des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="75ca1-113">Application Settings Overview</span></span>](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
