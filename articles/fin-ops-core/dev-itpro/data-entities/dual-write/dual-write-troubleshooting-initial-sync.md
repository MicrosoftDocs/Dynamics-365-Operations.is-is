---
title: Úrræðaleit vandamála við fyrstu samstillingu
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410082"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Úrræðaleit vandamála við fyrstu samstillingu

[!include [banner](../../includes/banner.md)]

Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Athugaðu hvort fyrstu samstillingarvillur eru í forriti Finance and Operations

Eftir að þú hefur gert kortlagningarsniðmát virkt ætti staða korta að vera **Í keyrslu**. Ef staðan er **Ekki í gangi** geta villur komið upp við fyrstu samstillingu. Til að skoða villurnar velurðu flipann **Upphaflegar samstillingarupplýsingar** á síðunni **Tvöfalt skrif**.

![Flipi upphafssamstillingar](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Þú getur ekki lokið fyrstu samstillingu: 400 Bad Request

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra vörpun og upphafssamstillingu:

*Fjartengdi þjónninn skilaði villu: (400) Bad Request.), AX export encountered an error*

Hér er dæmi um full villuboð.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Ef þessi villa kemur stöðugt fram og þú getur ekki klárað fyrstu samstillingu, fylgdu þessum skrefum til að laga málið.

1. Skráðu þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.
2. Opnaðu stjórnborð Microsoft.
3. Í glugganum **Þjónusta** skaltu ganga úr skugga um að Microsoft Dynamics 365 rammaþjónusta gagnainnflutnings-útflutnings er í gangi. Endurræstu það ef það hefur verið stöðvað, vegna þess að fyrsta samstillinga krefst þess.

## <a name="initial-synchronization-error-403-forbidden"></a>Upphafleg samstillingarvilla: 403 Forbidden

Þú gætir fengið eftirfarandi villuboð við fyrstu samstillingu:

*(\[Forbidden\], Fjartengdi þjónninn skilaði villu: (403) Forbidden.), AX export encountered an error*

Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Innskráning í forritið Finance and Operations.
2. Á síðunni **Azure Active Directory forrit** eyðirðu **DtAppID** biðlaranum og bætir honum síðan við aftur.

![Listi yfir Azure AD forrit](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Villur sjálfstilvísunar eða hringtilvísunar við fyrstu samstillingu

Hugsanlega birtast villuboð ef einhver vörpun er með tilvísanir í sjálfa sig eða hringtilvísanir. Villurnar falla í þessa flokka:

- [Einingavörpun lánardrottna V2 í msdyn_vendors](#error-vendor-map)
- [Einingavörpun viðskiptavina V3 til lykla](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Leysa úr villu í einingavörpun lánardrottna V2 til msdyn_vendors

Hugsanlega rekstu á eftirfarandi villur upphaflegrar samstillingar í vörpuninni **Lánardrottnar V2** í **msdyn_vendors** ef einingarnar eru með fyrirliggjandi færslum með gildi í reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**. Þetta er vegna þess að **InvoiceVendorAccountNumber** er reitur sem vísar í sjálfan sig og **PrimaryContactPersonId** er hringtilvísun í vörpun lánardrottins.

*Ekki tókst að leysa úr guid fyrir reitinn: <field>. Uppflettingin fannst ekki: <value>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

Hér eru nokkur dæmi:

- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Uppflettingin fannst ekki: V24-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Ef til eru færslur með gildum í þessum reitum í einingu lánardrottins skal fylgja skrefunum í hlutanum hér á eftir til að ljúka upphaflegu samstillingunni.

1. Í Finance and Operations-forritinu skal eyða reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** úr vörpuninni og vista breytingarnar.

    1. Farið á vörpunarsíðu tvöfaldra skrifa fyrir **Lánardrottnar V2 (msdyn_vendors)** og veljið flipann **Einingavarpanir**. Í vinstri síunni skal velja **Finance and Operations apps.Vendors V2**. Í hægri síunni skal velja **Sales.Vendor**.

    2. Leitið að **primarycontactperson** til að finna upprunareitinn **PrimaryContactPersonId**.
    
    3. Smellið á hnappinn **Aðgerðir** og veljið **Eyða**.
    
        ![sjálfs- eða hringtilvísun 3](media/vend_selfref3.png)
    
    4. Endurtakið til að eyða **InvoiceVendorAccountNumber** svæðinu.
    
        ![sjálfs- eða hringtilvísun 4](media/vend-selfref4.png)
    
    5. Vistið breytingar á vörpun.

2. Slökkvið á rakningu breytinga fyrir eininguna **Lánardrottnar V2**.

    1. Farið í **Gagnastjórnun \> Gagnaeiningar**.
    
    2. Veljið eininguna **Lánardrottnar V2**.
    
    3. Smellið á **Valkostir** í valmyndastikunni og síðan **Rakning breytinga**.
    
        ![sjálfs- eða hringtilvísun 5](media/selfref_options.png)
    
    4. Smellið á **Gera breytingarakningu óvirka**.
    
        ![sjálfs- eða hringtilvísun 6](media/selfref_tracking.png)

3. Keyrið fyrstu samstillingu vörpunarinnar **Lánardrottnar V2 (msdyn_vendors)**. Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.

4. Keyrið fyrstu samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**. Samstilla verður þessa vörpun ef óskað er eftir að samstilla reiti aðaltengiliða í einingu lánardrottna því að tengiliðafærslur verða einnig að vera samstilltar upphaflega.

5. Bætið reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** aftur við vörpunina **Lánardrottnar V2 (msdyn_vendors)** og vistið vörpunina.

6. Keyrið aftur fyrstu samstillingu fyrir vörpunina **Lánardrottnar V2 (msdyn_vendors)**. Allar færslur verða samstilltar því að rakning breytinga er óvirk.

7. Kveikið á rakningu breytinga fyrir eininguna **Lánardrottnar V2**.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Leysið úr villu í Einingavörpun viðskiptavina V3 til lykla

Hugsanlega rekstu á eftirfarandi villur upphaflegrar samstillingar í vörpuninni **Lánardrottnar V3** í **Lyklar** ef einingarnar eru með fyrirliggjandi færslum með gildi í reitunum **ContactPersonID** og **InvoiceAccount**. Þetta er vegna þess að **InvoiceAccount** er reitur sem vísar í sjálfan sig og **ContactPersonID** er hringtilvísun í vörpun lánardrottins.

*Ekki tókst að leysa úr guid fyrir reitinn: <field>. Uppflettingin fannst ekki: <value>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Ekki tókst að leysa úr guid fyrir reitinn: primarycontactid.msdyn_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn_billingaccount.accountnumber. Uppflettingin fannst ekki: 1206-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Ef til eru færslur með gildum í þessum reitum í einingu viðskiptavinar skal fylgja skrefunum í hlutanum hér á eftir til að ljúka upphaflegu samstillingunni. Hægt er að nota þessa nálgun fyrir allar tilbúnar einingar á borð við Lyklar og Tengiliðir.

1. Í Finance and Operations-forritinu skal eyða reitunum **ContactPersonID** og **InvoiceAccount** úr vörpuninni **Viðskiptavinir V3 (lyklar)** og vista hana.

    1. Farið á vörpunarsíðu tvöfaldra skrifa fyrir **Viðskiptavinir V3 (lyklar)** og veljið flipann **Einingavarpanir**. Í vinstri síunni skal velja **Finance and Operations apps.Customers V3**. Í hægri síunni skal velja **Common Data Service.Account**.

    2. Leitið að **contactperson** til að finna upprunareitinn **ContactPersonID**.
    
    3. Smellið á hnappinn **Aðgerðir** og veljið **Eyða**.
    
        ![sjálfs- eða hringtilvísun 3](media/cust_selfref3.png)
    
    4. Endurtakið til að eyða **InvoiceAccount** svæðinu.
    
        ![sjálfs- eða hringtilvísun](media/cust_selfref4.png)
    
    5. Vistið breytingar á vörpun.

2. Slökkvið á rakningu breytinga fyrir eininguna **Viðskiptavinir V3**.

    1. Farið í **Gagnastjórnun \> Gagnaeiningar**.
    
    2. Veljið eininguna **Viðskiptavinir V3**.
    
    3. Smellið á **Valkostir** í valmyndastikunni og síðan **Rakning breytinga**.
    
        ![sjálfs- eða hringtilvísun 5](media/selfref_options.png)
    
    4. Smellið á **Gera breytingarakningu óvirka**.
    
        ![sjálfs- eða hringtilvísun 6](media/selfref_tracking.png)

3. Keyrið fyrstu samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**. Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.

4. Keyrið fyrstu samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**. Það eru tvær varpanir með sama heitinu. Veljið þá með lýsinguna **Sniðmát tvöfaldra skrifa fyrir samstillingu FO.CDS Tengiliðir lánardrottins V2 við CDS.Contacts. Þarfnast nýs pakka \[Dynamics365SupplyChainExtended\].** í flipanum **Lýsing** fyrir vörpunina.

5. Bætið reitunum **InvoiceAccount** og **ContactPersonID** aftur við vörpunina **Viðskiptavinir V3 (Lyklar)** og vistið hana. Nú eru báðir reitirnir **InvoiceAccount** og **ContactPersonID** aftur orðnir hluti af samstillingarsniði í beinni. Í næsta skrefi er lokið við upphaflegu samstillinguna fyrir þessa reiti.

6. Keyrið aftur fyrstu samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**. Vegna þess að breytingarakning er óvirk mun keyrsla samstillingar samstilla gögnin fyrir **InvoiceAccount** og **ContactPersonID** úr Finance and Operations-forritinu við Common Data Service.

7. Til að samstilla gögnin fyrir **InvoiceAccount** og **ContactPersonId** úr Common Data Service við Finance and Operations er notað gagnasamþættingarverk.

    1. Í Power Apps skal stofna gagnasamþættingarverk á milli eininganna **Sales.Account** og **Finance and Operations apps.Customers V3**. Gagnastefnan verður að vera frá Common Data Service til Finance and Operations forritsins.  Þar sem **InvoiceAccount** er ný eigind í tvöföldum skrifum gætirðu viljað sleppa upphaflegri samstillingu fyrir þessa eigind. Nánari upplýsingar er að finna í [Sameina gögn í Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Eftirfarandi mynd sýnir verk sem uppfærir **CustomerAccount** og **ContactPersonId**.

        ![sjálfs- eða hringtilvísun](media/cust_selfref6.png)

    2. Bætið skilyrði fyrirtækis við síuna Common Data Service megin því að einungis færslurnar sem passa við síuskilyrði verða uppfærðar í Finance and Operations-forritinu. Til að bæta við síu skal smella á síutáknið. Í svarglugganum **Breyta fyrirspurn** er hægt að bæta við síufyrirspurn eins og **_msdyn_company_value eq '\<guid\>'**. Ef síutáknið er ekki til staðar skal stofna þjónustubeiðni til að biðja gagnasamþættingarteymið um að virkja síugetu leigjandans. Ef ekki er færð inn síufyrirspurn fyrir **_msdyn_company_value** verða allar færslurnar samstilltar.

        ![sjálfs- eða hringtilvísun](media/cust_selfref7.png)

        Þetta lýkur fyrstu samstillingu færslnanna.

8. Kveikið á rakningu breytinga fyrir eininguna **Viðskiptavinir V3** í Finance and Operations-forritinu.

