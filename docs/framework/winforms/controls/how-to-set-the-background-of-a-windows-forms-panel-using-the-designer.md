---
title: 'Procédure : définir l’arrière-plan d’un panneau Windows Forms à l’aide du concepteur'
ms.date: 03/30/2017
helpviewer_keywords:
- background colors [Windows Forms], Windows Forms Panel controls
- background images [Windows Forms], Windows Forms Panel controls
- Panel control [Windows Forms], background
- colors [Windows Forms], Windows Forms Panel controls
ms.assetid: db83cf54-3c69-4b08-ac6c-25b9b5abb1b0
ms.openlocfilehash: 6927a7118c43ced03623a9764a3ef1e0814c95cb
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211643"
---
# <a name="how-to-set-the-background-of-a-windows-forms-panel-using-the-designer"></a><span data-ttu-id="ac1d9-102">Procédure : Définir l’arrière-plan d’un contrôle panel Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="ac1d9-102">How to: Set the background of a Windows Forms panel using the Designer</span></span>

<span data-ttu-id="ac1d9-103">Un formulaire Windows <xref:System.Windows.Forms.Panel> contrôle peut afficher une couleur d’arrière-plan et une image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-103">A Windows Forms <xref:System.Windows.Forms.Panel> control can display both a background color and a background image.</span></span> <span data-ttu-id="ac1d9-104">Le <xref:System.Windows.Forms.Control.BackColor%2A> propriété définit la couleur d’arrière-plan pour les contrôles qui sont contenus dans le panneau de configuration, tels que des étiquettes et cases d’option.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-104">The <xref:System.Windows.Forms.Control.BackColor%2A> property sets the background color for controls that are contained in the panel, such as labels and radio buttons.</span></span> <span data-ttu-id="ac1d9-105">Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété n’est pas définie, le <xref:System.Windows.Forms.Control.BackColor%2A> sélectionnée remplit tout le panneau.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-105">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is not set, the <xref:System.Windows.Forms.Control.BackColor%2A> selection will fill all of the panel.</span></span> <span data-ttu-id="ac1d9-106">Si le <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété est définie, l’image est affichée derrière les contrôles qui sont contenus dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-106">If the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property is set, the image will be displayed behind the controls that are contained in the panel.</span></span>

<span data-ttu-id="ac1d9-107">La procédure suivante nécessite un **Windows Application** projet avec un formulaire qui contient un <xref:System.Windows.Forms.Panel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-107">The following procedure requires a **Windows Application** project with a form that contains a <xref:System.Windows.Forms.Panel> control.</span></span> <span data-ttu-id="ac1d9-108">Pour plus d’informations sur la façon de configurer un tel projet dans Visual Studio, consultez [Comment : Créer un projet d’application Windows Forms](/visualstudio/ide/step-1-create-a-windows-forms-application-project) et [Comment : Ajouter des contrôles aux Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="ac1d9-108">For information about how to set up such a project in Visual Studio, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

## <a name="set-the-background-in-the-windows-forms-designer"></a><span data-ttu-id="ac1d9-109">Définir l’arrière-plan dans le Concepteur de formulaires Windows</span><span class="sxs-lookup"><span data-stu-id="ac1d9-109">Set the background in the Windows Forms Designer</span></span>

1. <span data-ttu-id="ac1d9-110">Ouvrez le projet dans Visual Studio et sélectionnez le <xref:System.Windows.Forms.Panel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-110">Open the project in Visual Studio and select the <xref:System.Windows.Forms.Panel> control.</span></span>

2. <span data-ttu-id="ac1d9-111">Dans le **propriétés** fenêtre, cliquez sur la flèche située en regard du <xref:System.Windows.Forms.Control.BackColor%2A> propriété pour afficher une fenêtre avec trois onglets.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-111">In the **Properties** window, click the arrow button next to the <xref:System.Windows.Forms.Control.BackColor%2A> property to display a window with three tabs.</span></span>

3. <span data-ttu-id="ac1d9-112">Sélectionnez le **personnalisé** onglet pour afficher une palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-112">Select the **Custom** tab to display a palette of colors.</span></span>

4. <span data-ttu-id="ac1d9-113">Sélectionnez le **Web** ou **système** onglet pour afficher une liste de noms de couleurs prédéfinis, puis sélectionnez une couleur.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-113">Select the **Web** or **System** tab to display a list of predefined names for colors, and then select a color.</span></span>

5. <span data-ttu-id="ac1d9-114">Dans le **propriétés** fenêtre, cliquez sur la flèche située en regard du <xref:System.Windows.Forms.Control.BackgroundImage%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-114">In the **Properties** window, click the arrow button next to the <xref:System.Windows.Forms.Control.BackgroundImage%2A> property.</span></span>

6. <span data-ttu-id="ac1d9-115">Dans le **Open** boîte de dialogue, sélectionnez le fichier que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="ac1d9-115">In the **Open** dialog box, select the file that you want to display.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac1d9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac1d9-116">See also</span></span>

- <xref:System.Windows.Forms.Control.BackColor%2A>
- <xref:System.Windows.Forms.Control.BackgroundImage%2A>
- [<span data-ttu-id="ac1d9-117">Panel, contrôle</span><span class="sxs-lookup"><span data-stu-id="ac1d9-117">Panel Control</span></span>](panel-control-windows-forms.md)
- [<span data-ttu-id="ac1d9-118">Vue d’ensemble du contrôle Panel</span><span class="sxs-lookup"><span data-stu-id="ac1d9-118">Panel Control Overview</span></span>](panel-control-overview-windows-forms.md)
- [<span data-ttu-id="ac1d9-119">Guide pratique pour Contrôles de groupe avec le contrôle de panneau Windows Forms à l’aide du Concepteur</span><span class="sxs-lookup"><span data-stu-id="ac1d9-119">How to: Group Controls with the Windows Forms Panel Control Using the Designer</span></span>](group-controls-with-wf-panel-control-using-the-designer.md)
