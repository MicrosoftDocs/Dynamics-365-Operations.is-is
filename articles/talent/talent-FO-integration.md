---
title: Algengar spurningar um samþættingu Dynamics 365 for Talent til Dynamics 365 for Finance and Operations
description: Þetta efnisatriði útskýrir hvaða gögn eru samstillt í samþættingu á Talent og Finance and Operations.
author: negudava
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aea025bc4898d6399e82030cf1f52b21949e014f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304873"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a>Algengar spurningar um samþættingu Dynamics 365 for Talent til Dynamics 365 for Finance and Operations

[!include [banner](includes/banner.md)]

Þetta efnisatriði svarar algengum spurningum sem tengjast gögnunum sem eru samstillt þegar Dynamics 365 for Talent er samþætt við Dynamics 365 for Finance and Operations.

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Eru öll gögn samstillt eða bara sumar gagnaeiningar?

Með Core Human Resources er undirsafn af gögnunum samstillt við. Fyrir lista yfir allar einingarnar skal sjá [Samþætting frá Dynamics 365 for Talent til Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).

Fyrir Attract og Onboard eru öll gögn staðbundin við Common Data Service (CDS) for Apps.

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Get ég búið til nýja vörpun án þess að nota sniðmátin?

Sniðmát eru upphafspunktur. Hægt er að búa til sitt eigið sniðmát, en alltaf er þörf á sniðmáti þegar samþættingarverk er búið til. Nánari upplýsingar um Data Integrator (DI), sniðmát og verk er að finna í [Samþætta gögn í Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a>Er hægt að varpa fjárhagsvíddum í flutning milli Talent og Finance and Operations?

Sem stendur eru fjárhagsvíddir ekki í CDS for Apps og eru þar af leiðandi ekki hluti af sjálfgefna sniðmátinu. Þessi eining er fyrirhuguð en engin tímalína útgáfu er til eins og er.

Fyrir gögn sem eru í Finance and Operations en eru ekki til í Talent, skal tengja kerfin tvö saman með **Skilgreina tengla** í Talent. Nánari upplýsingar um hvernig á að skilgreina tengla milli Talent og Finance and Operations er að finna í [Hvað er nýtt eða breytt í Dynamics 365 for Talent Core HR (31. október 2018)](whats-new-talent-october-31.md).

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a>Stundum þegar ég flyt inn starfsmenn fara þeir í óvirka starfskrafta í Finance and Operations. Af hverju?

Þú gætir fengið þessa villu ef starfsmenn hafa ekki virka skrá með starfsupplýsingum í Talent. Til að leysa þetta skal fara í **Starfsmannastjórnun \> Starfsmenn \> Starfsferill \> Stjórnun dagsetninga** og staðfesta að til sé virk skrá starfsupplýsinga.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Ef ég vel að varpa eingöngu undirsafni af svæðum, munu breytingar sem gerðar eru á óvörpuðum reitum kveikja á samstillingu?

Samstilling gagna fylgir framkvæmdaráætlun. Samþættingin mun taka upp skrá ef eitthvert svæði í skránni breytist óháð því hvort svæðið er hluti af samþættingu vörpunar.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Hvernig get ég sent einungis breytingar á virkum starfskrafti og ekki riftum skrám?

Með því að nota „Ítarleg fyrirspurn“ geturðu síað og mótað upprunagögn áður en þau eru send inn í staðsetninguna.

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a>Get ég tilgreint hvaða svæði skal senda til Finance and Operations fyrir tiltekna einingu?

Hægt er að bæta við eða fjarlægja svæði úr samþættingarverkinu. Ekki öll gagnasvæði sem til eru í einingu CDS for Apps (CDS 2.0) verða fylltir út frá Core HR.
Hægt er að fylla út viðbótargögn í gegnum PowerApps.

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Ég setti upp samþættingu sem runuvinnslu en Talent missti tengingu við kerfi áfangastaðar. Hvernig get ég sent sama sett af breytingum til kerfi áfangastaðar?

Ekki er krafist sérstakrar uppsetningar fyrir meðhöndlun frávika. Data Integrator mun sjálfkrafa grípa og tilkynna villur sem gerast hjá uppruna og áfangastað og mun leyfa handvirkar endurtekningar. Hins vegar leyfir hún ekki handvirka gagnaleiðréttingu. Ef nauðsynlegt er að uppfæra gögn, þá ætti það að gerast annað hvort við uppruna eða áfangastað.

## <a name="can-i-set-up-bi-directional-integration"></a>Get ég sett upp samþættingu í báðar áttir?

Nei, sem stendur er samþætting í aðra áttina (Talent til Finance and Operations). Hins vegar er sjálfgefið sniðmát í boði til að senda gögn frá Talent til Finance and Operations.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Get ég leyft skráareyðingu sem hluta af samþættingu minni?

Nei, Data Integrator mun ekki sækja eyddar færslur fyrir gagnaflutning. Aðeins stofnun og uppfærslur á gögnum (UPSERT) eru innifaldar sem stendur.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Get ég keyrt aftur framkvæmd með villum? Ef svo er, mun það senda heila skrá eða aðeins breytingarnar?

Fyrsta keyrsla Data Integrator er alltaf full keyrsla. Næstu keyrslur byggjast á rakningu breytinga. Við framkvæmd villukeyrslu eru færslurnar dregnar út samkvæmt umfangi keyrslunnar og nýjustu breytingar eru sendar út úr CDS.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Þegar ég vista verkið fæ ég villuna: „Verk er með vörpunarvillur“. Hvað geri ég?

Athugaðu uppsetningu samþættingarlykla, gerðu nauðsynlegar breytingar á uppsetningunni og endurnýjaðu einingarnar í verkinu.

Þegar sjálfgefið sniðmát er notað verða samþættingarlyklarnir sjálfkrafa fluttir inn. Þetta vandamál getur komið fram þegar nýjum verkum eru bætt við núverandi sniðmát.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Ef ég er með N fjölda lögaðila þar sem starfskraftar hafa vinnu, þarf ég að búa til vörpun fyrir hvern þeirra?

Já, fyrir hvern lögaðila í Finance and Operations þarf sérstakt samþættingarverk í gagnasamþættingu.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Ég þarf að flytja gögn sem ekki eru hluti af sjálfgefna sniðmátinu sem Microsoft býður upp á. Get ég gert þetta?

Já, hægt er að bæta við eða fjarlægja svæði úr núverandi sniðmáti. Sniðmátinu má breyta til að innihalda viðbótarupplýsingar úr öðrum einingum CDS for Apps. Einingin verður að vera í CDS for Apps til að hún verði hluti af sniðmátinu. 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Ég var að stofna ný umhverfi Finance and Operations og Talent og ég fæ villuna: „Gagnagildið brýtur hömlur fyrir heilleika.“ Af hverju?

Ástæður þessarar villu geta falið í sér:

- Gagnaflutningurinn leiddi til tvítekningar á gögnum sem voru dregin út úr upprunanum (CDS).

- Gagnaflutningurinn hefur núll gildi fyrir svæði sem krafist er í Finance and Operations. Staðfestu að gögnin sem eru í CDS uppfylli kröfur Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Ef framkvæmdavillur koma upp og auðkenni starfsmanns samstilltist ekki, hvernig finn ég þá vinnsluferilinn sem inniheldur starfsmannafærsluna?

Data Integrator mun búa til mörg verk í Finance and Operations. Sambandið milli verks Data Integrator og verks Finance and Operations er einn á móti einum.

Rektu tímann frá framkvæmdaferil Data Integrator og leitaðu að vísinum -1 fyrir verk Finance and Operations. Ef verknúmerið er 9 í Data Integrator er vísirinn í Finance and Operations 8.

1. Sæktu vísi verksins úr Data Integrator (í þessu dæmi er hann „9“).

![Sæktu vísi verks úr Data Integrator](media/CaptureTaskIndex.png)

2. Rektu tíma framkvæmdar fyrir verkið.

![Rektu tíma framkvæmdar fyrir verk](media/CaptureTimeOfExecution.png)

3. Í Finance and Operations skal finna vísi -1. Í þessu dæmi passar verkið með viðskeytið „8“ og tíma framkvæmdar með vísi „0“ við tíma framkvæmdar í skrefi 2.

![Auðkenna vísi](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a>Eftir að hafa samþætt Talent og Finance and Operations, sé ég ekki Talent-gögnin mín í Finance and Operations. Hvað geri ég?

Samþættingin við Finance and Operations er ferli í tveimur skrefum. Fyrst skaltu staðfesta að Talent-gögnin séu uppfærð og tiltæk í CDS. Þetta er nærri því samstilling í rauntíma og hægt er að sannprófa hana í PowerApps með því að líta á gögnin innan gagnaeininganna.

![Gögn í CDS](media/DataInCDS.png)

Ef gögnin birtast ekki eins og búist er við í CDS skaltu staðfesta að einingin sé studd í samþættingunni. Til að bæta við viðbótargögnum í CDS verður breyting af hálfu Windows að gerast.

Ef einingin er studd og gögnin eru tiltæk á CDS skaltu staðfesta að vörpunin sé rétt í Data Integrator. Ef vörpun samþættingar lítur vel út skaltu staðfesta að keyrsla á vinnslum gagnastjórnunar hafi tekist. Villur geta komið fram meðan á framkvæmd runuvinnslunnar stendur. Nánari upplýsingar um stjórnun gagna er að finna í [Gagnastjórnun](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a>Heimilisföngin fyrir starfsmennina mína eru rangar eftir að ég flyt þær inn í Finance and Operations. Hvað ætti ég að gera?

Númeraröðin fyrir **Staðsetningarkenni** notar sama mynstur í bæði Talent og Finance and Operations. Númeraröðin þarf að vera einkvæm á báðum hliðum, svo að það verði engir árekstrar á heimilisföngum við samþættingu gagna frá CDS til Finance and Operations.

Við innleiðingu á Talent skal staðfesta að númeraraðirnar séu ekki þær sömu í Talent og Finance and Operations. Staðfestið að allar númeraraðir séu ekki eins þar sem gögn kunna að vera í báðum kerfum.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Þegar ég er bý til tengistillinguna mína, get ég ekki séð tenginguna í fellilista tengingarinnar. Hvað geri ég?

Gakktu úr skugga um að þegar þú býrð til tengingar velurðu Dynamics 365 for Finance and Operations (sem stendur í forskoðun) og Common Data Service.

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Við samstillingu starfsmanna fæ ég villurnar „CompanyInfo_FL er ekki til“ eða „Gildið '12/31/2154 11:59:59 pm‘ í reitnum „Lokadagur starfsmanns finnst ekki í tengdri töflu „Starfsmaður“.“ Hvað ætti ég að gera?

Gakktu úr skugga um að þú varpir í rétta lögaðila. Samstilling lögaðila er ekki hluti af sjálfgefna sniðmátinu, þannig að það er gert ráð fyrir að hver lögaðili sem er til staðar í Talent og CDS sé einnig til staðar í Finance and Operations.
Gakktu einnig úr skugga um að þú veljir rétta lögaðila fyrir tengda tengistillingu.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a>Eftir að verkefnið var sett upp virðist vörpun reita fyrir Finance and Operations vera tóm. Hvað ætti ég að gera?

Uppfæra gagnaeiningarnar í Finance and Operations með því að fara í **Gagnastjórnun \> Færibreytur ramma \> Einingastillingar \> Uppfæra einingalista.** Þetta ætti að taka nokkrar mínútur að klárast, síðan ættir þú að sjá þessar varpanir. Þetta mál kemur upp þegar ný verkefni eru búin til.

![Vörpun reita vantar](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- Data Integrator (DI): 

  - [Samþætta gögn í Common Data Service fyrir Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [Villumeðhöndlun og úrræðaleit Data Integrator](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [Viðbrögð við DSR-beiðnum fyrir kerfismyndaða kladda í PowerApps, Microsoft Flow, og Common Data Service fyrir Apps](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Stjórnun gagna:

  - [Gagnastjórnun](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)