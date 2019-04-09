---
title: 'Procédure : donner à votre contrôle un arrière-plan transparent'
ms.date: 03/30/2017
helpviewer_keywords:
- transparent backgrounds [Windows Forms], custom controls
- custom controls [Windows Forms], transparent background
- transparency [Windows Forms], Windows Forms custom controls
ms.assetid: 32433e63-f4e9-4305-9857-6de3edeb944a
ms.openlocfilehash: 671075973793d7fbf0b70ce77428a0a632305b9c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59206094"
---
# <a name="how-to-give-your-control-a-transparent-background"></a><span data-ttu-id="be6a4-102">Procédure : donner à votre contrôle un arrière-plan transparent</span><span class="sxs-lookup"><span data-stu-id="be6a4-102">How to: Give Your Control a Transparent Background</span></span>
<span data-ttu-id="be6a4-103">Dans les versions antérieures de .NET Framework, les contrôles ne prenaient pas en charge la définition de couleurs d’arrière-plan transparentes sans définition préalable de la méthode <xref:System.Windows.Forms.Control.SetStyle%2A> dans le constructeur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="be6a4-103">In earlier versions of the .NET Framework, controls didn't support setting transparent backcolors without first setting the <xref:System.Windows.Forms.Control.SetStyle%2A> method in the forms's constructor.</span></span> <span data-ttu-id="be6a4-104">Dans la version actuelle de l’infrastructure, vous pouvez affecter <xref:System.Drawing.Color.Transparent%2A> comme couleur d’arrière-plan de la plupart des contrôles  dans la fenêtre **Propriétés** au moment du design ou dans le code dans le constructeur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="be6a4-104">In the current framework version, the backcolor for most controls can be set to <xref:System.Drawing.Color.Transparent%2A> in the **Properties** window at design time, or in code in the form's constructor.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="be6a4-105">Les contrôles Windows Forms ne prennent pas en charge la véritable transparence.</span><span class="sxs-lookup"><span data-stu-id="be6a4-105">Windows Forms controls do not support true transparency.</span></span> <span data-ttu-id="be6a4-106">L’arrière-plan d’un contrôle Windows Forms transparent est peint par son parent.</span><span class="sxs-lookup"><span data-stu-id="be6a4-106">The background of a transparent Windows Forms control is painted by its parent.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="be6a4-107">Le contrôle <xref:System.Windows.Controls.Button> ne prend pas en charge une couleur d’arrière-plan transparente même quand la propriété <xref:System.Windows.Forms.ButtonBase.BackColor%2A> a la valeur <xref:System.Drawing.Color.Transparent%2A>.</span><span class="sxs-lookup"><span data-stu-id="be6a4-107">The <xref:System.Windows.Controls.Button> control doesn't support a transparent backcolor even when the <xref:System.Windows.Forms.ButtonBase.BackColor%2A> property is set to <xref:System.Drawing.Color.Transparent%2A>.</span></span>  
  
### <a name="to-give-your-control-a-transparent-backcolor"></a><span data-ttu-id="be6a4-108">Pour affecter un arrière-plan transparent à votre contrôle</span><span class="sxs-lookup"><span data-stu-id="be6a4-108">To give your control a transparent backcolor</span></span>  
  
-   <span data-ttu-id="be6a4-109">Dans la fenêtre Propriétés, choisissez le <xref:System.Windows.Forms.ButtonBase.BackColor%2A> propriété et affectez-lui la valeur</span><span class="sxs-lookup"><span data-stu-id="be6a4-109">In the Properties window, choose the <xref:System.Windows.Forms.ButtonBase.BackColor%2A> property and set it to</span></span> <xref:System.Drawing.Color.Transparent%2A>  
  
## <a name="see-also"></a><span data-ttu-id="be6a4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be6a4-110">See also</span></span>

- <xref:System.Drawing.Color.FromArgb%2A>
- [<span data-ttu-id="be6a4-111">Développement de contrôles Windows Forms personnalisés avec le .NET Framework</span><span class="sxs-lookup"><span data-stu-id="be6a4-111">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](developing-custom-windows-forms-controls.md)
- [<span data-ttu-id="be6a4-112">Utilisation de classes graphiques managées</span><span class="sxs-lookup"><span data-stu-id="be6a4-112">Using Managed Graphics Classes</span></span>](../advanced/using-managed-graphics-classes.md)
- [<span data-ttu-id="be6a4-113">Procédure : dessiner des lignes opaques et translucides</span><span class="sxs-lookup"><span data-stu-id="be6a4-113">How to: Draw Opaque and Semitransparent Lines</span></span>](../advanced/how-to-draw-opaque-and-semitransparent-lines.md)
