---
title: 'Procédure : définir et retourner des valeurs numériques avec le contrôle NumericUpDown Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- numeric values [Windows Forms], Windows Forms
- Windows Forms, numeric values
- Windows Forms controls, NumericUpDown
- NumericUpDown control [Windows Forms], setting and returning values
ms.assetid: 5bd8f8cd-4c12-49ea-9cc3-2a647d064689
ms.openlocfilehash: 3da2c7b057732e9b2db5e048dec037e4e9910c0a
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64625731"
---
# <a name="how-to-set-and-return-numeric-values-with-the-windows-forms-numericupdown-control"></a><span data-ttu-id="0cf0f-102">Procédure : définir et retourner des valeurs numériques avec le contrôle NumericUpDown Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0cf0f-102">How to: Set and Return Numeric Values with the Windows Forms NumericUpDown Control</span></span>
<span data-ttu-id="0cf0f-103">La valeur numérique des formulaires Windows <xref:System.Windows.Forms.NumericUpDown> contrôle est déterminé par son <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-103">The numeric value of the Windows Forms <xref:System.Windows.Forms.NumericUpDown> control is determined by its <xref:System.Windows.Forms.NumericUpDown.Value%2A> property.</span></span> <span data-ttu-id="0cf0f-104">Vous pouvez écrire des tests conditionnels pour la valeur du contrôle comme avec toute autre propriété.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-104">You can write conditional tests for the control's value just as with any other property.</span></span> <span data-ttu-id="0cf0f-105">Une fois le <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété est définie, vous pouvez l’ajuster directement en écrivant du code pour effectuer des opérations sur celui-ci, ou vous pouvez appeler la <xref:System.Windows.Forms.NumericUpDown.UpButton%2A> et <xref:System.Windows.Forms.NumericUpDown.DownButton%2A> méthodes.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-105">Once the <xref:System.Windows.Forms.NumericUpDown.Value%2A> property is set, you can adjust it directly by writing code to perform operations on it, or you can call the <xref:System.Windows.Forms.NumericUpDown.UpButton%2A> and <xref:System.Windows.Forms.NumericUpDown.DownButton%2A> methods.</span></span>  
  
### <a name="to-set-the-numeric-value"></a><span data-ttu-id="0cf0f-106">Pour définir la valeur numérique</span><span class="sxs-lookup"><span data-stu-id="0cf0f-106">To set the numeric value</span></span>  
  
1. <span data-ttu-id="0cf0f-107">Affecter une valeur à la <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété dans le code ou dans la fenêtre Propriétés.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-107">Assign a value to the <xref:System.Windows.Forms.NumericUpDown.Value%2A> property in code or in the Properties window.</span></span>  
  
    ```vb  
    NumericUpDown1.Value = 55  
    ```  
  
    ```csharp  
    numericUpDown1.Value = 55;  
    ```  
  
    ```cpp  
    numericUpDown1->Value = 55;  
    ```  
  
     <span data-ttu-id="0cf0f-108">ou</span><span class="sxs-lookup"><span data-stu-id="0cf0f-108">-or-</span></span>  
  
2. <span data-ttu-id="0cf0f-109">Appelez le <xref:System.Windows.Forms.NumericUpDown.UpButton%2A> ou <xref:System.Windows.Forms.NumericUpDown.DownButton%2A> méthode pour augmenter ou diminuer la valeur de la quantité spécifiée dans le <xref:System.Windows.Forms.NumericUpDown.Increment%2A> propriété.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-109">Call the <xref:System.Windows.Forms.NumericUpDown.UpButton%2A> or <xref:System.Windows.Forms.NumericUpDown.DownButton%2A> method to increase or decrease the value by the amount specified in the <xref:System.Windows.Forms.NumericUpDown.Increment%2A> property.</span></span>  
  
    ```vb  
    NumericUpDown1.UpButton()  
    ```  
  
    ```csharp  
    numericUpDown1.UpButton();  
    ```  
  
    ```cpp  
    numericUpDown1->UpButton();  
    ```  
  
### <a name="to-return-the-numeric-value"></a><span data-ttu-id="0cf0f-110">Pour retourner la valeur numérique</span><span class="sxs-lookup"><span data-stu-id="0cf0f-110">To return the numeric value</span></span>  
  
- <span data-ttu-id="0cf0f-111">Accès le <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété dans le code.</span><span class="sxs-lookup"><span data-stu-id="0cf0f-111">Access the <xref:System.Windows.Forms.NumericUpDown.Value%2A> property in code.</span></span>  
  
    ```vb  
    If NumericUpDown1.Value >= 65 Then  
       MessageBox.Show("Age is: " & NumericUpDown1.Value.ToString)  
    Else  
       MessageBox.Show("The customer is ineligible for a senior citizen discount.")  
    End If  
    ```  
  
    ```csharp  
    if(numericUpDown1.Value >= 65)  
    {  
       MessageBox.Show("Age is: " + numericUpDown1.Value.ToString());  
    }  
    else  
    {  
       MessageBox.Show("The customer is ineligible for a senior citizen discount.");  
    }  
    ```  
  
    ```cpp  
    if(numericUpDown1->Value >= 65)  
    {  
       MessageBox::Show(String::Concat("Age is: ",  
          numericUpDown1->Value.ToString()));  
    }  
    else  
    {  
       MessageBox::Show  
          ("The customer is ineligible for a senior citizen discount.");  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="0cf0f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cf0f-112">See also</span></span>

- <xref:System.Windows.Forms.NumericUpDown>
- <xref:System.Windows.Forms.NumericUpDown.Value%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.NumericUpDown.Increment%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.NumericUpDown.UpButton%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.NumericUpDown.DownButton%2A?displayProperty=nameWithType>
- [<span data-ttu-id="0cf0f-113">NumericUpDown, contrôle</span><span class="sxs-lookup"><span data-stu-id="0cf0f-113">NumericUpDown Control</span></span>](numericupdown-control-windows-forms.md)
- [<span data-ttu-id="0cf0f-114">Vue d’ensemble du contrôle NumericUpDown</span><span class="sxs-lookup"><span data-stu-id="0cf0f-114">NumericUpDown Control Overview</span></span>](numericupdown-control-overview-windows-forms.md)
