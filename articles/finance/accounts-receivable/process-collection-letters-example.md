---
title: Dæmi um úrvinnslu innheimtubréfs
description: Þessi grein fer í gegnum dæmi sem sýnir ferlið við að búa til, prenta og senda innheimtubréf.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9022051ce1c99da7ff62e30583a20656c77d89f9
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778546"
---
# <a name="process-collection-letters-example"></a>Dæmi um úrvinnslu innheimtubréfs

[!include [banner](../../includes/banner.md)]

Þessi grein fer í gegnum dæmi sem sýnir ferlið við að búa til, prenta og senda innheimtubréf. Þetta dæmi byggist á valkostinum **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** í Skuldir og innheimta. Það notar gögn úr sýnifyrirtækinu USMF og nýjan viðskiptavin, US-045.

Til að hefjast handa skal fara í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**, velja **Nýr** og síðan færa inn nauðsynlegar upplýsingar til að stofna viðskiptavin US-045.

Þegar því er lokið skal fylgja þessum skrefum.

1. Farið í **Skuldir og innheimta \> Innheimtubréf \> Uppsetning innheimtubréfaraðar** og setjið upp innheimtubréfaröðina eins og sýnt er í eftirfarandi töflu sem er úthlutað á bókunarreglu viðskiptavinar.

|   Innheimtubréfaflokkur      |     lýsing       |     Gjaldmiðill      |     Aðallykill        |     Gjald í gjaldmiðli       |   Lágmark yfir  |   Dagar útilokunar        |
|-----------------------------  |--------------------   |-----------------  |-----------------------    |--------------------   |-----------------------    |------------------ |
|  Innheimtubréf 1          |     Fyrsta tilkynning |     USD          |                   |     0,00              |     0,00                  |     2                 |
|  Innheimtubréf 2          |     Önnur tilkynning með gjaldi      |     USD      |     403150         |     20.00         |     10,00     |     3                 |
|  Innheimta                   |     Lokatilkynning með gjaldi       |     USD           |     403150    |     50.00         |     100.00                |     15            |

Eftirfarandi mynd sýnir upplýsingarnar sem eru í töflunni eins og þær myndu birtast á síðunni **Innheimtubréf**. 

[![Innheimtubréfaröð sett upp.](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)

 Nú þarf að stilla þessar tvær færibreytur sem eru nauðsynlegar fyrir þetta dæmi.

2. Farið í **Skuldir og innheimta \> Uppsetning \> Færibreytur viðskiptakrafna** og fylgjið þessum skrefum:

    1. Í flipanum **Innheimtur** skal stilla valkostinn **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** á **Já**.
    2. Ganga skal úr skugga um að reiturinn **Stofna innheimtubréf eftir** sé stilltur á **Viðskiptavinur**.

    [![Færibreytur viðskiptakrafna settar upp fyrir innheimtu skulda.](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)

3. Farið í **Viðskiptakröfur \> Reikningar \> Allir reikningar með frjálsum texta**, veljið **Nýr** og fylgið því næst þessum skrefum:

    1. Í reitnum **Viðskiptavinalykill** skal velja **US-045**.
    2. Í reitinn **Reikningsdagsetning** skal slá inn **1/15/2021**.
    3. Í reitinn **Gjalddagi** skal slá inn **1/16/2021**.
    4. Í flýtiflipann **Reikningslínur**, í reitinn **Aðallykill**, skal færa inn **401100**.
    5. Í reitinn **Einingarverð** skal slá inn **500.00**.
    6. Veldu **Bóka**.

    Nú skal færa inn tvær kreditnótur fyrir viðskiptavininn.

4. Veljið **Ný** og fylgið síðan þessum skrefum:

    1. Í reitnum **Viðskiptavinalykill** skal velja **US-045**.
    2. Í reitinn **Reikningsdagsetning** skal slá inn **1/15/2021**.
    3. Í reitinn **Gjalddagi** skal slá inn **1/16/2021**.
    4. Í flýtiflipann **Reikningslínur**, í reitinn **Aðallykill**, skal færa inn **401100**.
    5. Í reitinn **Einingarverð** skal slá inn **-100,00**.
    6. Veldu **Bóka**.

5. Endurtakið skref 4, en færið inn **-200,00** í reitinn **Einingarverð**.
6. Farið í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir** og veljið viðskiptavininn **US-045**. Á aðgerðasvæðinu skal síðan velja **Færslur \> Færslur** til að fara yfir færslur viðskiptavina sem voru bókaðar hér áður.

    [![Bókaðar færslur viðskiptavina yfirfarnar.](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)

    Nú þarf að stofna innheimtubréf fyrir viðskiptavin US-045.

7. Farið í **Skuldir og innheimta \> Innheimtubréf \> Stofna innheimtubréf** og fylgið þessum skrefum:

    1. Stillið valkostina **Reikningur** og **Kreditnóta** á **Já**.

        Sjálfgefið er að reiturinn **Innheimtubréf** sé stilltur á **Innheimta eftir viðskiptavini**.

    2. Í reitinn **Dagsetning innheimtubréfs** skal slá inn **1/19/2021**.
    3. Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** og því næst, í reitnum **Viðskiptavinalykill**, skal bæta við viðskiptavini **US-045**.
    4. Veljið **Í lagi**.
    5. Veljið **Í lagi** til að stofna innheimtubréf.

8. Farið í **Skuldir og innheimta \> Innheimtubréf \> Yfirfara og vinna úr innheimtubréfum** og fylgið þessum skrefum:

    1. Athugið að kóði innheimtubréfs í bæði haus og færslulínum er **Innheimtubréf 1** vegna þess að þetta er fyrsta innheimtubréfið í röðinni. (Til að skoða færslulínur gæti þurft að velja flýtiflipann **Færslur**.)

   [![Staðfesting á því að sami kóði innheimtubréfs komi fram í haus og í línum.](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)

    2. Á aðgerðasvæðinu skal velja **Bóka**.
    3. Í reitinn **Bókunardagssetning** skal færa inn **1/19/2021**.

    Nú þarf að stofna innheimtubréf aftur fyrir viðskiptavin US-045.

9. Farið í **Skuldir og innheimta \> Innheimtubréf \> Stofna innheimtubréf** og fylgið þessum skrefum:

    1. Stillið valkostina **Reikningur** og **Kreditnóta** á **Já**.

        Sjálfgefið er að reiturinn **Innheimtubréf** sé stilltur á **Innheimta eftir viðskiptavini**.

    2. Í reitinn **Dagsetning innheimtubréfs** skal slá inn **1/23/2021**.
    3. Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** og því næst, í reitnum **Viðskiptavinalykill**, skal bæta við viðskiptavini **US-045**.
    4. Veljið **Í lagi**.
    5. Veljið **Í lagi** til að stofna innheimtubréf.

10. Farið í **Skuldir og innheimta \> Innheimtubréf \> Yfirfara og vinna úr innheimtubréfum** og fylgið þessum skrefum:

    1. Takið eftir að kóði innheimtubréfs í hausnum er **Innheimtubréf 1**. Kóðinn í færslulínunum er hins vegar **Innheimtubréf 2**.

   [![Staðfestir að mismunandi kóðar innheimtubréfs koma fram í haus og línum.](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)

  Kóðarnir eru ólíkir vegna þess að valkosturinn **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** er stilltur á **Já**.

  2. Ekki bóka þetta innheimtubréf.

11. Farið í **Skuldir og innheimta \> Uppsetning \> Færibreytur viðskiptakrafna** og því næst í flipanum **Innheimtur** skal stilla valkostinn **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** á **Nei**.

    [![Hunsa greiðslur og kreditnótur stillt þegar valkostur fyrir útreikning innheimtubréfakóða er stilltur á nei.](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)

    Nú þarf að stofna innheimtubréf aftur fyrir viðskiptavin US-045.

12. Farið í **Skuldir og innheimta \> Innheimtubréf \> Stofna innheimtubréf** og fylgið þessum skrefum:

    1. Stillið valkostina **Reikningur** og **Kreditnóta** á **Já**.

        Sjálfgefið er að reiturinn **Innheimtubréf** sé stilltur á **Innheimta eftir viðskiptavini**.

    2. Í reitinn **Dagsetning innheimtubréfs** skal slá inn **1/23/2021**.
    3. Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** og því næst, í reitnum **Viðskiptavinalykill**, skal bæta við viðskiptavini **US-045**.
    4. Veljið **Í lagi**.
    5. Veljið **Í lagi** til að stofna innheimtubréf.

13. Farið í **Skuldir og innheimta \> Innheimtubréf \> Yfirfara og vinna úr innheimtubréfum** og takið eftir því að kóði innheimtubréfs bæði í haus og færslulínum er **Innheimtubréf 2**.

    [![Sýnir aftur að sami kóði innheimtubréfs komi fram í haus og í línum.](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)

    Sami kóðinn kemur fram á báðum stöðum vegna þess að valkosturinn **Hunsa greiðslur og kreditnótur þegar kóði innheimtubréfs er reiknaður út** er stilltur á **Nei**.
