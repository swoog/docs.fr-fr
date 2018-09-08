---
title: Utilisation de l'activité Switch avec des types personnalisés
ms.date: 03/30/2017
ms.assetid: 482a48c4-eb83-40c3-a4e2-2f9a8af88b75
ms.openlocfilehash: b24a03573b31f3fb1c34d4aa6e03bc11f5b25455
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44179765"
---
# <a name="usage-of-the-switch-activity-with-custom-types"></a>Utilisation de l'activité Switch avec des types personnalisés
Cet exemple montre comment permettre à une activité <xref:System.Activities.Statements.Switch%601> d'évaluer un type complexe défini par l'utilisateur au moment de l'exécution. Dans la plupart des langages de programmation procéduraux, un [basculer](https://go.microsoft.com/fwlink/?LinkId=180521) instruction sélectionne une logique d’exécution basée sur l’évaluation conditionnelle d’une variable. D'ordinaire, une instruction `switch` opère sur une expression qui peut être évaluée statiquement. Par exemple, en C#, cela signifie que seuls des types primitifs, tels que <xref:System.Boolean>, <xref:System.Int32>, <xref:System.String>, et des types énumération sont pris en charge.  
  
 Pour permettre la commutation sur une classe personnalisée, la logique doit être implémentée pour évaluer les valeurs du type complexe personnalisé au moment de l'exécution. Cet exemple montre comment permettre la commutation sur un type complexe personnalisé nommé `Person`.  
  
-   Dans la classe personnalisée `Person`, un attribut <xref:System.ComponentModel.TypeConverter> est déclaré avec le nom du <xref:System.ComponentModel.TypeConverter> personnalisé.  
  
    ```  
    [TypeConverter(typeof(PersonConverter))]  
    public class Person  
    {  
       public string Name { get; set; }  
       public int Age { get; set; }  
    ...  
    ```  
  
-   Dans la classe personnalisée `Person`, les classes <xref:System.Object.Equals%2A> et <xref:System.Object.GetHashCode%2A> sont remplacées.  
  
    ```  
    public override bool Equals(object obj)  
    {  
        Person person = obj as Person;  
  
        if (person != null)  
        {  
            return string.Equals(this.Name, person.Name);  
        }  
  
        return false;  
    }  
  
    public override int GetHashCode()  
    {  
        if (this.Name != null)  
        {  
            return this.Name.GetHashCode();  
        }  
  
        return 0;  
    }  
    ```  
  
-   Une classe <xref:System.ComponentModel.TypeConverter> personnalisée qui effectue la conversion d'une instance de la classe personnalisée en chaîne et d'une chaîne en instance d'une classe personnalisée est implémentée.  
  
    ```  
    public class PersonConverter : TypeConverter  
    {  
        public override bool CanConvertFrom(ITypeDescriptorContext context,  
           Type sourceType)  
        {  
            return (sourceType is string);  
        }  
  
        // Overrides the ConvertFrom method of TypeConverter.  
        public override object ConvertFrom(ITypeDescriptorContext context,  
           CultureInfo culture, object value)  
        {  
            if (value == null)  
            {  
                return null;  
            }  
  
            if (value is string)  
            {  
                return new Person  
                {  
                    Name = (string)value  
                };  
            }  
  
            return base.ConvertFrom(context, culture, value);  
        }  
  
        // Overrides the ConvertTo method of TypeConverter.  
        public override object ConvertTo(ITypeDescriptorContext context,  
           CultureInfo culture, object value, Type destinationType)  
        {  
            if (destinationType == typeof(string))  
            {  
                if (value != null)  
                {  
                    return ((Person) value).Name;  
                }  
                else  
                {  
                    return null;  
                }  
            }  
  
            return base.ConvertTo(context, culture, value, destinationType);  
        }  
    }  
    ```  
  
 Les fichiers suivants sont inclus dans cet exemple :  
  
-   **Person.cs**: définit la `Person` classe.  
  
-   **PersonConverter.cs**: convertisseur de type pour la `Person` classe.  
  
-   **Sequence.XAML**: un workflow qui bascule le `Person` type.  
  
-   **Program.cs**: la fonction principale qui exécute le flux de travail.  
  
#### <a name="to-use-this-sample"></a>Pour utiliser cet exemple  
  
1.  Chargez Switch.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Appuyez sur Ctrl+Maj+B pour générer la solution.  
  
3.  Appuyez sur CTRL+F5 pour exécuter l'exemple.  
  
> [!IMPORTANT]
>  Les exemples peuvent déjà être installés sur votre ordinateur. Recherchez le répertoire (par défaut) suivant avant de continuer.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples. Cet exemple se trouve dans le répertoire suivant.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\Switch`  
  
## <a name="see-also"></a>Voir aussi  
 [Bibliothèque d’activités intégrée](../../../../docs/framework/windows-workflow-foundation/net-framework-4-5-built-in-activity-library.md)
