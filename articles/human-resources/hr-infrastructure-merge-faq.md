---
title: Algengar spurningar um sameiningu Dynamics 365 Human Resources tölvukerfis
description: Þessi grein svarar algengum spurningum um samruna innviða fyrir Microsoft Dynamics 365 Human Resources og fjármála- og rekstraröpp.
author: twheeloc
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32698d887b4d228ded588984b09068e3e2fef9a4
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702068"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Algengar spurningar um sameiningu Dynamics 365 Human Resources tölvukerfis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Hvað er Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources býður upp á verkfæri sem hjálpa starfsmannateymum að auka snerpu í skipulagi, umbreyta upplifun starfsmanna og hámarka mannauðsáætlanir til að skapa vinnustað þar sem fólk og fyrirtæki geta dafnað. Til að læra meira um Dynamics 365 Human Resources, sjá [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Umbreyttu reynslu starfsmanna.** Haltu í fremstu röð með því að styrkja stjórnendur og starfsmenn með tengdri sjálfsafgreiðsluupplifun sem ýtir undir þátttöku og vöxt.
- **Fínstilltu HR forrit.** Dragðu úr rekstrarkostnaði og búðu til fólksmiðaða orlofs- og fjarvistaráætlanir, tíma, ávinning og launastjórnun.
- **Auka snerpu í skipulagi.** Gerðu HR kleift að starfa með þeirri handlagni sem fyrirtækið krefst með því að nota Dataverse og Microsoft Power Platform til að miðstýra gögnum fólks og lengja auðveldlega Dynamics 365 Human Resources.
- **Uppgötvaðu innsýn í vinnuafl.** Taktu gagnadrifnar ákvarðanir með því að greina og sjá fyrir fólki gögn á ríkulegum mælaborðum sem eru tiltæk í hvaða tæki sem er.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Ávinningur og fríðindi vegna sameiningar tölvukerfis

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Hvað er sameining Dynamics 365 Human Resources tölvukerfis?

Eins og er eru tvö aðskilin sett af HR getu á tveimur mismunandi innviðum í Dynamics 365:

- **Dynamics 365 Human Resources**– Sjálfstætt app sem keyrir á sjálfstæðum innviðum. Þegar þetta forrit var opnað var innviði aðskilið frá öðrum Dynamics 365 rekstrarforritum. Viðskiptavinir okkar nota þetta forrit til að auka snerpu skipulagsheildar, fínstilla HR forrit, umbreyta upplifun starfsmanna og öðlast innsýn í vinnuafl.
- **HR mát** – Eldra sett af getu sem áður var hluti af Unified Operations licensing stock keeping unit (SKU). HR-einingin keyrir á fjármála- og rekstrarinnviðum, sem er eins í öllum rekstraröppum. Þessi forrit innihalda Dynamics 365 Finance,Dynamics 365 Project Operations, og Dynamics 365 Supply Chain Management. Viðskiptavinir fengu HR getu sem hluti af Dynamics 365 Finance eða Dynamics 365 Supply Chain Management.

Undanfarin þrjú ár hefur Microsoft engum nýjum möguleikum eða endurbótum bætt við HR-eininguna. Þess í stað hafa vegvísisfjárfestingar okkar beinst að Dynamics 365 Human Resources app.

Með því að koma þessum tveimur hæfileikum yfir á sama innviði munum við hjálpa viðskiptavinum að öðlast eftirfarandi kosti:

- Viðbætur sem hefur verið bætt við Dynamics 365 Human Resources á síðustu þremur árum, þar með talið aukið leyfi og fjarvistir, bótastjórnun og skýrslugerð.
- Bættur teygjanleiki í gegnum Microsoft Power Platform og getu til að auka viðskiptarökfræði til að sérsníða síður.
- Bætt uppsetning, uppfærslur og viðhald sem eru í samræmi hvað varðar líftímastjórnun forrita (ALM), lífsferilsþjónustu, landfræðilegt framboð og fleira.
- Meiri tækninýjungar þar sem verkfræðingateymi okkar notar sameiginlega þjónustu, verkfæri og minni kostnað á palli.

Þessi umskipti munu hafa áhrif á viðskiptavini sem eru að nota annað hvort Dynamics 365 Human Resources eða eldri mannauðseiningunni.

## <a name="glossary-of-terms-used-in-this-faq"></a>Orðalisti yfir hugtök sem notuð eru í þessum algengum spurningum

- **Dynamics 365 Human Resources**– Núverandi og framtíðarvara okkar sem býður markaðnum HR getu.
- **HR mát** – Safn af eldri getu sem áður var veitt leyfi með Sameinað aðgerðatilboðinu. Möguleikarnir eru virkjaðir þegar viðskiptavinur á Dynamics 365 Finance eða Dynamics 365 Supply Chain Management.
- **Fjármál og rekstrarinnviðir** – Þróunararkitektúrinn sem er notaður af rekstrarsafninu, þar á meðal Dynamics 365 Finance,Dynamics 365 Supply Chain Management, og Dynamics 365 Project Operations. Þessi innviði er sá sem verður notaður í framtíðinni. Í þessum algengum spurningum er hugtakið *sameinuð innviði* átt við fjármála- og rekstrarumhverfi.
- **Mannauðsinnviðir** – Þróunararkitektúrinn sem var sögulega notaður fyrir Dynamics 365 Human Resources app. Innviðasameiningarverkefnið hefur í för með sér Dynamics 365 Human Resources á innviði fjármála og rekstrar. Hætt verður við sjálfstæða innviði.

## <a name="general-questions-about-the-infrastructure-merge"></a>Almennar spurningar um innviðina sameinast

### <a name="will-customers-lose-any-features-or-capabilities"></a>Munu viðskiptavinir missa einhverja eiginleika eða getu?

Markmið okkar er að lágmarka áhrifin sem þessi umskipti hafa á viðskiptavini. Við munum ekki fjarlægja neina eiginleika eða möguleika. Það verður starfrænt jafnræði á milli Dynamics 365 Human Resources og HR einingunni. Í þeim tilvikum þar sem eiginleiki er til staðar í báðum innviðum, er Dynamics 365 Human Resources reynsla verður notuð.

### <a name="will-the-user-experience-change"></a>Mun upplifun notenda breytast?

Notendaupplifunin mun vera í samræmi við staðlaða Dynamics 365 pallupplifun. Þrátt fyrir að almenn upplifun fyrir mælaborðið og valmyndirnar verði áfram svipuð, mun hún vera í takt við hefðbundna Dynamics 365 Finance app upplifun. Leiðsögn mun innihalda bæði einingar og vinnusvæði, leyfa eftirlæti og fleira. The Dynamics 365 Human Resources vinnurými, svo sem **Starfsmannastjórnun** og **Fólk**, mun renna inn í innviði fjármála og rekstrar. Í framtíðinni verða nýir möguleikar afhentir í gegnum eiginleikastjórnun, sem gerir viðskiptavinum kleift að skoða nýja eiginleika og ákveða hverja þeir vilja nota. Fyrir frekari upplýsingar, sjá [Yfirlit yfir eiginleikastjórnun](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og [Notendaviðmótsskjöl](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Hvenær mun Dynamics 365 Human Resources sameiningu innviða verði lokið?

Innviðasamruninn mun rúlla út í áföngum til að gefa viðskiptavinum tíma til að skipuleggja og ljúka nauðsynlegum skrefum. Við byrjuðum að útfæra möguleika í Dynamics 2021 útgáfubylgju 2. Við ætlum að ljúka öllum vöruþróunaraðgerðum fyrir þetta verkefni fyrir lok 2022 útgáfubylgju 2. Athugið að tímalínur geta breyst. Fyrir nýjustu upplýsingarnar, sjá [útgáfuáætlanir](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Hvaða þjálfun og úrræði verða í boði til að aðstoða við sameiningu innviða?

Við munum útvega skjöl sem lýsa hverju skrefi innviðasameiningarferlisins í smáatriðum. Við munum útvega viðbótarþjálfunarúrræði, svo sem myndbönd og vinnustofur, eftir þörfum til að hjálpa viðskiptavinum og samstarfsaðilum við hnökralaus umskipti.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Verða breytingar á þróunarmöguleikum eftir að innviðasamruni er lokið?

Til að læra meira um þróunarmöguleika, sjá [Þróa og sérsníða heimasíðu](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Spurningar um framboð eiginleika

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Mun LinkedIn Talent Hub samþætting vinna á fjármála- og rekstrarinnviðum?

Nei, LinkedIn Talent Hub samþættingin verður ekki hluti af sameinuðum innviðum. Opinber forritunarviðmót (API) eru fáanleg til að byggja upp samþættingu við ráðningar- og umsækjendurakningarlausnir. Viðskiptavinir sem hyggjast nota LinkedIn Talent Hub ættu að vinna með Microsoft samstarfsaðila sínum að samþættingu með því að nota meðfylgjandi API. Fyrir frekari upplýsingar um ATS (Applicant Tracking System) samþættingarforritaskil, sjá [Kynning á API um samþættingu umsækjenda um rekja kerfi](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Mun hæfileikarnir sem eru nú aðeins fáanlegir í Dynamics 365 Human Resources (td orlofsstjórnun og fríðindastjórnun) vera tiltæk eftir að sameiningunni er lokið?

Já. Allt Dynamics 365 Human Resources verið er að færa umsóknarmöguleika til fjármála- og rekstrarinnviða. Eiginleikarnir verða aðgengilegir í áföngum. Til að fá uppfærðar upplýsingar um aðgengi að eiginleikum fyrir sameinaða innviðina skaltu skoða reglulega [útgáfuáætlanir](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Mun Ceridian samþættingar við Dynamics 365 Human Resources vera tiltækar eftir að innviðasamruni er lokið?

Ceridian er í því ferli að búa til V2 samþættingu við Dynamics 365 Human Resources sem nýtir sér Payroll API. Skráarsamþættingin sem nú er til í Dynamics 365 Human Resources verður ekki flutt til fjármála- og rekstrarinnviða. Frekari upplýsingar er að finna í [Kynning á API-launaskrá](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Verður rakning umsækjanda eða inn-/afstýring á virkni starfsmanns innifalin?

Í fyrri útgáfum bjuggum við til ATS Integration API til að gera samstarfsaðilum og viðskiptavinum kleift að búa til ATS samþættingu við mannauð. Viðbótar ATS-tengd virkni varð fáanleg í 2022 bylgju 1. Við munum halda áfram að bæta þessi API í komandi útgáfum.

HR virkni sem nú er til staðar í fjármála- og rekstrarinnviðum felur í sér nokkra ráðningarstjórnunarvirkni sem er ekki til í Dynamics 365 Human Resources. Þegar innviðasamruna er lokið verður þessi virkni í boði fyrir alla mannauðs viðskiptavini. Þessi virkni veitir létta ATS virkni. Hins vegar ætlum við ekki að auka þessa virkni í framtíðinni. Viðskiptavinir sem þurfa háþróaða virkni geta nýtt sér ATS samþættingu samstarfsaðila. Fyrir frekari upplýsingar um ATS samþættingu API, sjá [Kynning á API um samþættingu umsækjenda um rekja kerfi](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Mun Dynamics AX 2012 uppfærsluverkfæri til að uppfæra HR eininguna í AX 2012 til Dynamics 365 Human Resources app?

Já. Uppfærðu úr Dynamics AX 2012 til Dynamics 365 Human Resources mun fylgja sömu uppfærsluleið og verkfærum sem notuð eru til að uppfæra í nýjustu útgáfuna af öðrum Dynamics 365 rekstrarforritum, eins og Dynamics 365 Finance eða Dynamics 365 Supply Chain Management.

Fyrir frekari upplýsingar um flutninginn yfir í fjármála- og rekstrarinnviði, sjá [Algengar spurningar um flutning viðskiptavina mannauðs](./customer-migration.md).
