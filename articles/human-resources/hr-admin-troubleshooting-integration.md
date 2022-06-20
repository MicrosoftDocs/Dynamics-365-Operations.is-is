---
title: Algengar spurningar um samþættingu við Finance
description: Þessi grein útskýrir hvaða gögn eru samstillt í samþættingu á Human Resources og Finance.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f150c87b6d4e6575bc61a8f36bdf344ebba9c571
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879280"
---
# <a name="integration-with-finance-faq"></a>Algengar spurningar um samþættingu við Finance


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Þessi grein svarar algengum spurningum um hvaða gögn eru samstillt hvenær Dynamics 365 Human Resources er samþætt við Dynamics 365 Finance.

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a>Get ég breytt Dynamics 365 Talent notanda í Power Apps?

Nr. Ef notanda Human Resources er breytt gæti samþætting milli Human Resources og Dataverse mistekist. Eftirfarandi tafla sýnir sjálfgefnar stillingar fyrir Talent notanda.

| Fullt nafn | Kenni umsóknar | Azure AD Kenni hlutar | URI forritskennis |
| --- | --- | --- | --- |
| Dynamics 365 for Talent | f9be0c49-aa22-4ec6-911a-c5da515226ff | 27fd8129-4b3c-43f7-b1bf-47495d3a049b | f9be0c49-aa22-4ec6-911a-c5da515226ff |

![Sjálfgefnar stillingar fyrir notanda Talent-forrits.](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a>Eru öll gögn samstillt eða bara sumar gagnaeiningar?

Undirsafn af gögnunum er samstillt. Fyrir lista yfir allar einingar, sjá [Samþætting við Dynamics 365 Finance](hr-admin-integration-finance.md).

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a>Af hverju sé ég engin gögn samstillt við Dataverse?

Sjálfgefið er að slökkt sé á samþættingu Dataverse í nýju umhverfi sem inniheldur ekki meðfylgjandi kynningargögn. Sjálfgefið er að kveikt sé á því í nýju umhverfi sem innihalda kynningargögn og samstilling gagna hefst þegar umhverfið er útvegað. Eftir að umhverfi þitt er tilbúið til að samstilla gögn geturðu kveikt á samþættingunni. Nánari upplýsingar er að finna í [Skilgreina Dataverse samþættingu](hr-admin-integration-common-data-service.md).

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a>Get ég búið til nýja vörpun án þess að nota sniðmátin?

Sniðmát eru upphafspunktur. Hægt er að búa til sitt eigið sniðmát, en alltaf er þörf á sniðmáti þegar samþættingarverk er búið til. Nánari upplýsingar um Data Integrator (DI), sniðmát og verk er að finna í [Samþætta gögn í Microsoft Dataverse](/powerapps/administrator/data-integrator).

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a>Er hægt að varpa fjárhagsvíddum í flutning milli Human Resources og Finance?

Sem stendur eru fjárhagsvíddir ekki í Dataverse og eru þar af leiðandi ekki hluti af sjálfgefna sniðmátinu. Þessi eining er fyrirhuguð en engin tímalína útgáfu er til eins og er.

Fyrir gögn sem eru í Finance en eru ekki til í Human Resources, skal tengja kerfin tvö saman með **Skilgreina tengla** í Human Resources.

![Varpa fjárhagsvíddum.](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a>Stundum þegar ég flyt inn starfsmenn fara þeir í óvirka starfskrafta í Finance. Af hverju?

Þú gætir fengið þessa villu ef starfsmenn hafa ekki virka skrá með starfsupplýsingum í Human Resources. Til að leysa þetta skal fara í **Starfsmannastjórnun \> Starfsmenn \> Starfsferill \> Stjórnun dagsetninga** og staðfesta að til sé virk skrá starfsupplýsinga.

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a>Ef ég vel að varpa eingöngu undirsafni af svæðum, munu breytingar sem gerðar eru á óvörpuðum reitum kveikja á samstillingu?

Samstilling gagna fylgir framkvæmdaráætlun. Samþættingin mun taka upp skrá ef eitthvert svæði í skránni breytist óháð því hvort svæðið er hluti af samþættingu vörpunar.

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a>Hvernig get ég sent einungis breytingar á virkum starfskrafti og ekki riftum skrám?

Með því að nota „Ítarleg fyrirspurn“ geturðu síað og mótað upprunagögn áður en þau eru send inn í staðsetninguna.

![Ítarleg fyrirspurn virkra starfskrafta.](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a>Get ég tilgreint hvaða svæði skal senda til Finance fyrir tiltekna einingu?

Hægt er að bæta við eða fjarlægja svæði úr samþættingarverkinu. Ekki öll gagnasvæði sem til eru í töflu Dataverse verða fyllt út í Human Resources.
Hægt er að fylla út viðbótargögn í gegnum Power Apps.

![Bæta við eða fjarlægja reiti í eða úr samþættingarverki.](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a>Ég setti upp samþættingu sem runuvinnslu en Human Resources missti tengingu við kerfi áfangastaðar. Hvernig get ég sent sama sett af breytingum til kerfi áfangastaðar?

Ekki er krafist sérstakrar uppsetningar fyrir meðhöndlun frávika. Data Integrator mun sjálfkrafa grípa og tilkynna villur sem gerast hjá uppruna og áfangastað og mun leyfa handvirkar endurtekningar. Hins vegar leyfir hún ekki handvirka gagnaleiðréttingu. Ef nauðsynlegt er að uppfæra gögn, þá ætti það að gerast annað hvort við uppruna eða áfangastað.

## <a name="can-i-set-up-bi-directional-integration"></a>Get ég sett upp samþættingu í báðar áttir?

Nei, samþætting er eins og er í einstefnu (mannauðs til fjármála og rekstrar). Hins vegar er sjálfgefið sniðmát í boði til að senda gögn frá Human Resources til Finance.

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a>Get ég leyft skráareyðingu sem hluta af samþættingu minni?

Nei, Data Integrator mun ekki sækja eyddar færslur fyrir gagnaflutning. Aðeins stofnun og uppfærslur á gögnum (UPSERT) eru innifaldar sem stendur.

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a>Get ég keyrt aftur framkvæmd með villum? Ef svo er, mun það senda heila skrá eða aðeins breytingarnar?

Fyrsta keyrsla Data Integrator er alltaf full keyrsla. Næstu keyrslur byggjast á rakningu breytinga. Við framkvæmd villukeyrslu eru færslurnar dregnar út samkvæmt umfangi keyrslunnar og nýjustu breytingar eru sendar út úr Dataverse.

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a>Þegar ég vista verkið fæ ég villuna: „Verk er með vörpunarvillur“. Hvað geri ég?

Athugaðu uppsetningu samþættingarlykla, gerðu nauðsynlegar breytingar á uppsetningunni og endurnýjaðu einingarnar í verkinu.

Þegar sjálfgefið sniðmát er notað verða samþættingarlyklarnir sjálfkrafa fluttir inn. Þetta vandamál getur komið fram þegar nýjum verkum eru bætt við núverandi sniðmát.

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a>Ef ég er með N fjölda lögaðila þar sem starfskraftar hafa vinnu, þarf ég að búa til vörpun fyrir hvern þeirra?

Já, fyrir hvern lögaðila í Finance þarf sérstakt samþættingarverk í gagnasamþættingu.

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a>Ég þarf að flytja gögn sem ekki eru hluti af sjálfgefna sniðmátinu sem Microsoft býður upp á. Get ég gert þetta?

Já, hægt er að bæta við eða fjarlægja svæði úr núverandi sniðmáti. Sniðmátinu má breyta til að innihalda viðbótarupplýsingar úr öðrum töflum Dataverse. Einingin verður að vera í Dataverse til að hún verði hluti af sniðmátinu. 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a>Ég var að stofna ný umhverfi Finance og Human Resources og ég fæ villuna: „Gagnagildið brýtur hömlur fyrir heilleika.“ Af hverju?

Ástæður þessarar villu geta falið í sér:

- Gagnaflutningurinn leiddi til tvítekningar á gögnum sem voru dregin út úr upprunanum (Dataverse).

- Gagnaflutningurinn hefur núll gildi fyrir svæði sem krafist er í Finance and Operations. Staðfestu að gögnin sem eru í Dataverse uppfylli kröfur Finance and Operations.

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a>Ef framkvæmdavillur koma upp og auðkenni starfsmanns samstilltist ekki, hvernig finn ég þá vinnsluferilinn sem inniheldur starfsmannafærsluna?

Data Integrator mun búa til mörg verk í Finance. Sambandið milli verks Data Integrator og verks Finance er einn á móti einum.

Rektu tímann frá framkvæmdaferil Data Integrator og leitaðu að vísinum -1 fyrir verk Finance. Ef verknúmerið er 9 í Data Integrator er vísirinn í Finance 8.

1. Sæktu vísi verksins úr Data Integrator (í þessu dæmi er hann „9“).

    ![Sæktu vísi verks úr Data Integrator.](media/CaptureTaskIndex.png)

2. Rektu tíma framkvæmdar fyrir verkið.

    ![Rektu tíma framkvæmdar fyrir verk.](media/CaptureTimeOfExecution.png)

3. Í Fjármálum skaltu bera kennsl á vísitölu - 1. Í þessu dæmi passar verkið með viðskeytið „8“ og tíma framkvæmdar með vísi „0“ við tíma framkvæmdar í skrefi 2.

    ![Auðkenna vísi.](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a>Eftir að hafa samþætt Human Resources og Finance, fæ ég ekki séð Human Resources-gögnin mín í Finance. Hvað geri ég?

Samþættingin við Finance er ferli í tveimur skrefum. Fyrst skaltu staðfesta að Human Resources-gögnin séu uppfærð og tiltæk í Dataverse. Þetta er nærri því samstilling í rauntíma og hægt er að sannprófa hana í Power Apps með því að líta á gögnin innan gagnataflanna.

![Gögn í Dataverse.](media/DataInCDS.png)

Ef gögnin birtast ekki eins og búist er við í Dataverse skaltu staðfesta að einingin sé studd í samþættingunni. Til að bæta við viðbótargögnum í Dataverse verður breyting af hálfu Windows að gerast.

Ef einingin er studd og gögnin eru tiltæk í Dataverse skaltu staðfesta að vörpunin sé rétt í Data Integrator. Ef vörpun samþættingar lítur vel út skaltu staðfesta að keyrsla á vinnslum gagnastjórnunar hafi tekist. Villur geta komið fram meðan á framkvæmd runuvinnslunnar stendur. Nánari upplýsingar um stjórnun gagna er að finna í [Gagnastjórnun](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a>Heimilisföngin fyrir starfsmennina mína eru rangar eftir að ég flyt þær inn í Finance. Hvað ætti ég að gera?

Númeraröðin fyrir **Staðsetningarkenni** notar sama mynstur í bæði Human Resources og Finance. Númeraröðin þarf að vera einkvæm á báðum hliðum, svo að það verði engir árekstrar á heimilisföngum við samþættingu gagna frá Dataverse til Finance and Operations.

Við innleiðingu á Human Resources skal staðfesta að númeraraðirnar séu ekki þær sömu í Human Resources og Finance. Staðfestið að allar númeraraðir séu ekki eins þar sem gögn kunna að vera í báðum kerfum.

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a>Þegar ég er bý til tengistillinguna mína, get ég ekki séð tenginguna í fellilista tengingarinnar. Hvað geri ég?

Gakktu úr skugga um að þegar þú býrð til tengingar þínar velurðu Dynamics 365 Finance og Dataverse.

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a>Við samstillingu starfsmanna fæ ég villurnar „CompanyInfo_FL er ekki til“ eða „Gildið '12/31/2154 11:59:59 pm‘ í reitnum „Lokadagur starfsmanns finnst ekki í tengdri töflu „Starfsmaður“.“ Hvað ætti ég að gera?

Gakktu úr skugga um að þú varpir í rétta lögaðila. Samstilling lögaðila er ekki hluti af sjálfgefna sniðmátinu, þannig að það er gert ráð fyrir að hver lögaðili sem er til staðar í Human Resources og Dataverse sé einnig til staðar í Finance. Gakktu einnig úr skugga um að þú veljir rétta lögaðila fyrir tengda tengistillingu.

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a>Eftir að verkefnið var sett upp virðist vörpun reita fyrir Finance vera tóm. Hvað ætti ég að gera?

Uppfæra gagnaeiningarnar í Finance með því að fara í **Gagnastjórnun \> Færibreytur ramma \> Einingastillingar \> Uppfæra einingalista.** Þetta ætti að taka nokkrar mínútur að klárast, síðan ættir þú að sjá þessar varpanir. Þetta mál kemur upp þegar ný verkefni eru búin til.

![Vörpun reits sem vantar.](media/MissingFieldMapping.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- Data Integrator (DI): 

  - [Samþætta gögn í Microsoft Dataverse](/powerapps/administrator/data-integrator)

  - [Villumeðhöndlun og úrræðaleit Data Integrator](/powerapps/administrator/data-integrator-error-management)

  - [Viðbrögð við DSR-beiðnum fyrir kerfismyndaða kladda í Power Apps, Microsoft Power Automate og Dataverse](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- Stjórnun gagna:

  - [Gagnastjórnun](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
