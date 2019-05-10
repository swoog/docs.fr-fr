---
title: 'Procédure pas à pas : exécution de tâches courantes à l’aide de balises actives dans les contrôles Windows Forms'
ms.date: 03/30/2017
helpviewer_keywords:
- DesignerAction object model
- smart tags
- designer actions
ms.assetid: cac337e6-00f6-4584-80f4-75728f5ea113
ms.openlocfilehash: 1cc854d735ba88a301d6e2f6a83fe5c8bf881380
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65211415"
---
# <a name="walkthrough-performing-common-tasks-using-smart-tags-on-windows-forms-controls"></a><span data-ttu-id="442fb-102">Procédure pas à pas : exécution de tâches courantes à l’aide de balises actives dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="442fb-102">Walkthrough: Performing Common Tasks Using Smart Tags on Windows Forms Controls</span></span>

<span data-ttu-id="442fb-103">Lorsque vous construisez des formulaires et contrôles pour votre application Windows Forms, il existe de nombreuses tâches que vous allez effectuer à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="442fb-103">As you construct forms and controls for your Windows Forms application, there are many tasks you will perform repeatedly.</span></span> <span data-ttu-id="442fb-104">Il existe quelques tâches courantes que vous rencontrerez :</span><span class="sxs-lookup"><span data-stu-id="442fb-104">These are some of the commonly performed tasks you will encounter:</span></span>

- <span data-ttu-id="442fb-105">Ajout ou suppression d’un onglet sur un <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="442fb-105">Adding or removing a tab on a <xref:System.Windows.Forms.TabControl>.</span></span>

- <span data-ttu-id="442fb-106">Ancrage d’un contrôle à son parent.</span><span class="sxs-lookup"><span data-stu-id="442fb-106">Docking a control to its parent.</span></span>

- <span data-ttu-id="442fb-107">Modification de l’orientation d’un <xref:System.Windows.Forms.SplitContainer> contrôle.</span><span class="sxs-lookup"><span data-stu-id="442fb-107">Changing the orientation of a <xref:System.Windows.Forms.SplitContainer> control.</span></span>

<span data-ttu-id="442fb-108">Pour accélérer le développement, de nombreux contrôles offrent des balises actives, qui sont des menus contextuels qui vous permettent d’effectuer des tâches courantes comme celles-ci en un seul geste au moment du design.</span><span class="sxs-lookup"><span data-stu-id="442fb-108">To speed development, many controls offer smart tags, which are context-sensitive menus that allow you to perform common tasks like these in a single gesture at design time.</span></span> <span data-ttu-id="442fb-109">Ces tâches sont appelées *verbes de balise active*.</span><span class="sxs-lookup"><span data-stu-id="442fb-109">These tasks are called *smart-tag verbs*.</span></span>

<span data-ttu-id="442fb-110">Balises actives restent attachées à une instance de contrôle pour sa durée de vie dans le concepteur et sont toujours disponibles.</span><span class="sxs-lookup"><span data-stu-id="442fb-110">Smart tags remain attached to a control instance for its lifetime in the designer and are always available.</span></span>

<span data-ttu-id="442fb-111">Cette procédure pas à pas décrit notamment les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="442fb-111">Tasks illustrated in this walkthrough include:</span></span>

- <span data-ttu-id="442fb-112">Création d’un projet Windows Forms</span><span class="sxs-lookup"><span data-stu-id="442fb-112">Creating a Windows Forms project</span></span>

- <span data-ttu-id="442fb-113">À l’aide de balises actives</span><span class="sxs-lookup"><span data-stu-id="442fb-113">Using smart tags</span></span>

- <span data-ttu-id="442fb-114">Activation et désactivation des balises actives</span><span class="sxs-lookup"><span data-stu-id="442fb-114">Enabling and Disabling Smart Tags</span></span>

<span data-ttu-id="442fb-115">À l’issue de cette procédure, vous comprendrez le rôle joué par ces fonctionnalités de disposition importantes.</span><span class="sxs-lookup"><span data-stu-id="442fb-115">When you are finished, you will have an understanding of the role played by these important layout features.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="442fb-116">Créer le projet</span><span class="sxs-lookup"><span data-stu-id="442fb-116">Create the project</span></span>

<span data-ttu-id="442fb-117">La première étape consiste à créer le projet et à configurer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="442fb-117">The first step is to create the project and set up the form.</span></span>

1. <span data-ttu-id="442fb-118">Dans Visual Studio, créez un projet d’application Windows appelé « SmartTagsExample » (**fichier** > **New** > **projet**  >  **Visual C#**  ou **Visual Basic** > **bureau classique** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="442fb-118">In Visual Studio, create a Windows-based application project called "SmartTagsExample" (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>

2. <span data-ttu-id="442fb-119">Sélectionnez le formulaire dans le **Windows Forms Designer**.</span><span class="sxs-lookup"><span data-stu-id="442fb-119">Select the form in the **Windows Forms Designer**.</span></span>

## <a name="use-smart-tags"></a><span data-ttu-id="442fb-120">Utiliser des balises actives</span><span class="sxs-lookup"><span data-stu-id="442fb-120">Use smart tags</span></span>

<span data-ttu-id="442fb-121">Balises actives sont toujours disponibles au moment du design sur les contrôles qui les proposent.</span><span class="sxs-lookup"><span data-stu-id="442fb-121">Smart tags are always available at design time on controls that offer them.</span></span>

1. <span data-ttu-id="442fb-122">Faites glisser un <xref:System.Windows.Forms.TabControl> à partir de la **boîte à outils** vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="442fb-122">Drag a <xref:System.Windows.Forms.TabControl> from the **Toolbox** onto your form.</span></span> <span data-ttu-id="442fb-123">Notez le glyphe de balise active (![glyphe de balise active](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) qui apparaît sur le côté du <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="442fb-123">Note the smart-tag glyph (![Smart Tag Glyph](./media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) that appears on the side of the <xref:System.Windows.Forms.TabControl>.</span></span>

2. <span data-ttu-id="442fb-124">Cliquez sur le glyphe de balise active.</span><span class="sxs-lookup"><span data-stu-id="442fb-124">Click the smart-tag glyph.</span></span> <span data-ttu-id="442fb-125">Dans le menu contextuel qui s’affiche en regard du glyphe, sélectionnez le **ajouter un onglet** élément.</span><span class="sxs-lookup"><span data-stu-id="442fb-125">In the shortcut menu that appears next to the glyph, select the **Add Tab** item.</span></span> <span data-ttu-id="442fb-126">Observez qu’une nouvelle page d’onglets est ajoutée à la <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="442fb-126">Observe that a new tab page is added to the <xref:System.Windows.Forms.TabControl>.</span></span>

3. <span data-ttu-id="442fb-127">Faites glisser un contrôle <xref:System.Windows.Forms.TableLayoutPanel> de la **boîte à outils** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="442fb-127">Drag a <xref:System.Windows.Forms.TableLayoutPanel> control from the **Toolbox** onto your form.</span></span>

4. <span data-ttu-id="442fb-128">Cliquez sur le glyphe de balise active.</span><span class="sxs-lookup"><span data-stu-id="442fb-128">Click the smart-tag glyph.</span></span> <span data-ttu-id="442fb-129">Dans le menu contextuel qui s’affiche en regard du glyphe, sélectionnez le **ajouter une colonne** élément.</span><span class="sxs-lookup"><span data-stu-id="442fb-129">In the shortcut menu that appears next to the glyph, select the **Add Column** item.</span></span> <span data-ttu-id="442fb-130">Observez qu’une nouvelle colonne est ajoutée à la <xref:System.Windows.Forms.TableLayoutPanel> contrôle.</span><span class="sxs-lookup"><span data-stu-id="442fb-130">Observe that a new column is added to the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

5. <span data-ttu-id="442fb-131">Faites glisser un contrôle <xref:System.Windows.Forms.SplitContainer> de la **boîte à outils** vers le formulaire.</span><span class="sxs-lookup"><span data-stu-id="442fb-131">Drag a <xref:System.Windows.Forms.SplitContainer> control from the **Toolbox** onto your form.</span></span>

6. <span data-ttu-id="442fb-132">Cliquez sur le glyphe de balise active.</span><span class="sxs-lookup"><span data-stu-id="442fb-132">Click the smart-tag glyph.</span></span> <span data-ttu-id="442fb-133">Dans le menu contextuel qui s’affiche en regard du glyphe, sélectionnez le **l’orientation du fractionnement Horizontal** élément.</span><span class="sxs-lookup"><span data-stu-id="442fb-133">In the shortcut menu that appears next to the glyph, select the **Horizontal splitter orientation** item.</span></span> <span data-ttu-id="442fb-134">Observez que le <xref:System.Windows.Forms.SplitContainer> barre de fractionnement du contrôle est maintenant orientée horizontalement.</span><span class="sxs-lookup"><span data-stu-id="442fb-134">Observe that the <xref:System.Windows.Forms.SplitContainer> control's splitter bar is now oriented horizontally.</span></span>

## <a name="see-also"></a><span data-ttu-id="442fb-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="442fb-135">See also</span></span>

- <xref:System.Windows.Forms.TextBox>
- <xref:System.Windows.Forms.TabControl>
- <xref:System.Windows.Forms.SplitContainer>
- <xref:System.ComponentModel.Design.DesignerActionList>
- <span data-ttu-id="442fb-136">[Procédure pas à pas : Ajout de balises actives à un composant de formulaires Windows](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171829(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="442fb-136">[Walkthrough: Adding Smart Tags to a Windows Forms Component](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/ms171829(v=vs.120))</span></span>
