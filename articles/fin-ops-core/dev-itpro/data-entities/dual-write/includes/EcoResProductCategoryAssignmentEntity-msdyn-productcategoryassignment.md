## <a name="product-category-assignments-to-msdyn_productcategoryassignments"></a>Úthlutanir afurðategundar í msdyn_productcategoryassignments

Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Common Data Service.

Svæði í Finance and Operations | Gerð vörpunar | Annar Dynamics 365 reitur | Sjálfgildi
---|---|---|---
PRODUCTNUMBER | = | msdyn_globalproduct.msdyn_productnumber | 
PRODUCTCATEGORYNAME | = | msdyn_productcategory.msdyn_name | 
PRODUCTCATEGORYHIERARCHYNAME | = | msdyn_productcategory.msdyn_hierarchy.msdyn_name | 
PRODUCTNUMBER | >> | msdyn_name | 
