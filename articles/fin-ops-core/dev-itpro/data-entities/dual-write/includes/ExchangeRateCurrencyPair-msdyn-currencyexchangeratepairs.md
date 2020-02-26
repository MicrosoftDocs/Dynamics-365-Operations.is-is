## <a name="exchange-rate-currency-pair-to-msdyn_currencyexchangeratepairs"></a>Gjaldmiðlapar gengis í msdyn_currencyexchangeratepairs

Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Common Data Service.

Svæði í Finance and Operations | Gerð vörpunar | Annar Dynamics 365 reitur | Sjálfgildi
---|---|---|---
EXCHANGERATEDISPLAYFACTOR | >< | msdyn_displayfactor | 
EXCHANGERATETYPENAME | = | msdyn_currencyexchangeratetypeid.msdyn_name | 
FROMCURRENCYCODE | = | msdyn_fromtransactioncurrencyid.isocurrencycode | 
TOCURRENCYCODE | = | msdyn_totransactioncurrencyid.isocurrencycode | 
