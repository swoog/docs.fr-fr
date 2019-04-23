---
title: Mapper les contraintes keyref de schéma XML (XSD) aux contraintes de DataSet
ms.date: 03/30/2017
ms.assetid: 5b634fea-cc1e-4f6b-9454-10858105b1c8
ms.openlocfilehash: dcb295aef6d93222e682ef7f720c83963036e795
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59229743"
---
# <a name="map-keyref-xml-schema-xsd-constraints-to-dataset-constraints"></a>Mapper les contraintes keyref de schéma XML (XSD) aux contraintes de DataSet
Le **keyref** élément vous permet d’établir des liens entre les éléments dans un document. Le résultat est similaire à une relation de clé étrangère dans une base de données relationnelle. Si un schéma spécifie le **keyref** élément, l’élément est converti pendant le processus de mappage de schéma pour une contrainte de clé étrangère correspondante sur les colonnes dans les tables de la <xref:System.Data.DataSet>. Par défaut, le **keyref** élément génère aussi une relation, avec le **ParentTable**, **ChildTable**, **ParentColumn**et  **ChildColumn** propriétés spécifiées sur la relation.  
  
 Le tableau suivant présente le **msdata** attributs que vous pouvez spécifier dans le **keyref** élément.  
  
|Nom d'attribut|Description|  
|--------------------|-----------------|  
|**msdata:ConstraintOnly**|Si **ConstraintOnly = « true »** est spécifié sur le **keyref** élément dans le schéma, une contrainte est créée, mais aucune relation est créée. Si cet attribut n’est pas spécifié (ou a la valeur **False**), la contrainte et la relation sont créés dans le **DataSet**.|  
|**msdata:ConstraintName**|Si le **ConstraintName** attribut est spécifié, sa valeur est utilisée comme nom de la contrainte. Sinon, le **nom** attribut de la **keyref** élément dans le schéma fournit le nom de la contrainte dans le **DataSet**.|  
|**msdata:UpdateRule**|Si le **UpdateRule** attribut est spécifié dans le **keyref** élément dans le schéma, sa valeur est assignée à la **UpdateRule** propriété contrainte dans le  **Jeu de données**. Sinon le **UpdateRule** propriété est définie sur **Cascade**.|  
|**msdata:DeleteRule**|Si le **DeleteRule** attribut est spécifié dans le **keyref** élément dans le schéma, sa valeur est assignée à la **DeleteRule** propriété contrainte dans le  **Jeu de données**. Sinon le **DeleteRule** propriété est définie sur **Cascade**.|  
|**msdata:AcceptRejectRule**|Si le **AcceptRejectRule** attribut est spécifié dans le **keyref** élément dans le schéma, sa valeur est assignée à la **AcceptRejectRule** propriété contrainte dans le  **Jeu de données**. Sinon le **AcceptRejectRule** propriété est définie sur **aucun**.|  
  
 L’exemple suivant contient un schéma qui spécifie le **clé** et **keyref** relations entre les **OrderNumber** élément enfant de le **ordre**  élément et le **OrderNo** élément enfant de le **OrderDetail** élément.  
  
 Dans l’exemple, le **OrderNumber** élément enfant de le **OrderDetail** élément fait référence à la **OrderNo** élément enfant clé de la **ordre**élément.  
  
```xml  
<xs:schema id="MyDataSet" xmlns=""   
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  
 <xs:element name="MyDataSet" msdata:IsDataSet="true">  
  <xs:complexType>  
    <xs:choice maxOccurs="unbounded">  
      <xs:element name="OrderDetail">  
       <xs:complexType>  
         <xs:sequence>  
           <xs:element name="OrderNo" type="xs:integer" />  
           <xs:element name="ItemNo" type="xs:string" />  
         </xs:sequence>  
       </xs:complexType>  
      </xs:element>  
      <xs:element name="Order">  
        <xs:complexType>  
          <xs:sequence>  
            <xs:element name="OrderNumber" type="xs:integer" />  
            <xs:element name="EmpNumber" type="xs:integer" />  
          </xs:sequence>  
        </xs:complexType>  
      </xs:element>  
    </xs:choice>  
  </xs:complexType>  
  
  <xs:key name="OrderNumberKey"  >  
    <xs:selector xpath=".//Order" />  
    <xs:field xpath="OrderNumber" />  
  </xs:key>  
  
  <xs:keyref name="OrderNoRef" refer="OrderNumberKey">  
    <xs:selector xpath=".//OrderDetail" />  
    <xs:field xpath="OrderNo" />  
  </xs:keyref>  
 </xs:element>  
</xs:schema>  
```  
  
 Le processus de mappage de schéma XML Schema definition langage (XSD XML) produit la suivante **DataSet** avec deux tables :  
  
```  
OrderDetail(OrderNo, ItemNo) and  
Order(OrderNumber, EmpNumber)  
```  
  
 En outre, le **DataSet** définit les contraintes suivantes :  
  
-   Une contrainte unique sur la **ordre** table.  
  
    ```  
              Table: Order  
    Columns: OrderNumber   
    ConstraintName: OrderNumberKey  
    Type: UniqueConstraint  
    IsPrimaryKey: False  
    ```  
  
-   Une relation entre la **ordre** et **OrderDetail** tables. Le **Nested** propriété est définie sur **False** , car les deux éléments ne sont pas imbriqués dans le schéma.  
  
    ```  
              ParentTable: Order  
    ParentColumns: OrderNumber   
    ChildTable: OrderDetail  
    ChildColumns: OrderNo   
    ParentKeyConstraint: OrderNumberKey  
    ChildKeyConstraint: OrderNoRef  
    RelationName: OrderNoRef  
    Nested: False  
    ```  
  
-   Une contrainte de clé étrangère sur la **OrderDetail** table.  
  
    ```  
              ConstraintName: OrderNoRef  
    Type: ForeignKeyConstraint  
    Table: OrderDetail  
    Columns: OrderNo   
    RelatedTable: Order  
    RelatedColumns: OrderNumber   
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Mappage des contraintes de schéma XML (XSD) aux contraintes de DataSet](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/mapping-xml-schema-xsd-constraints-to-dataset-constraints.md)
- [Génération de relations de DataSet à partir du schéma XML (XSD)](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md)
- [Fournisseurs managés ADO.NET et centre de développement DataSet](https://go.microsoft.com/fwlink/?LinkId=217917)
