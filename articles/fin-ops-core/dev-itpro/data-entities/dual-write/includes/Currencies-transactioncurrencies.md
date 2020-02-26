## <a name="currencies-to-transactioncurrencies"></a>Gjaldmiðlar í færslugjaldmiðla

Þetta sniðmát samstillir gögn á milli Finance and Operations -forrita og Common Data Service.

Upprunasía: ((CURRENCYCODE != "999"))

Svæði í Finance and Operations | Gerð vörpunar | Annar Dynamics 365 reitur | Sjálfgildi
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
HEITI | = | currencyname | 
SYMBOL | = | currencysymbol | 
ekkert | >> | exchangerate | 1
