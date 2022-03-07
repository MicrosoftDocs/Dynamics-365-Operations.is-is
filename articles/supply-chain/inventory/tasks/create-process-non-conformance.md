---
title: Stofna og meðhöndla ósamkvæmi
description: Þetta efnisatriði lýsir því hvernig á að nota framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032f5b712c2be5312524129cd25e655e778f5f44
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580865"
---
# <a name="create-and-process-nonconformances"></a>Stofna og meðhöndla ósamkvæmi

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að nota framkvæma stjórnun ósamkvæmis, samkvæmt fyrirliggjandi gæðapöntun. Yfirleitt er stjórnun ósamkvæmi framkvæmd af eftirlitsaðila. Þess er krafist að hægt sé að panta gæðapöntun. (Nánari upplýsingar um hvernig á að stofna gæðapöntun eru í [Skoða gæði vara](inspect-quality-goods.md).)

Áður en notandi getur unnið úr samþykki ósamkvæmis verður að úthluta honum starfsmanni í reitnum **Einstaklingur** á síðunni **Notendur**. Auk þess, áður en notandinn getur notað athugasemdir skjalsins, verður að stilla valkostinn **Virkja skjalastjórnun** á *Já* í valkostum notanda.

## <a name="create-a-nonconformance"></a>Stofna ósamkvæmistilvik

Til að búa til ósamkvæmi skal fylgja eftirfarandi skrefum.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svarglugganum **Búa til ósamkvæmni**, í reitnum **Gerð vandamáls**, skal velja gerð vandamálsins sem var fundið í skoðunarferlinu.
1. Veljið **Í lagi**.

## <a name="approve-or-reject-a-nonconformance"></a>Samþykkja eða hafna ósamkvæmistilviki

Fylgið eftirfarandi skrefum til að samþykkja eða hafna ósamkvæmi.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Á listanum skal velja það ósamkvæmi sem á að uppfæra.

    > [!NOTE]
    > Einungis er hægt að bæta leiðréttingu við ósamkvæmi sem er samþykkt.

1. Á aðgerðarsvæðinu skal velja **Aðgerðir \> Samþykkja ósamkvæmni** til að samþykkja ósamkvæmnina eða **Aðgerðir \> Hafna ósamkvæmni** til að hafna henni. Hægt er að tengja samþykkt ósamkvæmi við [tengdar aðgerðir](../quality-operations.md). Á þennan hátt er hægt að skrá vinnu sem er gerð sem hluti af meðhöndlun ósamkvæmi og úrvinnslu leiðréttingarmeðhöndlunar.
1. Beðið er um staðfestingu á valinu. Veldu **Já** til að halda áfram.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Bættu við aðgerðum og öðrum upplýsingum um ósamkvæmi

Þegar ósamkvæmi hefur verið stofnuð er hægt að byrja að bæta við tengdum aðgerðum og tilgreina viðbótarupplýsingar fyrir þær aðgerðir. Þú getur aðeins bætt tengdum aðgerðum við ósamkvæmi sem er samþykkt.

Auk grunnupplýsinganna er hægt að bæta eftirfarandi upplýsingum við aðgerð:

- **Vörur** – Hægt er að búa til lista yfir vörur sem eru notaðar til að framkvæma leiðréttinguna. Til dæmis gætu vörurnar verið vörur sem eru nauðsynlegar til viðgerðar á búnaði eða innihaldsefnum sem þarf til að endurvinna tilbúna afurð.
- **Gæðagjöld** – Hægt er að stofna lista af gjöldum sem myndast eða eru reikningsfærð til ytri aðila.
- **Vinnukort** – Hægt er að búa til kladda yfir þann tíma sem hver starfsmaður eyðir í aðgerðina.

Aðrar stillingar eru valfrjálsar. Kostnaður fyrir hverja vöru, gæðagjöld og vinnukortið er tekið saman og sýnt á aðgerðinni. Þú getur ekki breytt reitnum **Kostnaður** beint í aðgerðinni.

### <a name="create-an-operation-for-a-nonconformance"></a>Búa til aðgerð fyrir ósamkvæmni

Fylgja skal eftirfarandi skrefum til að búa til aðgerð vegna ósamkvæmi.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Á listanum skal velja það ósamkvæmi sem á að uppfæra.

    > [!NOTE]
    > Aðeins er hpægt að bæta við eða uppfæra aðgerðir fyrir ósamræmi sem eru samþykkt.

1. Á aðgerðasvæðinu skal velja **Tengdar aðgerðir**.
1. Á síðunni **Tengdar aðgerðir**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Aðgerð** – Veldu kóða aðgerðarinnar sem verður framkvæmd vegna ósamkvæminnar.
    - **Ástæða** – Færið inn ítarlega lýsingu sem skýrir hvers vegna aðgerð er nauðsynleg.
    - **Sölupöntun** – Ef valinn aðgerðarkóði tengist gerð sölupöntunar skal velja sölupöntunina sem aðgerðin er tengd við.
    - **Innkaupapöntun** – Ef valinn aðgerðarkóði tengist gerð innkaupapöntunar skal velja innkaupapöntunina sem tengja á við aðgerðina.

1. Lokaðu síðunum.

### <a name="add-items-to-an-operation"></a>Bæta vörum við aðgerð

Fylgja skal eftirfarandi skrefum til að bæta atriðum við aðgerð.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Á listanum skal velja það ósamkvæmi sem á að uppfæra.

    > [!NOTE]
    > Aðeins er hpægt að bæta við eða uppfæra aðgerðir fyrir ósamræmi sem eru samþykkt.

1. Á aðgerðasvæðinu skal velja **Tengdar aðgerðir**.
1. Á síðunni **Tengdar aðgerðir** er valin aðgerðin sem bæta á vörum við.
1. Á aðgerðasvæðinu skal velja **Vörur**.
1. Á síðunni **Tengdar aðgerðir**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið. Stillið síðan eftirtalin svæði fyrir nýja röð:

    - **Vörunúmer** – Veldu vöruna sem verður notuð sem hluti af völdu aðgerðinni.
    - **Magn** – Færið inn fjölda vara sem verða notaðar.

    > [!NOTE]
    > Hægt er að skoða kostnað á vörunni í reitnum **Kostnaður** í flipanum **Almennt**. Kostnaðurinn sem er sýndur þar kemur frá kostnaðinum sem er settur upp á síðunni **Útgefin afurð**. Ekki er hægt að uppfæra kostnaðinn beint á síðuna **Tengdar aðgerðir**. Kostnaður á öllum vörum sem bætt er við síðuna **Vörur tengdrar aðgerðar** er sjálfkrafa bætt við reitinn **Kostnaður** á síðunni **Tengdar aðgerðir**.

1. Endurtaka skal fyrri skref fyrir hvern viðbótarhlut sem þú verður að bæta við.
1. Lokaðu síðunum.

### <a name="add-quality-charges-to-an-operation"></a>Bæta gæðagjöldum við aðgerð

Fylgja skal eftirfarandi skrefum til að bæta gæðagjöldum við aðgerð.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Á listanum skal velja það ósamkvæmi sem á að uppfæra.

    > [!NOTE]
    > Aðeins er hpægt að bæta við eða uppfæra aðgerðir fyrir ósamræmi sem eru samþykkt.

1. Á aðgerðasvæðinu skal velja **Tengdar aðgerðir**.
1. Á síðunni **Tengdar aðgerðir** er valin aðgerðin sem bæta á gæðagjöldum við.
1. Á aðgerðasvæðinu skal velja **Gæðagjöld**.
1. Á síðunni **Gjöld tengdrar aðgerðar**, á aðgerðasvæðinu, skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Gjaldakóði** – Veljið gæðagjaldið sem bæta á við.
    - **Lýsing** – Færið inn ítarlega lýsingu á gjaldinu.
    - **Gildi gjalda** – Færið inn upphæð gjaldsins.

1. Endurtaka skal fyrri skref fyrir hver viðbótargjöld sem þú þarft að bæta við.
1. Lokaðu síðunum.

> [!NOTE]
> Upphæðin í reitnum **Gildi gjalds** er sjálfkrafa tekin saman fyrir öll gæðagjöld og bætt við allar aðrar upphæðir í reitnum **Kostnaður** á síðunni **Tengdar aðgerðir**.

### <a name="create-a-timesheet-on-an-operation"></a>Búa til vinnukort á aðgerð

Fylgja skal eftirfarandi skrefum til að bæta vinnukorti við aðgerð.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Á listanum skal velja það ósamkvæmi sem á að uppfæra.

    > [!NOTE]
    > Aðeins er hpægt að bæta við eða uppfæra aðgerðir fyrir ósamræmi sem eru samþykkt.

1. Á aðgerðasvæðinu skal velja **Tengdar aðgerðir**.
1. Á síðunni **Tengdar aðgerðir** er valin aðgerðin sem bæta á vinnukorti við.
1. Á aðgerðasvæðinu skal velja **Tímablað**.
1. Á síðunni **Vinnuskýrslur tengdrar aðgerðar**, á aðgerðasvæðinu, skal velja **Ný** til að bæta nýrri línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Dagsetning** – Tilgreinið dagsetninguna þegar verkið var unnið. Reiturinn er sjálfgefið stilltur á núgildandi dagsetningu.
    - **Starfskraftur** – Veljið starfskraft sem vann vinnuna. Þessi reitur er sjálfgefið stilltur á starfskraftinn sem er úthlutað á núverandi notanda.
    - **Aðgerðartímar** – Færið inn þann fjölda klukkustunda sem voru notaðar fyrir valda aðgerð.
    - **Reikningsfært** – Veljið þennan gátreit ef tíminn hefur verið skuldfærður viðskiptavin eða lánardrottinn á reikningi.

    > [!NOTE]
    > Hægt er að skoða kostnaðinn í reitnum **Kostnaður** í flipanum **Almennt**. Kostnaðurinn er reiknaður með því að nota taxtann sem þú skilgreinir á síðunni **Færibreytur birgðastjórnunar**.

1. Endurtaka skal fyrri skref fyrir hverja vinnukortslínu til viðbótar sem þú verður að bæta við.
1. Lokaðu síðunum.

> [!NOTE]
> Upphæðin í reitnum **Kostnaður** er tekin saman fyrir allar vinnukortslínur og bætt við allar aðrar upphæðir í reitnum **Kostnaður** á síðunni **Tengdar aðgerðir**.

## <a name="add-a-correction-to-a-nonconformance"></a>Bæta leiðréttingu við ósamkvæmni

Fylgja skal eftirfarandi skrefum til að bæta leiðréttingu við ósamkvæmi.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Á listanum skal velja það ósamkvæmi sem á að uppfæra.

    > [!NOTE]
    > Einungis er hægt að bæta leiðréttingu við ósamkvæmi sem er samþykkt.

1. Á aðgerðasvæðinu skal velja **Lagfæringar**.
1. Á síðunni **Leiðréttingar**, á aðgerðasvæðinu, skal velja **Nýtt** til að bæta við röð við hnitið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Greining** – Veljið þá gerð greiningar sem auðkennir þá gerð leiðréttingar sem verið er að búa til.
    - **Starfskraftur** – Veljið einstaklinginn sem er ábyrgur fyrir leiðréttingunni.
    - **Forgangur leiðréttingar** – Veljið valkost til að tilgreina hvernig forgangsraða á leiðréttingu (*Lág*, *Miðlungs* eða *Há*).
    - **Umbeðin dagsetning** – Færið inn dagsetninguna þegar óskað var eftir leiðréttingu.
    - **Áætluð dagsetning** – Færa inn dagsetninguna þegar búist er við að leiðréttingunni verði lokið.
    - **Skammtímalausn** – Veljið þennan gátreit ef leiðréttingaraðgerðin leiðréttir einungis ósamkvæmið í stuttan tíma.

1. Lokaðu síðunum.

## <a name="mark-a-correction-as-completed"></a>Merkja leiðréttingu sem lokið

Fylgið eftirfarandi skrefum til að merkja leiðréttingu ósamkvæmi sem lokið.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Á listanum skal velja það ósamkvæmi sem á að uppfæra.

    > [!NOTE]
    > Einungis er hægt að bæta leiðréttingu við ósamkvæmi sem er samþykkt.

1. Á aðgerðasvæðinu skal velja **Lagfæringar**.
1. Á síðunni **Leiðréttingar** í hnitanetinu skal velja leiðréttinguna sem á að merkja sem lokkna.
1. Á aðgerðasvæðinu skal velja **Merkja sem lokið**.
1. Beðið er um staðfestingu á valinu. Veldu **Í lagi** til að halda áfram. Reiturinn **Dagsetning og tími sem tilbúið er** er stilltur á núverandi dagsetningu og tíma og gátreiturinn **Lokið** er valinn.
1. Lokið síðunni.

## <a name="reopen-a-completed-correction"></a>Enduropna lokna leiðréttingu

Til að opna aftur lokinni leiðréttingu skal fylgja eftirfarandi skrefum.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Ósamkvæmnistilvik**.
1. Á listanum skal velja það ósamkvæmi sem á að uppfæra.
1. Á aðgerðasvæðinu skal velja **Lagfæringar**.
1. Á síðunni **Leiðréttingar** í hnitanetinu skal velja leiðréttinguna sem á að opna aftur.
1. Á aðgerðasvæðinu skal velja **Enduropna**.
1. Beðið er um staðfestingu á valinu. Veldu **Í lagi** til að halda áfram. Gildið er hreinsað úr reitnum **Dagsetning og tími verkloka** og gátreiturinn **Lokið** er hreinsaður.
1. Lokið síðunni.

Nú er hægt að gera frekari breytingar eða uppfærslur á leiðréttingunni. Þegar því er lokið er hægt að merkja leiðréttinguna sem lokið aftur.

## <a name="close-a-nonconformance"></a>Loka ósamkvæmistilviki

Til að loka ósamkvæmni skal fylgja eftirfarandi skrefum.

1. Farðu í **Birgðastjórnun \> Reglubundin verk \> Gæðastjórnun \> Gæðapantanir**.
1. Veljið gæðaröð í hnitanetinu.
1. Veljið **Fyrirspurnir \> Ósamkvæmni** á aðgerðarúðunni.
1. Á síðunni **Ósamkvæmi** skal velja markmið ósamkvæmis í hnitanetinu.
1. Á aðgerðasvæðinu skal velja **Aðgerðir \> Loka ósamkvæmni**.
1. Beðið er um staðfestingu á valinu. Veldu **Já** til að halda áfram.
1. Lokaðu síðunum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gæðastjórnunaryfirlit](../quality-management-processes.md)
- [Virkja stjórnun gæða og ósamkvæmni](../enable-quality-management.md)
- [Starfsmenn ábyrgir fyrir samþykki ósamkvæmni](../quality-responsible-workers.md)
- [Biðgeymslusvæði fyrir ósamkvæmi](../quality-quarantine-zones.md)
- [Gerðir greininga fyrir ósamkvæmni](../quality-diagnostic-types.md)
- [Gæðagjöld fyrir ósamkvæmi](../quality-charges.md)
- [Aðgerðir fyrir ósamkvæmni.](../quality-operations.md)
- [Gæðastjórnun fyrir vöruhúsaferli](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
