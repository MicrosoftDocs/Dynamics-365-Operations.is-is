---
title: Bóka komur og sendingar fyrir Intrastat.
description: Þetta efnisatriði sýnir hvernig á að bóka komur og sendingar fyrir Intrastat.
author: andosip
ms.date: 8/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfender
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: f7bd1811fd0e580a6b6655244c689268915d320e
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414788"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>Bóka komur og sendingar fyrir Intrastat.

[!include [banner](../includes/banner.md)]

Þetta efnisatriði sýnir hvernig á að bóka komur og sendingar fyrir Intrastat. Í dæminu er notast við lögaðilann **ITCO**.

## <a name="setup"></a>Setja upp

1. Flyttu inn nýjustu útgáfuna af eftirfarandi skilgreiningum fyrir rafræna skýrslugerð:

    - Intrastat-líkan
    - Intrastat-skýrsla
    - Intrastat (IT)

    Þú finnur frekari upplýsingar í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. Í Microsoft Dynamics 365 Finance skal skilgreina eftirfarandi númeraraðir sem samfelldar: **Gene\_397**, **Acco\_16403**, **Gene\_407** og **PUR\_EU**.

    1. Farðu í **Fyrirtækisstjórnun** > **Númeraraðir** > **Númeraraðir**.
    2. Í hnitanetinu skal velja einn af kóðum númeraraðar.
    3. Á aðgerðarúðunni skal velja **Breyta**.
    4. Í flýtflipanum **Almennt**, í hlutanum **Uppsetning**, skal stilla valkostinn **Samfellt** á **Já**.
    5. Í aðgerðarúðunni skal velja **Vista**.

3. Stilltu aðsetur vöruhúss.

    1. Farðu í **Vöruhúsakerfi** &gt; **Uppsetning** &gt; **Vöruhús** &gt; **Vöruhús**.
    2. Í listanum skal velja vöruhús **11**.
    3. Í flýtiflipanum **Aðsetur** skal velja **Bæta við**.
    4. Í svarglugganum **Nýtt** **aðsetur**, í reitinn **Heiti** **eða** **Lýsing**, skal færa inn **Aðal**.
    5. Í reitnum **Land/svæði** skal velja **ITA (Ítalía)**.
    6. Í reitnum **Borg** skal velja **Aprilia**.
    7. Veldu **Í lagi**.

4. Setja upp færslukóða.

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færslukóðar**.
    2. Veldu **Nýr** og settu upp færslukóða fyrir eignafærslur.

        - Í reitinn **Færslukóði** skal færa inn **1**.
        - Í reitinn **Heiti** skal færa inn **Eignafærsla**.

    3. Veldu **Nýr** og settu upp færslukóða fyrir skil.

        - Í reitinn **Færslu** **kóði** skaltu slá inn **2**.
        - Í reitinn **Heiti** skal færa inn **Vöruskil**.

5.  Setja upp færibreytur erlendra viðskipta.

    1. Farið í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Færibreytur erlendra viðskipta**.
    2. Í flýtiflipanum **Intrastat** á **Almennt** flipanum í **Færslukóði** reitknum velurðu **1**.
    3. Í reitnum **Kreditnóta** skal velja **2**.
    4. Í reitnum **Skýrslutímabil sölu** skal velja **Mánuður**.
    5. Í reitnum **Skýrslutímabil innkaupa** skal velja **Mánuður**.
    6. Í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Vörpun skráarsniðs**, skal velja **Intrastat (IT)**.
    7. Í reitnum **Vörpun skýrslusniðs** skal velja **Intrastat-skýrslu**.
    8. Í flýtiflipanum **Stigveldi vörukóða**, í reitnum **Tegundastigveldi**, skal velja **Intrastat**.
    9. Í flýtiflipanum **Tölfræðilegt gildi** skal stilla valkostinn **Prenta og flytja út talnagögn** á **Já**.
    10. Í flipanum **Eiginleikar lands/svæðis** skal staðfesta að eftirfarandi lína sé til staðar.

        | **Aðili/land/svæði** | **Intrastat-kóði** | **Gjaldmiðill** | **Gerð lands/svæðis** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Innlent                |
        | SMR                      | SM                 | EUR          | Sérstakt innanlands        |

    11. Á tækjastikunni skal velja **Ný** til að stofna eftirfarandi línu.

        | **Aðili/land/svæði** | **Intrastat-kóði** | **Gjaldmiðill** | **Gerð lands/svæðis** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | ESB                      |

6. Setja upp skattundanþágunúmer.

    1. Farðu í **Skattur** > **Uppsetning** > **Söluskattur** > **Skattaundanþágunúmer**.
    2. Á aðgerðasvæðinu skal velja **Ný** til að stofna eftirfarandi línur.

        | **Land/svæði** | **Skattundanþágunúmer** | **Heiti fyrirtækis** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE VENDOR        |
        | DNK                | DK0987654321          | Rafræn skýrslugerð viðskiptavinar      |

7. Stilltu aðsetur lánardrottins.

    1. Farið í **Viðskiptaskuldir** &gt; **Lánardrottnar** &gt; **Allir lánardrottnar**.
    2. Í hnitanetinu skal velja **UE Lánardrottinn**.
    3. Í flýtiflipanum **Aðsetur** skal velja **Bæta við**.
    4. Í svargluggann **Nýtt aðsetur**, í reitinn **Heiti eða lýsing**, skal færa inn **Þýskaland**.
    5. Í reitnum **Land/svæði** skal velja **DEU**.
    6. Veldu **Í lagi** til að stofna nýja aðsetrið.
    7. Í flýtiflipanum **Reikningur og afhending**, í hlutanum **Söluskattur**, í reitnum **Skattundanþágunúmer**, skal velja **Allt** og síðan velja **DE1234567890**.
    8. Í aðgerðarúðunni skal velja **Vista**.

8. Stilla aðsetur viðskiptavinar.

    1. Farið í **Viðskiptakröfur** > **Viðskiptavinir** > **Allir viðskiptavinir**.
    2. Í hnitanetinu skal velja **ITCO-000001**.
    3. Í flýtiflipanum **Aðsetur** skal velja **Breyta**.
    4. Í svargluggann **Nýtt aðsetur**, í reitinn **Heiti eða lýsing**, skal færa inn **San Marínó**.
    5. Í reitnum **Land/svæði** skal velja **SMR**.
    6. Veldu **Í lagi** til að stofna nýja aðsetrið.
    7. Í flýtiflipanum **Reikningur og afhending**, í hlutanum **Reikningur**, í reitnum **Reikningslykill**, skal velja **ITCO-000001**.
    8. Í reitnum **Númeraraðaflokkur** skal velja **IT\_VENDOM**.
    9. Í aðgerðarúðunni skal velja **Vista** og loka síðunni.
    10. Á síðunni **Allir viðskiptavinir**, í hnitanetinu, skal velja **ITCO-000002**.
    11. Í flýtiflipanum **Aðsetur** skal velja **Bæta við**.
    12. Í svargluggann **Nýtt aðsetur**, í reitinn **Heiti eða lýsing**, skal færa inn **Danmörk**.
    13. Í reitnum **Land/svæði** skal velja **DNK**.
    14. Veldu **Í lagi** til að stofna nýja aðsetrið.
    15. Í flýtiflipanum **Lýðfræðilegar upplýsingar um sölu**, í reitnum **Gjaldmiðill**, skal velja **DKK**.
    16. Í flýtiflipanum **Reikningur og afhending**, í hlutanum **Söluskattur**, í reitnum **VSK-flokkur**, skal velja **IT\_PUREA**.
    17. Í reitnum **Skattundanþágunúmer** skal velja **Allt** og síðan velja **DK0987654321**.
    18. Í aðgerðarúðunni skal velja **Vista**.

9. Settu upp tegundastigveldi.

    1. Farðu í **Afurðaupplýsingastjórnun** > **Uppsetning** > **Flokkar og eigindir** > **Flokkastigveldi**.
    2. Í hnitanetinu skal velja **Intrastat**.
    3. Á aðgerðasvæðinu skal velja **Nýr tegundarhnútur**.
    4. Í reitinn **Heiti** skal færa inn **Þjónusta**.
    5. Í reitinn **Kóði** skal færa inn **123456**.
    6. Í aðgerðarúðunni skal velja **Vista**.

10. Setja upp afurðir.

    1. Opna **Afurðaupplýsingastjórnun** > **Afurðir** > **Útgefnar afurðir**.
    2. Í hnitanetinu skal velja **ITEM**.
    3. Í flýtiflipanum **Innkaup**, í hlutanum **Stjórnun**, í reitnum **Lánardrottinn**, skal velja **ITCO-000001**.
    4. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja **\[100 200 30\] Hátalari**.
    5. Í hlutanum **Uppruni**, í reitnum **Land/svæði**, skal velja **DEU**.
    6. Í reitnum **Ríki/hérað** skal velja **BE**.
    7. Í flýtiflipanum **Stjórna birgðum**, í hlutanum **Nettómælingar**, í reitinn **Nettóþyngd**, skal færa inn **5**.
    8. Í aðgerðarúðunni skal velja **Vista**.
    9. Á síðunni **Útgefnar afurðir**, í hnitanetinu, skal velja **Þjónustuvöru**.
    10. Í flýtiflipanum **Erlend viðskipti**, í hlutanum **Intrastat**, í reitnum **Varningur**, skal velja **\[123456\] Þjónusta**.
    11. Í aðgerðarúðunni skal velja **Vista**.

11. Settu upp flutningsmáta.

    1. Farðu í **Skattur** > **Uppsetning** > **Erlend viðskipti** > **Flutningsmáti**.
    2. Á aðgerðasvæðinu skal velja **Nýr** til að stofna nýja flutningsmáta.

        | **Flutningur** | **Lýsing** |
        |---------------|-----------------|
        | 1             | Vegur            |
        | 2             | Loft             |

12. Settu upp afhendingarmáta.

    1. Farðu í **Innkaup og aðföng** > **Uppsetning** > **Dreifing** > **Flutningsmátar**.
    2. Í aðgerðarúðunni velurðu **Nýtt**.
    3. Í reitinn **Afhendingarmáti** skal færa inn **1**.
    4. Í reitinn **Lýsing** skal færa inn **Flutningabíll**.
    5. Í flýtiflipanum **Erlend viðskipti**, í reitnum **Flutningur**, skal velja **1 Landleiðis**.
    6. Í aðgerðarúðunni skal velja **Vista**.

13. Setja upp afhendingarskilmála.

    1. Farðu í **Viðskiptaskuldir** > **Uppsetning** > **Afhendingarskilmálar**.
    2. Í listanum skal velja **CFR**.
    3. Í flýtiflipann **Almennt**, í reitinn **Intrastat-kóði**, skal færa inn **1**.

## <a name="post-arrivals-for-intrastat"></a>Bóka komur fyrir Intrastat

### <a name="purchase-goods-by-using-a-purchase-order"></a>Kaupa varning með innkaupapöntun

Þessi hluti dæmisins sýnir hvernig nota á innkaupapöntun til að kaupa varning (vörur) frá löndum Evrópusambandsins (ESB).

1. Farðu í **Viðskiptaskuldir** > **Innkaupapantanir** > **Allar innkaupapantanir**.
2.  Í aðgerðarúðunni velurðu **Nýtt**.
3.  Í svarglugganum **Stofna innkaupapöntun**, í reitnum **Lánardrottnalykill**, skal velja **UE Lánardrottinn**.
4.  Í flýtiflipanum **Stjórnun**, í reitnum **Tungumál**, skal velja **hana**.
5.  Veldu **Í lagi**.
6.  Í **Hausyfirlitinu**, í flýtiflipanum **Erlend** **viðskipti** skal staðfesta að reiturinn **Færslukóði** sé stilltur á **1**.
7.  Staðfestu að reiturinn **Uppruna/viðtökuumdæmi** sé stilltur á **RM**.
8.  Í flýtiflipanum **Afhending**, í hlutanum **Afhending**, í reitnum **Afhendingarmáti**, skal velja **1**.
9.  Í reitnum **Afhendingarskilmálar** skal velja **CFR**.
10. Í yfirlitinu **Línur**, í flýtiflipanum **Innkaupapöntunarlínur**, í reitnum **Vörunúmer**, skal velja **Vala**.
11. Í reitnum **Svæði** skal velja **1**.
12. Í reitnum **Vöruhús** skal velja **11**.
13. Í **Magn** reitinn er fært inn **10**.
14. Í reitinn **Einingarverð** skal slá inn **100**.
15. Í flipanum **Uppsetning**, í hlutanum **Söluskattur**, í reitnum **VSK-flokkur vöru**, skal velja **22%EU**.
16. Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Aðgerðir**, skal velja **Staðfesta**.
17. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.
18. Á aðgerðasvæðinu skal velja **Sjálfgefið frá**.
19. Í reitnum **Sjálfgefið magn fyrir línur** skal velja **Pantað magn** og velja **Í lagi**.
20. Í flýtiflipanum **Reikningshaus lánardrottins**, í hlutann **Auðkenning reiknings**, í reitinn **Númer**, skal færa inn **0001**.
21. Í hlutanum **Reikningsdagsetningar**, í reitnum **Reikningsdagsetning**, skal velja **7/9/2021**.
22. Á aðgerðasvæðinu skal velja **Bóka** til að bóka reikninginn.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Þjónusta keypt með lánardrottnareikningi

Þessi hluti dæmisins sýnir hvernig á að nota lánardrottnareikning til að kaupa þjónustu frá ESB-löndum.

1. Farðu í **Viðskiptaskuldir** > **Reikningar** > **Reikningabók**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í reitnum **Heiti** skal velja **VEND\_EUINV**.
4. Á aðgerðasvæðinu skal velja **Línur**.
5. Í reitinn **Dagsetning** skal færa inn **7/9/2021**.
6. Í reitnum **Gerð reiknings** skal velja **Lánardrottinn**.
7. Í reitnum **Reikningur** skal velja **UE lánardrottinn**.
8. Í reitnum **Reikningsdagsetning** skal velja **7/9/2021**.
9. Í reitnum **Reikningur** skal færa inn **ITA-0004**.
10. Í reitinn **Kreditfæra** skal slá inn **120000**.
11. Í **gerð** **mótlykils** reitinn skaltu velja **Fjárhagur**.
12. Í **Gerð mótlykils** reitnum skal velja **110130**.
13. Í reitnum **VSK-flokkur** skal velja **IT\_PUREU**.
14. Í reitnum **VSK-flokkur vöru** skal velja **22%EU**.
15. Í flipanum **Erlend viðskipti** skal fylgja þessum skrefum:

    1. Í reitnum **Færslukóði** skal velja **1**.
    2. Í reitnum **Flutningur** skal velja **2 Flugleiðis**.
    3. Í reitnum **Vara** skal velja **\[123456\] Þjónusta**.
    4. Í reitnum **Land/svæði** skal velja **ITA**.
    5. Í reitnum **Ríki/hérað** skal velja **LAZ**.
    6. Í reitnum **Uppruna/viðtökuumdæmi** skal velja **LT**.


16. Á aðgerðasvæðinu skal velja **Bóka**.
17. Búðu til Intrastat-skattskýrsla fyrir komur.

    1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
    2. Á aðgerðasvæðinu skal velja **Flutningur**.
    3. Í svarglugganum **Intrastat (flutningur)** skal stilla valkostinn **Reikningur lánardrottins** á **Já**.
    4. Veldu **Í lagi** til að flytja færslurnar og síðan skoða Intrastat-bókina.

   ![Síða í Intrastat-bók, yfirlitsflipi.](media/ita_intrastat_journal_vendor_invoice.png)

18. Farðu yfir flipann **Almennt** fyrir innkaupapöntunina.

    ![Upplýsingar um línu Intrastatbókar fyrir innkaupapöntun](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Farðu yfir flipann **Almennt** fyrir reikning lánardrottins.

    ![Upplýsingar um línu Intrastat-bókar fyrir reikning lánardrottins](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Búðu til Intrastat skýrsluna fyrir komur.

    1. Á aðgerðasvæðinu skal velja **Úttak**  >  **Skýrsla**.
    2. Í svarglugganum **Intrastat-skýrsla**, í hlutanum **Dagsetning**, í reitnum **Frá dagsetningu**, skal velja **7/1/2021**.
    3. Í reitnum **Til dagsetningar** skal velja **7/31/2021**.
    4. Í hlutanum **Valkostir útflutnings** skal stilla valkostina **Mynda skrá** og **Mynda skýrslu** á **Já**.
    5. Í reitinn **Skráarheiti** skal færa inn **Komuskrá**.
    6. Í reitinn **Heiti skýrsluskráar** skal færa inn **Komuskýrsla**.
    7. Í reitnum **Stefna** skal velja **Komur**.
    8. Í reitinn **Tilvísunarnúmer** skal færa inn **123456**.
    9. Veldu **Í lagi** til að búa til Intrastat-skýrsluna og Intrastat-skrána og farðu yfir þær.

    Eftirfarandi skýringarmynd sýnir dæmi um Intrastat skýrslu.

    ![Intrastat-komuskýrsla.](media/ita_intrastat_arrivals_report.png)

    Eftirfarandi skýringarmynd sýnir dæmi um Intrastat-skrá.

    ![Intrastat-komuskrá.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Bóka sendingar fyrir Intrastat

### <a name="sell-goods-by-using-a-sales-order"></a>Selja varning með sölupöntun

Þessi hluti dæmisins sýnir hvernig nota á sölupöntun til að selja varning (vörur) til landa Evrópusambandsins (ESB).

1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna sölupöntun**, í reitnum **Viðskiptavinalykill**, skal velja **ITCO-000002**.
4. Veldu **Í lagi**.
5. Í **Hausyfirlitinu**, í flýtiflipanum **Afhending**, í hlutanum **Ýmsar afhendingarupplýsingar**, í reitnum **Afhendingarmáti**, skal velja **1 Flutningabíll**.
6. Í reitnum **Afhendingarskilmálar** skal velja **CFR**.
7. Í yfirlitinu **Línur**, í flýtiflipanum **Sölupöntunarlínur**, í reitnum **Vörunúmer**, skal velja **VARA**.
8. Í **Magn** reitinn er fært inn **50**.
9. Í reitnum **Svæði** skal velja **1**.
10. Í reitnum **Vöruhús** skal velja **11**.
11. Í reitinn **Einingarverð** skal slá inn **250**.
12. Í flipanum **Upplýsingar um línu** flipanum á **Uppsetning** í **Söluskattur** hlutanum í **VSK-flokkur vöru** reitnum skaltu velja **22%EU**.
13. Í aðgerðarúðunni skal velja **Vista**.
14. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja **Reikningur** til að búa til reikning fyrir pöntunina.
15. Í svarglugganum **Bókun reiknings**, í flýtiflipanum **Færibreytur**, í hlutanum **Færibreyta**, í reitnum **Magn**, skal velja **Allt**.
16. Í **Uppsetning** flipanum á **Reiknings** **dagsetning** reitnum skal velja **7/9/2021**.
17. Veldu **Í lagi**.
18. Farðu yfir línurnar í Intrastat-bókinni.

    1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
    2. Á aðgerðasvæðinu skal velja **Flutningur**.
    3. Í svarglugganum **Intrastat (flutningur)** skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
    4. Veldu **Í lagi** til að flytja færslurnar og fara yfir Intrastat-bókina. Færsla kreditnótu er merkt sem leiðrétting og er með neikvæðri reikningsupphæð.

        ![Síða Intrastat-bókar](media/ita_intrastat_journal_sales_order.png)

        ![Upplýsingar um línu Intrastat-bókar fyrir sölupöntun](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Skil á vörum með kreditnótu

Þessi hluti dæmisins sýnir hvernig nota á kreditnótu til að skila varningi (vörum) frá löndum Evrópusambandsins (ESB).

1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna sölupöntun**, í reitnum **Viðskiptavinalykill**, skal velja **ITCO-000002**.
4. Veldu **Í lagi**.
5. Í **Hausyfirlitinu**, í flýtiflipanum **Afhending**, í hlutanum **Ýmsar afhendingarupplýsingar**, í reitnum **Afhendingarmáti**, skal velja **1 Flutningabíll**.
6. Í reitnum **Afhendingarskilmálar** skal velja **CFR**.
7. Í flýtiflipanum **Erlend viðskipti**, í reitnum **Færslukóði**, skal velja **2**.
8. Í flipanum **Línur**, í flýtiflipanum **Sölupöntunarlínur**, í reitnum **Vörunúmer**, skal velja **VARA**.
9. Í **Magn** reitinn er fært inn **-10**.
10. Í reitnum **Svæði** skal velja **1**.
11. Í reitnum **Vöruhús** skal velja **11**.
12. Í reitinn **Einingarverð** skal slá inn **250**.
13. Í flipanum **Upplýsingar um línu** flipanum á **Uppsetning** í **Söluskattur** hlutanum í **VSK-flokkur vöru** reitnum skaltu velja **22%EU**.
14. Í hlutanum **Skiluð pöntun**, í reitnum **Skila lotukenni** skal velja lotuna sem þú bjóst til áður.
15. Í aðgerðarúðunni skal velja **Vista**.
16. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja **Reikningur** til að búa til reikning fyrir pöntunina.
17. Í flýtiflipanum **Færibreytur** í **Færibreyta** hlutanum **Magn** skaltu velja **Allt**.
18. Í svarglugganum **Bókun reiknings** í **Uppsetning** flipanum í **Reiknings** **dagsetning** reitnum skal velja **7/9/2021**.
19. Veldu svo **Í lagi** til að bóka reikninginn.
20. Farðu yfir línurnar í Intrastat-bókinni.

    1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
    2. Á aðgerðasvæðinu skal velja **Flutningur**.
    3. Í svarglugganum **Intrastat (flutningur)** skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
    4. Veldu **Í lagi** til að flytja færslurnar og fara yfir Intrastat-bókina. Færsla kreditnótu er merkt sem leiðrétting og er með neikvæðri reikningsupphæð.

    ![Kreditnóta Intrastat-bókar](media/ita_intrastat_journal_credit_note.png)

    ![Upplýsingar um línu Intrastat-bókar fyrir kreditnótu](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Selja varning til San Marínó með sölupöntun

Þessi hluti dæmisins sýnir hvernig á að nota sölupöntun til að kaupa varning (vörur) til San Marínó.

1. Farið í **Viðskiptakröfur**  >  **Pantanir**  >  **Allar sölupantanir**.
2. Í aðgerðarúðunni velurðu **Nýtt**.
3. Í svarglugganum **Stofna sölupöntun**, í reitnum **Viðskiptavinalykill**, skal velja **ITCO-000001**.
4. Veldu **Í lagi**.
5. Í **Hausyfirlitinu**, í flýtiflipanum **Afhending**, í hlutanum **Ýmsar afhendingarupplýsingar**, í reitnum **Afhendingarmáti**, skal velja **1**.
6. Í reitnum **Afhendingarskilmálar** skal velja **CFR**.
7. Í flipanum **Línur**, í flýtiflipanum **Sölupöntunarlínur**, í reitnum **Vörunúmer**, skal velja **VARA**.
8. Í **Magn** reitinn er fært inn **30**.
9. Í reitnum **Svæði** skal velja **1**.
10. Í reitnum **Vöruhús** skal velja **11**.
11. Í reitinn **Einingarverð** skal slá inn **200**.
12. Í aðgerðarúðunni skal velja **Vista**.
13. Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja **Reikningur** til að búa til reikning fyrir pöntunina.
14. Í flýtiflipanum **Færibreytur** í **Færibreyta** hlutanum **Magn** skaltu velja **Allt**.
15. Í svarglugganum **Bókun reiknings** í **Uppsetning** flipanum í **Reiknings** **dagsetning** reitnum skal velja **7/9/2021**.
16. Veldu svo **Í lagi** til að bóka reikninginn.
17. Farðu yfir línurnar í Intrastat-bókinni.

    1. Farðu í **Skattur**  >  **Skattskýrslur**  >  **Erlend viðskipti**  >  **Intrastat**.
    2. Á aðgerðasvæðinu skal velja **Flutningur**.
    3. Í svarglugganum **Intrastat (flutningur)** skal stilla valkostinn **Reikningur viðskiptavinar** á **Já**.
    4. Veldu **Í lagi** til að flytja færslurnar og fara yfir Intrastat-bókina.

   ![Intrastat-bók fyrir San Marínó](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![Upplýsingar um línu Intrastat-bókar fyrir San Marínó](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Búðu til Intrastat-skattskýrslu fyrir sendingar.

    1. Farðu í **Skattur** &gt; **Skattskýrslur** &gt; **Erlend viðskipti** &gt; **Intrastat**.
    2. Á aðgerðasvæðinu skal velja **Úttak** &gt; **Skýrsla**.
    3. Í svarglugganum **Intrastat-skýrsla**, í hlutanum **Dagsetning**, í reitnum **Frá dagsetningu**, skal velja **7/1/2021**.
    4. Í reitnum **Til dagsetningar** skal velja **7/31/2021**.
    5. Í hlutanum **Valkostir útflutnings** skal stilla valkostina **Mynda skrá** og **Mynda skýrslu** á **Já**.
    6. Í reitinn **Skráarheiti** skal færa inn **Skrá sendinga**.
    7. Í reitinn **Heiti skýrsluskráar** skal færa inn **Skýrsla sendinga**.
    8. Í reitnum **Stefna** skal velja **Sendingar**.
    9. Í reitinn **Tilvísunarnúmer** skal færa inn **98754**.
    10. Veldu **Í lagi** til að búa til Intrastat-skýrsluna og Intrastat-skrána.

        Eftirfarandi skýringarmynd sýnir dæmi um prentaða Intrastat skýrslu.

        ![Intrastat-skýrsla](media/ita_intrastat_report_for_dispatches.png)

        Eftirfarandi skýringarmynd sýnir dæmi um prentaða Intrastat-skrá.

        ![Intrastat-skrá fyrir sendingar](media/ita_intrastat_file_for_dispatches.png)
