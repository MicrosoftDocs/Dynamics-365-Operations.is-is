---
title: Bóka sem tilbúið úr verkspjaldstæki
description: Þetta efnisatriði lýsir því hvernig skilgreina á kerfið þannig að notendur verkspjaldtækis geti bókað tilbúnar afurðir úr framleiðslupöntun í birgðir.
author: johanhoffmann
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6ba5d8bc0c22f97e6d2ce61c636090e04fae5abd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430265"
---
# <a name="report-as-finished-from-the-job-card-device"></a>Bóka sem tilbúið úr verkspjaldstæki

[!include [banner](../includes/banner.md)]

Starfsmenn nota síðuna **Tilkynna um framvindu** í verkspjaldstækinu til að tilkynna magn sem hefur verið lokið fyrir framleiðsluverk. Þetta efnisatriði lýsir því hvernig setja á upp ýmsa valmöguleika sem ákveða hvernig starfsmenn geta tilkynnt um að eitthvað sé búið með þessari síðu og hvað gerist næst. Á meðal valkosta er:

- Stjórna því hvort og hvernig magn sem tilkynnt er sem búið er bætt við birgðir.
- Stjórna því hvort og hvernig rununúmer eru mynduð og notuð þegar tilkynnt er um að eitthvað sé búið.
- Stjórna því hvort og hvernig raðnúmer eru mynduð og notuð þegar tilkynnt er um að eitthvað sé búið.
- Stjórna því hvort og hvernig á að tilkynna um búið fyrir númeraplötu.

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a>Stjórna því hvort magn sem er tilkynnt sem lokið verði bætt við birgðir

Til að stjórna því hvort og hvernig magnið sem tilkynnt er sem lokið í síðustu aðgerð eigi að vera bætt við birgðir skal fylgja þessum skrefum.

1. Farið í **Framleiðslustjórnun \> Uppsetning \> Framkvæmd framleiðslu \> Sjálfgildi framleiðslupöntunar**.
1. Í flipanum **Tilkynna sem lokið** skal stilla reitinn **Uppfæra skýrslu um tilbúið á netinu** á eitt af eftirfarandi gildum:

    - **Ekkert** - Engu magni verður bætt við birgðir þegar magn er tilkynnt í síðustu aðgerðinni. Staða framleiðslupöntunar breytist aldrei.
    - **Staða + magn** – Staða framleiðslupöntunar breytist í *Tilkynna sem lokið* og magnið verður gefið upp sem lokið í birgðum.
    - **Magn** - Magnið verður tilkynnt sem lokið í birgðum, en staða framleiðslupöntunarinnar breytist aldrei.
    - **Staða** - Aðeins staða framleiðslupöntunar breytist. Engu magni verður bætt við birgðir þegar magn er tilkynnt í síðustu aðgerð.

> [!NOTE]
> Magn er ekki rakið í birgðum ef aðgerðirnar sem það er skráð sem lokið í eru ekki skilgreindar sem síðasta aðgerð. Hins vegar er hægt að nota þetta magn til að skoða framvindu. Einnig er hægt að taka það með í reglur sem stjórna því hvort starfsmenn geti hafið næstu aðgerð áður en skilgreindum mörkum um tilkynnt magn úr síðustu aðgerð er náð. Hægt er að skilgreina þessar reglur í flipanum **Staðfesting magns** á síðunni **Sjálfgildi framleiðslupöntunar**.

Frekari upplýsingar um hvernig á að vinna með síðuna **Sjálfgildi framleiðslupöntunar** er að finna í [Færibreytur framleiðslu í framkvæmd framleiðslu](production-parameters-manufacturing-execution.md).

## <a name="report-batch-controlled-items-as-finished"></a>Skrá runustýrðar vörur sem tilbúnar

Verkspjaldstækið styður þrjár atburðarásir fyrir tilkynningu á vörum með runu. Þessar atburðarásir eiga bæði við um vörur sem eru virkjaðar fyrir ítarlega vöruhúsaferla og vörur sem ekki eru virkjaðar fyrir ítarlega vöruhúsaferla.

- **Rununúmer úthlutuð handvirkt** - Starfsmenn slá inn sérsniðið rununúmer. Þetta rununúmer gæti komið frá ytri uppruna sem kerfið þekkir ekki.
- **Fyrirframskilgreind rununúmer** - Starfsmenn velja rununúmer í lista yfir rununúmer sem kerfið myndar sjálfkrafa áður en framleiðslupöntunin er losuð í verkspjaldstækið.
- **Föst rununúmer** - Starfsmenn slá ekki inn eða velja rununúmer. Þess í stað úthlutar kerfið sjálfkrafa rununúmeri á framleiðslupöntunina áður en hún er losuð.


### <a name="enable-the-feature-on-your-system"></a>Virkja eiginleikann í kerfinu

Til að gera verkspjaldstæki kleift að samþykkja rununúmer við tilkynningu um lokið þarf að nota [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eftirfarandi eiginleikum (í þessari röð):

1. Enn notandavænni svargluggi fyrir gerð framvinduskýrslu á verkspjaldstækinu.
1. Virkja til að færa inn runu og raðnúmer þegar skýrslugerð er lokið úr verkspjaldstækinu (forútgáfa).

### <a name="configure-products-that-require-batch-number-reporting"></a>Skilgreina afurðir sem krefjast tilkynningu um rununúmer

Til að virkja afurð til að styðja við einhverja af tiltækum runustýrðum aðstæðum skal fylgja þessum skrefum:

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið afurð til að skilgreina.
1. Í flýtiflipanum **Birgðastjórnun**, í reitnum **Rununúmeraflokkur**, skal velja flokk rakningarnúmera sem er settur upp til að styðja atburðarásina.

> [!NOTE]
> Ef engum flokki rununúmera er úthlutað á runustýrða afurð, býður verkspjaldstækið sjálfkrafa upp á handvirkan innslátt fyrir rununúmerið fyrir tilkynningu um lokið.

Eftirfarandi kaflar lýsa því hvernig á að setja upp flokka rakningarnúmera til að styðja hverja atburðarás fyrir tilkynningu um vörur með rununúmeri.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a>Setja upp flokk rakningarnúmera sem gerir starfsmönnum kleift að úthluta rununúmeri handvirkt

Til að leyfa handvirka úthlutun rununúmera skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.

1. Farið í **Birgðastjórnun \> Uppsetning \> Víddir \> Flokkar rakningarnúmera**.
1. Stofna eða velja flokk rakningarnúmera sem á að setja upp.
1. Í flipanum **Almennt** skal stilla valkostinn **Handvirkt** á **Já**.

    ![Rakningarnúmeraflokkur fyrir handvirk rununúmer](media/tracking-number-group-manual.png "Rakningarnúmeraflokkur fyrir handvirk rununúmer")

1. Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk rununúmera fyrir útgefnar afurðir sem á að nota í þessari atburðarás.

Þegar þessi atburðarás er notuð er reiturinn **Rununúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á textareitur þar sem starfsmenn geta slegið inn hvaða gildi sem er.

![Tilkynningarsíða framvindu með reit fyrir handvirk rununúmer](media/job-card-device-batch-manual.png "Tilkynningarsíða framvindu með reit fyrir handvirk rununúmer")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a>Setja upp flokk rakningarnúmera sem býður upp á lista af fyrirframskilgreindum rununúmerum

Til að bjóða upp á lista af fyrirframskilgreindum rununúmerum skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.

1. Farið í **Birgðastjórnun \> Uppsetning > Víddir \> Flokkar rakningarnúmera**.
1. Stofna eða velja flokk rakningarnúmera sem á að setja upp.
1. Í flipanum **Almennt** skal stilla valkostinn **Aðeins fyrir birgðafærslur** á **Já**.
1. Notið reitinn **Á magn** til að skipta rununúmerum eftir magni byggt á gildinu sem slegið er inn. Til dæmis er hægt að hafa framleiðslupöntun fyrir tíu stykki og reiturinn **Á magn** er stilltur á *2*. Í þessu tilfelli verður fimm rununúmerum úthlutað á framleiðslupöntunina þegar hún er stofnuð.

    ![Rakningarnúmeraflokkur fyrir fyrirframskilgreind rununúmer](media/tracking-number-group-predefined.png "Rakningarnúmeraflokkur fyrir fyrirframskilgreind rununúmer")

1. Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk rununúmera fyrir útgefnar afurðir sem á að nota í þessari atburðarás.

Þegar þessi atburðarás er notuð er reiturinn **Rununúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á fellilisti þar sem starfsmenn verða að velja fyrirframskilgreint gildi.

![Tilkynningarsíða framvindu með lista yfir fyrirframskilgreind rununúmer](media/job-card-device-batch-predefined.png "Tilkynningarsíða framvindu með lista yfir fyrirframskilgreind rununúmer")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a>Setja upp flokk rakningarnúmera sem sjálfkrafa úthluta rununúmerum

Ef úthluta á rununúmerum sjálfkrafa, án innsláttar starfsmanns, skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.

1. Farið í **Birgðastjórnun \> Uppsetning \> Víddir \> Flokkar rakningarnúmera**.
1. Stofna eða velja flokk rakningarnúmera sem á að setja upp.
1. Í flipanum **Almennt** skal stilla valkostinn **Aðeins fyrir birgðafærslur** á **Nei**.
1. Stillið **Handvirkt** valkostinn á **Nei**.

    ![Rakningarnúmeraflokkur fyrir föst rununúmer](media/tracking-number-group-fixed.png "Rakningarnúmeraflokkur fyrir föst rununúmer")

1. Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk rununúmera fyrir útgefnar afurðir sem á að nota í þessari atburðarás.

Þegar þessi atburðarás er notuð mun reiturinn **Rununúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á sýna gildi, en starfsmenn geta ekki breytt því.

![Tilkynningarsíða framvindu með ákveðnu rununúmeri](media/job-card-device-batch-fixed.png "Tilkynningarsíða framvindu með ákveðnu rununúmeri")

## <a name="report-serial-controlled-items-as-finished"></a>Skrá runustýrðar vörur sem tilbúnar

Verkspjaldstækið styður þrjár atburðarásir fyrir tilkynningu á runustýrðum vörum. Þessar atburðarásir eiga bæði við um vörur sem eru virkjaðar fyrir ítarlega vöruhúsaferla og vörur sem ekki eru virkjaðar fyrir ítarlega vöruhúsaferla.

- **Raðnúmerum úthlutað handvirkt** - Starfsmenn færa inn sérsniðið raðnúmer. Þetta raðnúmer gæti komið frá ytri uppruna sem kerfið þekkir ekki.
- **Fyrirframskilgreind raðnúmer** - Starfsmenn velja raðnúmer í lista yfir raðnúmer sem kerfið myndar sjálfkrafa áður en framleiðslupöntunin er losuð í verkspjaldstækið.
- **Föst raðnúmer** - Starfsmenn slá ekki inn eða velja raðnúmer. Þess í stað úthlutar kerfið sjálfkrafa raðnúmer á framleiðslupöntunina áður en hún er losuð.

### <a name="enable-the-feature-on-your-system"></a>Virkja eiginleikann í kerfinu

Til að gera verkspjaldstæki kleift að samþykkja raðnúmer við tilkynningu um að eitthvað sé búið þarf að nota [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eftirfarandi eiginleikum (í þessari röð):

1. Enn notandavænni svargluggi fyrir gerð framvinduskýrslu á verkspjaldstækinu.
1. Virkja til að færa inn runu og raðnúmer þegar skýrslugerð er lokið úr verkspjaldstækinu (forútgáfa).

### <a name="configure-products-that-require-serial-number-reporting"></a>Skilgreina afurðir sem krefjast tilkynningu um raðnúmer

Til að virkja afurð til að styðja við einhverja af tiltækum raðnúmerastýrðum aðstæðum skal fylgja þessum skrefum:

Til að virkja hverja atburðarás skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið afurð til að skilgreina.
1. Í flýtiflipanum **Birgðastjórnun**, í reitnum **Raðnúmeraflokkur**, skal velja flokk rakningarnúmera sem er settur upp til að styðja atburðarásina.

> [!NOTE]
> Ef engum flokki raðnúmera er úthlutað á raðnúmerastýrða afurð, býður verkspjaldstækið sjálfkrafa upp á handvirkan innslátt fyrir raðnúmerið fyrir tilkynningu um lokið.

Eftirfarandi kaflar lýsa því hvernig á að setja upp flokka rakningarnúmera til að styðja hverja atburðarás fyrir tilkynningu um raðnúmerastýrðar vörur.

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-serial-number"></a>Setja upp flokk rakningarnúmera sem gerir starfsmönnum kleift að úthluta raðnúmeri handvirkt

Til að leyfa handvirka úthlutun raðnúmers skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.

1. Farið í **Birgðastjórnun \> Uppsetning \> Víddir \> Flokkar rakningarnúmera**.
1. Stofna eða velja flokk rakningarnúmera sem á að setja upp.
1. Í flipanum **Almennt** skal stilla valkostinn **Handvirkt** á **Já**.

    ![Síða rakningarnúmeraflokka, raðnúmer](media/tracking-number-group-manual-serial.png "Síða rakningarnúmeraflokka, raðnúmer")

1. Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk raðnúmers fyrir útgefnar afurðir sem á að nota í þessari atburðarás.

Þegar þessi atburðarás er notuð er reiturinn **Raðnúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á textareitur þar sem starfsmenn geta slegið inn hvaða gildi sem er fyrir raðnúmerið. Þegar gildi er slegið inn, bætist það við raðnúmeralistann. Í þessum lista geta starfsmenn gert eftirfarandi:

- Til að merkja raðnúmer sem úrelt skal velja hnappinn **Úrelt** fyrir viðeigandi línu. Starfsmaðurinn verður beðinn um að leggja fram **Orsök villu**.
- Til að eyða raðnúmeri skal velja hnappinn **Eyða** fyrir viðeigandi línu.

![Tilkynningarsíða framvindu með reit fyrir handvirk raðnúmer](media/job-card-device-serial-manual.png "Tilkynningarsíða framvindu með reit fyrir handvirk raðnúmer")

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-serial-numbers"></a>Setja upp flokk rakningarnúmera sem býður upp á lista af fyrirframskilgreindum raðnúmerum

Til að bjóða upp á lista með fyrirframskilgreindum raðnúmerum skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.

1. Farið í **Birgðastjórnun \> Uppsetning \> Víddir \> Flokkar rakningarnúmera**.
1. Stofna eða velja flokk rakningarnúmera sem á að setja upp.
1. Í flipanum **Almennt** skal stilla valkostinn **Aðeins fyrir birgðafærslur** á **Já**.
1. Notið reitinn **Á magn** til að skipta raðnúmerum eftir magni.

    ![Rakningarnúmeraflokkur fyrir fyrirframskilgreind raðnúmer](media/tracking-number-group-predefined-sn.png "Rakningarnúmeraflokkur fyrir fyrirframskilgreind raðnúmer")

1. Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk raðnúmers fyrir útgefnar afurðir sem á að nota í þessari atburðarás.

Þegar þessi atburðarás er notuð er reiturinn **Raðnúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á fellilisti þar sem starfsmenn verða að velja fyrirframskilgreint gildi.

![Tilkynningarsíða framvindu með lista yfir fyrirframskilgreind raðnúmer](media/job-card-device-serial-predefined.png "Tilkynningarsíða framvindu með lista yfir fyrirframskilgreind raðnúmer")

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-serial-numbers"></a>Setja upp flokk rakningarnúmera sem sjálfkrafa úthluta raðnúmerum

Ef úthluta á raðnúmeri sjálfkrafa, án innsláttar starfsmanns, skal fylgja þessum skrefum til að setja upp flokk rakningarnúmera.

1. Farið í **Birgðastjórnun \> Uppsetning \> Víddir \> Flokkar rakningarnúmera**.
1. Stofna eða velja flokk rakningarnúmera sem á að setja upp.
1. Í flipanum **Almennt** skal stilla valkostinn **Aðeins fyrir birgðafærslur** á **Nei**.
1. Stillið **Handvirkt** valkostinn á **Nei**.

    ![Rakningarnúmeraflokkur fyrir föst raðnúmer](media/tracking-number-group-fixed-sn.png "Rakningarnúmeraflokkur fyrir föst raðnúmer")

1. Stillið önnur gildi eftir þörfum og veljið síðan þennan flokk rakningarnúmera sem flokk raðnúmers fyrir útgefnar afurðir sem á að nota í þessari atburðarás.

Þegar þessi atburðarás er notuð mun reiturinn **Raðnúmer** sem síðan **Tilkynna framvindu** í verkspjaldstækinu býður upp á sýna gildi, en starfsmenn geta ekki breytt því. Þessar aðstæður eiga aðeins við þegar framleiðslupöntun er stofnuð fyrir magn sem nemur einu stykki af raðnúmerastýrðri vöru.

![Tilkynningarsíða framvindu með ákveðnu raðnúmeri](media/job-card-device-serial-fixed.png "Tilkynningarsíða framvindu með föstum raðnúmerum")

## <a name="report-as-finished-to-a-license-plate"></a>Tilkynna sem lokið til númeraplötu

Ítarleg vöruhúsaferli geta notað númeraplötuvídd til að rekja birgðir í vöruhúsastaðsetningum sem hafa verið settar upp í þessum tilgangi. Í þessu tilvikum er krafist númer númeraplötu starfskraftur tilkynnir magn sem lokið.

### <a name="enable-license-plate-reporting-and-label-printing"></a>Virkja tilkynningu númeraplötu og prentun merkis

Til að nota eiginleikana sem lýst er í þessum hluta þarf að nota [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eftirfarandi eiginleikum (í þessari röð):

1. Númeraplata fyrir tilkynningu um lok var bætt við verkspjaldstækið
1. Kveiktu á sjálfvirkri myndun á númeraplötunúmeri þegar tilkynnt er um lok í verkspjaldstækinu.
1. Prenta merki úr verkspjaldstæki

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a>Setja upp tilkynna sem lokið til númeraplötu

Til að geta stjórnað því hvort starfsmenn ættu að endurnýta fyrirliggjandi númeraplötu eða mynda nýja númeraplöttu þegar þeir tilkynna að magn sé búið skal fylgja þessum skrefum.

1. Farið í **Framleiðslustjórnun \> Uppsetning \> Framkvæmd framleiðslu \> Skilgreina verkspjald fyrir tæki**.
2. Velja eftirfarandi valmöguleika fyrir hvert tæki:

    - **Mynda númeraplötu** - Stillið þennan valkost á **Já** til að mynda nýja númeraplötu fyrir hverja tilkynningu um lokið. Stillið hann á **Nei** ef nota á fyrirliggjandi númeraplötu fyrir hverja tilkynningu um lokið.
    - **Prenta merki** – Stillið þennan valkost á **Já** ef starfsmaðurinn verður að prenta númeraplötumerki fyrir hverja tilkynningu um lokið. Stillið þetta á **Nei** ef engra merkinga er krafist. 

![Síðan fyrir skilgreiningu verkspjalds fyrir tæki](media/config-job-card-raf.png "Síðan fyrir skilgreiningu verkspjalds fyrir tæki")

> [!NOTE]
> Til að skilgreina merkið skal fara í **Vöruhúsastjórnun \> Uppsetning \> Skjalaleið \> Skjalaleið**. Frekari upplýsingar er að finna í [Leyfa prentun númeraplötumerkis](../warehousing/tasks/license-plate-label-printing.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]