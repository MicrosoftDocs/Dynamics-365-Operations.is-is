---
title: Úrræðaleit vandamála við fyrstu samstillingu
description: Þessi grein veitir bilanaleit sem getur hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.
author: RamaKrishnamoorthy
ms.date: 06/24/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d9d74eea90cc2dfca2d5decf6e5cd1d7f52da2a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289485"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Úrræðaleit vandamála við fyrstu samstillingu

[!include [banner](../../includes/banner.md)]



Þessi grein veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita fjármála- og reksturs og Dataverse. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þessi grein fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Athugaðu með fyrstu samstillingarvillur í forriti fjármála- og reksturs

Eftir að þú hefur gert kortlagningarsniðmát virkt ætti staða korta að vera **Í keyrslu**. Ef staðan er **Ekki í gangi** geta villur komið upp við fyrstu samstillingu. Til að skoða villurnar velurðu flipann **Upphaflegar samstillingarupplýsingar** á síðunni **Tvöfalt skrif**.

![Villa í flipa upphaflegra samstillingarupplýsinga.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Þú getur ekki lokið fyrstu samstillingu: 400 Bad Request

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra vörpun og upphafssamstillingu:

*(\[Villa í beiðni\], fjartengdur þjónn skilaði villu: (400) Villa í beiðni.), villa kom upp í AX útflutningi.*

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

1. Skráðu þig inn á sýndarvélina (VM) fyrir forrit fjármála- og reksturs.
2. Opnaðu stjórnborð Microsoft.
3. Í glugganum **Þjónusta** skaltu ganga úr skugga um að Microsoft Dynamics 365 rammaþjónusta gagnainnflutnings-útflutnings er í gangi. Endurræstu það ef það hefur verið stöðvað, vegna þess að fyrsta samstillinga krefst þess.

## <a name="initial-synchronization-error-403-forbidden"></a>Upphafleg samstillingarvilla: 403 Forbidden

Þú gætir fengið eftirfarandi villuboð við fyrstu samstillingu:

*(\[Forbidden\], Fjartengdi þjónninn skilaði villu: (403) Forbidden.), AX export encountered an error*

Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Skráið inn á forrit fjármála- og reksturs.
2. Á síðunni **Azure Active Directory forrit** eyðirðu **DtAppID** biðlaranum og bætir honum síðan við aftur.

![DtAppID-biðlari á lista yfir Azure AD-forrit.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Villur sjálfstilvísunar eða hringtilvísunar við fyrstu samstillingu

Hugsanlega birtast villuboð ef einhver vörpun er með tilvísanir í sjálfa sig eða hringtilvísanir. Villurnar falla í þessa flokka:

- [Villur í töfluvörpuninni Lánardrottinn V2–to–msdyn_vendors](#error-vendor-map)
- [Villur í töfluvörpuninni Viðskiptavinir V3–to–Accounts](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Leysa villur í töfluvörpuninni Lánardrottinn V2–to–msdyn_vendors

Villur upphaflegrar samstillingar gætu komið upp fyrir vörpun **Lánardrottnar V2** í **msdyn\_lánardrottnar** ef töflurnar eru með fyrirliggjandi línur þar sem eru gildi í dálkunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**. Þessar villur koma upp vegna þess að **InvoiceVendorAccountNumber** er dálkur sem vísar í sjálfan sig og **PrimaryContactPersonId** er hringtilvísun í vörpun lánardrottins.

Villuboðin sem koma upp verða á eftirfarandi formi.

*Ekki tókst að leysa úr guid fyrir reitinn: \<field\>. Uppflettingin fannst ekki: \<value\>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Hér eru nokkur dæmi:

- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Uppflettingin fannst ekki: V24-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Ef einhverjar línur í töflu lánardrottins eru með gildi í dálkunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** skal fylgja þessum skrefum til að ljúka upphaflegu samstillingunni.

1. Í forriti fjármála- og reksturs skal eyða dálkunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** úr vörpuninni og vista síðan vörpunina.

    1. Á vörpunarsíðu tvöfaldra skrifa fyrir **Lánardrottnar V2 (msdyn\_lánardrottnar)**, í flipanum **Töfluvarpanir**, í vinstri síunni, skal velja **forrit fjármála- og reksturs.Vendors V2**. Í hægri síunni skal velja **Sales.Vendor**.
    2. Leitið að **primarycontactperson** til að finna upprunadálkinn **PrimaryContactPersonId**.
    3. Veljið **Aðgerðir** og veljið svo **Eyða**.

        ![Eyða dálkinum PrimaryContactPersonId.](media/vend_selfref3.png)

    4. Endurtakið þessi skref til að eyða dálkinum **InvoiceVendorAccountNumber**.

        ![Eyða dálkinum InvoiceVendorAccountNumber.](media/vend-selfref4.png)

    5. Vistið breytingarnar í vörpunina.

2. Slökkvið á rakningu breytinga fyrir töfluna **Lánardrottnar V2**.

    1. Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Gagnatöflur**.
    2. Veljið töfluna **Lánardrottnar V2**.
    3. Á aðgerðasvæðinu skal velja **Valkostir** og síðan velja **Breytingarakning**.

        ![Valkostur breytingarakningar valinn.](media/selfref_options.png)

    4. Veljið **Gera breytingarakningu óvirka**.

        ![Gera breytingarakningu óvirka valið.](media/selfref_tracking.png)

3. Keyrið upphaflega samstillingu fyrir vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)**. Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.
4. Keyrið upphaflega samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**. Samstilla verður þessa vörpun ef á að samstilla dálk aðaltengiliða í töflu lánardrottins, því einnig þarf að gera upphaflega samstillingu fyrir tengiliðalínurnar.
5. Bætið dálkumi, **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** aftur við vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)** og vistið síðan vörpunina.
6. Keyrið upphaflega samstillingu aftur fyrir vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)**. Slökkt er á rakningu breytinga og verða því allar línur samstilltar.
7. Kveikið aftur á rakningu breytinga fyrir töfluna **Lánardrottnar V2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Leysa úr villum í töfluvörpuninni Viðskiptavinir V3–to–Accounts

Villur upphaflegrar samstillingar gætu komið upp fyrir vörpun **Viðskiptavinir V3** í **Lyklar** ef töflurnar eru með fyrirliggjandi línur þar sem eru gildi í dálkunum **ContactPersonID** og **InvoiceAccount**. Þessar villur koma upp vegna þess að **InvoiceAccount** er dálkur sem vísar í sjálfan sig og **ContactPersonID** er hringtilvísun í vörpun lánardrottins.

Villuboðin sem koma upp verða á eftirfarandi formi.

*Ekki tókst að leysa úr guid fyrir reitinn: \<field\>. Uppflettingin fannst ekki: \<value\>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Hér eru nokkur dæmi:

- *Ekki tókst að leysa úr guid fyrir reitinn: primarycontactid.msdyn\_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_billingaccount.accountnumber. Uppflettingin fannst ekki: 1206-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Ef einhverjar línur í töflu viðskiptavinar eru með gildi í dálkunum **ContactPersonID** og **InvoiceAccount** skal fylgja þessum skrefum til að ljúka upphaflegu samstillingunni. Hægt er að nota þessa nálgun fyrir allar tilbúnar töflur á borð við **Lyklar** og **Tengiliðir**.

1. Í forriti fjármála- og reksturs skal eyða dálkunum **ContactPersonID** og **InvoiceAccount** úr vörpuninni **Viðskiptavinir V3 (lyklar)** og síðan vista hana.

    1. Á vörpunarsíðu tvöfaldra skrifa fyrir **Viðskiptavinir V3 (lyklar)**, á flipanum **Töfluvarpanir**, á vinstri síunni, skal velja **Forrit fjármála- og reksturs.Customers V3**. Í hægri síunni skal velja **Dataverse.Account**.
    2. Leitið að **contactperson** til að finna upprunadálkinn **ContactPersonID**.
    3. Veljið **Aðgerðir** og veljið svo **Eyða**.

        ![Dálkinum ContactPersonID eytt.](media/cust_selfref3.png)

    4. Endurtakið þessi skref til að eyða dálkinum **InvoiceAccount**.

        ![Dálkinum InvoiceAccount eytt.](media/cust_selfref4.png)

    5. Vistið breytingarnar í vörpunina.

2. Slökkvið á rakningu breytinga fyrir töfluna **Viðskiptavinir V3**.

    1. Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Gagnatöflur**.
    2. Veljið töfluna **Viðskiptavinir V3**.
    3. Á aðgerðasvæðinu skal velja **Valkostir** og síðan velja **Breytingarakning**.

        ![Valkostur breytingarakningar valinn.](media/selfref_options.png)

    4. Veljið **Gera breytingarakningu óvirka**.

        ![Gera breytingarakningu óvirka valið.](media/selfref_tracking.png)

3. Keyrið upphaflega samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**. Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.
4. Keyrið upphaflega samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**.

    > [!NOTE]
    > Tvær varpanir eru með sama heitið. Verið viss um að velja þá vörpun sem er með eftirfarandi lýsingu í flipanum **Upplýsingar**: **Sniðmát tvöfaldra skrifa fyrir samstillingu milli FO.CDS Tengiliður lánardrottins V2 og CDS.Contacts. Þarfnast nýs pakka \[Dynamics365SupplyChainExtended\].**

5. Bætið dálkunum **InvoiceAccount** og **ContactPersonID** aftur við vörpunina **Viðskiptavinir V3 (Lyklar)** og vistið hana síðan. Nú eru báðir dálkarnir **InvoiceAccount** og **ContactPersonId** aftur orðnir hluti af samstillingarsniði í beinni. Í næsta skrefi verður gerð upphafleg samstilling fyrir þessa dálka.
6. Keyrið aftur upphaflega samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**. Vegna þess að slökkt er á breytingarakningu, verða gögnin fyrir **InvoiceAccount** og **ContactPersonId** samstillt úr forriti fjármála- og reksturs við Dataverse.
7. Til að samstilla gögnin fyrir **InvoiceAccount** og **ContactPersonId** úr Dataverse við forrit fjármála- og reksturs þarf að nota gagnasamþættingarverk.

    1. Í Power Apps skal stofna gagnasamþættingarverk á milli **Sales.Account** og **Forrit fjármála- og reksturs.Customers V3**. Gagnastefnan verður að vera frá Dataverse til forrits fjármála- og reksturs. Þar sem **InvoiceAccount** er ný eigind í tvöföldum skrifum gætirðu viljað sleppa upphaflegri samstillingu fyrir hana. Nánari upplýsingar er að finna í [Sameina gögn í Dataverse](/power-platform/admin/data-integrator).

        Eftirfarandi skýringarmynd sýnir verk sem uppfærir **CustomerAccount** og **ContactPersonId**.

        ![Gagnasamþættingarver til að uppfæra CustomerAccount og ContactPersonId.](media/cust_selfref6.png)

    2. Bætið skilyrði fyrirtækis við síuna Dataverse megin þannig að einungis línur sem passa við síuskilyrði verða uppfærðar í forriti fjármála- og reksturs. Til að bæta við síu skal velja síuhnappinn. Því næst, í svarglugganum **Breyta fyrirspurn** er hægt að bæta við síufyrirspurn á borð við **\_msdyn\_fyrirtæki\_gildi jafngildir „\<guid\>“**.

        > [ATHUGASEMD] Ef síuhnappurinn er ekki til staðar skal stofna þjónustubeiðni til að biðja gagnasamþættingarteymið um að virkja síugetu leigjandans.

        Ef ekki er slegin inn síufyrirspurn fyrir **\_msdyn\_fyrirtæki\_gildi** verða allar línurnar samstilltar.

        ![Síufyrirspurn bætt við.](media/cust_selfref7.png)

    Upphaflegri samstillingu línanna er nú lokið.

8. Í forriti fjármála- og reksturs skal kveikja aftur á rakningu breytinga fyrir töfluna **Viðskiptavinir V3**.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Upphafleg mistök við samstillingu á tengingum með fleiri en 10 uppsláttarreitum

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra fyrstu samstillingu bilana í vörpunum **Viðskiptavinir V3 -  Lyklar**, **Sölupantanir** eða einhverri vörpun með fleiri en 10 uppflettireiti:

*CRMExport: Framkvæmd pakka lokið. Villa í lýsingu 5 Tilraunir til að sækja gögn úr https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$ orderby=accountnumber asc mistókst.*

Vegna takmörkunar á uppflettingu fyrirspurnarinnar mistekst upphafleg samstilling þegar vörpun einingarinnar inniheldur fleiri en 10 uppflettingar. Nánari upplýsingar er að finna í [Sækja tengdar töflufærslur með fyrirspurn](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Til að laga þetta vandamál skal fylgja þessum skrefum:

1. Fjarlægðu valfrjálsa uppflettireiti úr vörpunareiningu tvöfaldrar skráningar þannig að fjöldi uppflettinga sé 10 eða færri.
2. Vistaðu vörpunina og gerðu fyrstu samstillinguna.
3. Þegar upphafleg samstilling fyrir fyrsta skrefið hefur tekist skaltu bæta við eftirstandandi uppflettireitum og fjarlægja uppflettireiti sem þú samstilltir í fyrsta skrefinu. Gakktu úr skugga um að fjöldi uppflettisvæða sé 10 eða færri. Vistaðu vörpunina og keyrðu fyrstu samstillinguna.
4. Endurtaktu skrefin þar til allir uppflettireitir hafa verið samstilltir.
5. Bættu öllum uppflettireitunum aftur við vörpunina, vistaðu hana og keyrðu hana með **Sleppa upphaflegri samstillingu**.

Þetta ferli virkjar vörpun fyrir samstillingu í rauntíma.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Þekkt vandamál við fyrstu samstillingu á póstföngum aðila og rafrænum aðsetrum aðila

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra upphaflega vörpun á póstföngum aðila og rafrænum aðsetrum aðila:

*Númer aðila fannst ekki í Dataverse.*

Það er svið sett á **DirPartyCDSEntity** í forritum fjármála- og reksturs sem síar aðila af gerðinni **Einstaklingur** og **Fyrirtæki**. Þar af leiðandi mun upphafleg samstilling vörpunarinnar **CDS-aðilar – msdyn_parties** ekki samstilla aðila af annarri gerð, þ.m.t. **Lögaðili** og **Rekstrareining**. Þegar upphafleg samstilling er keyrð fyrir **Póstföng CDS-aðila (msdyn_partypostaladdresses)** eða **Tengiliðir aðila V3 (msdyn_partyelectronicaddresses)** gæti komið upp villa.

Við erum að vinna að lagfæringu til að fjarlægja svið fyrir gerð aðila í einingu fjármála- og reksturs þannig að aðilar af öllum gerðum geti samstillst við Dataverse.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Eru einhver vandamál varðandi frammistöðu við keyrslu á upphaflegri samstillingu fyrir gögn viðskiptavinar eða tengiliðar?

Ef þú hefur keyrt upphaflega samstillingu fyrir gögn **Viðskiptavinar** og hefur varpanir **Viðskiptavinar** í gangi og keyrir síðan upphaflega samstillingu fyrir gögn **Tengiliðar** gætu komið upp vandamál við innsetningar og uppfærslur á töflunum **LogisticsPostalAddress** og **LogisticsElectronicAddress** fyrir aðsetur **Tengiliðar**. Sömu altæku töflur póstfangs og rafræns aðseturs eru raktar fyrir **CustCustomerV3Entity** og **VendVendorV2Entity** og tvöföld skráning reynir að búa til fleiri fyrirspurnir til að skrifa gögn á hina hliðina. Ef þú hefur þegar keyrt upphaflega samstillingu fyrir **Viðskiptavin** skaltu stöðva samsvarandi vörpun á meðan þú keyrir upphaflega samstillingu fyrir gögn **Tengiliðar**. Gerðu það sama fyrir gögn **Lánardrottins**. Þegar upphaflegri samstillingu er lokið er hægt að keyra allar varpanir með því að sleppa upphaflegu samstillingunni.

## <a name="float-data-type-that-has-a-zero-value-cant-be-synchronized"></a>Ekki er hægt að samstilla gerð flotgagna sem hefur núllgildi

Upphafleg samstilling gæti mistekist fyrir færslur sem eru með núllgildi fyrir verðreit, t.d. **Fasta greiðsluupphæð** eða **Upphæð** í gjaldmiðli færslunnar. Í þessu tilviki færðu villuboð sem líkjast eftirfarandi dæmi:

*Villa kom upp við staðfestingu á innsláttarfæribreytu: Microsoft.OData.ODataException: Ekki er hægt að umbreyta „000000“ í væntanlega gerð „Edm.Decimal“,...*

Vandamálið er tengt gildinu fyrir **Landsstaðal tungumáls** undir **Snið upprunagagna** í einingunni **Gagnastjórnun**. Breyttu gildinu í reitnum **Landsstaðall tungumáls** í **en-us** og reyndu síðan aftur.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

