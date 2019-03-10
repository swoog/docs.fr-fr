---
title: 'Procédure : Modifier l’apparence du contrôle de MonthCalendar de formulaires Windows'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], calendar controls
- MonthCalendar control [Windows Forms], formatting display
ms.assetid: d09b95c9-e108-4608-9b31-b9100c0677bf
ms.openlocfilehash: 2e26f7a9db8e19b584000089f99e99aab7c25a32
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2019
ms.locfileid: "57716372"
---
# <a name="how-to-change-the-windows-forms-monthcalendar-controls-appearance"></a><span data-ttu-id="fa760-102">Procédure : Modifier l’apparence du contrôle de MonthCalendar de formulaires Windows</span><span class="sxs-lookup"><span data-stu-id="fa760-102">How to: Change the Windows Forms MonthCalendar Control's Appearance</span></span>
<span data-ttu-id="fa760-103">Les formulaires Windows <xref:System.Windows.Forms.MonthCalendar> contrôle vous permet de personnaliser l’apparence du calendrier de nombreuses façons.</span><span class="sxs-lookup"><span data-stu-id="fa760-103">The Windows Forms <xref:System.Windows.Forms.MonthCalendar> control allows you to customize the calendar's appearance in many ways.</span></span> <span data-ttu-id="fa760-104">Par exemple, vous pouvez définir le jeu de couleurs et choisir d’afficher ou masquer les numéros de semaine et la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="fa760-104">For example, you can set the color scheme and choose to display or hide week numbers and the current date.</span></span>  
  
### <a name="to-change-the-month-calendars-color-scheme"></a><span data-ttu-id="fa760-105">Pour modifier le modèle de couleurs du calendrier du mois</span><span class="sxs-lookup"><span data-stu-id="fa760-105">To change the month calendar's color scheme</span></span>  
  
-   <span data-ttu-id="fa760-106">Définir des propriétés telles que <xref:System.Windows.Forms.MonthCalendar.TitleBackColor%2A>, <xref:System.Windows.Forms.MonthCalendar.TitleForeColor%2A> et <xref:System.Windows.Forms.MonthCalendar.TrailingForeColor%2A>.</span><span class="sxs-lookup"><span data-stu-id="fa760-106">Set properties such as <xref:System.Windows.Forms.MonthCalendar.TitleBackColor%2A>, <xref:System.Windows.Forms.MonthCalendar.TitleForeColor%2A> and <xref:System.Windows.Forms.MonthCalendar.TrailingForeColor%2A>.</span></span> <span data-ttu-id="fa760-107">Le <xref:System.Windows.Forms.MonthCalendar.TitleBackColor%2A> propriété détermine également la couleur de police pour les jours de la semaine.</span><span class="sxs-lookup"><span data-stu-id="fa760-107">The <xref:System.Windows.Forms.MonthCalendar.TitleBackColor%2A> property also determines the font color for the days of the week.</span></span> <span data-ttu-id="fa760-108">Le <xref:System.Windows.Forms.MonthCalendar.TrailingForeColor%2A> propriété détermine la couleur des dates qui précèdent et suivent l’ou les mois affichés.</span><span class="sxs-lookup"><span data-stu-id="fa760-108">The <xref:System.Windows.Forms.MonthCalendar.TrailingForeColor%2A> property determines the color of the dates that precede and follow the displayed month or months.</span></span>  
  
    ```vb  
    MonthCalendar1.TitleBackColor = System.Drawing.Color.Blue  
    MonthCalendar1.TrailingForeColor = System.Drawing.Color.Red  
    MonthCalendar1.TitleForeColor = System.Drawing.Color.Yellow  
    ```  
  
    ```csharp  
    monthCalendar1.TitleBackColor = System.Drawing.Color.Blue;  
    monthCalendar1.TrailingForeColor = System.Drawing.Color.Red;  
    monthCalendar1.TitleForeColor = System.Drawing.Color.Yellow;  
    ```  
  
    ```cpp  
    monthCalendar1->TitleBackColor = System::Drawing::Color::Blue;  
    monthCalendar1->TrailingForeColor = System::Drawing::Color::Red;  
    monthCalendar1->TitleForeColor = System::Drawing::Color::Yellow;  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="fa760-109">À compter de Windows Vista et selon le thème, la définition de certaines propriétés ne modifiera pas nécessairement l’apparence du calendrier.</span><span class="sxs-lookup"><span data-stu-id="fa760-109">Starting with Windows Vista and depending on the theme, setting some properties might not change the appearance of the calendar.</span></span> <span data-ttu-id="fa760-110">Par exemple, si Windows est configuré pour utiliser le thème Aero, affecter le <xref:System.Windows.Forms.MonthCalendar.BackColor%2A>, <xref:System.Windows.Forms.MonthCalendar.TitleBackColor%2A>, <xref:System.Windows.Forms.MonthCalendar.TitleForeColor%2A>, ou <xref:System.Windows.Forms.MonthCalendar.TrailingForeColor%2A> propriétés n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="fa760-110">For example, if Windows is set to use the Aero theme, setting the <xref:System.Windows.Forms.MonthCalendar.BackColor%2A>, <xref:System.Windows.Forms.MonthCalendar.TitleBackColor%2A>, <xref:System.Windows.Forms.MonthCalendar.TitleForeColor%2A>, or <xref:System.Windows.Forms.MonthCalendar.TrailingForeColor%2A> properties has no effect.</span></span> <span data-ttu-id="fa760-111">Il s’agit, car une version mise à jour du calendrier est restituée avec une apparence qui est dérivée en cours d’exécution le thème du système d’exploitation actuel.</span><span class="sxs-lookup"><span data-stu-id="fa760-111">This is because an updated version of the calendar is rendered with an appearance that is derived at run time from the current operating system theme.</span></span> <span data-ttu-id="fa760-112">Si vous souhaitez utiliser ces propriétés et activer la version antérieure du calendrier, vous pouvez désactiver les styles visuels pour votre application.</span><span class="sxs-lookup"><span data-stu-id="fa760-112">If you want to use these properties and enable the earlier version of the calendar, you can disable visual styles for your application.</span></span> <span data-ttu-id="fa760-113">La désactivation de styles visuels peut affecter l’apparence et le comportement d’autres contrôles dans votre application.</span><span class="sxs-lookup"><span data-stu-id="fa760-113">Disabling visual styles might affect the appearance and behavior of other controls in your application.</span></span> <span data-ttu-id="fa760-114">Pour désactiver des styles visuels dans Visual Basic, ouvrez le Concepteur de projets et désactivez le **les styles visuels XP activer** case à cocher.</span><span class="sxs-lookup"><span data-stu-id="fa760-114">To disable visual styles in Visual Basic, open the Project Designer and uncheck the **Enable XP visual styles** check box.</span></span> <span data-ttu-id="fa760-115">Pour désactiver des styles visuels dans c#, ouvrez Program.cs et commentez `Application.EnableVisualStyles();`.</span><span class="sxs-lookup"><span data-stu-id="fa760-115">To disable visual styles in C#, open Program.cs and comment out `Application.EnableVisualStyles();`.</span></span> <span data-ttu-id="fa760-116">Pour plus d’informations sur les styles visuels, consultez [activation des Styles visuels](/windows/desktop/controls/cookbook-overview).</span><span class="sxs-lookup"><span data-stu-id="fa760-116">For more information about visual styles, see [Enabling Visual Styles](/windows/desktop/controls/cookbook-overview).</span></span>  
  
### <a name="to-display-the-current-date-at-the-bottom-of-the-control"></a><span data-ttu-id="fa760-117">Pour afficher la date actuelle en bas du contrôle</span><span class="sxs-lookup"><span data-stu-id="fa760-117">To display the current date at the bottom of the control</span></span>  
  
-   <span data-ttu-id="fa760-118">Affectez à la propriété <xref:System.Windows.Forms.MonthCalendar.ShowToday%2A> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="fa760-118">Set the <xref:System.Windows.Forms.MonthCalendar.ShowToday%2A> property to `true`.</span></span> <span data-ttu-id="fa760-119">L’exemple suivant bascule entre l’affichage et l’omission du jour lorsque le formulaire est sur lequel double-cliquer.</span><span class="sxs-lookup"><span data-stu-id="fa760-119">The example below toggles between displaying and omitting today's date when the form is double-clicked.</span></span>  
  
    ```vb  
    Private Sub Form1_DoubleClick(ByVal sender As Object, _  
    ByVal e As System.EventArgs) Handles MyBase.DoubleClick  
       ' Toggle between True and False.  
       MonthCalendar1.ShowToday = Not MonthCalendar1.ShowToday  
    End Sub  
    ```  
  
    ```csharp  
    private void Form1_DoubleClick(object sender, System.EventArgs e)  
    {  
       // Toggle between True and False.  
       monthCalendar1.ShowToday = !monthCalendar1.ShowToday;  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void Form1_DoubleClick(System::Object ^  sender,  
          System::EventArgs ^  e)  
       {  
          // Toggle between True and False.  
          monthCalendar1->ShowToday = !monthCalendar1->ShowToday;  
       }  
    ```  
  
     <span data-ttu-id="fa760-120">(Visual c#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) placez le code suivant dans le constructeur du formulaire pour inscrire le Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="fa760-120">(Visual C#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.DoubleClick += new System.EventHandler(this.Form1_DoubleClick);  
    ```  
  
    ```cpp  
    this->DoubleClick += gcnew System::EventHandler(this,  
       &Form1::Form1_DoubleClick);  
    ```  
  
### <a name="to-display-week-numbers"></a><span data-ttu-id="fa760-121">Pour afficher les numéros de semaine</span><span class="sxs-lookup"><span data-stu-id="fa760-121">To display week numbers</span></span>  
  
-   <span data-ttu-id="fa760-122">Affectez à la propriété <xref:System.Windows.Forms.MonthCalendar.ShowWeekNumbers%2A> la valeur `true`.</span><span class="sxs-lookup"><span data-stu-id="fa760-122">Set the <xref:System.Windows.Forms.MonthCalendar.ShowWeekNumbers%2A> property to `true`.</span></span> <span data-ttu-id="fa760-123">Vous pouvez définir cette propriété dans le code ou dans la fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="fa760-123">You can set this property either in code or in the Properties window.</span></span>  
  
     <span data-ttu-id="fa760-124">Numéros de semaine s’affichent dans une autre colonne à gauche du premier jour de la semaine.</span><span class="sxs-lookup"><span data-stu-id="fa760-124">Week numbers appear in a separate column to the left of the first day of the week.</span></span>  
  
    ```vb  
    MonthCalendar1.ShowWeekNumbers = True  
    ```  
  
    ```csharp  
    monthCalendar1.ShowWeekNumbers = true;  
    ```  
  
    ```cpp  
    monthCalendar1->ShowWeekNumbers = true;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="fa760-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa760-125">See also</span></span>
- [<span data-ttu-id="fa760-126">MonthCalendar, contrôle</span><span class="sxs-lookup"><span data-stu-id="fa760-126">MonthCalendar Control</span></span>](monthcalendar-control-windows-forms.md)
- [<span data-ttu-id="fa760-127">Guide pratique pour Sélectionnez une plage de Dates dans le contrôle MonthCalendar Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fa760-127">How to: Select a Range of Dates in the Windows Forms MonthCalendar Control</span></span>](how-to-select-a-range-of-dates-in-the-windows-forms-monthcalendar-control.md)
- [<span data-ttu-id="fa760-128">Guide pratique pour Afficher en gras certains jours avec les Windows Forms du contrôle MonthCalendar</span><span class="sxs-lookup"><span data-stu-id="fa760-128">How to: Display Specific Days in Bold with the Windows Forms MonthCalendar Control</span></span>](display-specific-days-in-bold-with-wf-monthcalendar-control.md)
- [<span data-ttu-id="fa760-129">Guide pratique pour Afficher plusieurs mois dans le contrôle MonthCalendar Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fa760-129">How to: Display More than One Month in the Windows Forms MonthCalendar Control</span></span>](display-more-than-one-month-wf-monthcalendar-control.md)
