---
title: Mapper les contraintes uniques de schéma XML (XSD) aux contraintes de DataSet
ms.date: 03/30/2017
ms.assetid: 56da90bf-21d3-4d1a-8bb8-de908866b78d
ms.openlocfilehash: 650cd6b8b8149529f115f22a11d19178fbd6d302
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108223"
---
# <a name="map-unique-xml-schema-xsd-constraints-to-dataset-constraints"></a>Mapper les contraintes uniques de schéma XML (XSD) aux contraintes de DataSet
Dans un schéma de langage (XSD XML) de définition de schéma XML, le **unique** élément spécifie la contrainte d’unicité sur un élément ou attribut. Dans le processus de conversion d'un schéma XML en schéma relationnel, la contrainte unique spécifiée sur un élément ou un attribut du schéma XML est mappée à une contrainte unique dans l'objet <xref:System.Data.DataTable> de l'objet <xref:System.Data.DataSet> correspondant qui est généré.  
  
 Le tableau suivant présente le **msdata** attributs que vous pouvez spécifier dans le **unique** élément.  
  
|Nom d'attribut|Description|  
|--------------------|-----------------|  
|**msdata:ConstraintName**|Si cet attribut est spécifié, sa valeur est utilisée comme nom de la contrainte. Sinon, le **nom** attribut fournit la valeur de la contrainte.|  
|**msdata:PrimaryKey**|Si `PrimaryKey="true"` est présent dans le **unique** élément, une contrainte unique est créée avec le **IsPrimaryKey** propriété définie sur **true**.|  
  
 L’exemple suivant montre un schéma XML qui utilise le **unique** élément pour spécifier une contrainte d’unicité.  
  
```xml  
<xs:schema id="SampleDataSet"   
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  <xs:element name="Customers">  
    <xs:complexType>  
      <xs:sequence>  
        <xs:element name="CustomerID" type="xs:integer"   
           minOccurs="0"/>  
        <xs:element name="CompanyName" type="xs:string"   
           minOccurs="0"/>  
       <xs:element name="Phone" type="xs:string" />  
     </xs:sequence>  
   </xs:complexType>  
 </xs:element>  
  
 <xs:element name="SampleDataSet" msdata:IsDataSet="true">  
  <xs:complexType>  
    <xs:choice maxOccurs="unbounded">  
      <xs:element ref="Customers" />  
    </xs:choice>  
  </xs:complexType>  
   <xs:unique     msdata:ConstraintName="UCustID"     name="UniqueCustIDConstr" >       <xs:selector xpath=".//Customers" />       <xs:field xpath="CustomerID" />     </xs:unique>  
</xs:element>  
</xs:schema>  
```  
  
 Le **unique** élément dans le schéma spécifie que pour tous les **clients** éléments dans un document d’instance, la valeur de la **CustomerID** élément enfant doit être unique. Dans la génération du **DataSet**, le processus de mappage lit ce schéma et génère le tableau suivant :  
  
```  
Customers (CustomerID, CompanyName, Phone)  
```  
  
 Le processus de mappage crée aussi une contrainte unique sur la **CustomerID** colonne, comme indiqué dans le code suivant **DataSet**. (Par souci de simplicité, seules les propriétés pertinentes sont représentées.)  
  
```  
      DataSetName: MyDataSet  
TableName: Customers  
  ColumnName: CustomerID  
      AllowDBNull: True  
      Unique: True  
  ConstraintName: UcustID       Type: UniqueConstraint  
      Table: Customers  
      Columns: CustomerID   
      IsPrimaryKey: False  
```  
  
 Dans le **DataSet** qui est généré, le **IsPrimaryKey** propriété est définie sur **False** pour la contrainte unique. Le **unique** propriété sur la colonne indique que le **CustomerID** les valeurs de colonne doivent être uniques (mais ils peuvent être une référence null, comme spécifié par le **AllowDBNull** propriété de la colonne).  
  
 Si vous modifiez le schéma et définir l’en-tête facultatif **msdata : PrimaryKey** attribut valeur à **True**, la contrainte unique est créée sur la table. Le **AllowDBNull** propriété de colonne est définie sur **False**et le **IsPrimaryKey** propriété de la contrainte définie sur **True**, faisant ainsi le **CustomerID** colonne une colonne clé primaire.  
  
 Vous pouvez spécifier une contrainte unique sur une combinaison d'éléments ou d'attributs dans le schéma XML. L’exemple suivant montre comment spécifier qu’une combinaison de **CustomerID** et **CompanyName** valeurs doivent être uniques pour tous les **clients** dans n’importe quelle instance, par Ajouter une autre **xs : Field** élément dans le schéma.  
  
```xml  
      <xs:unique     
         msdata:ConstraintName="SomeName"    
         name="UniqueCustIDConstr" >   
  <xs:selector xpath=".//Customers" />   
  <xs:field xpath="CustomerID" />   
  <xs:field xpath="CompanyName" />   
</xs:unique>  
```  
  
 Il s’agit la contrainte qui est créée dans le résultat **DataSet**.  
  
```  
ConstraintName: SomeName  
  Table: Customers  
  Columns: CustomerID CompanyName   
  IsPrimaryKey: False  
```  
  
## <a name="see-also"></a>Voir aussi

- [Mappage des contraintes de schéma XML (XSD) aux contraintes de DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/mapping-xml-schema-xsd-constraints-to-dataset-constraints.md)
- [Génération de relations de DataSet à partir du schéma XML (XSD)](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
