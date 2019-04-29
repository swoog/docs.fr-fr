---
title: Applications d'interface multidocument (MDI, Multiple Document Interface)
ms.date: 03/30/2017
helpviewer_keywords:
- forms [Windows Forms], MDI
- windows [Windows Forms], mDI
- Windows Forms, MDI applications
- MDI
ms.assetid: 599faf75-13cf-49cc-ad3c-255545e5cb97
ms.openlocfilehash: 0ce7c66946d03d566b21473711cb6b3315885236
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61952046"
---
# <a name="multiple-document-interface-mdi-applications"></a><span data-ttu-id="0f4db-102">Applications d'interface multidocument (MDI, Multiple Document Interface)</span><span class="sxs-lookup"><span data-stu-id="0f4db-102">Multiple-Document Interface (MDI) Applications</span></span>
<span data-ttu-id="0f4db-103">Applications d’interface multidocument (MDI) permettent d’afficher plusieurs documents en même temps, chaque document affiché dans sa propre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0f4db-103">Multiple-document interface (MDI) applications enable you to display multiple documents at the same time, with each document displayed in its own window.</span></span> <span data-ttu-id="0f4db-104">Les applications MDI ont souvent un élément de menu Fenêtre avec les sous-menus pour basculer entre les fenêtres ou aux documents.</span><span class="sxs-lookup"><span data-stu-id="0f4db-104">MDI applications often have a Window menu item with submenus for switching between windows or documents.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0f4db-105">Il existe des différences de comportement entre des formulaires MDI et fenêtres d’interface monodocument (SDI) dans les Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="0f4db-105">There are some behavior differences between MDI forms and single-document interface (SDI) windows in Windows Forms.</span></span> <span data-ttu-id="0f4db-106">Le `Opacity` propriété n’affecte pas l’apparence des formulaires enfants MDI.</span><span class="sxs-lookup"><span data-stu-id="0f4db-106">The `Opacity` property does not affect the appearance of MDI child forms.</span></span> <span data-ttu-id="0f4db-107">En outre, le <xref:System.Windows.Forms.Form.CenterToParent%2A> méthode n’affecte pas le comportement des formulaires enfants MDI.</span><span class="sxs-lookup"><span data-stu-id="0f4db-107">Additionally, the <xref:System.Windows.Forms.Form.CenterToParent%2A> method does not affect the behavior of MDI child forms.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="0f4db-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="0f4db-108">In This Section</span></span>  
 [<span data-ttu-id="0f4db-109">Guide pratique pour Créer des formulaires MDI parents</span><span class="sxs-lookup"><span data-stu-id="0f4db-109">How to: Create MDI Parent Forms</span></span>](how-to-create-mdi-parent-forms.md)  
 <span data-ttu-id="0f4db-110">Explique comment créer le conteneur de plusieurs documents dans une application MDI.</span><span class="sxs-lookup"><span data-stu-id="0f4db-110">Gives directions for creating the container for the multiple documents within an MDI application.</span></span>  
  
 [<span data-ttu-id="0f4db-111">Guide pratique pour Créer des formulaires MDI enfants</span><span class="sxs-lookup"><span data-stu-id="0f4db-111">How to: Create MDI Child Forms</span></span>](how-to-create-mdi-child-forms.md)  
 <span data-ttu-id="0f4db-112">Fournit des instructions pour la création d’une ou plusieurs fenêtres qui opèrent au sein d’un formulaire MDI parent.</span><span class="sxs-lookup"><span data-stu-id="0f4db-112">Gives directions for creating one or more windows that operate within an MDI parent form.</span></span>  
  
 [<span data-ttu-id="0f4db-113">Guide pratique pour Déterminer l’enfant MDI actif</span><span class="sxs-lookup"><span data-stu-id="0f4db-113">How to: Determine the Active MDI Child</span></span>](how-to-determine-the-active-mdi-child.md)  
 <span data-ttu-id="0f4db-114">Explique comment déterminer la fenêtre enfant qui a le focus (et envoyer son contenu dans le Presse-papiers).</span><span class="sxs-lookup"><span data-stu-id="0f4db-114">Gives directions for verifying the child window that has focus (and sending its contents to the Clipboard).</span></span>  
  
 [<span data-ttu-id="0f4db-115">Guide pratique pour Envoyer des données à l’enfant MDI actif</span><span class="sxs-lookup"><span data-stu-id="0f4db-115">How to: Send Data to the Active MDI Child</span></span>](how-to-send-data-to-the-active-mdi-child.md)  
 <span data-ttu-id="0f4db-116">Explique comment transmettre des informations dans la fenêtre enfant active.</span><span class="sxs-lookup"><span data-stu-id="0f4db-116">Gives directions for transporting information to the active child window.</span></span>  
  
 [<span data-ttu-id="0f4db-117">Guide pratique pour Réorganiser des formulaires MDI enfants</span><span class="sxs-lookup"><span data-stu-id="0f4db-117">How to: Arrange MDI Child Forms</span></span>](how-to-arrange-mdi-child-forms.md)  
 <span data-ttu-id="0f4db-118">Explique comment la mosaïque, en cascade ou réorganiser les fenêtres enfants d’une application MDI.</span><span class="sxs-lookup"><span data-stu-id="0f4db-118">Gives directions for tiling, cascading, or arranging the child windows of an MDI application.</span></span>
