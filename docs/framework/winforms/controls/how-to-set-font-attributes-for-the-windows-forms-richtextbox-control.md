---
title: 'Procédure : définir des attributs de police pour le contrôle RichTextBox Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- .rtf files [Windows Forms], formatting in RichTextBox control
- fonts [Windows Forms], changing attributes in RichTextBox control
- RTF files [Windows Forms], formatting in RichTextBox control
- RichTextBox control [Windows Forms], setting font attributes
- text [Windows Forms]
- text boxes [Windows Forms], formatting text
- formatting [Windows Forms]
ms.assetid: 2bc23ddb-0529-4489-a1a2-ad253cb43f9a
ms.openlocfilehash: a6fe5b30c457fae2d53c946092b214f492fe5e9b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62013268"
---
# <a name="how-to-set-font-attributes-for-the-windows-forms-richtextbox-control"></a><span data-ttu-id="28738-102">Procédure : définir des attributs de police pour le contrôle RichTextBox Windows Forms</span><span class="sxs-lookup"><span data-stu-id="28738-102">How to: Set Font Attributes for the Windows Forms RichTextBox Control</span></span>
<span data-ttu-id="28738-103">Les formulaires Windows <xref:System.Windows.Forms.RichTextBox> contrôle a de nombreuses options pour mettre en forme le texte affiché.</span><span class="sxs-lookup"><span data-stu-id="28738-103">The Windows Forms <xref:System.Windows.Forms.RichTextBox> control has numerous options for formatting the text it displays.</span></span> <span data-ttu-id="28738-104">Vous pouvez afficher les caractères sélectionnés en gras, italique ou en souligné, à l’aide de la <xref:System.Windows.Forms.RichTextBox.SelectionFont%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="28738-104">You can make the selected characters bold, underlined, or italic, using the <xref:System.Windows.Forms.RichTextBox.SelectionFont%2A> property.</span></span> <span data-ttu-id="28738-105">Vous pouvez également utiliser cette propriété pour changer la taille et la police des caractères sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="28738-105">You can also use this property to change the size and typeface of the selected characters.</span></span> <span data-ttu-id="28738-106">Le <xref:System.Windows.Forms.RichTextBox.SelectionColor%2A> propriété permet de modifier la couleur des caractères sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="28738-106">The <xref:System.Windows.Forms.RichTextBox.SelectionColor%2A> property enables you to change the selected characters' color.</span></span>  
  
### <a name="to-change-the-appearance-of-characters"></a><span data-ttu-id="28738-107">Pour changer l’apparence de caractères</span><span class="sxs-lookup"><span data-stu-id="28738-107">To change the appearance of characters</span></span>  
  
1. <span data-ttu-id="28738-108">Définir le <xref:System.Windows.Forms.RichTextBox.SelectionFont%2A> propriété à une police appropriée.</span><span class="sxs-lookup"><span data-stu-id="28738-108">Set the <xref:System.Windows.Forms.RichTextBox.SelectionFont%2A> property to an appropriate font.</span></span>  
  
     <span data-ttu-id="28738-109">Pour permettre aux utilisateurs de définir la famille de polices, la taille et le type de caractères dans une application, vous utiliserez généralement le <xref:System.Windows.Forms.FontDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="28738-109">To enable users to set the font family, size, and typeface in an application, you would typically use the <xref:System.Windows.Forms.FontDialog> component.</span></span> <span data-ttu-id="28738-110">Pour une vue d’ensemble, consultez [Vue d’ensemble du composant FontDialog](fontdialog-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="28738-110">For an overview, see [FontDialog Component Overview](fontdialog-component-overview-windows-forms.md).</span></span>  
  
2. <span data-ttu-id="28738-111">Définir le <xref:System.Windows.Forms.RichTextBox.SelectionColor%2A> propriété sur une couleur appropriée.</span><span class="sxs-lookup"><span data-stu-id="28738-111">Set the <xref:System.Windows.Forms.RichTextBox.SelectionColor%2A> property to an appropriate color.</span></span>  
  
     <span data-ttu-id="28738-112">Pour permettre aux utilisateurs de définir la couleur dans une application, vous utiliserez généralement le <xref:System.Windows.Forms.ColorDialog> composant.</span><span class="sxs-lookup"><span data-stu-id="28738-112">To enable users to set the color in an application, you would typically use the <xref:System.Windows.Forms.ColorDialog> component.</span></span> <span data-ttu-id="28738-113">Pour une vue d’ensemble, consultez [Vue d’ensemble du composant ColorDialog](colordialog-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="28738-113">For an overview, see [ColorDialog Component Overview](colordialog-component-overview-windows-forms.md).</span></span>  
  
    ```vb  
    RichTextBox1.SelectionFont = New Font("Tahoma", 12, FontStyle.Bold)  
    RichTextBox1.SelectionColor = System.Drawing.Color.Red  
    ```  
  
    ```csharp  
    richTextBox1.SelectionFont = new Font("Tahoma", 12, FontStyle.Bold);  
    richTextBox1.SelectionColor = System.Drawing.Color.Red;  
    ```  
  
    ```cpp  
    richTextBox1->SelectionFont =  
       gcnew System::Drawing::Font("Tahoma", 12, FontStyle::Bold);  
    richTextBox1->SelectionColor = System::Drawing::Color::Red;  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="28738-114">Ces propriétés affectent uniquement le texte sélectionné ou, si aucun texte n’est sélectionné, le texte tapé à l’emplacement actif du point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="28738-114">These properties only affect selected text, or, if no text is selected, the text that is typed at the current location of the insertion point.</span></span> <span data-ttu-id="28738-115">Pour plus d’informations sur la sélection de texte par programmation, consultez <xref:System.Windows.Forms.TextBoxBase.Select%2A>.</span><span class="sxs-lookup"><span data-stu-id="28738-115">For information on selecting text programmatically, see <xref:System.Windows.Forms.TextBoxBase.Select%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28738-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28738-116">See also</span></span>

- <xref:System.Windows.Forms.RichTextBox>
- [<span data-ttu-id="28738-117">RichTextBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="28738-117">RichTextBox Control</span></span>](richtextbox-control-windows-forms.md)
- [<span data-ttu-id="28738-118">Contrôles à utiliser dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="28738-118">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
