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
ms.openlocfilehash: 281fbbd4459230056fcac2e6c684422c91dc0817
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59119884"
---
# <a name="how-to-set-and-return-numeric-values-with-the-windows-forms-numericupdown-control"></a>Procédure : définir et retourner des valeurs numériques avec le contrôle NumericUpDown Windows Forms
La valeur numérique des formulaires Windows <xref:System.Windows.Forms.NumericUpDown> contrôle est déterminé par son <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété. Vous pouvez écrire des tests conditionnels pour la valeur du contrôle comme avec toute autre propriété. Une fois le <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété est définie, vous pouvez l’ajuster directement en écrivant du code pour effectuer des opérations sur celui-ci, ou vous pouvez appeler la <xref:System.Windows.Forms.NumericUpDown.UpButton%2A> et <xref:System.Windows.Forms.NumericUpDown.DownButton%2A> méthodes.  
  
### <a name="to-set-the-numeric-value"></a>Pour définir la valeur numérique  
  
1.  Affecter une valeur à la <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété dans le code ou dans la fenêtre Propriétés.  
  
    ```vb  
    NumericUpDown1.Value = 55  
    ```  
  
    ```csharp  
    numericUpDown1.Value = 55;  
    ```  
  
    ```cpp  
    numericUpDown1->Value = 55;  
    ```  
  
     - ou -  
  
2.  Appelez le <xref:System.Windows.Forms.NumericUpDown.UpButton%2A> ou <xref:System.Windows.Forms.NumericUpDown.DownButton%2A> méthode pour augmenter ou diminuer la valeur de la quantité spécifiée dans le <xref:System.Windows.Forms.NumericUpDown.Increment%2A> propriété.  
  
    ```vb  
    NumericUpDown1.UpButton()  
    ```  
  
    ```csharp  
    numericUpDown1.UpButton();  
    ```  
  
    ```cpp  
    numericUpDown1->UpButton();  
    ```  
  
### <a name="to-return-the-numeric-value"></a>Pour retourner la valeur numérique  
  
-   Accès le <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété dans le code.  
  
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
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.NumericUpDown>
- <xref:System.Windows.Forms.NumericUpDown.Value%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.NumericUpDown.Increment%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.NumericUpDown.UpButton%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.NumericUpDown.DownButton%2A?displayProperty=nameWithType>
- [NumericUpDown, contrôle](numericupdown-control-windows-forms.md)
- [Vue d’ensemble du contrôle NumericUpDown](numericupdown-control-overview-windows-forms.md)
