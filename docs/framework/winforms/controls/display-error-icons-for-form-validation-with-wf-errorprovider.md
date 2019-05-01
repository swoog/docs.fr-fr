---
title: 'Procédure : afficher des icônes d’erreur pour la validation de formulaire à l’aide du composant ErrorProvider Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- errors [Windows Forms], displaying to users
- error icons
- ErrorProvider component [Windows Forms], displaying error icons
- error messages [Windows Forms], displaying icons
ms.assetid: 3b681a32-9db4-497b-a34b-34980eabee46
ms.openlocfilehash: 9487d4f82878ffefe17c576b16f654293ef01106
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61972183"
---
# <a name="how-to-display-error-icons-for-form-validation-with-the-windows-forms-errorprovider-component"></a><span data-ttu-id="0f5b8-102">Procédure : afficher des icônes d’erreur pour la validation de formulaire à l’aide du composant ErrorProvider Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0f5b8-102">How to: Display Error Icons for Form Validation with the Windows Forms ErrorProvider Component</span></span>
<span data-ttu-id="0f5b8-103">Vous pouvez utiliser un formulaire Windows <xref:System.Windows.Forms.ErrorProvider> composant pour afficher une icône d’erreur lorsque l’utilisateur entre des données non valides.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-103">You can use a Windows Forms <xref:System.Windows.Forms.ErrorProvider> component to display an error icon when the user enters invalid data.</span></span> <span data-ttu-id="0f5b8-104">Vous devez disposer d’au moins deux contrôles du formulaire afin d’onglet entre eux et ainsi appeler le code de validation.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-104">You must have at least two controls on the form in order to tab between them and thereby invoke the validation code.</span></span>  
  
### <a name="to-display-an-error-icon-when-a-controls-value-is-invalid"></a><span data-ttu-id="0f5b8-105">Pour afficher une icône d’erreur lors de la valeur d’un contrôle n’est pas valide</span><span class="sxs-lookup"><span data-stu-id="0f5b8-105">To display an error icon when a control's value is invalid</span></span>  
  
1. <span data-ttu-id="0f5b8-106">Ajoutez deux contrôles, par exemple, les zones de texte, à un formulaire Windows.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-106">Add two controls — for example, text boxes — to a Windows Form.</span></span>  
  
2. <span data-ttu-id="0f5b8-107">Ajouter un <xref:System.Windows.Forms.ErrorProvider> composant au formulaire.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-107">Add an <xref:System.Windows.Forms.ErrorProvider> component to the form.</span></span>  
  
3. <span data-ttu-id="0f5b8-108">Sélectionnez le premier contrôle et ajoutez du code à son <xref:System.Windows.Forms.Control.Validating> Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-108">Select the first control and add code to its <xref:System.Windows.Forms.Control.Validating> event handler.</span></span> <span data-ttu-id="0f5b8-109">Dans l’ordre pour que ce code s’exécute correctement, la procédure doit être connectée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-109">In order for this code to run properly, the procedure must be connected to the event.</span></span> <span data-ttu-id="0f5b8-110">Pour plus d'informations, voir [Procédure : Créer des gestionnaires d’événements en cours d’exécution pour les Windows Forms](../how-to-create-event-handlers-at-run-time-for-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="0f5b8-110">For more information, see [How to: Create Event Handlers at Run Time for Windows Forms](../how-to-create-event-handlers-at-run-time-for-windows-forms.md).</span></span>  
  
     <span data-ttu-id="0f5b8-111">Le code suivant teste la validité des données entrées par l’utilisateur ; Si les données ne sont pas valides, le <xref:System.Windows.Forms.ErrorProvider.SetError%2A> méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-111">The following code tests the validity of the data the user has entered; if the data is invalid, the <xref:System.Windows.Forms.ErrorProvider.SetError%2A> method is called.</span></span> <span data-ttu-id="0f5b8-112">Le premier argument de la <xref:System.Windows.Forms.ErrorProvider.SetError%2A> méthode spécifie le contrôle à afficher à côté de l’icône.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-112">The first argument of the <xref:System.Windows.Forms.ErrorProvider.SetError%2A> method specifies which control to display the icon next to.</span></span> <span data-ttu-id="0f5b8-113">Le deuxième argument est le texte d’erreur à afficher.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-113">The second argument is the error text to display.</span></span>  
  
    ```vb  
    Private Sub TextBox1_Validating(ByVal Sender As Object, _  
       ByVal e As System.ComponentModel.CancelEventArgs) Handles _  
       TextBox1.Validating  
          If Not IsNumeric(TextBox1.Text) Then  
             ErrorProvider1.SetError(TextBox1, "Not a numeric value.")  
          Else  
             ' Clear the error.  
             ErrorProvider1.SetError(TextBox1, "")  
          End If  
    End Sub  
    ```  
  
    ```csharp  
    protected void textBox1_Validating (object sender,  
       System.ComponentModel.CancelEventArgs e)  
    {  
       try  
       {  
          int x = Int32.Parse(textBox1.Text);  
          errorProvider1.SetError(textBox1, "");  
       }  
       catch (Exception ex)  
       {  
          errorProvider1.SetError(textBox1, "Not an integer value.");  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void textBox1_Validating(System::Object ^  sender,  
          System::ComponentModel::CancelEventArgs ^  e)  
       {  
          try  
          {  
             int x = Int32::Parse(textBox1->Text);  
             errorProvider1->SetError(textBox1, "");  
          }  
          catch (System::Exception ^ ex)  
          {  
             errorProvider1->SetError(textBox1, "Not an integer value.");  
          }  
       }  
    ```  
  
     <span data-ttu-id="0f5b8-114">(Visual c#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-114">(Visual C#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.textBox1.Validating += new  
    System.ComponentModel.CancelEventHandler(this.textBox1_Validating);  
    ```  
  
    ```cpp  
    this->textBox1->Validating += gcnew  
       System::ComponentModel::CancelEventHandler  
       (this, &Form1::textBox1_Validating);  
    ```  
  
4. <span data-ttu-id="0f5b8-115">Exécuter le projet.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-115">Run the project.</span></span> <span data-ttu-id="0f5b8-116">Tapez les données non valides (dans cet exemple, non numérique) dans le premier contrôle, puis onglet à la seconde.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-116">Type invalid (in this example, non-numeric) data into the first control, and then tab to the second.</span></span> <span data-ttu-id="0f5b8-117">Lorsque l’icône d’erreur s’affiche, placez le pointeur de la souris pour afficher le texte d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0f5b8-117">When the error icon is displayed, point at it with the mouse pointer to see the error text.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0f5b8-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f5b8-118">See also</span></span>

- <xref:System.Windows.Forms.ErrorProvider.SetError%2A>
- [<span data-ttu-id="0f5b8-119">Vue d’ensemble du composant ErrorProvider</span><span class="sxs-lookup"><span data-stu-id="0f5b8-119">ErrorProvider Component Overview</span></span>](errorprovider-component-overview-windows-forms.md)
- [<span data-ttu-id="0f5b8-120">Guide pratique pour Afficher les erreurs au sein d’un jeu de données avec l’aide du composant ErrorProvider Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0f5b8-120">How to: View Errors Within a DataSet with the Windows Forms ErrorProvider Component</span></span>](view-errors-within-a-dataset-with-wf-errorprovider-component.md)
