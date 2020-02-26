## <a name="cds-contacts-v2-to-contacts"></a>Tengiliðir fyrir skuldatryggingu V2 til tengiliða

Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Common Data Service.

Upprunasía: (AssociatedContactType = 1)

Bakfærð upprunasía: msdyn_contactforvendor eq true og msdyn_sellable eq false og msdyn_contactpersonid ne ''

Svæði í Finance and Operations | Gerð vörpunar | Annar Dynamics 365 reitur | Sjálfgildi
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | ekkert | Lánardrottinn
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
EFTIRNAFN | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | fax | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | deild | 
ATHUGASEMDIR | = | lýsing | 
GENDER | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | nafn maka | 
ekkert | >> | msdyn_contactforvendor | Satt
CONTACTPERSONID | = | msdyn_contactpersonid | 
