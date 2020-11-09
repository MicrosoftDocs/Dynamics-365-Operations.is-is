---
title: Hafist handa með innbót rafrænna reikninga
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7b2a3aae43d42060c7fcd9e1ea3db814fc5d8f22
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039847"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Hafist handa með innbót rafrænna reikninga

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu. Fyrst leiðir það þig í gegnum grunnstillingarskrefin í Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) og Dynamics 365 Finance. Því næst er lýst ferlinu við að senda skjöl inn í gegnum þjónustuna með því að nota Dynamics 365 Finance eða Dynamics 365 Supply Chain Management. Einnig verður fjallað um hvernig á að túlka innsendingarkladdana.

## <a name="availability"></a>Til ráðstöfunar

Innbót rafrænnar reikningsfærslu er í upphafi í boði fyrir nokkur lönd. Innbótin styður stofnun rafrænna reikninga og innsendingu eftirfarandi viðskiptaskjala:

| Land/svæði  | Viðskiptaskjal                          |
|-----------------|--------------------------------------------|
| Austurríki         | Sölu- og verkreikningar                 |
| Belgía         | Sölu- og verkreikningar                 |
| Brasilía          | Rafrænt fjárhagsskjalslíkan 55 (NF-e) |
| Danmörk         | Sölu- og verkreikningar                 |
| Eistland         | Sölu- og verkreikningar                 |
| Finnland         | Sölu- og verkreikningar                 |
| Frakkland          | Sölu- og verkreikningar                 |
| Þýskaland         | Sölu- og verkreikningar                 |
| Ítalía           | Sölu- og verkreikningar                 |
| Mexíkó          | CFDI-reikningur                               |
| Holland     | Sölu- og verkreikningar                 |
| Noregur          | Sölu- og verkreikningar                 |
| Spánn           | Sölu- og verkreikningar                 |
| Evrópa          | PEPPOL sölu- og verkreikningar          |
    
## <a name="licensing"></a>Leyfisveiting

Hægt er að nota viðbót rafrænnar reikningsfærslu með núverandi leyfi. Ekki er krafist frekari leyfa til að nota þjónustuna.

## <a name="prerequisites"></a>Forkröfur

Áður en farið er í gegnum skrefin í þessu efnisatriði þarf að halda eftirfarandi skilyrðum til haga:

- Aðgangur að LCS-reikningnum þínum.
- LCS-uppsetningarverk sem inniheldur Finance and Supply Chain Management, útgáfu 10.0.13 eða nýrri.
- Aðgangur að RCS-reikningnum þínum.
- Kveikja á altækum eiginleika fyrir RCS-reikninginn í gegnum eininguna **Eiginleikastjórnun**. Frekari upplýsingar er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md)
- Stofna tilfang lyklageymslu og geymslureikning í Azure. Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).

## <a name="overview"></a>Yfirlit

Eftirfarandi mynd sýnir fimm helstu skrefin sem verður farið í gegnum í þessu efnisatriði.

![Yfirlit yfir skrefin fimm í þessu efnisatriði](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Uppsetning á Azure-tilföngum:** Skilgreinið Azure-geymslu og upphleðslu stafrænna vottorða í Azure-lyklageymslu.
2. **LCS-Uppsetning:** Setjið upp innbótina fyrir smáþjónustu.
3. **RCS-Uppsetning:** Setjið upp umhverfið, notandaaðgang og eiginleika rafrænnar reikningsfærslu.
4. **Uppsetning biðlara:** Setjið upp tenginguna milli biðlarans og viðbót rafrænnar reikningsfærslu og slökkvið á gömlum eiginleikum til að senda inn og taka á móti svörum fyrir rafræn skjöl.
5. **Senda reikninga:** Sendið inn rafræn skjöl í gegnum viðbót rafrænnar reikningsfærslu og takið á móti svörum.

> [!NOTE]
> Sum grunnstillingarskrefin í þessu efnisatriði eru sameiginleg og óháð landi/svæði. Skrefin og uppsetningarferlið sem fer eftir landi/svæði er lýst í efnisatriðum sem taka tillit til lands/svæðis.

## <a name="lcs-setup"></a>LCS-uppsetning

1. Skráðu þig inn á LCS-reikninginn þinn.
2. Veljið reitinn **Stjórnun forskoðunareiginleika** og í reitahópnum **Eiginleikar opinnar forútgáfu** skal velja **BusinessDocumentSubmission**.
3. Merkið við reitinn **Virkja eiginleika forskoðunar**.
4. Veljið LCS-uppsetningarverkið. Áður en hægt er að velja verkið verður það að vera í gangi.
5. Í flýtiflipanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.
6. Veljið **Innsending viðskiptaskjals**.
7. Í svargluggann **Setja upp innbót** , í reitinn **AAD-forritskenni** , skal færa inn **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Gildið er fast.
8. Í reitinn **AAD-leigjandakenni** skal færa inn auðkenni Azure-áskriftareiknings.

    ![Setja upp svarglugga innbótar í LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

9. Velja þarf gátreitinn til að samþykkja skilmálana.
10. Velja **Setja upp**.

## <a name="rcs-setup"></a>RCS-uppsetning

Við RCS-uppsetningu verður farið í gegnum þessi skref:

1. Setjið upp lyklageymslu í RCS.
2. Setjið upp RCS-samþættingu með þjóni rafrænnar reikningsfærsluviðbótar.
3. Stofnið umhverfi rafrænnar reikningsfærsluviðbótar fyrir fyrirtækið þitt.

### <a name="set-up-the-key-vault-in-rcs"></a>Setja upp lyklageymslu í RCS

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækir eiginleikar** , undir **Umhverfi** , skal velja reitinn **Rafræn reikningsfærsla**.
3. Veljið **Þjónustuumhverfi**.

    ![Þjónustuumhverfi valin](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Valkosturinn **Tengd forrit** veitir aðgang að sjálfvirkri skilgreiningu á viðbót rafrænnar reikningsfærslu í Finance eða Supply Management í gegnum RCS. Þessi eiginleiki er hins vegar í þróun sem stendur.

4. Á aðgerðasvæðinu skal velja **Færibreytur lyklageymslu**.

    ![Færibreyta lyklageymslu valin](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Á aðgerðasvæðinu skal velja **Ný** til að bæta við lyklageymslu.
6. Í reitinn **URI lyklageymslu** skal færa inn gildi eigindarinnar **DNS-heiti** fyrir tilfang lyklageymslunnar sem var skilgreind í Azure. Upplýsingar um hvar hægt er að finna gildi fyrir **DNS-heiti** er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).

    ![Reitur URI lyklageymslu](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Í flýtiflipanum **Vottorð** skal velja **Bæta við** til að færa inn öll heiti stafrænna vottorða og leynilykla lyklageymslu sem þarf til að koma á öruggri tengingu. Í dálkinum **Gerð** er hægt að tilgreina hvort það er vottorð eða leynilykill. Bæði gildin eru skilgreind í tilfangi lyklageymslunnar í Azure.

    ![Vottorðum bætt við](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Ef reikningurinn þinn fyrir ákveðið land/svæði þarf vottorðakeðju til að nota stafræna undirskrift, skal velja **Vottorðakeðja** á aðgerðasvæðinu og síðan færa inn vottorðaröðina eða leynilykla lyklageymslunnar sem keðjan er gerð úr.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>Setja upp RCS-samþættingu með þjóni rafrænnar reikningsfærsluviðbótar

1. Á vinnusvæðinu **Altækir eiginleikar** , í hlutanum **Viðeigandi stillingar** , skal velja tengilinn **Færibreytur rafrænnar skýrslugerðar**.
2. Veljið **Smella hér til að tengjast við Lifecycle Service**. Ef ekki á að tengjast við LCS skal velja **Hætta við**.
3. Í flipanum **Rafræn reikningsfærsluþjónusta** , í reitinn **Endastöð URI þjónustu**. skal færa inn gildið samkvæmt tiltækum staðsetningum: `https://businessdocumentsubmission.us.operations365.dynamics.com/` eða `https://businessdocumentsubmission.eu.operations365.dynamics.com/`.
4. Í reitnum **Forritskenni** skal staðfesta að hann sýni kennið **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Gildið er fast.
5. Í reitinn **LCS-umhverfiskenni** skal færa inn auðkenni LCS-áskriftarreiknings.

![Færibreytur rafrænnar reikningsfærsluviðbótar færðar inn](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Bæta við umhverfi rafrænnar reikningsfærsluviðbótar

Hægt er að búa til mismunandi umhverfi fyrir viðbót rafrænnar reikningsfærslu, svo sem þróunar-, prófunar- eða framleiðsluumhverfi.

1. Á vinnusvæðinu **Altækir eiginleikar** , undir **Umhverfi** , skal velja reitinn **Rafræn reikningsfærsla**.
2. Veljið **Nýtt** til að búa til umhverfi.
3. Í reitinn **Reikningur SAS-lyklageymslu** skal færa inn heiti á leynilykli lyklageymslunnar sem var skilgreind í lyklageymslunni í RCS.

    ![Reitur SAS-lyklageymslureiknings](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. Í flýtiflipanum **Notendur** skal velja **Nýr** til að veita notendum aðgang að þessu umhverfi.

    ![Notendum þjónustu bætt við](media/e-invoicing-services-get-started-enter-service-users.png)

5. Á aðgerðasvæðinu skal velja **Birta** til að birta umhverfið á þjóni rafrænnar reikningsfærsluviðbótar.

    ![Birta hnapp](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>Uppsetning á eiginleika rafrænnar reikningsfærslu

„Eiginleiki rafrænnar reikningsfærslu“ er almennt heiti fyrir tilfangið sem er skilgreint og gefið út til að nota þjón rafrænnar reikningsfærsluviðbótar. Uppsetning á eiginleika rafrænnar reikningsfærslu sameinar meðal annars notkun á sniðum rafrænna skýrslugerðarskilgreininga til að búa til stillanlegar útflutnings- og innflutningsskrá, og notkun á aðgerðum og aðgerðarflæði til að virkja stofnun á stillanlegum reglum til að senda beiðnir, flytja inn svör og þátta innihald svara.

Vegna frávika í reikningssniðum og aðgerðarflæði er uppsetning á eiginleika rafrænnar reikningsfærslu breytileg eftir löndum/svæðum.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Setja upp samþættingu rafrænnar reikningsfærsluviðbótar í Finance eða Supply Chain Management 

Í þessari uppsetningu verða eftirfarandi verk kláruð:

1. Opna eiginleika tilraunaútgáfu
2. Kveikið á eiginleika fyrir samþættingu rafrænnar reikningsfærsluviðbótar til að virkja samþættingu við Finance.
3. Setjið upp vefslóð fyrir endastöð rafrænnar reikningsfærsluviðbótar.
4. Flytjið inn skilgreiningar rafrænnar skýrslugerðar sem tengjast eiginleika rafrænnar reikningsfærslu eftir landi/svæði.
5. Kveikið á viðeigandi eiginleika rafrænnar reikningsfærslu eftir landi/svæði.
6. Flytjið inn skilgreiningar rafrænnar skýrslugerðar og setjið upp svargerðirnar sem þarf til að uppfæra rafrænt skjal, sem er breytilegt eftir landi/svæði, í framhaldi af innsendingarferlinu.

### <a name="open-flighted-feature"></a>Opna eiginleika tilraunaútgáfu
Eiginleiki fyrir samþættingu rafræns reiknings er virkjaður með tilraunaútgáfu. Tilraunaútgáfa leyfir að kveikt eða slökkt er á eiginleika að sjálfgefnu. Eftirfarandi skref virkja tilraunaútgáfu í umhverfi sem er ekki framleiðsluumhverfi. 

1. Framkvæmið eftirfarandi SQL-skipun:

    SETJA INN Í SYSFLIGHTING (ÚTGÁFUHEITI, VIRKJAÐ) GILDI ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    SETJA INN Í SYSFLIGHTING (ÚTGÁFUHEITI, VIRKJAÐ) GILDI ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Þegar ofangreind breyting hefur verið gerð skal framkvæma IISReset á öllum AOS

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>Kveikið á eiginleika fyrir samþættingu rafrænnar reikningsfærsluviðbótar

1. Skráðu þig inn í Finance eða Supply Chain Management.
2. Á vinnusvæðinu **Eiginleikastjórnun** skal leita að nýja eiginleikanum, **Samþætting á stillanlegri rafrænni reikningsfærslu**. Ef eiginleikinn er enn ekki sýndur á síðu eiginleikastjórnunar skal keyra aðgerðina **Athuga með uppfærslur**
3. Veljið eiginleikann og veljið svo **Virkja núna**.

### <a name="set-up-the-service-endpoint-url"></a>Setja upp vefslóð fyrir endastöð þjónustu

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipann **Innsendingarþjónusta** , í reitinn **Vefslóð á endastöð þjónustu** , skal færa inn `https://businessdocumentsubmission.us.operations365.dynamics.com/`.
3. Í reitinn **Umhverfi** skal færa inn heiti á umhverfi rafrænnar reikningsfærsluviðbótar sem stofnað var í RCS-uppsetningu.

![Þjónustufæribreytur færðar inn](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>Flytja inn skilgreiningar rafrænnar skýrslugerðar

Til að gera kleift að safna saman viðskiptagögnum og senda þau til viðbótar rafrænnar reikningsfærslu, þarf fyrst að flytja inn gagnalíkan rafrænnar skýrslugerðar og skilgreiningu á gagnalíkani rafrænnar skýrslugerðar sem tengjast eiginleika rafrænnar reikningsfærslu, sem er breytilegur eftir landi/svæði, sem ætlunin er að nota.

1. Á vinnusvæðinu **Rafræn skýrslugerð** , í hlutanum **Veitendur skilgreininga** , skal velja reitinn **Microsoft**. Gangið úr skugga um að þessi skilgreiningarveita sé stillt á **Virk**. Frekari upplýsingar um hvernig á að stilla veitu á **Virk** er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Veldu **Geymslur**.
4. Veljið **Altækt tilfang** og síðan **Opna**.
5. Í svarglugganum **Tengjast við Lifecycle Services** skal velja **Smella hér til að tengjast við Lifecycle Services**.
6. Það fer eftir landi eða svæði sem nota á eiginleika rafrænnar reikningsfærslu, en flytja þarf inn viðeigandi gagnalíkan, gagnalíkanavörpun og snið. Upplýsingar um skilgreiningar rafrænnar skýrslugerðar sem á að flytja inn er að finna í lands-/svæðismiðaða efnisatriðinu „Hafist handa með viðbót rafrænnar reikningsfærslu“.
7. Flytjið inn **Samhengislíkan viðskiptavinareiknings**. Þetta líkan inniheldur viðbótarfæribreytur sem lýsa meðal annars umhverfinu í Finance sem er notað fyrir viðbót rafrænnar reikningsfærslu þegar viðskiptagögn eru send inn.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>Kveikja á lands-/svæðisbundnum eiginleikum rafrænnar reikningsfærslu

Til að kveikja á lands-/svæðisbundnum eiginleikum rafrænnar reikningsfærslu þannig að þeir vinni með viðbót rafrænnar reikningsfærslu, þarf að kveikja á eiginleikanum í hverjum lögaðila fyrir sig þar sem á að nota hann. Í kjölfarið verður ekki lengur hægt að nota gömlu samþættingu rafrænnar reikningsfærslu og kveikt er á samþættingunni við nýja viðbót rafrænu reikningsfærslunnar.

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipanum **Eiginleikar** , í línunni fyrir eiginleikann sem tengist lands-/svæðisbundnum eiginleika rafrænnar reikningsfærslu, skal velja gátreitinn í dálknum **Virkjað**. Upplýsingar um hvaða eiginleika skal kveikja á er að finna í lands-/svæðisbundna efnisatriðinu „Hafist handa með viðbót rafrænnar reikningsfærslu“.

![Kveikt á eiginleika rafrænnar reikningsfærslu](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Ef margir lögaðilar eru skilgreindir fyrir mismunandi lönd eða svæði, er hægt að kveikja á lands-/svæðisbundnum eiginleika rafrænnar reikningsfærslu fyrir hvern lögaðila fyrir sig.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>Flytja inn skilgreiningar rafrænnar skýrslugerðar og setja upp svargerðir til að uppfæra lands-/svæðisbundið reikningsskjal

Ef innsent reikningsskjal krefst uppfærslu eftir svar við innsendingu til heimildarþjónustu yfirvalda, þarf að flytja inn sérstakt gagnalíkan rafrænnar skýrslugerðar til að virkja stöðu reikningsskjalsins eða einhvern annan viðbótarreit sem á að uppfæra.

1. Á vinnusvæðinu **Rafræn skýrslugerð** , í hlutanum **Veitendur skilgreininga** , skal velja reitinn **Microsoft**.
2. Veldu **Geymslur**.
3. Veljið **Altækt tilfang** og síðan **Opna**.
4. Flytjið inn **Líkan svarskilaboða** , **Innflutningssnið svarskilaboða** , **Líkanavörpun svarskilaboða á áfangastað** og **Innflutningssnið innihalds skáar**.
5. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
6. Í flipanum **Rafrænt skjal** skal velja **Bæta við** til að færa inn heiti töflunnar sem tengist lands-/svæðisbundnu reikningsskjali. Upplýsingar um hvaða töfluheiti skulu valin er að finna í lands-/svæðisbundna efnisatriðinu „Hafist handa með viðbót rafrænnar reikningsfærslu“.
7. Veljið **Svargerðir** til að skilgreina svargerðirnar. Upplýsingar um hvaða töfluheiti skulu valin er að finna í lands-/svæðisbundna efnisatriðinu „Hafist handa með viðbót rafrænnar reikningsfærslu“.

![Svargerðir settar upp](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>Heiti eiginleika rafrænnar reikningsfærslu eftir landi 
Eftirfarandi tafla útskýrir öðrum eiginleikum rafrænnar reikningsfærslu sem er hægt að sækja úr altækri geymslu rafrænnar skýrslugerðar til að búa til rafræna reikninga.
Í RCS er hægt að sækja eiginleika rafrænnar reikningsfærslu sem er að finna í þessari töflu, skilgreiningar rafrænnar skýrslugerðar og uppsetningar á tiltækum eiginleikum rafrænnar reikningsfærslu.
Í Finance er hægt að virkja tengdar tilvísanir í eiginleika á síðunni **Færibreytur rafrænna skjala** til að gefa út rafræna reikninga fyrir þessi lönd. Frekari upplýsingar er að finna í hlutanum [Kveikja á lands-/svæðisbundnum eiginleikum rafrænnar reikningsfærslu](#region-specific) fyrr í þessu efnisatriði.

| Heiti eiginleika                      | lýsing                                 | ER grunnstillingar                                                                                                  | Uppsetningar                                                                                                                                                         | Land/svæði  | Tilvísun eiginleika      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Rafrænir reikningar í Austurríki (AT) | Sölu- og verkreikningar fyrir Austurríki      | - OIOUBL sölureikningur <br>- OIOUBL verkreikningur <br>- OIOUBL sölukreditnóta <br>- OIOUBL kreditnóta verks | - Myndun sölureiknings (AT) <br>- Myndun verkreiknings (AT) <br>- Myndun sölukreditnótu (AT) <br>- Myndun kreditnótu verks (AT)         | Austurríki         | EUR-00023              |
| Belgískur rafrænn reikningur (BE)   | Sölu- og verkreikningar fyrir Belgíu      | - UBL sölureikningur BE <br>- UBL verkreikningur BE <br>- UBL kreditnóta verks BE <br>- UBL sölukreditnóta BE | - Myndun sölureiknings (BE)<br>- Myndun verkreiknings (BE) <br>- Myndun sölukreditnótu (BE) <br>- Myndun kreditnótu verks (BE)         | Belgía         | EUR-00023              |
| Danskur rafrænn reikningur (DK)    | Sölu- og verkreikningar fyrir Danmörku      | - OIOUBL sölureikningur <br>- OIOUBL verkreikningur <br>- OIOUBL sölukreditnóta <br>- OIOUBL kreditnóta verks | - Myndun sölureiknings (DK) <br>- Myndun verkreiknings (DK) <br>- Myndun sölukreditnótu (DK)<br>- Myndun kreditnótu verks (DK)         | Danmörk         | EUR-00023<br> DK-00001 |
| Hollenskur rafrænn reikningur (NL)     | Sölu- og verkreikningar fyrir Holland  | - UBL sölureikningur NL <br>- UBL verkreikningur NL <br>- UBL sölukreditnóta NL <br>- UBL kreditnóta verks NL | - Myndun sölureiknings (NL) <br> - Myndun verkreiknings (NL) <br> - Myndun sölukreditnótu (NL) <br>- Myndun kreditnótu verks (NL)          | Hollandi | EUR-00023              |
| Eistneskur rafrænn reikningur (EE)  | Sölu- og verkreikningar fyrir Eistland      | - Sölureikningur (EE) <br> - Verkreikningur (EE)                                                                     | - Myndun sölureiknings (EE) <br>- Myndun verkreiknings (EE)                                                                                           | Eistland         | EUR-00023              |
| Finnskur rafrænn reikningur (FI)   | Sölu- og verkreikningar fyrir Finnland      | - Sölureikningur (FI) <br>- Myndun verkreiknings (FI)                                                          | - Myndun sölureiknings (FI) <br>- Myndun verkreiknings (FI)                                                                                           | Finnland         | EUR-00023              |
| Franskur rafrænn reikningur (FR)    | Sölu- og verkreikningar fyrir Frakkland    | - UBL sölureikningur FR <br> - UBL verkreikningur FR <br> - UBL sölukreditnóta FR <br>- UBL kreditnóta verks FR | - Myndun sölureiknings (FR) <br> - Myndun verkreiknings (FR) <br>- Myndun sölukreditnótu (FR) <br>- Myndun kreditnótu verks (FR)         | Frakkland          | EUR-00023              |
| Þýskur rafrænn reikningur (DE)    | Á vsk- og verkreikninga      |- Sölureikningur (DE) <br> - Verkreikningur <DE>                                                                     | - Myndun sölureiknings (DE) <br>- Myndun verkreiknings (DE)                                                                                           | Þýskaland         | EUR-00023              |
| Norskur rafrænn reikningur (NO) | Sölu- og verkreikningar fyrir Noreg       | - OIOUBL sölureikningur <br>- OIOUBL verkreikningur <br>- OIOUBL sölukreditnóta <br>- OIOUBL kreditnóta verks | - Myndun sölureiknings (NO) <br>- Myndun verkreiknings (NO) <br>- Myndun sölukreditnótu (NO) <br>- Myndun kreditnótu verks (NO)          | Noregur          | EUR-00023<br> NO-00010 |
| Spænskur rafrænn reikningur (ES)   | Sölu- og verkreikningar fyrir Spán        | - Sölureikningur (ES) <br>- Verkreikningur (ES)                                                                     | - Myndun sölureiknings (ES) <br>- Myndun verkreiknings (ES)                                                                                           | Spánn           | EUR-00023 <br>ES-00025 |
| Ítalskur rafrænn reikningur (IT)   | Sölu- og verkreikningar fyrir Ítalíu        | - (Forskoða) Sölureikningur (IT) <br> - Verkreikningur (IT)                                                           | - Sölureikningur <br> - Verkreikningur                                                                                                                           | Ítalía           | EUR-00023 <br>IT-00036 |
| PEPPOL rafrænn reikningur         | Myndun PEPPOL sölu- og verkreikninga | - PEPPOL sölureikningur <br>- PEPPOL verkreikningur <br>- PEPPOL sölukreditnóta <br> - PEPPOL kreditnóta verks | - Myndun PEPPOL sölureiknings <br>- Myndun PEPPOL verkreiknings <br>- Myndun PEPPOL sölukreditnótu <br>- Myndun PEPPOL kreditnótu verks |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Úrvinnsla rafrænnar reikningsfærslu í Finance og Supply Chain Management

Við úrvinnslu er þessum verkum lokið:

1. Sendið inn viðskiptaskjal (reikning) í gegnum viðbót rafrænnar reikningsfærslu.
2. Skoða keyrslukladda fyrir sendingar.

### <a name="submit-business-documents"></a>Senda inn viðskiptaskjöl

Við reglubundna innsendingarferlið eru samskiptin milli biðlara og viðbótar rafrænnar reikningsfærslu í báðar áttir. Tilgangurinn er að vinna tvö meginverk við innsendingu á rafrænum skjölum:

1. Sendið öll rafræn skjöl sem bíða sendingar úr Finance og sem eru með rétta stöðu til sendingar og uppfylla valskilyrðin.
2. Flytjið inn, í Finance, svarið sem viðbót rafrænnar reikningsfærslu skilar fyrir rafrænu skjölin sem voru send inn. Eftir innflutning eru svörin þáttuð og staða viðskiptaskjalanna er uppfærð í samræmi við það.

Hægt er að senda inn viðskiptaskjöl annaðhvort handvirkt eða samkvæmt kröfum áætlunar.

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Senda inn rafræn skjöl**.
2. Fyrir fyrstu innsendingu á skjali skal alltaf stilla valkostinn **Senda skjöl inn aftur** á **Nei**. Ef senda þarf skjal inn aftur í gegnum þjónustuna skal stilla þennan valkost á **Já**.
3. Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann **Fyrirspurn** þar sem hægt er að búa til fyrirspurn til að velja skjöl til innsendingar.

![Svarglugginn fyrir innsendingu rafrænna skjala](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Síufyrirspurn

1. Í svargluggann **Fyrirspurn** , í flipann **Svið** , skal færa inn síuskilyrði með því að nota reitina **Tafla** , **Afleidd tafla** , **Reitur** og **Skilyrði**.
2. Veljið **Bæta við** til að bæta við eins mörgum skilyrðum til viðbótar og þörf er á til að velja viðskiptaskjölin.

    ![Síuskilyrði innsendingar stillt](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Veljið **Í lagi** til að loka svarglugganum **Fyrirspurn**.
4. Veljið **Í lagi** til að senda valin viðskiptaskjöl inn í rafræna reikningsfærsluviðbótina.

    > [!NOTE]
    > Í fyrstu tilraun til að senda inn skjal í gegnum þjónustuna verður beðið um að staðfesta tenginguna við viðbót rafrænnar reikningsfærslu. Veljið **Smelltu hér til að tengjast sendingarþjónustu rafrænna skjala**.
    >
    > ![Tengjast við glugga þjónustuskilaboða fyrir sendingarþjónustu rafræns skjals](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Ef tengingin heppnast birtast staðfestingarboð.
    >
    > ![Staðfesting á tengingu við viðbót rafrænnar reikningsfærslu](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Lokið svarglugganum.

> [!NOTE]
> Eftir hverja sendingu sýnir aðgerðamiðstöðin fjölda innsendra skjala.
>
> ![Skilaboð aðgerðamiðstöðvar](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Innsending eftir runu

Í stað þess að senda skjöl handvirkt í vinnslu er hægt að gera sendingarferlið sjálfvirkt og keyra það í bakgrunni samkvæmt skilgreindri tíðni á runukeyrslu.

1. Í svarglugganum **Senda inn rafræn skjöl** , í flýtiflipanum **Keyra í bakgrunni** , skal stilla valkostinn **Runuvinnsla** á **Já**.
2. Í flipanum **Endurtekning** skal skilgreina tíðni runuvinnslunnar.

![Uppsetning innsendingar eftir runu](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Skoða alla innsendingarkladda

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.
2. Í reitnum **Gerð skjals** skal velja gerð skjalsins til að sía eftir.

    ![Gerð skjals sem er valin til að skoða innsendingarkladda fyrir](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > Gildið sem er sýnt í dálknum **Staða innsendingar** táknar stöðuna sem tengist fullnustu á innsendingarferlinu sjálfu. Það gefur til kynna hvort flæði aðgerða sem eru skilgreindar í RCS var keyrt til enda, óháð því hvort rafræna skjalið var samþykkt eða því hafnað. Gildið í dálknum **Staða innsendingar** stendur ekki fyrir stöðu innsends skjals. Hægt er að skoða stöðu á innsendu skjali (þ.e. hvort skjalið var samþykkt eða hafnað) í flýtiflipanum **Úrvinnsla aðgerðarkladda** í upplýsingum um innsendingarkladda eins og lýst er hér í framhaldinu.

3. Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu**.
4. Skoðið upplýsingar innsendingarkladdans.

    ![Upplýsingar um sendingu](media/e-invoicing-services-get-started-view-submission-log-form.png)

Niðurstöðurnar sem eru sýndar í sendingarkladdanum fara eftir því hvernig eiginleiki rafrænnar reikningsfærslu var settur upp í RCS. Hins vegar, án tillits til uppsetningarinnar, er innsendingarkladdinn alltaf með þrjá flýtiflipa:

- **Vinnsluaðgerðir** - Þessi flýtiflipi sýnir keyrslukladdann fyrir aðgerðirnar sem eru skilgreindar í útgáfu eiginleikans sem var sett upp í RCS. Dálkurinn **Staða** sýnir hvort tekist hafi að keyra aðgerðina.
- **Aðgerðaskrár** – Þessi flýtiflipi sýnir milliskrárnar sem voru myndaðar við keyrslu aðgerðanna. Hægt er að velja **Skoða** til að hlaða niður skránni og skoða innihald hennar.
- **Aðgerðarkladdi vinnslu** - Þessi flýtiflipi sýnir niðurstöður samskiptanna milli viðbótar rafrænnar reikningsfærslu og tilheyrandi vefþjónustu. Hann sýnir einnig hverju úrvinnsla vefþjónustunnar skilaði.

## <a name="related-topics"></a>Tengd efnisatriði

- [Yfirlit innbótar rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Brasilíu](e-invoicing-bra-get-started.md)
- [Hafist handa með innbót rafrænna reikninga fyrir Mexíkó](e-invoicing-mex-get-started.md)
- [Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Ítalíu](e-invoicing-ita-get-started.md)
- [Setja upp viðbót rafrænnar reikningsfærslu](e-invoicing-setup.md)
