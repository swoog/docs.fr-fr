---
title: 'Procédure : Reconnaître les mouvements d’application'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application gestures [WPF], recognizing
- gestures [WPF], recognizing
ms.assetid: d58b740f-5192-4a3e-af59-7aa162e6ca15
ms.openlocfilehash: 647e7c9c1d785cebfdc362dc48511d865f3945dc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59767433"
---
# <a name="how-to-recognize-application-gestures"></a><span data-ttu-id="0e849-102">Procédure : Reconnaître les mouvements d’application</span><span class="sxs-lookup"><span data-stu-id="0e849-102">How To: Recognize Application Gestures</span></span>
<span data-ttu-id="0e849-103">L’exemple suivant montre comment effacer l’encre lorsqu’un utilisateur apporte une <xref:System.Windows.Ink.ApplicationGesture.ScratchOut> de mouvements sur un <xref:System.Windows.Controls.InkCanvas>.</span><span class="sxs-lookup"><span data-stu-id="0e849-103">The following example demonstrates how to erase ink when a user makes a <xref:System.Windows.Ink.ApplicationGesture.ScratchOut> gesture on an <xref:System.Windows.Controls.InkCanvas>.</span></span> <span data-ttu-id="0e849-104">Cet exemple suppose un <xref:System.Windows.Controls.InkCanvas>, appelé `inkCanvas1`, est déclaré dans le fichier XAML.</span><span class="sxs-lookup"><span data-stu-id="0e849-104">This example assumes an <xref:System.Windows.Controls.InkCanvas>, called `inkCanvas1`, is declared in the XAML file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0e849-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="0e849-105">Example</span></span>  
 [!code-csharp[HowToRecognizeGestures#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToRecognizeGestures/CSharp/Window1.xaml.cs#1)]
 [!code-vb[HowToRecognizeGestures#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToRecognizeGestures/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="0e849-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e849-106">See also</span></span>

- <xref:System.Windows.Ink.ApplicationGesture>
- <xref:System.Windows.Controls.InkCanvas>
- <xref:System.Windows.Controls.InkCanvas.Gesture>
