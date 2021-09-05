---
title: Hafist handa með rafrænr reikningsfærslur fyrir Brasilíu
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með rafrænni reikningsfærslu fyrir Brasilíu í Finance and Supply Chain Management.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ccf2a78a5ffdb95b334f751944fdd010bf8cbf01
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345198"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Hafist handa með rafrænr reikningsfærslur fyrir Brasilíu 

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Brasilíu. Efnisatriðið leiðir þig í gegnum skilgreiningarskrefi sem eru landsmiðuð í Regulatory Configuration Services (RCS) og bætast ofan á skrefin sem lýst er í efnisatriðinu [Hafist handa með rafrænni reikningsfærslu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landsbundin skilgreining fyrir eiginleika rafrænnar reikningsfærslu fyrir brasilískt NF-e (BR)

Sumar færibreyturnar úr **rafræna reikningseiginleikanum fyrir Brasilískt NF-e (BR)** eru birtar með sjálfgefnum gildum. Farið yfir gildin og, ef þörf krefur, uppfærið gildin svo þau endurspegli betur fyrirtækjareksturinn áður en rafræni reikningseiginleikinn er notaður í þjónustuumhverfinu.

Þessi hluti tengist **Landsbundin skilgreining fyrir eiginleika rafrænnar reikningsfærslu** hlutanum í efnisatriðinu [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki**, skal velja reitinn **Rafræn reikningsfærsla**.
2. Á síðunni **Eiginleikar fyrir rafræna reikningsfærslu** skal staðfesta að rafræni reikningsfærslueiginleikinn **Brasilískt NF-e (BR)** sem var stofnaður sé valinn.
3. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
4. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja **Senda inn** og síðan velja **Breyta**.
5. Í flipanum **Aðgerðir**, í reitahópnum **Aðgerðir**, skal velja aðgerðina **(Forútgáfa) Skrifa undir xml-skjal**.
6. Í reitahópnum **Færibreytur** skal velja **Heiti vottorðs** og í reitinn **Gildi** skal færa inn heiti vottorðs sem tengist færibreytu lyklageymslunnar.
7. Í flipanum **Aðgerðir**, í reitahópnum **Aðgerðir** skal velja **(Forútgáfa) Hringja í SEFAZ-þjónustu í Brasilíu**.
8. Í reitahópnum **Færibreytur** skal velja færibreytuna **Veffang**.
9. Í reitnum **Gildi**, ef nauðsynlegt, skal fara yfir og uppfæra vefslóð vefþjónustnnar sem SEFAZ-fylgiskjölin birta fyrir fylkið þitt og velja **Vista**.
10. Í flipanum **Gildissviðsreglur**, í reitahópnum **Setja upp gildissviðsreglu**, skal fara yfir og uppfæra reitarskilyrðið **Fylki** eftir þörfum fyrir sama fylkið og vefslóð vefþjónustunnar er vísað til.
11. Veljið **Vista** og lokið síðunni.
12. Til að nota eiginleika rafrænnar reikningsfærslu skal skoða [Hafist handa með rafrænni reikningsfærslu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Landsbundin skilgreining forritsuppsetningar fyrir eiginleika rafrænnar reikningsfærslu fyrir brasilískt NF-e (BR)

Ljúkið þessum skrefum áður en uppsetning forritsins er virkjuð í forriti sem er tengt við Finance eða Supply Chain Management.

Þessi hluti tengist **Landsháð grunnstilling á uppsetningu forrits** hlutanum í efnisatriðinu [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki**, skal velja reitinn **Rafræn reikningsfærsla**.
2. Á síðunni **Eiginleikar fyrir rafræna reikningsfærslu** skal staðfesta að rafræni reikningsfærslueiginleikinn **Brasilískt NF-e (BR)** sem sé valinn.
3. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
4. Í flipanum **Uppsetningar** skal velja **Uppsetning forrits** og í reitnum **Tengt forrit** skal velja forritið þangað sem á að setja upp.
5. Í reitnum **Töfluheiti** skal staðfesta hvort **Haus fjárhagsskjals** sé valinn.
6. Veljið **Svargerðir** og veljið síðan **Ný**.
7. Í reitinn **Svargerð** skal færa inn „Svar“ sem fast gildi og í reitinn **Lýsing** skal færa inn „Lýsing“.
8. Í reitnum **Staða sendingar** skal velja **Í bið**.
9. Í reitnum **Líkanavörpun** skal velja **Líkanavörpun úr svarskilaboðum** með **(Forútgáfa) Innflutningssnið svarskilaboða** og síðan velja **Vista**.
10. Veljið **Ný** og í reitinn **Svargerð** skal færa inn „ResponseData“ sem fast gildi og í reitinn **Lýsing** skal færa inn „Lýsing“.
11. Í reitnum **Staða sendingar** skal velja **Í bið**.
12. Í reitinn **Líkanavörpun** skal velja **Gagnainnflutningur svars** með **(Forútgáfa) Innflutningssnið á svargögnum NF-e (BR)** og veljið síðan **Vista**.
13. Til að virkja uppsetningu forritsins í Finance eða Supply Chain tengd forrit skal skoða [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landsbundin skilgreining fyrir eiginleika rafrænnar reikningsfærslu fyrir brasilískt NFS-e ABRASF Curtiba (BR)

Sumar færibreyturnar úr **rafræna reikningseiginleikanum fyrir Brasilískt NFS-e ABRASF Curitiba (BR)** eru birtar með sjálfgefnum gildum. Farðu yfir og, ef þörf krefur, uppfærðu gildin svo þau falli betur að fyrirtækjarekstri þínum áður en þú notar rafræna reikningseiginleikann í þjónustuumhverfinu.

Þessi hluti tengist **Landsbundin skilgreining fyrir eiginleika rafrænnar reikningsfærslu** hlutanum í efnisatriðinu [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki**, skal velja reitinn **Rafræn reikningsfærsla**.
2. Á síðunni **Eiginleikar fyrir rafræna reikningsfærslu** skal staðfesta að rafræni reikningsfærslueiginleikinn **Brasilískt NFS-e ABRASF Curitiba (BR)** sem var stofnaður sé valinn.
3. Í flipanum **Útgáfur** skal staðfesta að útgáfan **Drög** sé valin og í flipanum **Uppsetningar**, í hnitanetinu, skal velja **Senda inn**.
4. Veljið **Breyta** og í flipanum **Aðgerðir**, í reitahópnum **Aðgerðir**, skal velja fyrsta tilvikið af **(Forútgáfa) Skrifa undir xml-skjal**.
5. Í reitahópnum **Færibreytur** skal velja **Heiti vottorðs**.
6. Í reitinn **Gildi** skal færa inn heiti vottorðs sem tengist færibreytu lyklageymslunnar.
7. Í reitahópnum **Aðgerðir** skal velja annað tilvik af **(Forútgáfa) Skrifa undir xml-skjal**.
8. Í reitahópnum **Færibreytur** skal velja **Heiti vottorðs**.
9. Í reitinn **Gildi** skal færa inn heiti vottorðs sem tengist færibreytu lyklageymslunnar.
10. Í flipanum **Aðgerðir**, í reitahópnum **Aðgerðir** skal velja **(Forútgáfa) Hringja í SEFAZ-þjónustu í Brasilíu**.
11. Í reitahópnum **Færibreytur** skal velja færibreytuna **Veffang**.
12. Í reitnum **Gildi**, ef nauðsynlegt, skal fara yfir og uppfæra vefslóð vefþjónustunnar sem skatturinn birtir fyrir Curitiba og síðan velja **Vista**.
13. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja **Spyrjast fyrir um** og síðan velja **Breyta**.
14. Í flipanum **Aðgerðir**, í reitahópnum **Aðgerðir** skal velja **(Forútgáfa) Hringja í SEFAZ-þjónustu í Brasilíu**.
15. Í reitahópnum **Færibreytur** skal velja færibreytuna **Veffang**.
16. Í reitnum **Gildi**, ef nauðsynlegt, skal fara yfir og uppfæra vefslóð vefþjónustunnar sem skatturinn birtir fyrir Curitiba.
17. Veljið **Vista** og lokið síðan síðunni.
18. Til að nota eiginleika rafrænnar reikningsfærslu skal skoða [Hafist handa með rafrænni reikningsfærslu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Landsbundin skilgreining forritsuppsetningar fyrir eiginleika rafrænnar reikningsfærslu fyrir brasilískt NFS-e ABRASF Curtiba (BR)

Ljúkið þessum skrefum áður en uppsetning forritsins er virkjuð í forriti sem er tengt við Finance eða Supply Chain Management.

Þessi hluti tengist **Landsháð grunnstilling á uppsetningu forrits** hlutanum í efnisatriðinu [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki**, skal velja reitinn **Rafræn reikningsfærsla**.
2. Á síðunni **Eiginleikar fyrir rafræna reikningsfærslu** skal staðfesta að rafræni reikningsfærslueiginleikinn **Brasilískt NFS-e ABRASF Curitiba (BR)** sé valinn.
3. Í flipanum **Útgáfur** skal staðfesta að útgáfan **Drög** sé valin og í flipanum **Uppsetningar** skal velja **Uppsetning forrits**.
4. Í reitnum **Tengt forrit** skal velja forritið þar sem á að setja upp.
5. Í reitnum **Töfluheiti** skal staðfesta hvort haus fjárhagsskjals sé valinn.
6. Veljið **Svargerðir** og veljið **Ný**.
7. Í reitinn **Svargerð** skal færa inn „ABRASFCuritibaSubmitResponse“ sem fast gildi og í reitinn **Lýsing** skal færa inn „Lýsing“.
8. Í reitnum **Staða sendingar** skal velja **Í bið**.
9. Í reitnum **Líkanavörpun** skal velja **Innflutningur svarskilaboða** með **(Forútgáfa) Innflutningur á svarskilaboðum NFS-e ABRASF Curitiba (BR)** og síðan velja **Vista**.
10. Veljið **Ný** og í reitinn **Svargerð** skal færa inn „ABRASFCuritibaSubmitResponseData“ og í reitinn **Lýsing** skal færa inn „Lýsing“.
11. Í reitnum **Staða sendingar** skal velja **Í bið**.
12. Í reitinn **Líkanavörpun** skal velja **Gagnainnflutningur svars** með **(Forútgáfa) Innflutningssnið á svargögnum NFS-e ABRASF (BR)** og veljið síðan **Vista**.
13. Veljið **Ný** og í reitinn **Svargerð** skal færa inn „ABRASFCuritibaInquireResponse“ og í reitinn **Lýsing** skal færa inn „Lýsing“.
14. Í reitnum **Staða sendingar** skal velja **Í bið**.
15. Í reitnum **Líkanavörpun** skal velja **Innflutningur svarskilaboða** með **(Forútgáfa) Innflutningur á svarskilaboðum NFS-e ABRASF Curitiba (BR)**.
16. Veljið **Vista** og lokið síðunni.
17. Til að virkja uppsetningu forritsins í Finance eða Supply Chain tengd forrit skal skoða [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Tilkynning um persónuvernd
Ef eiginleikarnir **NF-e Federal - Rafrænn reikningur fyrir Brasilíu (BR)** og **NFS-e - Rafrænn reikningur brasilískrar þjónustu (borg)** eru virkjaðir, þá gæti þurft að senda takmörkuð gögn, þ.m.t. skattskráningarkenni fyrirtækisins. Þessi gögn eru send til stofnana þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda. Sem stjórnandi geturðu kveikt eða slökkt á eiginleikunum **NF-e Federal - Rafrænn reikningur fyrir Brasilíu (BR)** og **NFS-e - Rafrænn reikningur brasilískrar þjónustu (borg)**. Eftirfarandi skref sýna hvernig á að gera það: 

1. Farið í **Fyrirtækisstjórnun** > **Uppsetning** > **Færibreytur rafræns skjals**. 
2. Í flipanum **Eiginleikar** skal velja línuna sem inniheldur eiginleikann **NF-e Federal - Rafrænn reikningur fyrir Brasilíu (BR)** og **NFS-e - Rafrænn reikningur brasilískrar þjónustu (borg)** og velja eiginleikann. Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í köflunum um persónuverndaryfirlýsingu í fylgiskjölum um eiginleika eftir löndum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
