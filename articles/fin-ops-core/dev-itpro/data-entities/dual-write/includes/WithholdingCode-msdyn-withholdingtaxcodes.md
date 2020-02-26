## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a>Staðgreiðsluskattskóðar í msdyn_withholdingtaxcodes

Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Common Data Service.

Svæði í Finance and Operations | Gerð vörpunar | Annar Dynamics 365 reitur | Sjálfgildi
---|---|---|---
WITHHOLDINGCODE | = | msdyn_name | 
WITHHOLDINGTAXNAME | = | msdyn_description | 
WITHHOLDINGTAXROUNDOFF | = | msdyn_roundoff | 
WITHHOLDINGTAXROUNDOFFTYPE | >< | msdyn_roundofftype | 
CURRENCYCODEID | = | msdyn_currency.isocurrencycode | 
WITHHOLDINGTAXBASE | >< | msdyn_taxableamountorigin | 
