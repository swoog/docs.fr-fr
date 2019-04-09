---
title: 'Procédure : modifier l’aspect du contrôle LinkLabel Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- LinkLabel properties
- LinkLabel control [Windows Forms], changing appearance of links
- links [Windows Forms], changing appearance
- examples [Windows Forms], LinkLabel control
- LinkLabel control [Windows Forms], examples
ms.assetid: fdc5854f-5162-4457-8cbe-1042feb2d132
ms.openlocfilehash: be2f6e8e10d9f9b23b4f57fa696f1fb88c4726c0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59105025"
---
# <a name="how-to-change-the-appearance-of-the-windows-forms-linklabel-control"></a><span data-ttu-id="697ea-102">Procédure : modifier l’aspect du contrôle LinkLabel Windows Forms</span><span class="sxs-lookup"><span data-stu-id="697ea-102">How to: Change the Appearance of the Windows Forms LinkLabel Control</span></span>
<span data-ttu-id="697ea-103">Vous pouvez modifier le texte affiché par le <xref:System.Windows.Forms.LinkLabel> contrôle pour l’adapter à différentes fins.</span><span class="sxs-lookup"><span data-stu-id="697ea-103">You can change the text displayed by the <xref:System.Windows.Forms.LinkLabel> control to suit a variety of purposes.</span></span> <span data-ttu-id="697ea-104">Par exemple, il est courant d’indiquer à l’utilisateur que vous pouvez cliquer sur texte en définissant le texte s’affiche dans une couleur spécifique avec un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="697ea-104">For example, it is common practice to indicate to the user that text can be clicked by setting the text to appear in a specific color with an underline.</span></span> <span data-ttu-id="697ea-105">Une fois que l’utilisateur clique sur le texte, la couleur est remplacée par une couleur différente.</span><span class="sxs-lookup"><span data-stu-id="697ea-105">After the user clicks the text, the color changes to a different color.</span></span> <span data-ttu-id="697ea-106">Pour contrôler ce comportement, vous pouvez définir cinq propriétés différentes : le <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A>, <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>, <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>, <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>, et <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> propriétés.</span><span class="sxs-lookup"><span data-stu-id="697ea-106">To control this behavior, you can set five different properties: the <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A>, <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>, <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>, <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>, and <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> properties.</span></span>  
  
### <a name="to-change-the-appearance-of-a-linklabel-control"></a><span data-ttu-id="697ea-107">Pour modifier l’apparence d’un contrôle LinkLabel</span><span class="sxs-lookup"><span data-stu-id="697ea-107">To change the appearance of a LinkLabel control</span></span>  
  
1.  <span data-ttu-id="697ea-108">Définir le <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> et <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> propriétés pour les couleurs de votre choix.</span><span class="sxs-lookup"><span data-stu-id="697ea-108">Set the <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> and <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> properties to the colors you want.</span></span>  
  
     <span data-ttu-id="697ea-109">Cela peut être effectué par programme, soit au moment du design dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="697ea-109">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    ' You can set the color using decimal values for red, green, and blue  
    LinkLabel1.LinkColor = Color.FromArgb(0, 0, 255)  
    ' Or you can set the color using defined constants  
    LinkLabel1.VisitedLinkColor = Color.Purple  
    ```  
  
    ```csharp  
    // You can set the color using decimal values for red, green, and blue  
    linkLabel1.LinkColor = Color.FromArgb(0, 0, 255);  
    // Or you can set the color using defined constants  
    linkLabel1.VisitedLinkColor = Color.Purple;  
    ```  
  
    ```cpp  
    // You can set the color using decimal values for red, green, and blue  
    linkLabel1->LinkColor = Color::FromArgb(0, 0, 255);  
    // Or you can set the color using defined constants  
    linkLabel1->VisitedLinkColor = Color::Purple;  
    ```  
  
2.  <span data-ttu-id="697ea-110">Définir le <xref:System.Windows.Forms.LinkLabel.Text%2A> propriété à une légende appropriée.</span><span class="sxs-lookup"><span data-stu-id="697ea-110">Set the <xref:System.Windows.Forms.LinkLabel.Text%2A> property to an appropriate caption.</span></span>  
  
     <span data-ttu-id="697ea-111">Cela peut être effectué par programme, soit au moment du design dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="697ea-111">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    LinkLabel1.Text = "Click here to see more."  
    ```  
  
    ```csharp  
    linkLabel1.Text = "Click here to see more.";  
    ```  
  
    ```cpp  
    linkLabel1->Text = "Click here to see more.";  
    ```  
  
3.  <span data-ttu-id="697ea-112">Définir le <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> propriété pour déterminer quelle partie de la légende doit être affichée sous forme de lien.</span><span class="sxs-lookup"><span data-stu-id="697ea-112">Set the <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> property to determine which part of the caption will be indicated as a link.</span></span>  
  
     <span data-ttu-id="697ea-113">Le <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> la valeur est représentée avec un <xref:System.Windows.Forms.LinkArea> contenant deux nombres, la position de caractère de départ et le nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="697ea-113">The <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> value is represented with a <xref:System.Windows.Forms.LinkArea> containing two numbers, the starting character position and the number of characters.</span></span> <span data-ttu-id="697ea-114">Cela peut être effectué par programme, soit au moment du design dans le **propriétés** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="697ea-114">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    LinkLabel1.LinkArea = new LinkArea(6,4)  
    ```  
  
    ```csharp  
    linkLabel1.LinkArea = new LinkArea(6,4);  
    ```  
  
    ```cpp  
    linkLabel1->LinkArea = LinkArea(6,4);  
    ```  
  
4.  <span data-ttu-id="697ea-115">Définir le <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> propriété <xref:System.Windows.Forms.LinkBehavior.AlwaysUnderline>, <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, ou <xref:System.Windows.Forms.LinkBehavior.NeverUnderline>.</span><span class="sxs-lookup"><span data-stu-id="697ea-115">Set the <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> property to <xref:System.Windows.Forms.LinkBehavior.AlwaysUnderline>, <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, or <xref:System.Windows.Forms.LinkBehavior.NeverUnderline>.</span></span>  
  
     <span data-ttu-id="697ea-116">Si elle est définie sur <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, la partie de la légende déterminée par <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> sera souligné uniquement lorsque le pointeur se trouve sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="697ea-116">If it is set to <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, the part of the caption determined by <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> will only be underlined when the pointer rests on it.</span></span>  
  
5.  <span data-ttu-id="697ea-117">Dans le <xref:System.Windows.Forms.LinkLabel.LinkClicked> Gestionnaire d’événements, définissez la <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="697ea-117">In the <xref:System.Windows.Forms.LinkLabel.LinkClicked> event handler, set the <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> property to `true`.</span></span>  
  
     <span data-ttu-id="697ea-118">Lorsqu’un lien a été visité, il est courant de modifier son apparence d’une certaine façon, habituellement par couleur.</span><span class="sxs-lookup"><span data-stu-id="697ea-118">When a link has been visited, it is common practice to change its appearance in some way, usually by color.</span></span> <span data-ttu-id="697ea-119">Le texte change la couleur spécifiée par le <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="697ea-119">The text will change to the color specified by the <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> property.</span></span>  
  
    ```vb  
    Protected Sub LinkLabel1_LinkClicked (ByVal sender As Object, _  
       ByVal e As EventArgs) Handles LinkLabel1.LinkClicked  
       ' Change the color of the link text  
       ' by setting LinkVisited to True.  
       LinkLabel1.LinkVisited = True  
       ' Then do whatever other action is appropriate  
    End Sub  
    ```  
  
    ```csharp  
    protected void LinkLabel1_LinkClicked(object sender, System.EventArgs e)  
    {  
       // Change the color of the link text by setting LinkVisited   
       // to True.  
       linkLabel1.LinkVisited = true;  
       // Then do whatever other action is appropriate  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void linkLabel1_LinkClicked(System::Object ^  sender,  
          System::Windows::Forms::LinkLabelLinkClickedEventArgs ^  e)  
       {  
          // Change the color of the link text by setting LinkVisited   
          // to True.  
          linkLabel1->LinkVisited = true;  
          // Then do whatever other action is appropriate  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="697ea-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="697ea-120">See also</span></span>

- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>
- <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>
- <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>
- <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A>
- [<span data-ttu-id="697ea-121">Vue d’ensemble du contrôle LinkLabel</span><span class="sxs-lookup"><span data-stu-id="697ea-121">LinkLabel Control Overview</span></span>](linklabel-control-overview-windows-forms.md)
- [<span data-ttu-id="697ea-122">Procédure : établir un lien à un objet ou une page web avec le contrôle LinkLabel Windows Forms</span><span class="sxs-lookup"><span data-stu-id="697ea-122">How to: Link to an Object or Web Page with the Windows Forms LinkLabel Control</span></span>](link-to-an-object-or-web-page-with-wf-linklabel-control.md)
- [<span data-ttu-id="697ea-123">LinkLabel, contrôle</span><span class="sxs-lookup"><span data-stu-id="697ea-123">LinkLabel Control</span></span>](linklabel-control-windows-forms.md)
