---
title: Setja upp fjármálasamþættingu fyrir Commerce-rásir
description: Þetta efnisatriði veitir leiðbeiningar um uppsetningu á virkni fjárhagssamþættingar fyrir Commerce-rásir.
author: josaw
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 2ac8dc8787ab0bdb796ec849f9ede3f697b09680
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193645"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Setja upp fjármálasamþættingu fyrir Commerce-rásir

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Inngangur

Þetta efnisatriði veitir leiðbeiningar um uppsetningu á virkni fjárhagssamþættingar fyrir Commerce-rásir. Nánari upplýsingar um fjárhagssamþættingu er að finna í [Yfirlit yfir fjárhagssamþættingu fyrir Commerce-rásir](fiscal-integration-for-retail-channel.md).

Uppsetningarferli fjárhagssamþættingar felur í sér eftirfarandi atriði:

1. Grunnstilla fjárhagstengla sem tákna fjárhagstæki eða þjónustu sem er notuð til fjárhagsskráningar, t.d. strimlaprentarar.
2. Grunnstilla skjalaveitur sem mynda fjárhagsskjöl sem verða skráð í fjárhagstækjum eða þjónustu af fjárhagstenglum.
3. Grunnstilla skráningarferli fjárhags sem skilgreinir röð fjárhagsskráningarskrefa og fjárhagstenglana og fjárhagsskjalaveiturnar sem eru notaðar í hverju skrefi.
4. Úthluta skráningarferli fjárhags til POS-virknireglna.
5. Úthluta tækniforstillingum tengils til vélbúnaðarsniðs.

## <a name="set-up-a-fiscal-registration-process"></a>Setja upp skráningarferli fjárhags

Áður en þú notar virkni fjárhagssamþættingar ættir þú að skilgreina eftirfarandi stillingar.

1. Uppfæra færibreytur Commerce.

    1. Á síðunni **Samnýttar færibreytur Commerce**, í flipanum **Almennt**, skal stilla valkostinn **Virkja samþættingu fjárhags** á **Já**. Í flipanum **Númeraraðir** skal skilgreina númeraraðirnar fyrir eftirfarandi tilvísanir:

        - Númer tækniforstillingar fjárhags
        - Flokksnúmer fjárhagstengils
        - Númer skráningarferlis

    2. Á síðunni **Færibreytur Commerce** skal skilgreina númeraröðina fyrir númer tækniforstillingar fjárhags.

    > [!NOTE]
    > Númeraraðir eru valfrjálsar. Hægt er að búa til númer fyrir allar samþættingar fjárhags annaðhvort með númeraröðum eða handvirkt.

2. Hlaða upp grunnstillingum fyrir fjárhagstengla og fjárhagsskjalaveitur.

    Fjárhagsskjalaveita ber ábyrgð á því að mynda fjárhagsskjöl sem tákna færslur og tilvik sem eru skráð í POS á sniði sem er einnig notað í samskiptum við fjárhagstæki eða þjónustu. Til dæmis gæti fjárhagsskjalaveita myndað framsetningu á fjárhagskvittun á XML-sniði.

    Fjárhagstengill er ábyrgur fyrir samskiptum við fjárhagstæki eða þjónustu. Til dæmis gæti fjárhagstengill sent fjárhagskvittun, sem fjárhagsskjalaveita stofnaði á XML-sniði, til strimlaprentara. Nánari upplýsingar um íhluti fjárhagssamþættingar er að finna í [Fjárhagsskráningarferli og sýnishorn fjárhagssamþættingar fyrir fjárhagstæki](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. Á síðunni **Fjárhagstenglar** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Fjárhagstenglar**) skal hlaða upp XML-skilgreiningu fyrir hvert tæki eða þjónustu sem er áætlað að nota fyrir samþættingu fjárhags.

        > [!TIP]
        > Með því að velja **Skoða** er hægt að skoða allar virknir og tækniforstillingar sem tengjast núverandi fjárhagstengli.

    2. Á síðunni **Fjárhagsskalaveitur** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Fjárhagsskjalaveitur**) skal hlaða upp XML-skilgreiningu fyrir hvert tæki eða þjónustu sem er áætlað að nota.

        > [!TIP]
        > Með því að velja **Skoða** er hægt að skoða allar virkniforstillingar sem tengjast núverandi fjárhagsskjalaveitu.

    Fyrir dæmi um grunnstillingar á fjárhagstenglum og fjárhagsskjalaveitum skal sjá [Dæmi um samþættingu fjárhags í Retail SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Gagnavörpun er talin hluti af fjárhagsskjalaveitu. Til að setja upp mismunandi gagnavörpun fyrir sama tengilinn (til dæmis samkvæmt staðbundnum reglugerðum), ættir þú að búa til mismunandi fjárhagsskjalsveitur.

3. Búðu til virkniforstillingar tengils og tækniforstillingar tengils.

    1. Á síðunni **Virkniforstillingar tengils** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Virkniforstillingar tengils**) skal stofna virkniforstillingu tengils fyrir hverja samsetningu af fjárhagstengli og fjárhagsskjalsveitu sem tengist þessum fjárhagstengli.

        1. Veldu heiti tengils.
        2. Veldu skjalsveitu.

        Hægt er að breyta færibreytum gagnavörpunar í tækniforstillingu tengils. Til að endurheimta sjálfgefnar færibreytur sem eru skilgreindar í grunnstillingu fjárhagsskjalsveitu skal velja **Uppfæra**.

        **Dæmi**

        | Færibreyta  | Snið | Dæmi |
        |---|--------|---------|
        | **Stillingar VSK-hlutfalls** | gildi : VAThlutfall | 1 : 2000, 2 : 1800 |
        | **Vörpun VSK-kóða** | VSKkóði : gildi | vsk20: 1, vsk18: 2 |
        | **Setja upp greiðslumáta** | TenderType: gildi | Reiðufé: 1, kort: 2 |

        > [!NOTE]
        > Virkniforstillingar tengils eru sértækar fyrirtæki. Ef ætlunin er að nota sömu samsetningu af fjárhagstengli og fjárhagsskjalsveitu í mismunandi fyrirtækjum ætti að stofna virkniforstillingu tengils fyrir hvert fyrirtæki fyrir sig.

    2. Á síðunni **Tækniforstillingar tengils** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Tækniforstillingar tengils**) skal stofna tækniforstillingu tengils fyrir hvern fjárhagstengil fyrir sig.

        1. Veldu heiti tengils.
        2. Veldu gerð tengils. Fyrir tæki sem eru tengd við vélbúnaðarstöð skal velja **Staðbundið**.

            > [!NOTE]
            > Einungis staðbundnir tenglar eru studdir enn sem komið er.

        Hægt er að breyta færibreytum í flipunum **Tæki** og **Stillingar** í tækniforstillingu tengils. Til að endurheimta sjálfgefnar færibreytur sem eru skilgreindar í grunnstillingu fjárhagstengils skal velja **Uppfæra**. Á meðan verið er að hlaða nýrri útgáfu af XML-skilgreiningu færðu skilaboð um verið sé að nota núverandi fjárhagstengil eða fjárhagsskjal. Þetta ferli hnekkir ekki handvirkum breytingum sem voru gerðar áður í virkniforstillingum tengils og tækniforstillingum tengils. Til að setja á sjálfvirkt safn af færibreytum fyrir nýja grunnstillingu, á síðunni **Virkniforstillingar tengils** eða síðunni **Tækniforstillingar tengils**, skal velja **Uppfæra**.

4. Búa til fjárhagstenglahópa.

    Fjárhagstenglahópur sameinar virkniforstillingar fjárhagstengla sem framkvæma eins aðgerðir og eru notaðar í sama skrefi í skráningarferli fjárhags. Til dæmis, ef hægt er að nota nokkrar gerðir af strimlaprenturum í verslun, er hægt að sameina fjárhagstengla fyrir þessa strimlaprentara í fjárhagstenglahópi.

    1. Á síðunni **Fjárhagstenglahópur** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Fjárhagstenglahópar**) skal stofna nýjan fjárhagstenglahóp.
    2. Bæta virkniforstillingum við tenglahópinn. Í flipanum **Virkniforstillingar** skal velja **Bæta við** og velja forstillingarnúmer. Hver fjárhagstengill í tenglahópi getur aðeins haft eina virkniforstillingu.
    3. Til að hætta notkun á virkniforstillingu skal stilla valkostinn **Slökkva** á **Já**. Þessi breyting hefur aðeins áhrif á núverandi tenglahóp. Þú getur haldið áfram að nota sömu virkniforstillingu í öðrum tenglahópum.

5. Búa til skráningarferli fjárhags.

    Skráningarferli fjárhags er skilgreint eftir röð skráningarskrefanna og tenglahópnum sem notaður er í hverju skrefi.

    1. Á síðunni **Skráningarferli fjárhags** (**Retail og Commerce \> Uppsetning rásar \> Skráningarferli fjárhags \> Skráningarferli fjárhags**) skal stofna nýja færslu fyrir hvert einkvæmt ferli fjárhagsskráningar.
    2. Bæta við skráningarskrefum við ferlið:

        1. Veljið **Bæta við**.
        2. Veldu gerð fjárhagstengils.
        3. Í reitnum **Flokksnúmer** skal velja viðeigandi flokk fjárhagstengils.

6. Úthluta einingum úr skráningarferli fjárhags til POS-virknireglur.

    1. Á síðunni **POS-virknireglur** (**Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> POS-virknireglur \> Virknireglur**) skal úthluta skráningarferli fjárhags til POS-virknireglu. Veldu **Breyta** og síðan, í flipanum **Skráningarferli fjárhags**, í reitnum **Númer ferlis** skal velja ferli.
    2. Á síðunni **Vélbúnaðarregla sölustaðar** (**Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> POS-virknireglur \> Vélbúnaðarreglur**) skal úthluta tækniforstillingum til vélbúnaðarreglu. Veldu **Breyta**, bættu við línu á flipann **Jaðarbúnaður fjárhags** og síðan, í reitnum **Númer forstillingar** skal velja tækniforstillingu tengils.

    > [!NOTE]
    > Þú getur bætt nokkrum tækniforstillingum við sömu vélbúnaðarforstillinguna. Hins vegar ætti vélbúnaðarforstilling eða POS-virkniregla aðeins að vera með eina skörun við einhvern tengilhóp fjárhags.

    Flæði fjárhagsskráningar er skilgreint af skráningarferli fjárhags og einnig af nokkrum færibreytum fyrir íhluti fjárhagssamþættingar: viðbót Commerce-keyrslutíma fyrir fjárhagsskjalaveitu og viðbót vélbúnaðarstöðvar fyrir fjárhagstengil.

    - Áskrift af tilvikum og færslum til fjárhagsskráningar er skilgreind fyrirfram í fjárhagsskjalaveitunni.
    - Fjárhagsskjalaveitan er einnig ábyrg fyrir því að bera kennsl á fjárhagstengil sem er notaður fyrir fjárhagsskráningu. Það samsvarar virkniforstillingum tengils sem eru innifaldar í fjárhagstenglahópi sem er á við fyrir núverandi skref í skráningarferli fjárhags með tækniforstillingu tengils sem er úthlutað til vélbúnaðarforstillingu vélbúnaðarstöðvarinnar sem POS er parað við.
    - Fjárhagsskjalaveitan notar stillingar gagnavörpunar frá grunnstillingu fjárhagsskjalaveitunnar til að umbreyta gögnum færslu/tilviks á borð við skatta og greiðslur á meðan fjárhagsskjal er myndað.
    - Þegar fjárhagsskjalaveitan myndar fjárhagsskjal getur fjárhagstengillinn annaðhvort sent það til fjárhagstækis eins og það er, eða þáttað það og umbreytt því í röð skipana í forritunarviðmóti (API) tækis, háð því hvernig samskiptum er háttað.

7. Á síðunni **Skráningarferli fjárhags** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Skráningarferli fjárhags**) skal velja **Villuleita** til að villuleita skráningarferli fjárhags.

    Við mælum með að þú keyrir þessa tegund af villuleit í eftirfarandi tilvikum:

    - Eftir að þú hefur lokið öllum stillingum fyrir nýtt skráningarferli, þar á meðal þegar þú úthlutar skráningarferlum til POS-virknireglna og vélbúnaðarforstillinga.
    - Eftir að þú hefur gert breytingar á núverandi skráningarferli fjárhags og þessar breytingar gætu valdið því að annar fjárhagstengill sé valinn við keyrslu (til dæmis ef þú breytir tengilhópnum fyrir skref í skráningarferli fjárhags, virkjar virkniforstillingu tengils í tengilhóp eða bætir nýrri virkniforstillingu við tengilhóp).
    - Eftir að þú hefur gert breytingar á úthlutun á tækniforstillingum tengils til vélbúnaðarforstillinga.

8. Á síðunni **Dreifingaráætlun** skal keyra verkin **1070** og **1090** til að flytja gögn til gagnagrunns rásarinnar.

## <a name="set-up-fiscal-texts-for-discounts"></a>Setja upp fjárhagstexta fyrir afslætti

Í sumum tilfellum verður að prenta sérstakan texta á fjárhagskvittun ef afsláttur er notaður. Hægt er að setja upp fjárhagstexta fyrir afslætti á síðunni **Fjárhagstenglahópur** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Fjárhagstenglahópar**).

- Fyrir handvirka afslætti sem eru notaðir á sölustað ætti að stilla fjárhagstexta fyrir upplýsingakóðann eða flokk upplýsingakóða sem er tilgreindur sem upplýsingakóðinn **Afurðarafsláttur** í virknireglu sölustaðar.

    1. Á síðunni **Flokkur fjárhagstengils** skal velja **Texti fyrir fjárhagskvittun**.
    2. Í flipanum **Upplýsingakóðar** skal velja **Bæta við** og velja upplýsingakóða eða flokk upplýsingakóða.
    3. Í **Númer upplýsingakóða** skal velja gildi.
    4. Í reitnum **Númer undirkóða** skal velja gildi ef krafist er undirkóða fyrir valinn upplýsingakóða.
    5. Í reitnum **Texti fyrir fjárhagskvittun** skal tilgreina fjárhagstexta sem á að prenta á fjárhagskvittun.
    6. Stilltu valkostinn **Prenta innslátt notanda á fjárhagskvittun** á **Já** til að hnekkja textanum á fjárhagskvittun með upplýsingum sem notandi slær inn handvirkt á sölustaðnum. Þessi valkostur gildir aðeins um upplýsingakóða sem eru með gerð innsláttar sem **Texti**.

    > [!NOTE]
    > Hægt er að tilgreina fjárhagstexta fyrir ýmsa upplýsingakóða til að styðja við aðstæður þar sem flokkar upplýsingakóða, tengdir upplýsingakóðar og ræstir upplýsingakóðar eru notaðir. Við þessar aðstæður mun fjárhagskvittunin innihalda fjárhagstexta fyrir alla upplýsingakóða sem eru tengdir við færslulínuna þar sem afslátturinn var notaður.

- Fyrir afslætti sem miðast við rásir skal skilgreina fjárhagstexta fyrir afsláttarkennið.

    1. Á síðunni **Flokkur fjárhagstengils** skal velja **Texti fyrir fjárhagskvittun**.
    2. Í flipanum **Afslættir** skal velja **Bæta við** og velja afsláttarkenni.
    3. Í reitnum **Texti fyrir fjárhagskvittun** skal tilgreina fjárhagstexta sem á að prenta á fjárhagskvittun.

    > [!NOTE]
    > Ef nokkrir afslættir eru notaðir fyrir sömu færslulínuna mun fjárhagskvittunin innihalda fjárhagstexta frá öllum afsláttum sem eru tengdir við þessa færslulínu.

## <a name="set-error-handling-settings"></a>Velja stillingar villumeðhöndlunar

Valkostir villumeðhöndlunar sem eru í boði í samþættingu fjárhags eru stilltir í skráningarferli fjárhags. Nánari upplýsingar um villumeðhöndlun í samþættingu fjárhags er að finna í [Villumeðhöndlun](fiscal-integration-for-retail-channel.md#error-handling).

1. Á síðunni **Skráningarferli fjárhags** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Skráningarferli fjárhags**) er hægt að stilla eftirfarandi færibreytur fyrir hvert skref í skráningarferli fjárhags:

    - **Leyfa að sleppa** - Þessi færibreyta virkjar valkostinn **Sleppa** í svarglugga villumeðhöndlunar.
    - **Leyfa að merkja sem skráð** - Þessi færibreyta virkjar valkostinn **Merkja sem skráð** í svarglugga villumeðhöndlunar.
    - **Halda áfram á villu** - Ef þessi færibreyta er virkjuð getur ferli fjárhagsskráningar haldið áfram í afgreiðslukassa ef fjárhagsskráning færslu eða tilviks mistekst. Annars, til að keyra fjárhagsskráningu á næstu færslu eða tilviki, verður notandi að reyna misheppnuðu fjárhagsskráninguna aftur, sleppa henni eða merkja færsluna eða tilvikið sem skráð. Frekari upplýsingar er að finna í [Valfrjáls fjárhagsskráning](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Ef færibreytan **Halda áfram á villu** er virkjuð eru færibreyturnar **Leyfa að sleppa** og **Leyfa að merkja sem skráð** sjálfkrafa gerðar óvirkar.

2. Valkostirnir **Sleppa** og **Merkja sem skráð** í svarglugga villumeðhöndlunar krefjast heimildarinnar **Leyfa að sleppa skráningu eða merkja sem skráð**. Þar af leiðandi, á síðunni **Heimildaflokkar** (**Retail og Commerce \> Starfsmenn \> Heimildaflokkar**) skal virkja heimildina **Leyfa að sleppa skráningu eða merkja sem skráð**.
3. Valkostirnir **Sleppa** og **Merkja sem skráð** leyfa notendum að slá inn viðbótarupplýsingar þegar fjárhagsskráningin mistekst. Til að bjóða upp á þessa virkni ættir þú að tilgreina upplýsingakóðana **Sleppa** og **Merkja sem skráð** í fjárhagstenglahóp. Upplýsingarnar sem notendur slá inn eru síðan vistaðar sem færsla upplýsingakóða sem er tengd við fjárhagsfærsluna. Nánari upplýsingar um upplýsingakóða er að finna í [Upplýsingakóðar og upplýsingakóðaflokkar](../info-codes-retail.md).

    > [!NOTE]
    > Virkniræsingin **Afurð** er ekki studd fyrir upplýsingakóðana sem eru notaðir fyrir **Sleppa** og **Merkja sem skráð** í fjárhagstenglaflokkum.

    - Á síðunni **Flokkur fjárhagstengils**, í flipanum **Upplýsingakóðar**, skal velja upplýsingakóða eða upplýsingakóðaflokka í reitunum **Sleppa** og **Merkja sem skráð**.

    > [!NOTE]
    > Hægt er að búa til eitt fjárhagsskjal og eitt skjal sem er ekki fjárhagsskjal í hvaða skrefi sem er í skráningarferli fjárhags. Viðbót fjárhagsskjalaveitu ber kennsl á allar gerðir af færslum eða tilvikum sem tengdar við fjárhagsskjal eða skjals sem ekki er fjárhagsskjal. Eiginleiki villumeðhöndlunar á aðeins við um fjárhagsskjöl.
    >
    > - **Fjárhagsskjal** - Áskilið skjal sem ætti að skrá (t.d. fjárhagskvittun).
    > - **Skjal sem ekki er fjárhagsskjal** - Viðbótarskjal fyrir færsluna eða tilvikið (t.d. gjafakort).

4. Ef notandinn verður að geta haldið áfram til að vinna úr fyrirliggjandi aðgerð (t.d. stofnun eða frágang á færslu) eftir að villa í ástandsskoðun kemur upp, ættir þú virkja heimildina **Leyfa að sleppa villu í ástandsskoðun** á síðunni **Heimildaflokkar** (**Retail og Commerce \> Starfsmenn \> Heimildaflokkar**). Frekari upplýsingar um ástandsskoðunarferli er að finna í [Ástandsskoðun fjárhagsskráningar](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Setja upp X/Z-skýrslur fjárhags úr POS

Til að gera kleift að keyra X/Z-skýrslur úr POS ættir þú að bæta nýjum hnöppum við POS-útlit.

- Á síðunni **Hnappahnit** skal fylgja leiðbeiningunum í [Bæta sölustaðaraðgerðum við POS-útlit með hnappahnitshönnuði](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) til að setja upp hönnuðinn og uppfæra POS-útlit.

    1. Veldu útlitið til að uppfæra. 
    2. Bættu við nýjum hnapp og stilltu eiginleika hnappsins **Prenta fjárhag X**.
    3. Bættu við nýjum hnapp og stilltu eiginleika hnappsins **Prenta fjárhag Z**.
    4. Á síðunni **Dreifingaráætlun** skal keyra verkið **1090** til að flytja breytingar til gagnagrunns rásarinnar.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Virkja handvirka framkvæmd frestaðrar fjárhagsskráningu

Til að virkja handvirka framkvæmd á frestaðri fjárhagsskráningu ættir þú að bæta nýjum hnappi við útlit sölustaðar.

- Á síðunni **Hnappahnit** skal fylgja leiðbeiningunum í [Bæta sölustaðaraðgerðum við POS-útlit með hnappahnitshönnuði](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) til að setja upp hönnuðinn og uppfæra POS-útlit.

    1. Veldu útlitið til að uppfæra.
    2. Bættu við nýjum hnapp og stilltu eiginleika hnappsins **Ljúka skráningarferli fjárhags**.
    3. Á síðunni **Dreifingaráætlun** skal keyra verkið **1090** til að flytja breytingarnar þínar til gagnagrunns rásarinnar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]