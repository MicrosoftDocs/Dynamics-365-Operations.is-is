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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a7ba4fa4771324b4bcb8464649bd8ce8f32024c0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683562"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Úrræðaleit vandamála við fyrstu samstillingu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Athugaðu hvort fyrstu samstillingarvillur eru í forriti Finance and Operations

Eftir að þú hefur gert kortlagningarsniðmát virkt ætti staða korta að vera **Í keyrslu**. Ef staðan er **Ekki í gangi** geta villur komið upp við fyrstu samstillingu. Til að skoða villurnar velurðu flipann **Upphaflegar samstillingarupplýsingar** á síðunni **Tvöfalt skrif**.

![Villa í flipa upphaflegra samstillingarupplýsinga](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Þú getur ekki lokið fyrstu samstillingu: 400 Bad Request

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra vörpun og upphafssamstillingu:

*(\[Villa í beiðni\], fjartengdur þjónn skilaði villu: (400) Villa í beiðni.), villa kom upp í AX útflutningi*

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

![DtAppID-biðlari á lista yfir Azure AD-forrit](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Villur sjálfstilvísunar eða hringtilvísunar við fyrstu samstillingu

Hugsanlega birtast villuboð ef einhver vörpun er með tilvísanir í sjálfa sig eða hringtilvísanir. Villurnar falla í þessa flokka:

- [Villur í töfluvörpuninni Lánardrottinn V2–to–msdyn_vendors](#error-vendor-map)
- [Villur í töfluvörpuninni Viðskiptavinir V3–to–Accounts](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Leysa villur í töfluvörpuninni Lánardrottinn V2–to–msdyn_vendors

Villur upphaflegrar samstillingar gætu komið upp fyrir vörpun **Lánardrottnar V2** í **msdyn\_lánardrottnar** ef töflurnar eru með fyrirliggjandi línur þar sem eru gildi í reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber**. Þessar villur koma upp vegna þess að **InvoiceVendorAccountNumber** er reitur sem vísar í sjálfan sig og **PrimaryContactPersonId** er hringtilvísun í vörpun lánardrottins.

Villuboðin sem koma upp verða á eftirfarandi formi.

*Ekki tókst að leysa úr guid fyrir reitinn: \<field\>. Uppflettingin fannst ekki: \<value\>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Hér eru nokkur dæmi:

- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Uppflettingin fannst ekki: V24-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Ef einhverjar línur í einingu lánardrottins eru með gildi í reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** skal fylgja þessum skrefum til að ljúka upphaflegu samstillingunni.

1. Í Finance and Operations-forritinu skal eyða reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** úr vörpuninni og vista síðan vörpunina.

    1. Á vörpunarsíðu tvöfaldra skrifa fyrir **Lánardrottnar V2 (msdyn\_lánardrottnar)**, í flipanum **Töfluvarpanir**, í vinstri síunni, skal velja **Finance and Operations apps.Vendors V2**. Í hægri síunni skal velja **Sales.Vendor**.
    2. Leitið að **primarycontactperson** til að finna upprunareitinn **PrimaryContactPersonId**.
    3. Veljið **Aðgerðir** og veljið svo **Eyða**.

        ![Eyða reitnum PrimaryContactPersonId](media/vend_selfref3.png)

    4. Endurtakið þessi skref til að eyða reitnum **InvoiceVendorAccountNumber**.

        ![Eyða reitnum InvoiceVendorAccountNumber](media/vend-selfref4.png)

    5. Vistið breytingarnar í vörpunina.

2. Slökkvið á rakningu breytinga fyrir eininguna **Lánardrottnar V2**.

    1. Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Gagnatöflur**.
    2. Veljið eininguna **Lánardrottnar V2**.
    3. Á aðgerðasvæðinu skal velja **Valkostir** og síðan velja **Breytingarakning**.

        ![Valkostur breytingarakningar valinn](media/selfref_options.png)

    4. Veljið **Gera breytingarakningu óvirka**.

        ![Gera breytingarakningu óvirka valið](media/selfref_tracking.png)

3. Keyrið upphaflega samstillingu fyrir vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)**. Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.
4. Keyrið upphaflega samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**. Samstilla verður þessa vörpun ef á að samstilla reit aðaltengiliða í einingu lánardrottins, því einnig þarf að gera upphaflega samstillingu fyrir tengiliðalínurnar.
5. Bætið reitunum **PrimaryContactPersonId** og **InvoiceVendorAccountNumber** aftur við vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)** og vistið síðan vörpunina.
6. Keyrið upphaflega samstillingu aftur fyrir vörpunina **Lánardrottnar V2 (msdyn\_lánardrottnar)**. Slökkt er á rakningu breytinga og verða því allar línur samstilltar.
7. Kveikið aftur á rakningu breytinga fyrir eininguna **Lánardrottnar V2**.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Leysa úr villum í töfluvörpuninni Viðskiptavinir V3–to–Accounts

Villur upphaflegrar samstillingar gætu komið upp fyrir vörpun **Viðskiptavinir V3** í **Lyklar** ef töflurnar eru með fyrirliggjandi línur þar sem eru gildi í reitunum **ContactPersonID** og **InvoiceAccount**. Þessar villur koma upp vegna þess að **InvoiceAccount** er reitur sem vísar í sjálfan sig og **ContactPersonID** er hringtilvísun í vörpun lánardrottins.

Villuboðin sem koma upp verða á eftirfarandi formi.

*Ekki tókst að leysa úr guid fyrir reitinn: \<field\>. Uppflettingin fannst ekki: \<value\>. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Hér eru nokkur dæmi:

- *Ekki tókst að leysa úr guid fyrir reitinn: primarycontactid.msdyn\_contactpersonid. Uppflettingin fannst ekki: 000056. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Ekki tókst að leysa úr guid fyrir reitinn: msdyn\_billingaccount.accountnumber. Uppflettingin fannst ekki: 1206-1. Reynið þessa vefslóð(ir) til að athuga hvort tilvísunargögnin séu til: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Ef einhverjar línur í einingu viðskiptavinar eru með gildi í reitunum **ContactPersonID** og **InvoiceAccount** skal fylgja þessum skrefum til að ljúka upphaflegu samstillingunni. Hægt er að nota þessa nálgun fyrir allar tilbúnar töflur á borð við **Lyklar** og **Tengiliðir**.

1. Í Finance and Operations-forritinu skal eyða reitunum **ContactPersonID** og **InvoiceAccount** úr vörpuninni **Viðskiptavinir V3 (lyklar)** og síðan vista hana.

    1. Á vörpunarsíðu tvöfaldra skrifa fyrir **Viðskiptavinir V3 (lyklar)**, á flipanum **Töfluvarpanir**, á vinstri síunni, skal velja **Finance and Operations apps.Customers V3**. Í hægri síunni skal velja **Dataverse.Account**.
    2. Leitið að **contactperson** til að finna upprunareitinn **ContactPersonID**.
    3. Veljið **Aðgerðir** og veljið svo **Eyða**.

        ![Reitnum ContactPersonID eytt](media/cust_selfref3.png)

    4. Endurtakið þessi skref til að eyða reitnum **InvoiceAccount**.

        ![Reitnum InvoiceAccount eytt](media/cust_selfref4.png)

    5. Vistið breytingarnar í vörpunina.

2. Slökkvið á rakningu breytinga fyrir eininguna **Viðskiptavinir V3**.

    1. Á vinnusvæðinu **Gagnastjórnun** skal velja reitinn **Gagnatöflur**.
    2. Veljið eininguna **Viðskiptavinir V3**.
    3. Á aðgerðasvæðinu skal velja **Valkostir** og síðan velja **Breytingarakning**.

        ![Valkostur breytingarakningar valinn](media/selfref_options.png)

    4. Veljið **Gera breytingarakningu óvirka**.

        ![Gera breytingarakningu óvirka valið](media/selfref_tracking.png)

3. Keyrið upphaflega samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**. Upphafleg samstilling ætti að keyra með góðum árangri án nokkurra villna.
4. Keyrið upphaflega samstillingu fyrir vörpunina **CDS tengiliðir V2 (tengiliðir)**.

    > [!NOTE]
    > Tvær varpanir eru með sama heitið. Verið viss um að velja þá vörpun sem er með eftirfarandi lýsingu í flipanum **Upplýsingar**: **Sniðmát tvöfaldra skrifa fyrir samstillingu milli FO.CDS Tengiliður lánardrottins V2 og CDS.Contacts. Þarfnast nýs pakka \[Dynamics365SupplyChainExtended\].**

5. Bætið reitunum **InvoiceAccount** og **ContactPersonID** aftur við vörpunina **Viðskiptavinir V3 (Lyklar)** og vistið hana síðan. Nú eru báðir reitirnir **InvoiceAccount** og **ContactPersonId** aftur orðnir hluti af samstillingarsniði í beinni. Í næsta skrefi verður gerð upphafleg samstilling fyrir þessa reiti.
6. Keyrið aftur upphaflega samstillingu fyrir vörpunina **Viðskiptavinir V3 (Lyklar)**. Vegna þess að slökkt er á breytingarakningu, verða gögnin fyrir **InvoiceAccount** og **ContactPersonId** samstillt úr Finance and Operations-forritinu við Dataverse.
7. Til að samstilla gögnin fyrir **InvoiceAccount** og **ContactPersonId** úr Dataverse við forritið Finance and Operations þarf að nota gagnasamþættingarverk.

    1. Í Power Apps skal stofna gagnasamþættingarverk á milli **Sales.Account** og **Finance and Operations apps.Customers V3**. Gagnastefnan verður að vera frá Dataverse til Finance and Operations forritsins. Þar sem **InvoiceAccount** er ný eigind í tvöföldum skrifum gætirðu viljað sleppa upphaflegri samstillingu fyrir hana. Nánari upplýsingar er að finna í [Sameina gögn í Dataverse](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Eftirfarandi skýringarmynd sýnir verk sem uppfærir **CustomerAccount** og **ContactPersonId**.

        ![Gagnasamþættingarver til að uppfæra CustomerAccount og ContactPersonId](media/cust_selfref6.png)

    2. Bætið skilyrði fyrirtækis við síuna Dataverse megin þannig að einungis línur sem passa við síuskilyrði verða uppfærðar í Finance and Operations-forritinu. Til að bæta við síu skal velja síuhnappinn. Því næst, í svarglugganum **Breyta fyrirspurn** er hægt að bæta við síufyrirspurn á borð við **\_msdyn\_fyrirtæki\_gildi jafngildir „\<guid\>“**. 

        > [ATHUGASEMD] Ef síuhnappurinn er ekki til staðar skal stofna þjónustubeiðni til að biðja gagnasamþættingarteymið um að virkja síugetu leigjandans.

        Ef ekki er slegin inn síufyrirspurn fyrir **\_msdyn\_fyrirtæki\_gildi** verða allar línurnar samstilltar.

        ![Síufyrirspurn bætt við](media/cust_selfref7.png)

    Upphaflegri samstillingu línanna er nú lokið.

8. Í forritinu Finance and Operations skal kveikja aftur á rakningu breytinga fyrir eininguna **Viðskiptavinir V3**.
