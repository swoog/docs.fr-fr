---
title: 'Procédure : Déterminer la touche a été activée.'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- keyboard input
- shift keys
- events [Windows Forms], mouse
- Keys.ControlKey enumeration member
- keys [Windows Forms], control keys
- user input [Windows Forms], checking for keyboard
- keys [Windows Forms], determining last pressed
- keys [Windows Forms], shift keys
- keys [Windows Forms], modifier keys
- control keys
- keys [Windows Forms], alt keys
- alt keys
- Keys.Shift enumeration member
- events [Windows Forms], keyboard
- keyboards [Windows Forms], keyboard input
- Keys.Alt enumeration member
- modifier keys
ms.assetid: 1e184048-0ae3-4067-a200-d4ba31dbc2cb
ms.openlocfilehash: de8af53bbf065047541e030de7a174987e5785df
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57715982"
---
# <a name="how-to-determine-which-modifier-key-was-pressed"></a>Procédure : Déterminer la touche a été activée.
Lorsque vous créez une application qui accepte des séquences de touches de l’utilisateur, vous souhaiterez également analyser les touches de modification telles que les touches MAJ, ALT et CTRL. Lorsqu’une touche de modification est enfoncée en combinaison avec d’autres clés, ou avec les clics de souris, votre application peut réagir de façon appropriée. Par exemple, si l’utilisateur appuie sur la lettre S, cela peut entraîner tout simplement d’un « s » à l’écran, mais si les touches CTRL + S sont utilisées, le document actuel peut être enregistré. Si vous gérez le <xref:System.Windows.Forms.Control.KeyDown> événement, le <xref:System.Windows.Forms.KeyEventArgs.Modifiers%2A> propriété de la <xref:System.Windows.Forms.KeyEventArgs> reçu par l’événement gestionnaire spécifie les touches de modification sont enfoncées. Vous pouvez également le <xref:System.Windows.Forms.KeyEventArgs.KeyData%2A> propriété du <xref:System.Windows.Forms.KeyEventArgs> Spécifie le caractère qui a été enfoncé, ainsi que les touches de modification combinées avec une opération OR au niveau du bit. Toutefois, si vous gérez le <xref:System.Windows.Forms.Control.KeyPress> événement ou un événement de souris, le Gestionnaire d’événements ne reçoit pas ces informations. Dans ce cas, vous devez utiliser le <xref:System.Windows.Forms.Control.ModifierKeys%2A> propriété de la <xref:System.Windows.Forms.Control> classe. Dans les deux cas, vous devez effectuer une opération AND au niveau du bit d’approprié <xref:System.Windows.Forms.Keys> valeur et la valeur que vous testez. Le <xref:System.Windows.Forms.Keys> énumération offre des variations de chaque touche de modification, il est donc important d’effectuer l’opération de bits et avec la valeur correcte. Par exemple, la touche MAJ est représenté par <xref:System.Windows.Forms.Keys.Shift>, <xref:System.Windows.Forms.Keys.ShiftKey>, <xref:System.Windows.Forms.Keys.RShiftKey> et <xref:System.Windows.Forms.Keys.LShiftKey> la valeur correcte pour tester, MAJ comme une touche de modification est <xref:System.Windows.Forms.Keys.Shift>. De même, pour tester CTRL et ALT en tant que modificateurs vous devez utiliser le <xref:System.Windows.Forms.Keys.Control> et <xref:System.Windows.Forms.Keys.Alt> des valeurs, respectivement.  
  
> [!NOTE]
>  Les programmeurs Visual Basic peuvent également accéder à des informations de clé par le biais du <xref:Microsoft.VisualBasic.Devices.Computer.Keyboard%2A> propriété  
  
### <a name="to-determine-which-modifier-key-was-pressed"></a>Pour déterminer la touche a été activée.  
  
-   Utilisez l’opérateur de bits `AND` opérateur avec la <xref:System.Windows.Forms.Control.ModifierKeys%2A> propriété et une valeur de la <xref:System.Windows.Forms.Keys> énumération pour déterminer si une touche de modification particulière est enfoncée. L’exemple de code suivant montre comment déterminer si la touche MAJ est activée dans un <xref:System.Windows.Forms.Control.KeyPress> Gestionnaire d’événements.  
  
     [!code-cpp[System.Windows.Forms.DetermineModifierKey#5](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DetermineModifierKey/cpp/form1.cpp#5)]
     [!code-csharp[System.Windows.Forms.DetermineModifierKey#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DetermineModifierKey/CS/form1.cs#5)]
     [!code-vb[System.Windows.Forms.DetermineModifierKey#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DetermineModifierKey/VB/form1.vb#5)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.Keys>
- <xref:System.Windows.Forms.Control.ModifierKeys%2A>
- [Entrée au clavier dans une application Windows Forms](keyboard-input-in-a-windows-forms-application.md)
- [Guide pratique pour Déterminer que si CapsLock est activée dans Visual Basic](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/9c9d1fz9(v=vs.100))
