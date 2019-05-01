---
title: 'Procédure : dimensionner un contrôle Label Windows Forms pour qu’il s’ajuste à son contenu'
ms.date: 03/30/2017
helpviewer_keywords:
- captions [Windows Forms], sizing
- sizing controls
- size [Windows Forms], controls
- labels [Windows Forms], sizing to fit contents
- Label control [Windows Forms], sizing to fit contents
ms.assetid: 99648964-63b2-438c-980e-d24103ad602b
ms.openlocfilehash: 110aab0c0826bb4b06e22158afd6af37b5406be4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61971195"
---
# <a name="how-to-size-a-windows-forms-label-control-to-fit-its-contents"></a><span data-ttu-id="3a522-102">Procédure : dimensionner un contrôle Label Windows Forms pour qu’il s’ajuste à son contenu</span><span class="sxs-lookup"><span data-stu-id="3a522-102">How to: Size a Windows Forms Label Control to Fit Its Contents</span></span>
<span data-ttu-id="3a522-103">Les formulaires Windows <xref:System.Windows.Forms.Label> contrôle peut être une ou plusieurs lignes, et il peut être soit de taille fixe ou que vous pouvez redimensionner automatiquement pour prendre en charge sa légende.</span><span class="sxs-lookup"><span data-stu-id="3a522-103">The Windows Forms <xref:System.Windows.Forms.Label> control can be single-line or multi-line, and it can be either fixed in size or can automatically resize itself to accommodate its caption.</span></span> <span data-ttu-id="3a522-104">Le <xref:System.Windows.Forms.Label.AutoSize%2A> propriété vous permet de dimensionner les contrôles pour s’ajuster à la taille des légendes, ce qui est particulièrement utile si la changer au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3a522-104">The <xref:System.Windows.Forms.Label.AutoSize%2A> property helps you size the controls to fit larger or smaller captions, which is particularly useful if the caption will change at run time.</span></span>  
  
### <a name="to-make-a-label-control-resize-dynamically-to-fit-its-contents"></a><span data-ttu-id="3a522-105">Pour rendre un contrôle label redimensionné dynamiquement pour s’ajuster à son contenu</span><span class="sxs-lookup"><span data-stu-id="3a522-105">To make a label control resize dynamically to fit its contents</span></span>  
  
1. <span data-ttu-id="3a522-106">Définissez ses <xref:System.Windows.Forms.Label.AutoSize%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="3a522-106">Set its <xref:System.Windows.Forms.Label.AutoSize%2A> property to `true`.</span></span>  
  
 <span data-ttu-id="3a522-107">Si <xref:System.Windows.Forms.Label.AutoSize%2A> a la valeur `false`, les mots spécifiés dans le <xref:System.Windows.Forms.Label.Text%2A> propriété passe à la ligne suivante si possible, mais le contrôle n’augmentera pas.</span><span class="sxs-lookup"><span data-stu-id="3a522-107">If <xref:System.Windows.Forms.Label.AutoSize%2A> is set to `false`, the words specified in the <xref:System.Windows.Forms.Label.Text%2A> property will wrap to the next line if possible, but the control will not grow.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a522-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a522-108">See also</span></span>

- [<span data-ttu-id="3a522-109">Guide pratique pour Créer des clés d’accès avec les contrôles Label Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3a522-109">How to: Create Access Keys with Windows Forms Label Controls</span></span>](how-to-create-access-keys-with-windows-forms-label-controls.md)
- [<span data-ttu-id="3a522-110">Vue d'ensemble du contrôle Label</span><span class="sxs-lookup"><span data-stu-id="3a522-110">Label Control Overview</span></span>](label-control-overview-windows-forms.md)
- [<span data-ttu-id="3a522-111">Label, contrôle</span><span class="sxs-lookup"><span data-stu-id="3a522-111">Label Control</span></span>](label-control-windows-forms.md)
