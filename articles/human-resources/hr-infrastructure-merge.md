---
title: Dynamics 365 Human Resources yfirlit yfir sameiningu innviða
description: Þessi grein lýsir Microsoft Dynamics 365 Human Resources innviðasamrunanum.
author: twheeloc
ms.date: 10/24/2022
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
ms.openlocfilehash: e68b28bfde35b51605aa0b653265da6261b69a90
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819243"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources sameining innviða 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources útvegar verkfæri sem hjálpa starfsmannateymum að auka snerpu skipulagsheildar, umbreyta upplifun starfsmanna og hámarka mannauðsáætlanir til að skapa vinnustað þar sem fólk og fyrirtæki geta dafnað. Til að læra meira um Dynamics 365 Human Resources, sjá [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Umbreyttu upplifun starfsmanna.** Haltu í fremstu röð með því að styrkja stjórnendur og starfsmenn með tengdri sjálfsafgreiðsluupplifun sem ýtir undir þátttöku og vöxt.
- **Fínstilltu HR forrit.** Hjálpaðu til við að lækka rekstrarkostnað og búa til fólksmiðaða orlof og fjarveru, tíma, ávinning og bótastjórnunaráætlanir.
- **Auka snerpu í skipulagi.** Gerðu HR kleift að starfa með þeirri handlagni sem fyrirtækið krefst með því að nota Dataverse og Microsoft Power Platform til að miðstýra gögnum fólks og auka auðveldlega Dynamics 365 Human Resources.
- **Uppgötvaðu innsýn í vinnuafl.** Taktu gagnadrifnar ákvarðanir með því að greina og sjá fyrir fólki gögn á ríkulegum mælaborðum sem eru tiltæk í hvaða tæki sem er.

## <a name="human-resources-infrastructure-merge"></a>Samþætting innviða í Human Resources

Dynamics 365 Human Resources er sjálfstætt forrit sem nú notar aðra innviði en önnur fjármála- og rekstrarforrit, eins og Dynamics 365 Finance eða Dynamics 365 Supply Chain Management. Innviðasamruninn mun koma Dynamics 365 Human Resources inn í sama innviði og önnur fjármála- og rekstraröpp.

Til að læra meira um samruna mannauðsinnviða, sjá [Sameining starfsmannaframboða](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Fyrir svör við algengum spurningum, sjá [Algengar spurningar um samruna mannauðsinnviða](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Flutningur viðskiptavina á móti sameiningu viðskiptavina

Sem hluti af samruna innviða hefur allur möguleiki mannauðsforritsins verið aðgengilegur í fjármála- og rekstrarumhverfi. Viðskiptavinir geta flutt mannauðsumhverfi sitt með því að nota flutningsverkfærin sem eru fáanleg í Microsoft Dynamics Lifecycle Services. Þeir geta einnig valfrjálst sameinað gögn sín við núverandi fjármála- og rekstrarumhverfi. 

Flutningur viðskiptavina og sameining viðskiptavina eru mismunandi á eftirfarandi hátt:

- **Flutningur viðskiptavina** – Sjálfvirka flutningsverkfærin eru notuð til að framkvæma „lyfta-og-vakta flutning“ (hreyfingu) á gagnagrunni viðskiptavina frá mannauðsinnviði til fjármála- og rekstrarinnviða. Niðurstaðan er nýtt fjármála- og rekstrarumhverfi sem notar mannauðsgagnagrunn viðskiptavinarins. 
- **Sameining viðskiptavina** – Þetta viðbótarskref er ekki krafist af Microsoft. Það er gert að vild viðskiptavinarins og á eigin tímalínu viðskiptavinarins. Í þessu skrefi eru gögn viðskiptavina flutt inn í núverandi umhverfi, eins og fjármála- eða verkefnaumhverfi. Það er að mestu handvirkt og hægt að gera það með því að nota Data Management Framework (DMF) gagnaeiningar. 

## <a name="planning-a-human-resources-environment-migration"></a>Skipuleggja mannauðsumhverfi fólksflutninga

Sem hluti af innviðasamrunanum verður öllum viðskiptavinum gert að flytja núverandi mannauðsumhverfi sitt úr sjálfstæðu innviðunum. Til að hjálpa þessu ferli mælum við með því að þú notir sjálfvirk flutningsverkfæri í Lifecycle Services til að færa núverandi umhverfi þitt yfir í nýja innviði. 

Eftirfarandi hlutar veita frekari upplýsingar um hvernig á að nota Lifecycle Services verkfærin til að flytja sjálfstætt mannauðsumhverfi. 

Viðskiptavinir sem eru að skipuleggja flutning geta haft eftirfarandi væntingar:

- Allir viðskiptavinir þurfa að flytja sandkassaumhverfi áður en hægt er að flytja framleiðsluumhverfið. 
- Flutningatól gera aðeins kleift að flytja sandkassa í sandkassa og framleiðslu í framleiðslu. Þess vegna mun umhverfisgerð þín ákvarða hvaða umhverfi er hægt að flytja á viðeigandi hátt. 
- Viðskiptavinir geta flutt eins marga sandkassa og þarf áður en þeir flytja framleiðsluumhverfi sitt, að því tilskildu að marksandkassarauf sé tiltæk. Viðskiptavinir geta einnig eytt fluttum sandkassa og flutt aftur mörgum sinnum. 
- Ef sandkassaflutningur mistekst, eða ef þú vilt byrja upp á nýtt, geturðu eytt umhverfi á fjármála- og rekstrarinnviðum og flutt sama umhverfi aftur.
- Vefslóð starfsmannaumhverfisins þíns verður önnur eftir flutninginn.
- Skipuleggðu hæfilegan tíma í miðbænum fyrir flutning á framleiðsluumhverfi þínu. Áætlaður tími til að ljúka sjálfvirka flutningsferlinu er þrjár til fjórar klukkustundir. Tímaramminn er breytilegur, allt eftir gögnum fyrirtækisins þíns. Þú ættir að sannreyna þann tíma sem þarf við flutning á sandkassaumhverfinu þínu og gefa þér tíma fyrir öll handvirk viðbótarverk sem þarf að klára.

> [!IMPORTANT] 
> Þegar framleiðsluumhverfi hefur tekist að flytja til fjármála- og rekstrarinnviða er sjálfstætt framleiðsluumhverfi upprunans sjálfkrafa eytt. Þú ættir ekki að eyða fluttu framleiðsluumhverfinu. 

Ferlið við flutninginn er að mestu sjálfvirkt. Hins vegar munu viðskiptanotendur þínir þurfa að ljúka nokkrum handvirkum skrefum og staðfestingu eftir flutninginn.

Eftirfarandi handvirk skref verða að vera lokið:

- Búðu til nýtt Lifecycle Services verkefni fyrir flutninginn.
- Endurskoðaðu allar samþættingar í gamla umhverfi þínu yfir í nýja umhverfið með því að benda samþættingunni á nýju vefslóðina/endapunktana, byggt á hverri samþættingarstillingu.
- Endurnýjaðu gagnageymsluna fyrir innbyggðar Power BI skýrslur.
- Endurnýjaðu gagnaeiningalistann frá DMF vinnusvæðinu.
- Tengill á Lifecycle Services fyrir aðstoð.
- Búðu til fjárhagsdagatöl.

Meðan á sjálfvirka ferlinu stendur er eftirfarandi aðgerðum lokið og ætti að staðfesta þær:

- Gögn:

    - Afbrigði
    - Öryggishlutverk (þar á meðal sérsniðin hlutverk)
    - Verkflæði (þar á meðal tilkynningar)
    - Sérstillingar og vistaðar skoðanir
    - Færslur
    - Sérstillt svæði
    - Fylgiskjöl
    - Viðvaranir

- Gagnastjórnun - Komdu með þinn eigin gagnagrunn (BYOD).
- Eiginleikastjórnun - Virkir/óvirkir eiginleikar.
- Innfelld Power Apps.
- Power Platform tengd umhverfi stjórnendamiðstöðvar (aðeins framleiðsla).
- Runuvinnslur.
- Tóm fjárhagsbók er búin til fyrir hvern lögaðila. Sjálfgefin gengistegund og bókhaldsgjaldmiðill fyrir hverja fjárhagsbók eru stilltir.
- Ný reikningsyfirlit er sjálfkrafa búin til og tengd við **Hagbók** síðuna í hverjum lögaðila. Fjárhagsvíddir sem eru stilltar í mannauðsumhverfi þínu verða sjálfkrafa bætt við nýja reikningsuppbyggingu og tengdar við fjárhagsbókina. 

> [!NOTE]
> Fjárhagsbók er nauðsynleg á innviðum fjármála og rekstrar sem hluti af Dynamics 365 Finance vörunni. Sérsniðna víddarstýringin sem var til í Dynamics 365 Human Resources sjálfstæða forritinu er ekki tiltæk. Sameinaðir innviðir mannauðs eru háðir fjármálarökfræðinni til að sýna fjárhagsvíddir í **Human Resources** einingunni. Til að fræðast meira um reikningsyfirlit og fjárhagsvíddir, sjá [hér](../finance/general-ledger/plan-chart-of-accounts.md). 

## <a name="considerations"></a>Til athugunar

- Flutningur í umhverfi verður alltaf á nýjustu almennt fáanlegu (GA) útgáfunni. Það fer eftir flutnings- og prófunaráætlun þinni, ef flutningsfullgilding þín fyrir sandkassaumhverfi var á annarri útgáfu, mælum við með því að þú staðfestir sandkassaflutning á sömu útgáfu og framleiðsluumhverfið þitt. 
- Meðan á flutningi stendur verður fluttu umhverfið komið fyrir á sama svæði og upprunalega sjálfstæða mannauðsumhverfið.

## <a name="licensing"></a>Leyfisveiting

Engar breytingar eru á leyfisveitingum fyrir Dynamics 365 Human Resources á eftirfarandi sviðum: 

- **Lágmarkskröfur um leyfiskaup**
- **Leyfi fyrir framleiðslu- og sandkassaumhverfi** – Ef þú ert með fyrirliggjandi sjálfstæð mannauðsleyfi sem veitir eitt framleiðsluumhverfi og eitt sandkassaumhverfi, er sami fjöldi leyfa tiltækur á fjármála- og rekstrarinnviðum, kl. aukakostnaður.
- **Viðbótarsandkassaleyfi** – Ef þú hefur keypt viðbótarsandkassaleyfi fyrir sjálfstæða mannauðsforritið, er sami fjöldi sandkassaleyfa í boði fyrir staðlað samþykkispróf (sandkassa) umhverfi á fjármála- og rekstrarinnviðum, án aukakostnaðar. 
