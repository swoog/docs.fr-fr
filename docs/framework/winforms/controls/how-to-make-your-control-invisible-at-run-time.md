---
title: 'Procédure : rendre votre contrôle invisible au moment de l’exécution'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], making invisible at run time
- invisible controls
- user controls [Windows Forms], invisible
- custom controls [Windows Forms], invisible
- run time [Windows Forms], making controls invisible
ms.assetid: 69eb2e72-32f5-4f79-a157-c2c5f60c1628
ms.openlocfilehash: 06283a93c3b88d2febc1d64797139eee62661b42
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59201648"
---
# <a name="how-to-make-your-control-invisible-at-run-time"></a>Procédure : rendre votre contrôle invisible au moment de l’exécution
Il est parfois lorsque vous souhaiterez créer un contrôle utilisateur qui est invisible au moment de l’exécution. Par exemple, un contrôle réveil peut être invisible, sauf lorsque l’alarme sonne. Cela est facilement réalisable en définissant le <xref:System.Windows.Forms.Control.Visible%2A> propriété. Si le <xref:System.Windows.Forms.Control.Visible%2A> propriété est `true`, votre contrôle apparaît comme d’habitude. Si `false`, votre contrôle sera masqué. Bien que le code de votre contrôle peut-être toujours s’exécuter bien qu’invisible, vous ne serez pas en mesure d’interagir avec le contrôle via l’interface utilisateur. Si vous souhaitez créer un contrôle invisible qui continue de répondre aux entrées utilisateur (par exemple, les clics de souris), vous devez créer un contrôle transparent. Pour plus d’informations, consultez [affectation un arrière-plan Transparent à votre contrôle](how-to-give-your-control-a-transparent-background.md).  
  
### <a name="to-make-your-control-invisible-at-run-time"></a>Pour rendre votre contrôle invisible au moment de l’exécution  
  
1.  Affectez à la propriété <xref:System.Windows.Forms.Control.Visible%2A> la valeur `false`.  
  
    ```vb  
    ' To set the Visible property from within your object's own code.  
    Me.Visible = False  
    ' To set the Visible property from another object.  
    myControl1.Visible = False  
    ```  
  
    ```csharp  
    // To set the Visible property from within your object's own code.  
    this.Visible = false;  
    // To set the Visible property from another object.  
    myControl1.Visible = false;  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Control.Visible%2A>
- [Développement de contrôles Windows Forms personnalisés avec le .NET Framework](developing-custom-windows-forms-controls.md)
- [Procédure : donner à votre contrôle un arrière-plan transparent](how-to-give-your-control-a-transparent-background.md)
