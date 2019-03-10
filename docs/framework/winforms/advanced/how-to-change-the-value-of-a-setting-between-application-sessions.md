---
title: 'Procédure : Modifiez la valeur d’un paramètre entre des Sessions d’Application'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], changing
- application settings [Windows Forms], between application sessions
ms.assetid: 1a85911f-97b2-476c-930b-83379edd890c
ms.openlocfilehash: c1626cea581e5c180665d0ce805dea3e67f27a05
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57714357"
---
# <a name="how-to-change-the-value-of-a-setting-between-application-sessions"></a><span data-ttu-id="80d67-102">Procédure : Modifiez la valeur d’un paramètre entre des Sessions d’Application</span><span class="sxs-lookup"><span data-stu-id="80d67-102">How To: Change the Value of a Setting Between Application Sessions</span></span>
<span data-ttu-id="80d67-103">Dans certains cas, vous souhaiterez modifier la valeur d’un paramètre entre des sessions d’application une fois que l’application a été compilée et déployée.</span><span class="sxs-lookup"><span data-stu-id="80d67-103">At times, you might want to change the value of a setting between application sessions after the application has been compiled and deployed.</span></span> <span data-ttu-id="80d67-104">Par exemple, vous souhaiterez peut-être modifier une chaîne de connexion pour pointer vers l’emplacement de la base de données correcte.</span><span class="sxs-lookup"><span data-stu-id="80d67-104">For example, you might want to change a connection string to point to the correct database location.</span></span> <span data-ttu-id="80d67-105">Dans la mesure où les outils de conception ne sont pas disponibles une fois que l’application a été compilée et déployée, vous devez modifier la valeur du paramètre manuellement dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="80d67-105">Since design-time tools are not available after the application has been compiled and deployed, you must change the setting value manually in the file.</span></span>  
  
### <a name="to-change-the-value-of-a-setting-between-application-sessions"></a><span data-ttu-id="80d67-106">Pour modifier la valeur d’un paramètre entre des Sessions d’Application</span><span class="sxs-lookup"><span data-stu-id="80d67-106">To Change the Value of a Setting Between Application Sessions</span></span>  
  
1.  <span data-ttu-id="80d67-107">À l’aide de Microsoft Notepad ou un autre texte ou éditeur XML, ouvrez le fichier .config associé à votre application.</span><span class="sxs-lookup"><span data-stu-id="80d67-107">Using Microsoft Notepad or some other text or XML editor, open the .config file associated with your application.</span></span>  
  
2.  <span data-ttu-id="80d67-108">Recherchez l’entrée pour le paramètre que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="80d67-108">Locate the entry for the setting you want to change.</span></span> <span data-ttu-id="80d67-109">Il doit ressembler à l’exemple présenté ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="80d67-109">It should look similar to the example presented below.</span></span>  
  
    ```xml  
    <setting name="Setting1" serializeAs="String" >  
       <value>My Setting Value</value>  
    </setting>  
    ```  
  
3.  <span data-ttu-id="80d67-110">Tapez une nouvelle valeur pour votre paramètre et enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="80d67-110">Type a new value for your setting and save the file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="80d67-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80d67-111">See also</span></span>
- [<span data-ttu-id="80d67-112">Utilisation de paramètres d'application et de paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="80d67-112">Using Application Settings and User Settings</span></span>](using-application-settings-and-user-settings.md)
- [<span data-ttu-id="80d67-113">Vue d'ensemble des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="80d67-113">Application Settings Overview</span></span>](application-settings-overview.md)
