---
title: Un formulaire de démarrage n'a pas été spécifié
ms.date: 07/20/2015
f1_keywords:
- vbrAppModel_NoStartupForm
ms.assetid: 8e04af49-4bef-49de-a7ec-e407e9873da7
ms.openlocfilehash: f05358f76829768d8ff5c4ac85b5134f35254126
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54627211"
---
# <a name="a-startup-form-has-not-been-specified"></a>Un formulaire de démarrage n'a pas été spécifié
L’application utilise le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase> classe mais ne spécifie pas le formulaire de démarrage.  
  
 Cela peut se produire si le **activer l’infrastructure application** case à cocher est activée dans le Concepteur de projets, mais le **formulaire de démarrage** n’est pas spécifié. Pour plus d’informations, consultez [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Spécifiez un objet de démarrage de l’application.  
  
     Pour plus d’informations, consultez [Page Application, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/application-page-project-designer-visual-basic).  
  
2.  Remplacer le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A> méthode pour définir le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A> propriété vers le formulaire de démarrage.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OnCreateMainForm%2A>
- <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.MainForm%2A>
- [Vue d’ensemble du modèle d’application Visual Basic](../../../visual-basic/developing-apps/development-with-my/overview-of-the-visual-basic-application-model.md)
