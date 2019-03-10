---
title: 'Procédure : Créer une zone de texte en lecture seule (Windows Forms)'
ms.date: 03/30/2017
helpviewer_keywords:
- TextBox control [Windows Forms], read-only
- read-only text boxes
- text boxes [Windows Forms], read-only
ms.assetid: 60baa9ab-fa57-44ad-bb7c-61b05aa64296
ms.openlocfilehash: 0a29e1c4dcb0bcc8e7d292725e64ea967e160d06
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57707753"
---
# <a name="how-to-create-a-read-only-text-box-windows-forms"></a><span data-ttu-id="c62a0-102">Procédure : Créer une zone de texte en lecture seule (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="c62a0-102">How to: Create a Read-Only Text Box (Windows Forms)</span></span>
<span data-ttu-id="c62a0-103">Vous pouvez transformer une zone de texte modifiable Windows Forms en un contrôle en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c62a0-103">You can transform an editable Windows Forms text box into a read-only control.</span></span> <span data-ttu-id="c62a0-104">Par exemple, la zone de texte peut afficher une valeur qui est généralement de modification, mais ne peut pas être actuellement, en raison de l’état de l’application.</span><span class="sxs-lookup"><span data-stu-id="c62a0-104">For example, the text box may display a value that is usually edited but may not be currently, due to the state of the application.</span></span>  
  
### <a name="to-create-a-read-only-text-box"></a><span data-ttu-id="c62a0-105">Pour créer une zone de texte en lecture seule</span><span class="sxs-lookup"><span data-stu-id="c62a0-105">To create a read-only text box</span></span>  
  
1.  <span data-ttu-id="c62a0-106">Définir le <xref:System.Windows.Forms.TextBox> du contrôle <xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="c62a0-106">Set the <xref:System.Windows.Forms.TextBox> control's <xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A> property to `true`.</span></span> <span data-ttu-id="c62a0-107">Avec la propriété définie sur `true`, les utilisateurs peuvent toujours faire défiler et mettre en surbrillance du texte dans une zone de texte sans autoriser de modification.</span><span class="sxs-lookup"><span data-stu-id="c62a0-107">With the property set to `true`, users can still scroll and highlight text in a text box without allowing changes.</span></span> <span data-ttu-id="c62a0-108">Un **copie** commande est fonctionnelle dans une zone de texte, mais **couper** et **coller** commandes ne sont pas.</span><span class="sxs-lookup"><span data-stu-id="c62a0-108">A **Copy** command is functional in a text box, but **Cut** and **Paste** commands are not.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="c62a0-109">Le <xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A> propriété affecte uniquement l’interaction utilisateur au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="c62a0-109">The <xref:System.Windows.Forms.TextBoxBase.ReadOnly%2A> property only affects user interaction at run time.</span></span> <span data-ttu-id="c62a0-110">Vous pouvez toujours modifier contenu de zone de texte par programmation au moment de l’exécution en modifiant le <xref:System.Windows.Forms.TextBox.Text%2A> propriété de la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="c62a0-110">You can still change text box contents programmatically at run time by changing the <xref:System.Windows.Forms.TextBox.Text%2A> property of the text box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c62a0-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c62a0-111">See also</span></span>
- <xref:System.Windows.Forms.TextBox>
- [<span data-ttu-id="c62a0-112">Vue d’ensemble du contrôle TextBox</span><span class="sxs-lookup"><span data-stu-id="c62a0-112">TextBox Control Overview</span></span>](textbox-control-overview-windows-forms.md)
- [<span data-ttu-id="c62a0-113">Guide pratique pour Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c62a0-113">How to: Control the Insertion Point in a Windows Forms TextBox Control</span></span>](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [<span data-ttu-id="c62a0-114">Guide pratique pour Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c62a0-114">How to: Create a Password Text Box with the Windows Forms TextBox Control</span></span>](how-to-create-a-password-text-box-with-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="c62a0-115">Guide pratique pour Placez des guillemets doubles dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="c62a0-115">How to: Put Quotation Marks in a String</span></span>](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [<span data-ttu-id="c62a0-116">Guide pratique pour Sélectionner du texte dans le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c62a0-116">How to: Select Text in the Windows Forms TextBox Control</span></span>](how-to-select-text-in-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="c62a0-117">Guide pratique pour Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c62a0-117">How to: View Multiple Lines in the Windows Forms TextBox Control</span></span>](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="c62a0-118">TextBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="c62a0-118">TextBox Control</span></span>](textbox-control-windows-forms.md)
