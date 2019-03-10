---
title: TextBox, contrôle (Windows Forms)
ms.date: 03/30/2017
helpviewer_keywords:
- text boxes
- TextBox control [Windows Forms]
ms.assetid: e5a06987-8aec-4271-b196-2245ba992d62
ms.openlocfilehash: b687f83562b3a6f9dd5993f2af1c55ffe6dc8042
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716312"
---
# <a name="textbox-control-windows-forms"></a><span data-ttu-id="b28ec-102">TextBox, contrôle (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="b28ec-102">TextBox Control (Windows Forms)</span></span>
<span data-ttu-id="b28ec-103">Les zones de texte Windows Forms sont utilisés pour obtenir des données à partir de l’utilisateur ou pour afficher le texte.</span><span class="sxs-lookup"><span data-stu-id="b28ec-103">Windows Forms text boxes are used to get input from the user or to display text.</span></span> <span data-ttu-id="b28ec-104">Le `TextBox` contrôle est généralement utilisé pour le texte modifiable, bien qu’il peut également être en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b28ec-104">The `TextBox` control is generally used for editable text, although it can also be made read-only.</span></span> <span data-ttu-id="b28ec-105">Zones de texte peuvent afficher plusieurs lignes, habiller le texte à la taille du contrôle et ajouter une mise en forme.</span><span class="sxs-lookup"><span data-stu-id="b28ec-105">Text boxes can display multiple lines, wrap text to the size of the control, and add basic formatting.</span></span> <span data-ttu-id="b28ec-106">Le `TextBox` contrôle permet à un seul format de texte affiché ou entré dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b28ec-106">The `TextBox` control allows a single format for text displayed or entered in the control.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b28ec-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b28ec-107">In This Section</span></span>  
 [<span data-ttu-id="b28ec-108">Vue d’ensemble du contrôle TextBox</span><span class="sxs-lookup"><span data-stu-id="b28ec-108">TextBox Control Overview</span></span>](textbox-control-overview-windows-forms.md)  
 <span data-ttu-id="b28ec-109">Décrit un contrôle et ses principales fonctionnalités et propriétés.</span><span class="sxs-lookup"><span data-stu-id="b28ec-109">Explains what this control is and its key features and properties.</span></span>  
  
 [<span data-ttu-id="b28ec-110">Guide pratique pour Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b28ec-110">How to: Control the Insertion Point in a Windows Forms TextBox Control</span></span>](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)  
 <span data-ttu-id="b28ec-111">Explique comment spécifier où le point d’insertion apparaît lorsqu’un contrôle d’édition obtient d’abord le focus.</span><span class="sxs-lookup"><span data-stu-id="b28ec-111">Gives directions for specifying where the insertion point appears when an edit control first gets the focus.</span></span>  
  
 [<span data-ttu-id="b28ec-112">Guide pratique pour Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b28ec-112">How to: Create a Password Text Box with the Windows Forms TextBox Control</span></span>](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)  
 <span data-ttu-id="b28ec-113">Explique comment masquer la valeur tapée dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="b28ec-113">Explains how to conceal what is typed into a text box.</span></span>  
  
 [<span data-ttu-id="b28ec-114">Guide pratique pour Créer une zone de texte en lecture seule</span><span class="sxs-lookup"><span data-stu-id="b28ec-114">How to: Create a Read-Only Text Box</span></span>](how-to-create-a-read-only-text-box-windows-forms.md)  
 <span data-ttu-id="b28ec-115">Décrit comment empêcher que le contenu d’une zone de texte en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="b28ec-115">Describes how to prevent the contents of a text box from being changed.</span></span>  
  
 [<span data-ttu-id="b28ec-116">Guide pratique pour Placez des guillemets doubles dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="b28ec-116">How to: Put Quotation Marks in a String</span></span>](how-to-put-quotation-marks-in-a-string-windows-forms.md)  
 <span data-ttu-id="b28ec-117">Explique les guillemets ajout à une chaîne dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="b28ec-117">Explains adding quotation marks to a string in a text box.</span></span>  
  
 [<span data-ttu-id="b28ec-118">Guide pratique pour Sélectionner du texte dans le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b28ec-118">How to: Select Text in the Windows Forms TextBox Control</span></span>](how-to-select-text-in-the-windows-forms-textbox-control.md)  
 <span data-ttu-id="b28ec-119">Explique comment mettre en surbrillance du texte dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="b28ec-119">Explains how to highlight text in a text box.</span></span>  
  
 [<span data-ttu-id="b28ec-120">Guide pratique pour Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b28ec-120">How to: View Multiple Lines in the Windows Forms TextBox Control</span></span>](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)  
 <span data-ttu-id="b28ec-121">Décrit comment créer une zone de texte à défilement.</span><span class="sxs-lookup"><span data-stu-id="b28ec-121">Describes how to make a text box scrollable.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="b28ec-122">Référence</span><span class="sxs-lookup"><span data-stu-id="b28ec-122">Reference</span></span>  
 <span data-ttu-id="b28ec-123">Classe <xref:System.Windows.Forms.TextBox></span><span class="sxs-lookup"><span data-stu-id="b28ec-123"><xref:System.Windows.Forms.TextBox> class</span></span>  
 <span data-ttu-id="b28ec-124">Décrit cette classe et fournit des liens vers tous ses membres.</span><span class="sxs-lookup"><span data-stu-id="b28ec-124">Describes this class and has links to all its members.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="b28ec-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b28ec-125">Related Sections</span></span>  
 [<span data-ttu-id="b28ec-126">Contrôles à utiliser dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b28ec-126">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)  
 <span data-ttu-id="b28ec-127">Fournit une liste complète de contrôles Windows Forms, avec des liens vers des informations sur leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="b28ec-127">Provides a complete list of Windows Forms controls, with links to information on their use.</span></span>
