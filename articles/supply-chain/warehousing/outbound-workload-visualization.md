---
title: Myndræn framsetning vinnuálags á útleið
description: Þessi grein veitir upplýsingar um sjónrænt vinnuálag á útleið. Þessi virkni gerir stjórnendum vöruhúsa og yfirmönnum kleift að búa til sérsniðin vinnuálagsgröf sem má nota til að fylgjast með framvindu núverandi vinnu og hversu mikið er eftir af vinnunni. Vöruhúsastjórnendur geta búið til mörg yfirlit og sett upp sjálfvirka endurnýjun að vild.
author: Mirzaab
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0e5a2cd2aa458217ff212d45c0dd13c9d0623bd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851334"
---
# <a name="outbound-workload-visualization"></a>Myndræn framsetning vinnuálags á útleið

[!include [banner](../includes/banner.md)]

Ítarlegir valkostir uppsetningar sem eru aðgengilegir á síðunni **Myndræn framsetning vinnuálags á útleið** gerir stjórnendum vöruhúsa og yfirmönnum kleift að búa til sérsniðin vinnuálagsgröf sem má nota til að fylgjast með framvindu núverandi vinnu og hversu mikið er eftir af vinnunni. Vöruhúsastjórnendur geta búið til mörg yfirlit og sett upp sjálfvirka endurnýjun að vild. Myndræn framsetning vinnuálags á útleið hentar til birtingar á síðum yfir afköst vöruhúss.

Hægt er að nota þessa virkni til að rekja framvindu tiltektarvinnu. Eiginleikinn er samþættur við starfsmannaumsjón og ef starfsmannaumsjón er uppsett getur myndræn framsetning vinnuálags á útleið sýnt útreikning á tímafjöldanum sem eftir er við tiltektarvinnuna sem er sýnd (síuð).

## <a name="turn-the-outbound-workload-visualization-feature-on-or-off"></a>Kveiktu eða slökktu á myndbirtingu vinnuálags á útleið

Frá og með Supply Chain Management útgáfu 10.0.25 er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að *Sjónmynd af vinnuálagi á útleið* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="set-up-outbound-workload-visualizations"></a>Stilla myndræna framsetningu vinnuálags á útleið

Þú býrð til síusafn (skjámyndir) til að setja upp myndrænar framsetningar og hannar síurnar þannig að hver og ein birtir ólíka gerð af greiningu. Hægt er að nota síðuna **Skilgreina síur** til að hanna síurnar.

Til að setja upp myndræna framsetningu vinnuálags á útleið skal fylgja þessum skrefum.

1. Opnaðu **Vöruhúsakerfi \> Vöktunarskýrslur vöruhúsa \> Myndræn framsetning vinnuálags á útleið**.

    Síðan **Framsetning vinnuálags á útleið** birtist. Þegar lokið er við að búa til tiltekinn fjölda af síum birtist myndræna framsetningin á þessari síðu. Hægt er að stofna eins margar síur og óskað er eftir. Allar síurnar sem þú býrð til eru vistaðar á notandareikningnum þínum til að hægt sé að nota þær síðar. Með öðrum orðum hefur hver notandi hefur eigin síur sem hann hefur stofnað. Þessum síum verður ekki deilt með öðrum notendum.

1. Á síðunni **Myndræn framsetning vinnuálags** á aðgerðasvæðinu, á flipanum **Síur** skal velja **Skilgreina síur**.
1. Á síðunni **Skilgreina síur** á aðgerðasvæðinu skal velja **Nýtt** til að bæta við síu og síðan stilla eftirfarandi svæði fyrir síuna:

    - **Töfluflokkur á x-ás** – Veljið töfluna sem inniheldur svæðið sem á að nota til að flokka x-ás-gildin.
    - **Töflusvæði á x-ás** – Af svæðum töflunnar sem þú valdir á svæðinu **Töfluflokkur á x-ás** skal velja svæðið sem á að nota til að flokka x-ás gildin.
    - **Töflugildi á x-ás** – Veljið töfluna sem inniheldur svæðið sem á að nota til að greina flokkana betur.
    - **Svæðisgildi á x-ás** – Af svæðum töflunnar sem þú valdir á svæðinu **Töfluflokkur á x-ás** skal velja svæðið sem inniheldur gildin sem á að nota til greiningar á hverjum flokki.
    - **Sjálfvirk endurnýjun** – Veldu hvort eigi að endurnýja myndrænu framsetninguna sjálfkrafa.
    - **Tími milli endurnýjana (í mínútum)** – Sláðu inn mínútufjöldann á milli sjálfvirkra endurnýjana.
    - **Birtingarstig** – Veljið hvort graf eigi að sýna opnar línur eða opna hausatalningu.
    - **Gerð tiltektar** – Þegar svæðið **Birtingarstig** er stillt á _Opnar línur_ skal velja hvort fjöldi opinna vinnulína í grafinu skuli innihalda upprunalega tiltekt, þrepaskipta tiltekt eða bæði upprunalega tiltekt og þrepaskipta tiltekt.
    - **Svæði** – Veljið svæðið til að hlaða graf fyrir.
    - **Vöruhúsakerfi** – Veljið vöruhúsið sem hlaða á graf fyrir.
    - **Dagsetningar sem taka á með** – Sláðu inn dagafjöldann aftur í tíma sem mynda á graf fyrir.
    - **Gerð verkbeiðni** – Veldu gerðir verkbeiðna á útleið sem á að sía.

    ![Stillingasíða sía.](media/work-viz-filters-1.png "Stillingasíða sía")

1. Lokaðu síðunni **Skilgreina síur** til að fara aftur á síðuna **Myndræn framsetning vinnuálags á útleið**.

    Síðan **Myndræn framsetning vinnuálags á útleið** sýnir núna gögn út frá nýju síustillingunum þínum. Nýja sían er nú tiltæk og er valin á svæðinu **Sía**. Eftirfarandi reitir eru tiltækir efst á grafinu:

    - **Sía** – Svæðið inniheldur allar síur sem þú hefur búið til hingað til. Veljið síu til að skoða gögn hennar í myndritinu.
    - **Síðast endurnýjað** – Þetta svæði sýnir dagsetninguna og tímann þegar upplýsingarnar í grafinu voru síðast uppfærðar.
    - **Áætlaður tími/rauntími** – Þegar vinnustaðlar eru settir upp í kerfinu skal stilla þennan valkost á *Já* til að sýna uppsafnaða áætlaðan tiltektartíma efst í hverjum dálki grafsins. Þessi valkostur er ekki tiltækur þegar vinnustaðlar eru ekki notaðir.

    ![Myndræn útfærsla dæma.](media/work-viz-chart.png "Myndræn útfærsla dæma")

1. Velja skal hvaða stiku sem er í grafinu til að skoða tengdar upplýsingar vinnulínu.

    ![Upplýsingar um vinnulínu.](media/work-viz-work-details.png "Upplýsingar um vinnulínu")

## <a name="example-outbound-workload-visualization-for-zones"></a>Dæmi: Myndræn framsetning vinnuálags á útleið

Í þessu dæmi á að setja upp myndræna framsetningu sem sýnir vinnulínur fyrir hvert svæði og stöðu hverrar vinnulínu fyrir sig (_Opin_, _Lokuð_, eða _Hætt við_). Í þessu tilvikum er hægt að setja upp síu með eftirfarandi stillingum:

- **Heiti síu** – Sláðu inn heiti fyrir þessa síu (eins og _svæði miðað við stöðu vinnu_).
- **Lýsing** – Sláðu inn stutta lýsingu fyrir þessa síu (eins og _svæði miðað við stöðu vinnu_).
- **Töfluflokkur á x-ás** – Veljið _Staðsetningar._
- **Flokkur fyrir X-ás** – Veljið _Svæðiskenni_.
- **Töflugildi á x-ás** – Veldu _Vinna_, því ætlunin er að skoða vinnu eftir svæðum.
- **Svæðisgildi á x-ás** – Veldu _Staða vinnu_, því ætlunin er að skoða stöðu vinnu.
- **Sjálfvirk endurnýjun** – Veldu hvort eigi að endurnýja myndrænu framsetninguna sjálfkrafa.
- **Gerð tiltektar** – Veldu _Upphafleg tiltekt og þrepaskipt tiltekt_, því ætlunin er að hafa með bæði upphaflega og þrepaskipta tiltekt úr staðsetningum sviðsetningar. Í öðrum orðum viltu hafa með allar tiltektarvinnulínur sem eru til.
- **Birtingarstig** – Veldu _Opnar línur_, því ætlunin er að skoða upplýsingar í hverri línu fyrir sig en ekki í hverjum vinnuhaus fyrir sig.

Eftirfarandi skýringarmynd sýnir dæmi um graf.

![Myndræn framsetning svæða miðað við stöðu vinnu.](media/work-viz-chart.png "Myndræn framsetning svæða miðað við stöðu vinnu")

Þetta graf sýnir tvö svæði sem kallast **GÓLF** og **MAGN**, auk svæðis sem kallast **Autt**. Svæðið **Autt** táknar allar vinnulínur sem eru ekki hluti af svæðum. Grafið sýnir alltaf ótengd síuð gögn sem **Auð** til að veita eins mikinn sýnileika og hægt er. Á svæðinu **Gólf** sýnir grafið þrjár lokaðar línur og fjórar opnar línur. Á svæðinu **MAGN** sýnir grafið fjórar lokaðar línur, eina opna línu og 24 línur sem var hætt við. Grafið sýnir að endingu átta lokaðar línur sem eru ekki hluti af svæði og eru því flokkaðar sem **Auðar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]