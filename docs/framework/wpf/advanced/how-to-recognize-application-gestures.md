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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59191508"
---
# <a name="how-to-recognize-application-gestures"></a><span data-ttu-id="bbe12-102">Procédure : Reconnaître les mouvements d’application</span><span class="sxs-lookup"><span data-stu-id="bbe12-102">How To: Recognize Application Gestures</span></span>
<span data-ttu-id="bbe12-103">L’exemple suivant montre comment effacer l’encre lorsqu’un utilisateur apporte une <xref:System.Windows.Ink.ApplicationGesture.ScratchOut> de mouvements sur un <xref:System.Windows.Controls.InkCanvas>.</span><span class="sxs-lookup"><span data-stu-id="bbe12-103">The following example demonstrates how to erase ink when a user makes a <xref:System.Windows.Ink.ApplicationGesture.ScratchOut> gesture on an <xref:System.Windows.Controls.InkCanvas>.</span></span> <span data-ttu-id="bbe12-104">Cet exemple suppose un <xref:System.Windows.Controls.InkCanvas>, appelé `inkCanvas1`, est déclaré dans le fichier XAML.</span><span class="sxs-lookup"><span data-stu-id="bbe12-104">This example assumes an <xref:System.Windows.Controls.InkCanvas>, called `inkCanvas1`, is declared in the XAML file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bbe12-105">Exemple</span><span class="sxs-lookup"><span data-stu-id="bbe12-105">Example</span></span>  
 [!code-csharp[HowToRecognizeGestures#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToRecognizeGestures/CSharp/Window1.xaml.cs#1)]
 [!code-vb[HowToRecognizeGestures#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToRecognizeGestures/VisualBasic/Window1.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="bbe12-106">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbe12-106">See also</span></span>

- <xref:System.Windows.Ink.ApplicationGesture>
- <xref:System.Windows.Controls.InkCanvas>
- <xref:System.Windows.Controls.InkCanvas.Gesture>
