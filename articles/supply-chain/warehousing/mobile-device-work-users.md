---
title: Notandareikningar fartækis
description: Í þessari grein er því lýst hvernig setja skal upp og hafa umsjón með notandareikningum sem gera starfsmönnum kleift að skrá sig inn og nota vöruhúsaforritið.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ffb4a9842f454094b41a1765d1438f6a40ae610b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851305"
---
# <a name="mobile-device-user-accounts"></a>Notandareikningar fartækis

[!include [banner](../includes/banner.md)]

Í hvert sinn sem starfsmaður byrjar að nota vöruhúsaforritið verður hann að skrá sig inn með notandanafni og aðgangsorði. Allir notendur vöruhúsaforritsins geta tengst hverjum starfsmanni kerfisins og vöruhús eru yfirleitt tengd hverjum þessara notenda vöruhúsaforritsins. Ýmsir valkostir eru einnig grunnstilltir fyrir hvern starfsmann til að setja á sjálfgefnar stillingar og aðrar stillingar sem tengjast notkun vöruhúsaforritsins.

## <a name="set-up-the-required-worker-and-employee-records"></a>Setja upp nauðsynlegan starfsmann og starfsmannafærslur

Áður en hægt er að setja upp notendur vöruhúsaforrits þarf hver starfsmaður að vera til sem starfsmaður Supply Chain Management í einingunni **Human Resources**.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Setja upp notandareikninga fartækis

Þegar nauðsynlegir starfsmenn hafa verið settir upp í Human Resources er hægt að úthluta hverjum þeirra notanda úr vöruhúsaforritinu og setja upp aðra valkosti sem hafa áhrifa á hvernig þeir geta notað forritið.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Starfskraftur**.
1. Til að breyta fyrirliggjandi starfsmanni skal velja hann á listasvæðinu. Til að bæta við nýrri færslu skal velja **Ný** á aðgerðasvæðinu.
1. Ef nýr starfsmaður er settur upp skal fylgja þessum skrefum:

    1. Í reitnum **Starfskraftur** skal velja notandann í listanum yfir starfsmenn.
    1. Veljið **Velja**.
    1. Í aðgerðarúðunni skal velja **Vista**.

1. Hægt er að nota sjálfgefna forstillingu til að leiða starfsmanna vöruhússins á pökkunarstöðinni í gegnum ferlið sem er krafist hér. Að öðrum kosti er hægt að nota sjálfgefna forstillingu til að vista æskilegar forstillingar starfsmannsins. Á flýtiflipanum **Forstilling** skal stilla eftirfarandi reiti:

    - **Regla gámapökkunar** – Veldu gámapökkunarreglu sem skilgreinir hvernig á að afgreiða gáma á pökkunarstöðinni. Regla gámapökkunar sem er valin hér verður valin fyrirfram fyrir starfsmanninn þegar hann opnar pökkunarstöðina. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Bætt pökkunaraðferð](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Auðkenni pökkunarforstillingar** – Veldu auðkenni pökkunarforstillingar sem skilgreinir pökkunarreglu og gámastillingar sem eru notaðar. Ef valið auðkenni pökkunarforstillingar er tengt við reglu gámapökkunar verður ekki hægt að breyta stillingunni **Regla gámapökkunar** á þessari síðu.

1. Á flýtiflipanum **Sjálfgefin pökkunarstöð** skal stilla eftirfarandi reiti til að skilgreina sjálfgefna pökkunarstöð sem gildir þegar starfsmaður skráir sig inn. Starfsmaðurinn getur samt valið aðra pökkunarstöð eftir þörfum.

    - **Svæði** – Veldu svæðið þar sem sjálfgefna pökkunarstöðin er staðsett.
    - **Vöruhús** – Veldu vöruhúsið þar sem sjálfgefna pökkunarstöðin er staðsett.
    - **Staðsetning** – Veldu staðsetningu sjálfgefinnar pökkunarstöðvar.

1. Flýtiflipinn **Notendur** gerir þér kleift að stofna eins marga notandareikningi vöruhúsaforrits og þarf til fyrir valinn starfsmann. Hver reikningur er tengdur tilteknu vöruhúsi eða vöruhúsum. Notaðu tækjastikuna til að bæta við eða fjarlægja notandareikninga, endurstilla aðgangsorðið fyrir valinn reikning eða úthluta vöruhúsum á valinn reikning. Fyrir hvern notandareikning skal stilla eftirfarandi reiti:

    - **Notandakenni** Færðu inn einkvæmt kenni.
    - **Notandanafn** Færið inn heiti fyrir auðkennið.
    - **Sjálfgefið vöruhús** – Stilltu sjálfgefna vöruhúsið þar sem starfsmaðurinn vinnur yfirleitt. Hægt er að nota tækjastikuna til að úthluta fleiri vöruhúsum og starfsmaðurinn getur skipt á milli vöruhúsa með því að nota óbeina verkþáttinn **Breyta vöruhúsi** á valmyndaratriði fartækis.
    - **Valmyndarheiti** – Veldu rótarvalmyndina sem verður upphafssíða fyrir starfsmanninn. Möguleikinn á að setja upp rótarvalmynd fyrir hvern starfsmann er gagnlegur vegna þess að hann gerir þér kleift að stjórna valmyndarskipulaginu sem hver starfsmaður getur notað. Til dæmis er hægt að sérsníða valmyndina fyrir starfsmenn sem eru aðeins virkir á svæðum útleiðar fyrir verk sem tengjast aðgerðum útleiðar fyrir það svæði.
    - **Óvirkur** – Valinn gátreitur gefur til kynna að notandareikningurinn sé óvirkur. Notandareikningurinn er sjálfkrafa gerður óvirkur ef starfsmaður slær inn rangt aðgangsorð fimm sinnum í röð í vöruhúsaforritinu. Hins vegar er hægt að velja gátreitinn handvirkt. Hreinsaðu gátreitinn til að gera notandann aftur virkan.

1. Á flýtiflipanum **Vinna** stillirðu eftirfarandi reiti:

    - **Leyfa hnekkingu tiltektarstaðsetningar** – Stilltu þennan valkost á *Já* til að leyfa starfsmanni að hnekkja staðsetningu fyrir tiltektarskref. Þessi möguleiki getur verið gagnlegur ef efnislegar birgðir passa ekki við staðsetningu sem kerfið stingur upp á.
    - **Leyfa hnekkingu frágangsstaðsetningar** – Stilltu þennan valkost á *Já* til að leyfa starfsmanni að hnekkja staðsetningu fyrir frágangsskref. Þessi möguleiki getur verið gagnlegur ef frágangsstaðsetning sem stungið er upp á er full eða ekki í boði, eða ef geymslustaðsetningarnar breyttust.
    - **Leyfa umframtiltekt í sölu** – Stilltu þennan valkost á *Já* til að leyfa starfsmanni að gera umframtiltekt þegar sölupantanir eru tíndar. Frekari upplýsingar er að finna í [Umframtiltekt fyrir sölupantanir og flutningspantanir](over-picking-for-sales-and-transfer-orders.md).
    - **Leyfa umframtiltekt í flutningspöntun** – Stilltu þennan valkost á *Já* til að leyfa starfsmanni að gera umframtiltekt þegar flutningspantanir eru tíndar. Frekari upplýsingar er að finna í [Umframtiltekt fyrir sölupantanir og flutningspantanir](over-picking-for-sales-and-transfer-orders.md).
    - **Leyfa hreyfingu birgða með tengdri vinnu** – Stilltu þennan valkost á *Já* til að leyfa starfsmanninum að færa birgðir sem eru þegar fráteknar eða þegar tengdar annarri vinnu. Frekari upplýsingar er að finna í [Hreyfing birgða með tengdri vinnu í vöruhúsakerfi](move-inventory-associated-work.md).
    - **Leyfa handvirka endurúthlutun vöru** – Stilltu þennan valkost á *Já* til að virkja handvirka endurúthlutun fyrir starfsmanninn við of litla tiltekt. Endurúthlutun vöru vísar starfsmönnum á að staðsetningu til að tína birgðir. Þótt sjálfvirk endurúthlutun sé í boði fyrir alla starfsmenn krefst handvirkt endurúthlutun sérstakrar uppsetningar fyrir starfsmann. Möguleikinn á að stjórna handvirkri endurúthlutun fyrir hvern starfsmann getur verið gagnlegur vegna þess að hann gerir þér kleift að stjórna sýnileika hvers starfsmanns, til dæmis þegar vörutiltekt úr biðgeymslu eða magnsvæði takmarkast við áreiðanlega starfsmenn. Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Sjálfvirk og handvirk endurúthlutun vöru í stuttri tiltekt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Er stjórnandi reglulegrar talningar** – Stilltu þennan valkost á *Já* til að gera starfsmanninn að stjórnanda reglulegrar talningar. Í þessu tilfelli verða allar reglulegar talningar sem starfsmaðurinn framkvæmir í vöruhúsaforritinu samþykktar um leið. Reitirnir **Hámarksprósenta**, **Hámarksmagn** og **Hámarksvirði** eru ekki teknir til greina fyrir starfsmenn þar sem þessi valkostur er stilltur á *Já*.
    - **Hámarksprósenta** – Færðu inn hæstu prósentumörk sem regluleg talning má víkja frá væntanlegri talningu án þess að stjórnandi reglulegrar talningar þurfi að samþykkja.
    - **Hámarksmagn** – Færðu inn heildarmagnið sem innslegið magn má víkja frá væntanlegu magni (í einingum) án þess að samþykki þurfi frá stjórnanda reglulegrar talningar.
    - **Hámarksvirði** – Færðu inn hámarksupphæð sem kostnaður birgða má víkja frá væntanlegum kostnaði án þess að samþykki þurfi frá stjórnanda reglulegrar talningar.

1. Í aðgerðarúðunni skal velja **Vista**.
1. Ef þú bættir við nýjum notandareikningi birtist glugginn **Setja aðgangsorð** þar sem hægt er að búa til einfalt aðgangsorð sem notandinn getur notað til að skrá sig inn í forrit fartækis. Sláðu inn einfalda aðgangsorðið tvisvar sinnum og veldu svo **Vista aðgangsorð** til að halda áfram.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Stilla tungumálið, talnasniðið og tímabeltið fyrir hvern notanda vöruhúsaforritsins

Þegar starfsmaður skráir sig inn í farsímaforrit vöruhúsakerfis breytist tungumálið, talnasniðin og tímabeltið til að passa við kjörstillingar starfsmannsins. Reikningsstillingar fyrir starfsmanninn sem eru valdar í skrefi 3 í hlutanum [Setja upp notandareikninga fartækis](#set-wma-users) ákvarða stillingarnar sem eru notaðar. Ef þú þarft aðskildar stillingar fyrir hvern notanda skaltu nota mismunandi starfsmannareikninga. Eftirfarandi aðferð sýnir hvernig á að breyta tungumáli, talnasniði og tímabelti fyrir hvern notanda vöruhúsaforritsins.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Starfskraftur**.
1. Finndu nafn starfsmannsins sem þú vilt setja upp. Gakktu úr skugga um að starfsmaðurinn hafi alla nauðsynlega notandareikninga vöruhúsaforritsins sem eru gefnir upp á flýtiflipanum **Notendur**. Búðu til nýjan starfsmann og/eða notandareikninga vöruhúsaforrits eftir þörfum með því að fylgja skrefunum í hlutanum [Setja upp notandareikninga fartækis](#set-wma-users).
1. Farðu í **Kerfisstjórnun \> Notendur \> Notendur**.
1. Veldu notandareikninginn þar sem dálkurinn **Einstaklingur** sýnir nafn starfsmannsins sem þú fannst í skrefi 2.

    > [!IMPORTANT]
    > Gildin **Notandakenni** sem eru sýnd á síðunni **Notendur** eru *ekki* tengd gildinu sem er sýnt á flýtiflipanum **Notendur** á síðunni **Starfsmaður** sem þú opnaðir í skrefi 1.

1. Á aðgerðasvæðinu skal velja **Valkostir notanda**.
1. Á flipanum **Kjörstillingar** skal stilla eftirfarandi reiti:

    - **Tungumál** – Veldu tungumálið sem starfsmaðurinn kýs. Þessi reitur stýrir einnig númerasniðinu sem birtist í vöruhúsaforritinu.
    - **Dagsetning, tími og númerasnið** – Veldu dagsetningu og tímasnið sem starfsmaðurinn kýs. Vöruhúsaforritið notar númerasniðið sem tengist tungumálinu sem valið er fyrir reitinn **Tungumál** í staðinn fyrir þessa stillingu.
    - **Tímabelti** – Veldu tímabeltið þar sem starfsmaðurinn vinnur. Þessi reitur hefur áhrif á tímastimpil fyrir allar skráningar sem starfsmaðurinn gerir með því að nota forritið.

> [!NOTE]
> Í sumum tilvikum finnur vöruhúsaforritið ekki tilteknar stillingar starfsmanns sem skera úr um tungumál, talnasnið og tímabelti. Eftirfarandi reglur gilda:
>
> - Ef forritið er ekki tengt við umhverfi Supply Chain Management (til dæmis í fyrsta skipti sem forritið er ræst eftir uppsetningu) er tungumál staðbundins tækis notað. Þegar breyting verður á tungumáli tækis breytist tungumál forritsins líka. Frekari upplýsingar um hvernig á að stilla tungumál fyrir tæki á staðnum er að finna í fylgiskjölum fyrir tækið þitt og/eða stýrikerfið.
> - Ef forritið er tengt við umhverfi Supply Chain Management, en engar kjörstillingar eru stilltar fyrir innskráðan starfsmann, er tungumál, talnasnið og tímabelti valið samkvæmt reikningnum sem tengist biðlarakenninu sem tækið notar til að tengjast Supply Chain Management. Frekari upplýsingar er að finna í [Stofna og skilgreina notandareikning í Supply Chain Management](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Ef þú tekur eftir því að rangir tímastimplar eru sýndir fyrir skráningar sem gerðar eru með því að nota vöruhúsaforritið gætirðu þurft að breyta tímabeltinu sem er stillt fyrir notandareikninginn sem starfsmenn nota til að skrá sig inn og/eða auðkenna sig með Supply Chain Management. Eins og áður var nefnt gæti stillingin fyrir tímabelti komið frá notandareikningnum sem notaður er til að skrá sig inn í vöruhúsaforritið, eins og sett er upp á síðunni **Starfsmaður**. Að öðrum kosti, ef notandareikningurinn er ekki stilltur á síðunni **Starfsmaður**, kemur tímabeltið frá notandareikningnum sem tengist biðlarakenninu sem er notað fyrir auðkenningu, eins og það er sett upp á síðunni **[Azure Active Directory forrit](install-configure-warehouse-management-app.md)**.
