---
title: Un formulaire de démarrage n'a pas été spécifié
ms.date: 07/20/2015
f1_keywords:
- vbrAppModel_NoStartupForm
ms.assetid: 8e04af49-4bef-49de-a7ec-e407e9873da7
ms.openlocfilehash: 699d20e6afb2335336b3652be5907f0dd72299fa
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586784"
---
# <a name="a-startup-form-has-not-been-specified"></a><span data-ttu-id="274cc-102">Un formulaire de démarrage n'a pas été spécifié</span><span class="sxs-lookup"><span data-stu-id="274cc-102">A startup form has not been specified</span></span>
<span data-ttu-id="274cc-103">L’application utilise la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase> classe mais ne spécifie pas le formulaire de démarrage.</span><span class="sxs-lookup"><span data-stu-id="274cc-103">The application uses the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase> class but does not specify the startup form.</span></span>  
  
 <span data-ttu-id="274cc-104">Cela peut se produire si le **activer l’infrastructure d’application** case à cocher est activée dans le Concepteur de projet mais le **du formulaire de démarrage** n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="274cc-104">This can occur if the **Enable application framework** check box is selected in the project designer but the **Startup form** is not specified.</span></span> <span data-ttu-id="274cc-105">Pour plus d’informations, consultez [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="274cc-105">For more information, see [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="274cc-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="274cc-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="274cc-107">Spécifiez un objet de démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="274cc-107">Specify a startup object for the application.</span></span>  
  
     <span data-ttu-id="274cc-108">Pour plus d’informations, consultez [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="274cc-108">For more information, see [Application Page, Project Designer (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).</span></span>  
  
2.  <span data-ttu-id="274cc-109">Remplacer la <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A> pour définir le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A> propriété à l’écran de démarrage.</span><span class="sxs-lookup"><span data-stu-id="274cc-109">Override the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A> method to set the <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A> property to the startup form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="274cc-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="274cc-110">See Also</span></span>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A>  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A>  
 [<span data-ttu-id="274cc-111">Vue d’ensemble du modèle d’application Visual Basic</span><span class="sxs-lookup"><span data-stu-id="274cc-111">Overview of the Visual Basic Application Model</span></span>](../../../visual-basic/developing-apps/development-with-my/overview-of-the-visual-basic-application-model.md)
