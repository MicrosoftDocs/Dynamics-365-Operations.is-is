---
title: Samþættu rödd viðskiptavinar inn á vefsíður rafrænna viðskipta
description: Þetta efni lýsir því hvernig á að samþætta Microsoft Dynamics 365 Customer Voice inn í Dynamics 365 Commerce síðum rafrænna viðskipta.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 272ec1a59ed45b2d2336dcfea16051d27011360f
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767924"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Samþættu rödd viðskiptavinar inn á vefsíður rafrænna viðskipta

[!include [banner](../includes/banner.md)]

Þetta efni lýsir því hvernig á að samþætta Microsoft Dynamics 365 Customer Voice inn í Dynamics 365 Commerce síðum rafrænna viðskipta.

Þú getur samþætt [Rödd viðskiptavinar](https://dynamics.microsoft.com/customer-voice/overview/) inn á netverslunarsíðuna þína til að safna, greina og fylgjast með viðbrögðum viðskiptavina í rauntíma. Til að byrja með samþættinguna verður þú að búa til reikning og velja Customer Voice verkefnasniðmát fyrir þá tegund endurgjafar sem þú vilt safna.

## <a name="integrate-the-customer-voice-service"></a>Samþætta Customer Voice þjónustuna

Til að búa til Customer Voice reikning skaltu fara á [Rödd viðskiptavinar](https://dynamics.microsoft.com/customer-voice/overview/), og fylgdu leiðbeiningunum.

Eftir að þú hefur búið til Customer Voice reikning og skráð þig inn er næsta skref að velja verkefnissniðmát fyrir þá tegund endurgjafar sem þú vilt safna.

Til að velja Customer Voice verkefnasniðmát skaltu fylgja þessum skrefum.

1. Farðu í [Viðskiptavinur Voice verkefni sniðmát síða](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Veldu **Byrja**.
1. Veldu verkefnissniðmát fyrir þá tegund endurgjöfar sem þú vilt safna og veldu síðan **Næst**.
1. Á **Senda** flipi, undir **Veldu innfellda snið**, veldu innfellingarsnið. The **Innbyggður kóða** reiturinn sýnir kóðann sem verður að vera felldur inn í Commerce site builder.

Dæmin í þessu efni nota **Reglubundin viðskiptavinakönnun** verkefnissniðmát og **Takki** embed snið.

Eftirfarandi sýnishorn sýnir **Reglubundin viðskiptavinakönnun** verkefni sniðmát síða, þar sem valkostur fyrir **Takki** embed snið er valið og innfellingskóðinn fyrir þann valkost birtist í **Innbyggður kóða** sviði. Þrjár aðskildar aðgerðir eru nauðsynlegar til að fella kóðann inn á síðurnar þínar, eins og lýst er í eftirfarandi köflum.

![Viðskiptavinur Rödd Reglubundin viðskiptavinakönnun síða með hnappinn valinn.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Fella inn ytri skriftu slóðina

Á öllum síðum vefsvæðis sem ættu að vera með Customer Voice könnun, verður þú að fella inn ytri handritsslóðina sem Customer Voice gaf upp í innfellingarkóðanum. Besta leiðin til að fella handritið inn á margar síður er að búa til brot í vefsvæðisgerð sem inniheldur ytri handritsslóðina og bæta síðan brotinu við viðeigandi síðusniðmát. Eftir að þú hefur birt uppfært sniðmát mun innfelldi ytri forskriftarkóðinn líkjast eftirfarandi dæmi á vefsvæðissíðum sem verða fyrir áhrifum.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Fyrir upplýsingar um brot, sjá [Unnið með brot](work-with-fragments.md).

> [!NOTE]
> Þú þarft aðeins að bæta slóðinni við brotið. Ytri skriftareiningin mun bæta hinum skriftukóðanum við.

Fylgdu þessum skrefum til að fella ytri handritsslóðina inn í brot.

1. Í Site builder, búðu til brot sem er byggt á [Ytri forskriftareining](script-module.md).
1. Í nýja brotinu skaltu velja **Sjálfgefin ytri forskrift** rifa.
1. Í **Sjálfgefin ytri forskrift** eignarglugga, í **Heimild handrits** reit, sláðu inn ytri handritsslóðina, eins og sýnt er á eftirfarandi sýnishorni.

    ![Ytri forskriftarslóð í reitnum Forskriftaruppspretta fyrir nýja brotið.](media/customer-voice-integration-2.png)

1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Veldu **Birta** að birta brotið.

Nýja brotið sem inniheldur innfellda ytri skriftublokkina er nú tilbúið til að bæta við viðeigandi síðusniðmát.

### <a name="embed-the-external-style-sheet-code"></a>Fella inn ytri stílblaðskóðann

Næst, á öllum síðum sem ættu að hafa Customer Voice könnun, verður þú að fella inn ytri stílblaðskóðann sem Customer Voice gaf upp í innfellda kóðanum. Eins og í fyrri hlutanum er besta leiðin til að fella ytri stílblaðskóðann inn á margar síður að búa til brot í vefsvæðisgerð sem inniheldur stílblaðskóðann og bæta síðan brotinu við viðeigandi síðusniðmát. Innbyggði ytri stílblaðskóðinn mun líkjast eftirfarandi dæmikóða.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Til að fella ytri stílblaðskóðann inn í brot skaltu fylgja þessum skrefum.

1. Í Site builder, búðu til brot sem er byggt á [Metatags mát](metatags-module.md).
1. Í brotinu skaltu velja **Sjálfgefin lýsimerki** rifa.
1. Í **Sjálfgefin lýsimerki** eignarglugga, í **Metamerki** reit, sláðu inn stílblaðskóðann, eins og sýnt er á eftirfarandi dæmi.

    ![Ytri stílblaðskóði í Meta tags reitnum fyrir nýja brotið.](media/customer-voice-integration-3.png)

1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Veldu **Birta** að birta brotið.

Nýja brotið sem inniheldur innfellda ytri stílblaðskóðann er nú tilbúið til að bæta við viðeigandi síðusniðmát.

### <a name="embed-the-inline-script-code"></a>Fella inn innbyggða skriftarkóðann 

Næst, á öllum síðum sem ættu að vera með Customer Voice könnun, verður þú að fella inn innbyggða forskriftarkóðann sem Customer Voice gaf upp í innfellda kóðanum. Eins og í fyrri köflum er besta leiðin til að fella inn innbyggða forskriftarkóðann inn á margar síður síðna að búa til brot í vefsmiði sem inniheldur innbyggða forskriftarkóðann og bæta síðan brotinu við viðeigandi síðusniðmát.

Í eftirfarandi dæmi um innbyggða forskriftarkóða, **KÖNNUN\_ LYKILL** er staðgengill. Gildið fyrir **KÖNNUN\_ LYKILL** ætti að passa við raunverulegan könnunarlykil sem Customer Voice gaf upp í innfellingarkóðanum. Síðasta línan kallar á kóðann til að birta könnunarhnappinn eftir eina sekúndu, til að tryggja að forskriftirnar hafi nægan tíma til að hlaðast inn. Það fer eftir könnuninni sem þú valdir, þú gætir líka þurft að bæta við eða uppfæra önnur lýsigögn, eins og nafn fyrirtækis.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Til að fella innbyggða forskriftarkóðann inn í brot skaltu fylgja þessum skrefum.

1. Í Site builder, búðu til brot sem er byggt á [Innbyggð skriftareining](script-module.md).
1. Í brotinu skaltu velja **Sjálfgefin innbyggð skrift** rifa.
1. Í **Sjálfgefin innbyggð skrift** eignarglugga, í **Innbyggt handrit** reit, sláðu inn innbyggða skriftarkóðann, eins og sýnt er á eftirfarandi sýnishorni.

    ![Innbyggður skriftarkóði í reitnum Inline skriftu fyrir nýja brotið.](media/customer-voice-integration-4.png)

1. Veldu **Vista** og síðan **Ljúka við breytingar**.
1. Veldu **Birta** að birta brotið.

Nýja brotið sem inniheldur innbyggða innbyggða forskriftarkóðann er nú tilbúið til að bæta við viðeigandi síðusniðmát.

## <a name="add-fragments-to-a-template"></a>Bættu brotum við sniðmát

Þegar þú hefur lokið við að búa til brotin sem innihalda Customer Voice innbyggða kóðann, verður þú að bæta þeim við síðusniðmátin sem tengjast síðunum þar sem þú vilt nota þau. Í eftirfarandi sýnishorni hefur sýnishorninu þremur verið bætt við sniðmát vöruupplýsingasíðu (PDP).

![Dæmi um brot bætt við PDP sniðmát.](media/customer-voice-integration-5.png)

Eftir að uppfært sniðmát hefur verið gefið út mun raddmæling viðskiptavinarins birtast á öllum síðum sem er stjórnað af sniðmátinu.

Fyrir upplýsingar um sniðmát, sjá [Vinna með sniðmát](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Stilltu öryggisstefnu fyrir efni

Sjálfgefið er að innihaldsöryggisstefna (CSP) leyfir ekki símtöl í aðra þjónustu nema frekari stillingar séu gerðar. Þess vegna, eftir að þú hefur birt uppfærð sniðmát, er líklegt að könnuninni verði ekki hlaðið á viðkomandi vefsíður. Til að skoða CSP-tengdar villur skaltu opna þróunartól vafrans þíns (F12) og fara síðan á síðu sem hefur könnunina. CSP-tengdar villur munu birtast í stjórnborðsúttakinu.

Fylgdu þessum skrefum til að stilla CSP í Site builder til að laga villurnar.

1. Fara til **Vefstillingar \> Viðbætur**.
1. Á **Innihaldsöryggisstefna** flipa, bæta við`https://customervoice.microsoft.com/` til **barn-src** tilskipun.
1. Bæta við`https://customervoice.microsoft.com/` til **frame-src** tilskipun.
1. Bæta við`https://mfpembedcdnmsit.azureedge.net` og **.azureedge.net** til **img-src** tilskipun.

Nánari upplýsingar er að finna í [Öryggisregla um innihald](manage-csp.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Ytri forskriftareining](script-module.md)

[Metatags-eining](metatags-module.md)

[Innbyggð skriftareining](script-module.md)

[Innihaldsöryggisstefna](manage-csp.md)

[Vinna með brot](work-with-fragments.md)

[Vinna með sniðmát](work-with-templates.md)
