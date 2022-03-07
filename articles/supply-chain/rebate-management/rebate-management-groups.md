---
title: Hópa fyrir stjórnun eftirágreidds afsláttar
description: Í þessu efnisatriði er lýst hvernig á að setja upp hópa fyrir stjórnun eftirágreidds afsláttar. Hægt er að nota hópa fyrir stjórnun eftirágreidds afsláttar í útreikningum eftirágreidds afsláttar og hengja þá við aðalfærslu.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1f9deeedef504d1b2d0ba3431902c50bc65d62ba
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572698"
---
# <a name="rebate-management-groups"></a>Hópar fyrir stjórnun eftirágreidds afsláttar

[!include [banner](../includes/banner.md)]

Hópar geta keyrt útreikninga á eftirágreiddum afslætti. Hægt er að búa til hópa fyrir stjórnun eftirágreidds afsláttar fyrir viðskiptavini, lánardrottna og vörur. Hægt er að hengja þá við aðalfærslu.

## <a name="rebate-management-customer-groups"></a>Viðskiptavinahópar fyrir stjórnun eftirágreidds afsláttar

Útreikningurinn fyrir hóp viðskiptavina er oft stofnaður fyrir fyrirtækjakeðju á borð við verslunarkeðju eða vörumerki. Þessi gerð útreiknings tengist yfirleitt eftirágreiddum afslætti.

Lækkun er oftast reiknuð án þess að taka til greina hverjum pöntunin er seld til. Hins vegar eru til undantekningar. Til dæmis gæti leyfishafi búið til lækkunarskema þar sem viðskiptavinaflokkur A fær 4 prósent en viðskiptavinaflokkur B fær aðeins 3 prósent.

### <a name="set-up-customer-groups"></a>Setja upp viðskiptavinaflokka

Til að vinna með viðskiptavinaflokka fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Viðskiptavinaflokkar**. Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á. Fyrir hvern hóp skal stilla eftirfarandi reiti:

- **Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.
- **Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.

### <a name="manage-customer-group-assignments"></a>Stjórna úthlutunum viðskiptavinaflokka

Hver viðskiptavinur getur tilheyrt fjölda flokka í stjórnun eftirágreidds afsláttar. Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða viðskiptavinalistanum.

Til að skoða, bæta við eða fjarlægja lánardrottna fyrir valinn hóp skal fylgja þessum skrefum.

1. Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Viðskiptavinaflokkar**.
1. Veljið hópinn sem á að stjórna.
1. Í aðgerðarúðunni skal velja **Viðskiptavinir**. Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir viðskiptavini sem eru þegar meðlimir í völdum hópi.
1. Til að bæta nýjum viðskiptavini við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið. Stillið svo eftirfarandi reit fyrir nýju línuna:

    - **Viðskiptavinalykill** – Veljið kenni viðskiptavinalykils.

1. Til að fjarlægja viðskiptavin úr hópnum skal velja viðskiptavin og velja svo **Eyða** á aðgerðasvæðinu.

Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valinn viðskiptavin skal fylgja þessum skrefum.

1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
1. Veljið viðskiptavin til að vinna með.
1. Á aðgerðasvæðinu, í flipanum **Viðskiptavinur**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**. Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valinn viðskiptavinur tilheyrir.
1. Til að bæta viðskiptavininum við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið. Stillið svo eftirfarandi reit fyrir nýju línuna:

    - **Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta viðskiptavini við hann.

1. Til að fjarlægja viðskiptavin úr hópi skal velja hópinn og velja síðan **Eyða** á aðgerðasvæðinu.

## <a name="rebate-management-vendor-groups"></a>Lánardrottnaflokkar fyrir stjórnun eftirágreidds afsláttar

Útreikningurinn fyrir hóp lánardrottna er oft búinn til fyrir hóp afhendingarstaða. Þessi gerð útreiknings tengist yfirleitt eftirágreiddum afslætti.

### <a name="set-up-vendor-groups"></a>Uppsetning lánardrottnaflokka

Til að vinna með lánardrottnaflokk fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Lánardrottnaflokkar**. Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á. Fyrir hvern hóp skal stilla eftirfarandi reiti:

- **Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.
- **Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.

### <a name="manage-vendor-group-assignments"></a>Stjórna úthlutunum lánardrottnaflokka

Hver lánardrottinn getur tilheyrt fjölda hópa í stjórnun eftirágreidds afsláttar. Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða lánardrottnalistanum.

Til að skoða, bæta við eða fjarlægja lánardrottna fyrir valinn hóp skal fylgja þessum skrefum.

1. Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Lánardrottnaflokkar**.
1. Veljið hópinn sem á að stjórna.
1. Á aðgerðasvæðinu velurðu **Lánardrottnar**. Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir lánardrottna sem eru þegar meðlimir í völdum hópi.
1. Til að bæta nýjum lánardrottni við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið. Stillið svo eftirfarandi reit fyrir nýju línuna:

    - **Lánardrottnalykill** – Veljið kenni lánardrottnalykils.

1. Til að fjarlægja lánardrottin úr hópnum skal velja lánardrottin og velja svo **Eyða** á aðgerðasvæðinu.

Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valinn lánardrottinn skal fylgja þessum skrefum.

1. Farið í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar**.
1. Veljið lánardrottin til að vinna með.
1. Á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**. Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valinn lánardrottinn tilheyrir.
1. Til að bæta lánardrottni við hópinn skal velja **Nýr** á aðgerðasvæðinu til að bæta línu við hnitanetið. Stillið svo eftirfarandi reit fyrir nýju línuna:

    - **Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta lánardrottni við hann.

1. Til að fjarlægja lánardrottin úr hópi skal velja hópinn og velja síðan **Eyða** á aðgerðasvæðinu.

## <a name="item-rebate-groups"></a>Flokkar atriða eftirágreidds afsláttar

Með því að flokka vörur eykst sveigjanleiki þegar eftirágreiddur afsláttur og lækkanir eru reiknaðar út. Þessi nálgun er oft hagkvæmari leið til að setja upp eftirágreiddan afslátt og lækkanir fyrir viðskiptavini og lánardrottna.

### <a name="set-up-item-groups"></a>Setja upp vöruflokka

Til að vinna með vöruflokka fyrir stjórnun eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**. Hægt er að nota hnappana í aðgerðarúðunni til að bæta við eða fjarlægja hópa eins og þörf er á. Fyrir hvern hóp skal stilla eftirfarandi reiti:

- **Hópur fyrir stjórnun eftirágreidds afsláttar** – Sláið inn einkvæmt heiti fyrir hópinn.
- **Lýsing** – Sláið inn lýsingu hópsins til að veita frekari upplýsingar um hvernig á að setja hann upp.

### <a name="manage-item-group-assignments"></a>Stjórna úthlutunum vöruflokks

Hver vara getur tilheyrt fjölda hópa í stjórnun eftirágreidds afsláttar. Til að skoða og úthluta hópmeðlimum er hægt að byrja á hópalistanum eða vörulistanum. Einnig er hægt að bæta við vörum samkvæmt tegundastigveldinu.

Til að skoða, bæta við eða fjarlægja vörur fyrir valinn hóp skal fylgja þessum skrefum.

1. Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**.
1. Veljið hópinn sem á að stjórna.
1. Á aðgerðasvæðinu skal velja **Vörur**. Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir vörur sem eru þegar meðlimir í völdum hópi.
1. Til að bæta nýrri vöru við hópinn skal velja **Ný** á aðgerðasvæðinu til að bæta línu við hnitanetið. Stillið svo eftirfarandi reit fyrir nýju línuna:

    - **Vörureikningur** – Veljið kenni vörureiknings.

1. Til að fjarlægja vöru úr hópi skal velja vöruna og velja **Eyða** á aðgerðasvæðinu.

Til að skoða, bæta við eða fjarlægja hópverkefni fyrir valda vöru skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið vöruna til að vinna með.
1. Á aðgerðasvæðinu, í flipanum **Afurð**, í flokknum **Stjórnun eftirágreidds afsláttar**, skal velja **Hópar fyrir stjórnun eftirágreidds afsláttar**. Síðan **Hópar fyrir stjórnun eftirágreidds afsláttar** birtist og sýnir lista yfir hópa sem valin vara tilheyrir.
1. Til að bæta vöru við hópinn skal velja **Ný** á aðgerðasvæðinu til að bæta línu við hnitanetið. Stillið svo eftirfarandi reit fyrir nýju línuna:

    - **Hópur fyrir stjórnun eftirágreidds afsláttar** – Veljið hópinn til að bæta vöru við hann.

1. Til að fjarlægja vöru úr hópi skal velja hópinn og velja **Eyða** á aðgerðasvæðinu.

Til að bæta vörum við hóp samkvæmt tegundastigveldinu skal fylgja þessum skrefum.

1. Farið í **Stjórnun eftirágreidds afsláttar \> Uppsetning hóps fyrir stjórnun eftirágreidds afsláttar \> Vöruflokkar**.
1. Veljið hópinn sem á að stjórna.
1. Á aðgerðasvæðinu skal velja **Bæta við vörum**.
1. Í svarglugganum **Bæta við vörum**, í reitnum **Tegundastigveldi**, skal velja hóp á hæsta stigi.
1. Stigveldi vöru er opnað á svæðinu til vinstri. Veldu stigveldi sem þú ert að leita að. 
1. Vörur úr völdu stigveldi og stig stigveldis er nú sýnt á svæðinu til hægri. Fylgið þessum skrefum til að vinna með svæðið:

    - Veljið gátreitinn fyrir hverja vöru sem á að bæta við.
    - Veljið gátreitinn í haus hnitanetsins til að velja allar vörurnar sem eru sýndar.
    - Veljið hnappinn **Sýna valið** til að sía hnitanetið þannig að það sýni aðeins vörurnar sem hafa verið valdar fram að þessu. Veljið hnappinn aftur til að fara aftur í heildarlistann.

1. Veljið **Í lagi** til að færa vöruvalið yfir í valinn hóp.
