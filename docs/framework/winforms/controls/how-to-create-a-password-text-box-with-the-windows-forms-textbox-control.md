---
title: 'Procédure : Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TextBox control [Windows Forms], entering passwords
- password boxes [Windows Forms], creating
- PasswordChar property in text boxes
- passwords [Windows Forms], input mask
- passwords [Windows Forms], password text box
ms.assetid: d105d6b9-3d50-44cd-80d8-2c0e2f486727
ms.openlocfilehash: 93be2378e812ce909adaf9b640b37f8056fc09c3
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57710808"
---
# <a name="how-to-create-a-password-text-box-with-the-windows-forms-textbox-control"></a><span data-ttu-id="af82d-102">Procédure : Créer une zone de texte mot de passe avec le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="af82d-102">How to: Create a Password Text Box with the Windows Forms TextBox Control</span></span>
<span data-ttu-id="af82d-103">Une zone de mot de passe est une zone de texte Windows Forms qui affiche les caractères d’espace réservé pendant qu’un utilisateur tape une chaîne.</span><span class="sxs-lookup"><span data-stu-id="af82d-103">A password box is a Windows Forms text box that displays placeholder characters while a user types a string.</span></span>  
  
### <a name="to-create-a-password-text-box"></a><span data-ttu-id="af82d-104">Pour créer une zone de texte mot de passe</span><span class="sxs-lookup"><span data-stu-id="af82d-104">To create a password text box</span></span>  
  
1.  <span data-ttu-id="af82d-105">Définir le <xref:System.Windows.Forms.TextBox.PasswordChar%2A> propriété de la <xref:System.Windows.Forms.TextBox> contrôle à un caractère spécifique.</span><span class="sxs-lookup"><span data-stu-id="af82d-105">Set the <xref:System.Windows.Forms.TextBox.PasswordChar%2A> property of the <xref:System.Windows.Forms.TextBox> control to a specific character.</span></span>  
  
     <span data-ttu-id="af82d-106">Le <xref:System.Windows.Forms.TextBox.PasswordChar%2A> propriété spécifie le caractère affiché dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="af82d-106">The <xref:System.Windows.Forms.TextBox.PasswordChar%2A> property specifies the character displayed in the text box.</span></span> <span data-ttu-id="af82d-107">Par exemple, si vous souhaitez que des astérisques s’affichent dans la zone de mot de passe, spécifiez \* pour le <xref:System.Windows.Forms.TextBox.PasswordChar%2A> propriété dans la fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="af82d-107">For example, if you want asterisks displayed in the password box, specify \* for the <xref:System.Windows.Forms.TextBox.PasswordChar%2A> property in the Properties window.</span></span> <span data-ttu-id="af82d-108">Ensuite, indépendamment du caractère qu’un utilisateur tape dans la zone de texte, un astérisque est affiché.</span><span class="sxs-lookup"><span data-stu-id="af82d-108">Then, regardless of what character a user types in the text box, an asterisk is displayed.</span></span>  
  
2.  <span data-ttu-id="af82d-109">(Facultatif) Définir le <xref:System.Windows.Forms.TextBoxBase.MaxLength%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="af82d-109">(Optional) Set the <xref:System.Windows.Forms.TextBoxBase.MaxLength%2A> property.</span></span> <span data-ttu-id="af82d-110">La propriété détermine le nombre de caractères peut être tapé dans la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="af82d-110">The property determines how many characters can be typed in the text box.</span></span> <span data-ttu-id="af82d-111">Si la longueur maximale est dépassée, le système émet un signal sonore et la zone de texte n’accepte pas plus de caractères.</span><span class="sxs-lookup"><span data-stu-id="af82d-111">If the maximum length is exceeded, the system emits a beep and the text box does not accept any more characters.</span></span> <span data-ttu-id="af82d-112">Notez que vous ne pouvez pas effectuer cette opération car la longueur maximale d’un mot de passe peut-être être utiles aux pirates informatiques qui tentent de deviner le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="af82d-112">Note that you may not wish to do this as the maximum length of a password may be of use to hackers who are trying to guess the password.</span></span>  
  
     <span data-ttu-id="af82d-113">L’exemple de code suivant montre comment initialiser une zone de texte qui acceptent une chaîne de 14 caractères au maximum et affichera des astérisques à la place de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="af82d-113">The following code example shows how to initialize a text box that will accept a string up to 14 characters long and display asterisks in place of the string.</span></span> <span data-ttu-id="af82d-114">Le `InitializeMyControl` procédure s’exécutera pas automatiquement ; il doit être appelé.</span><span class="sxs-lookup"><span data-stu-id="af82d-114">The `InitializeMyControl` procedure will not execute automatically; it must be called.</span></span>  
  
    > [!IMPORTANT]
    >  <span data-ttu-id="af82d-115">À l’aide de la <xref:System.Windows.Forms.TextBox.PasswordChar%2A> propriété sur une zone de texte permet de garantir que les autres personnes ne sera pas en mesure de déterminer un mot de passe utilisateur observant l’entrer.</span><span class="sxs-lookup"><span data-stu-id="af82d-115">Using the <xref:System.Windows.Forms.TextBox.PasswordChar%2A> property on a text box can help ensure that other people will not be able to determine a user's password if they observe the user entering it.</span></span> <span data-ttu-id="af82d-116">Cette mesure de sécurité ne couvre pas une forme quelconque de stockage ou transmission du mot de passe qui peut se produire en raison de votre logique d’application.</span><span class="sxs-lookup"><span data-stu-id="af82d-116">This security measure does not cover any sort of storage or transmission of the password that can occur due to your application logic.</span></span> <span data-ttu-id="af82d-117">Étant donné que le texte entré n’est pas chiffré en aucune façon, vous devez le considérer comme vous le feriez pour d’autres données confidentielles.</span><span class="sxs-lookup"><span data-stu-id="af82d-117">Because the text entered is not encrypted in any way, you should treat it as you would any other confidential data.</span></span> <span data-ttu-id="af82d-118">Même si elle n’apparaît pas en tant que tel, le mot de passe est toujours traité comme une chaîne de texte brut (sauf si vous avez implémenté certaines mesures de sécurité supplémentaires).</span><span class="sxs-lookup"><span data-stu-id="af82d-118">Even though it does not appear as such, the password is still being treated as a plain-text string (unless you have implemented some additional security measure).</span></span>  
  
    ```vb  
    Private Sub InitializeMyControl()  
       ' Set to no text.  
       TextBox1.Text = ""  
       ' The password character is an asterisk.  
       TextBox1.PasswordChar = "*"  
       ' The control will allow no more than 14 characters.  
       TextBox1.MaxLength = 14  
    End Sub  
    ```  
  
    ```csharp  
    private void InitializeMyControl()  
    {  
       // Set to no text.  
       textBox1.Text = "";  
       // The password character is an asterisk.  
       textBox1.PasswordChar = '*';  
       // The control will allow no more than 14 characters.  
       textBox1.MaxLength = 14;  
    }  
    ```  
  
    ```cpp  
    private:  
       void InitializeMyControl()  
       {  
          // Set to no text.  
          textBox1->Text = "";  
          // The password character is an asterisk.  
          textBox1->PasswordChar = '*';  
          // The control will allow no more than 14 characters.  
          textBox1->MaxLength = 14;  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="af82d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af82d-119">See also</span></span>
- <xref:System.Windows.Forms.TextBox>
- [<span data-ttu-id="af82d-120">Vue d’ensemble du contrôle TextBox</span><span class="sxs-lookup"><span data-stu-id="af82d-120">TextBox Control Overview</span></span>](textbox-control-overview-windows-forms.md)
- [<span data-ttu-id="af82d-121">Guide pratique pour Contrôler le Point d’Insertion dans un contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="af82d-121">How to: Control the Insertion Point in a Windows Forms TextBox Control</span></span>](how-to-control-the-insertion-point-in-a-windows-forms-textbox-control.md)
- [<span data-ttu-id="af82d-122">Guide pratique pour Créer une zone de texte en lecture seule</span><span class="sxs-lookup"><span data-stu-id="af82d-122">How to: Create a Read-Only Text Box</span></span>](how-to-create-a-read-only-text-box-windows-forms.md)
- [<span data-ttu-id="af82d-123">Guide pratique pour Placez des guillemets doubles dans une chaîne</span><span class="sxs-lookup"><span data-stu-id="af82d-123">How to: Put Quotation Marks in a String</span></span>](how-to-put-quotation-marks-in-a-string-windows-forms.md)
- [<span data-ttu-id="af82d-124">Guide pratique pour Sélectionner du texte dans le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="af82d-124">How to: Select Text in the Windows Forms TextBox Control</span></span>](how-to-select-text-in-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="af82d-125">Guide pratique pour Afficher plusieurs lignes dans le contrôle de zone de texte Windows Forms</span><span class="sxs-lookup"><span data-stu-id="af82d-125">How to: View Multiple Lines in the Windows Forms TextBox Control</span></span>](how-to-view-multiple-lines-in-the-windows-forms-textbox-control.md)
- [<span data-ttu-id="af82d-126">TextBox, contrôle</span><span class="sxs-lookup"><span data-stu-id="af82d-126">TextBox Control</span></span>](textbox-control-windows-forms.md)
