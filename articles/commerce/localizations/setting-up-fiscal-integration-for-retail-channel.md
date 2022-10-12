---
title: Setja upp fjármálasamþættingu fyrir Commerce-rásir
description: Þessi grein veitir leiðbeiningar um að setja upp fjárhagslega samþættingarvirkni fyrir viðskiptarásir.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 28097341c7b39660b834eb81786c3f56045e1496
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631424"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Setja upp fjármálasamþættingu fyrir Commerce-rásir

[!include [banner](../includes/banner.md)]

Þessi grein veitir leiðbeiningar um að setja upp fjárhagslega samþættingarvirkni fyrir viðskiptarásir. Nánari upplýsingar um fjárhagssamþættingu er að finna í [Yfirlit yfir fjárhagssamþættingu fyrir Commerce-rásir](fiscal-integration-for-retail-channel.md).

## <a name="enable-features-in-commerce-headquarters"></a>Virkjaðu eiginleika í höfuðstöðvum Commerce

Fylgdu þessum skrefum til að virkja eiginleika sem tengjast fjárhagslegri samþættingu virkni fyrir viðskiptarásir.

1. Í Commerce Headquarters skal fara í **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
1. Finndu og virkjaðu eftirfarandi eiginleika:

    - **Bein fjárhagsleg samþætting frá POS skrám** – Þessi eiginleiki stækkar fjárhagslega samþættingarrammann með því að bæta við getu til að búa til fjárhagstengi sem verða keyrð á sölustað (POS). Þessi tegund tengis hefur samskipti við fjárhagslegt tæki eða þjónustu sem veitir HTTP forritunarviðmót (API) og krefst ekki sérstakrar líkamlegrar vélar í versluninni. Til dæmis gerir þessi virkni fjárhagslega samþættingu fyrir farsíma án þess að þurfa sameiginlega vélbúnaðarstöð.
    - **Tæknileg samþætting ríkisfjármála hnekkir** – Þessi eiginleiki gerir kleift að stækka uppsetningu fjárhagslegrar samþættingar og bætir við möguleikanum til að hnekkja færibreytum tæknisniðs. Til dæmis er hægt að tilgreina tengingarstrengi fjárhagslegra tækja á einstökum POS-skrárstigi. Eiginleikinn bætir einnig við möguleikanum á að athuga tengibreytur á **Stillingar** síðu POS skrár. 
    - **Fjárhagsskráningarríki POS-skráa** – Þegar þessi eiginleiki er virkur geturðu slökkt á fjárhagsskráningarferlinu fyrir tilteknar POS-skrár. Ef fjárhagsskráning er óvirk fyrir POS-skrá er ekki hægt að ljúka sölufærslum á þeirri skrá.
    - **Afrit af staðbundinni geymslu í ríkisfjármálum** – Þessi eiginleiki eykur villumeðhöndlunargetu fjárhagssamþættingarrammans með því að virkja sjálfvirkt öryggisafrit af fjárhagsskráningargögnum, þannig að hægt sé að endurheimta gögnin í staðbundinni geymslu á meðan tæki er virkjað.
    - **Frestað skráningu skjala** - Þessi eiginleiki útvíkkar villumeðferðargetu fjárhagssamþættingarrammans með því að gera möguleikann á að fresta fjárhagsskráningu ef bilun í fjárhagsskráningu verður og nota varakost fyrir fjárhagsskráningu eða ljúka fjárhagsskráningu síðar með öðrum hætti en fjárhagslegri samþættingarrammanum.

## <a name="set-up-commerce-parameters"></a>Settu upp viðskiptafæribreytur

Til að setja upp viðskiptafæribreytur skaltu fylgja þessum skrefum.

1. Á síðunni **Samnýttar færibreytur Commerce**, í flipanum **Almennt**, skal stilla valkostinn **Virkja samþættingu fjárhags** á **Já**.
1. Í flipanum **Númeraraðir** skal skilgreina númeraraðirnar fyrir eftirfarandi tilvísanir:

    - Númer tækniforstillingar fjárhags
    - Flokksnúmer fjárhagstengils
    - Númer skráningarferlis

1. Á síðunni **Færibreytur Commerce** skal skilgreina númeraröðina fyrir númer tækniforstillingar fjárhags.

> [!NOTE]
> Númeraraðir eru valfrjálsar. Hægt er að búa til númer fyrir allar samþættingar fjárhags annaðhvort með númeraröðum eða handvirkt.

## <a name="set-up-a-fiscal-registration-process"></a>Setja upp skráningarferli fjárhags

Uppsetningarferli fjárhagssamþættingar felur í sér eftirfarandi atriði:

- Grunnstilla fjárhagstengla sem tákna fjárhagstæki eða þjónustu sem er notuð til fjárhagsskráningar, t.d. strimlaprentarar.
- Grunnstilla skjalaveitur sem mynda fjárhagsskjöl sem verða skráð í fjárhagstækjum eða þjónustu af fjárhagstenglum.
- Grunnstilla skráningarferli fjárhags sem skilgreinir röð fjárhagsskráningarskrefa og fjárhagstenglana og fjárhagsskjalaveiturnar sem eru notaðar í hverju skrefi.
- Úthluta fjárhagsskráningarferlinu á POS virkniprófíla.
- Úthluta tækniforstillingum tengils til vélbúnaðarsniðs.
- Úthlutaðu tæknisniðum tengi til POS vélbúnaðar eða virkniprófíla.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Hladdu upp stillingum fyrir veitendur fjárhagsskjala

Fjárhagsskjalaveita ber ábyrgð á því að mynda fjárhagsskjöl sem tákna færslur og tilvik sem eru skráð í POS á sniði sem er einnig notað í samskiptum við fjárhagstæki eða þjónustu. Til dæmis gæti fjárhagsskjalaveita myndað framsetningu á fjárhagskvittun á XML-sniði.

Fylgdu þessum skrefum til að hlaða upp stillingum veitenda fjárhagsskjala.

1. Í höfuðstöðvum Commerce, farðu á **Veitendur ríkisfjármálaskjala** síða (**Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**).
1. Hladdu upp XML stillingu fyrir hvert tæki eða þjónustu sem þú ætlar að nota.

> [!TIP]
> Með því að velja **Skoða** er hægt að skoða allar virkniforstillingar sem tengjast núverandi fjárhagsskjalaveitu.

> [!NOTE]
> Gagnavörpun er talin hluti af fjárhagsskjalaveitu. Til að setja upp mismunandi gagnavörpun fyrir sama tengilinn (til dæmis samkvæmt staðbundnum reglugerðum), ættir þú að búa til mismunandi fjárhagsskjalsveitur.

### <a name="upload-configurations-of-fiscal-connectors"></a>Hladdu upp stillingum á fjárhagslegum tengjum

Fjárhagstengill er ábyrgur fyrir samskiptum við fjárhagstæki eða þjónustu. Til dæmis gæti fjárhagstengill sent fjárhagskvittun, sem fjárhagsskjalaveita stofnaði á XML-sniði, til strimlaprentara. Fyrir frekari upplýsingar um fjárhagslega samþættingarhluta, sjá [Fjárhagsskráningarferli og sýnishorn af samþættingu ríkisfjármála fyrir ríkisfjármálatæki og þjónustu](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Til að hlaða upp stillingum fjárhagstengja skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum viðskipta, farðu á **Fjárhagstengingar** síða (**Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**).
1. Hladdu upp XML-stillingu fyrir hvert tæki eða þjónustu sem þú ætlar að nota í fjárhagslegum samþættingu.

> [!TIP]
> Með því að velja **Skoða** er hægt að skoða allar virknir og tækniforstillingar sem tengjast núverandi fjárhagstengli.

Fyrir dæmi um grunnstillingar á fjárhagstenglum og fjárhagsskjalaveitum skal sjá [Dæmi um samþættingu fjárhags í Commerce SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Búðu til virka snið fyrir tengi

Fylgdu þessum skrefum til að búa til virka snið tengi.

1. Í höfuðstöðvum viðskipta, farðu á **Virknisnið fyrir tengi** síða (**Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Virknisnið fyrir tengi**).
1. Fyrir hverja samsetningu fjárhagstengis og fjárhagsskjalaveitu sem tengist þessu fjárhagstengi skaltu búa til virknisnið tengis með því að fylgja þessum skrefum:

    1. Veldu heiti tengils.
    1. Veldu skjalsveitu.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Breyta breytum gagnakortunar í virknisniði tengis

Hægt er að breyta færibreytum gagnavörpunar í tækniforstillingu tengils. Eftirfarandi tafla gefur nokkur dæmi um gagnakortunarfæribreytur í virknisniði tengis.

| Færibreyta | Snið | Dæmi |
|-----------|--------|---------|
| Stillingar VSK-hlutfalls | gildi : VAThlutfall | 1 : 2000, 2 : 1800 |
| Vörpun VSK-kóða | VSKkóði : gildi | vsk20: 1, vsk18: 2 |
| Setja upp greiðslumáta | TenderType: gildi | Reiðufé: 1, kort: 2 |

Til að endurheimta sjálfgefnar færibreytur sem eru skilgreindar í skilgreiningu fjárhagsskjalaveitu skaltu velja **Uppfærsla** á **Tengi virkni snið** síðu.

> [!NOTE]
> Virkniforstillingar tengils eru sértækar fyrirtæki. Ef þú ætlar að nota sömu samsetningu fjárhagstengis og fjárhagsskjalaveitu fyrir mismunandi fyrirtæki, ættir þú að búa til virka tengisnið fyrir hvert fyrirtæki.

### <a name="create-connector-technical-profiles"></a>Búðu til tæknisnið fyrir tengi

Fylgdu þessum skrefum til að búa til tæknisnið fyrir tengi.

1. Í höfuðstöðvum Commerce, farðu á **Tæknisnið fyrir tengi** síða (**Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**).
1. Búðu til tæknilegan tengiprófíl fyrir hvert fjárhagslegt tengi með því að fylgja þessum skrefum:

    1. Veldu heiti tengils.
    1. Veldu tengitegund:

        - Fyrir tæki eða þjónustu sem eru tengd við vélbúnaðarstöð eða til staðar á staðarnetinu skaltu velja **Staðbundið**.
        - Fyrir ytri þjónustu, veldu **Ytri**.
        - Fyrir innri tengi í Commerce runtime (CRT), veldu **Innri**. 

    1. Veldu staðsetningu tengis:

        - Ef tengið er staðsett á vélbúnaðarstöðinni skaltu velja **Vélbúnaðarstöð**.
        - Ef tengið er staðsett á POS skránni skaltu velja **Skráðu þig**.

Hægt er að breyta færibreytum í flipunum **Tæki** og **Stillingar** í tækniforstillingu tengils. Til að endurheimta sjálfgefnar færibreytur sem eru skilgreindar í grunnstillingu fjárhagstengils skal velja **Uppfæra**. Á meðan ný útgáfa af XML uppsetningu er að hlaðast, færðu skilaboð sem segja að núverandi fjárhagstengi eða fjárhagsskjalaveitan sé þegar í notkun. Þetta ferli hnekkir ekki handvirkum breytingum sem voru gerðar áður í virkniforstillingum tengils og tækniforstillingum tengils. Til að nota sjálfgefna sett af færibreytum úr nýrri stillingu skaltu velja **Uppfærsla** á annaðhvort **Virknisnið fyrir tengi** síðu eða **Tæknisnið fyrir tengi** síðu.

Ef þú verður að setja upp sérstakar færibreytur fyrir einstaka POS skrá eða verslun skaltu fylgja þessum skrefum.

1. Veldu **Hneka** valmyndaratriði.
1. Á **Hneka** síðu, búðu til nýja skrá.
1. Veldu verslun eða POS skrá. Þú getur hnekkt færibreytum völdu tæknisniðs fyrir einstaka POS-skrá eða allar POS-skrár í einstakri verslun.
1. Á **Tæki** flipa, sláðu inn færibreytur fyrir valda POS skrá eða verslun.

### <a name="create-fiscal-connector-groups"></a>Búðu til fjárhagslega tengihópa

Fjárhagstenglahópur sameinar virkniforstillingar fjárhagstengla sem framkvæma eins aðgerðir og eru notaðar í sama skrefi í skráningarferli fjárhags. Til dæmis, ef hægt er að nota nokkrar gerðir af strimlaprenturum í verslun, er hægt að sameina fjárhagstengla fyrir þessa strimlaprentara í fjárhagstenglahópi.

Fylgdu þessum skrefum til að búa til fjárhagstengihóp.

1. Farðu í **Fjárhagstengingarhópur** síða (**Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingarhópar**).
1. Búðu til nýjan fjárhagstengihóp.
1. Bæta virkniforstillingum við tenglahópinn. Í flipanum **Virkniforstillingar** skal velja **Bæta við** og velja forstillingarnúmer. Hver fjárhagstengill í tenglahópi getur aðeins haft eina virkniforstillingu.
1. Til að hætta notkun á virkniforstillingu skal stilla valkostinn **Slökkva** á **Já**. Þessi breyting hefur aðeins áhrif á núverandi tenglahóp. Þú getur haldið áfram að nota sömu virkniforstillingu í öðrum tenglahópum.

### <a name="create-a-fiscal-registration-process"></a>Búðu til fjárhagslega skráningarferli

Skráningarferli fjárhags er skilgreint eftir röð skráningarskrefanna og tenglahópnum sem notaður er í hverju skrefi.

Til að búa til fjárhagslega skráningarferli skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum Commerce, farðu á **Skráningarferli í ríkisfjármálum** síða (**Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**).
1. Búðu til nýja skrá fyrir hvert einstakt fjárhagsskráningarferli.
1. Bættu skráningarskrefum við ferlið með því að fylgja þessum skrefum:

    1. Veljið **Bæta við**.
    1. Veldu gerð fjárhagstengils.
    1. Í reitnum **Flokksnúmer** skal velja viðeigandi flokk fjárhagstengils.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Úthluta einingar fjárhagsskráningarferlisins á POS snið

Fylgdu þessum skrefum til að úthluta einingar fjárhagsskráningarferlisins á POS snið.

1. Í höfuðstöðvum Commerce, farðu á **POS virkni snið** síða (**Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Virkni snið**). 
1. Úthluta fjárhagsskráningarferlinu á POS virkniprófíl.
1. Veldu **Breyta** og síðan, í flipanum **Skráningarferli fjárhags**, í reitnum **Númer ferlis** skal velja ferli.
1. Á **Þjónusta í ríkisfjármálum** flipann, veldu tæknisnið fyrir tengi með staðsetningu tengisins **Skráðu þig**.
1. Farðu í **POS vélbúnaðarsnið** síða (**Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> POS snið \> Vélbúnaðarsnið**).
1. Úthlutaðu tæknisniðum tengis við vélbúnaðarsnið. 
1. Veldu **Breyta**, og síðan, á **Jaðartæki í ríkisfjármálum** flipa, bæta við línu. 
1. Í **Prófílnúmer** reit, veldu tæknisnið fyrir tengi.
1. Á **Jaðartæki í ríkisfjármálum** flipann, veldu tæknisnið fyrir tengi með staðsetningu tengisins **Vélbúnaðarstöð**.

> [!NOTE]
> Þú getur bætt nokkrum tækniforstillingum við sömu vélbúnaðarforstillinguna. Hins vegar ætti vélbúnaðarforstilling eða POS-virkniregla aðeins að vera með eina skörun við einhvern tengilhóp fjárhags.

Fjárhagsskráningarflæðið er skilgreint af fjárhagsskráningarferlinu og einnig af sumum breytum fjárhagslegra samþættingarþátta: the CRT framlenging fyrir ríkisfjármálaskjalaveituna og viðbyggingu vélbúnaðarstöðvar fyrir fjárhagstengi.

- Áskrift af tilvikum og færslum til fjárhagsskráningar er skilgreind fyrirfram í fjárhagsskjalaveitunni.
- Fjárhagsskjalaveitan er einnig ábyrg fyrir því að bera kennsl á fjárhagstengil sem er notaður fyrir fjárhagsskráningu. Það samsvarar virkniforstillingum tengils sem eru innifaldar í fjárhagstenglahópi sem er á við fyrir núverandi skref í skráningarferli fjárhags með tækniforstillingu tengils sem er úthlutað til vélbúnaðarforstillingu vélbúnaðarstöðvarinnar sem POS er parað við.
- Fjárhagsskjalaveitan notar stillingar gagnavörpunar frá grunnstillingu fjárhagsskjalaveitunnar til að umbreyta gögnum færslu/tilviks á borð við skatta og greiðslur á meðan fjárhagsskjal er myndað.
- Þegar fjárhagsskjalaveitan býr til fjárhagsskjal getur fjárhagstengi annaðhvort sent það til fjárhagsbúnaðarins eins og það er, eða flokkað það og umbreytt því í röð skipana á API tækisins, allt eftir því hvernig samskiptin eru meðhöndluð.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Settu upp skrár með takmarkanir á skattaskráningu

Þú getur valið skrár þar sem fjárhagsleg skráning er bönnuð, til dæmis í þeim tilvikum þar sem þú þarft aðeins að veita aðgerðir sem ekki eru fjárhagslegar eins og vörulistaleit, uppflettingu viðskiptavina eða gerð færsludrög á þessum tækjum.

Til að setja upp skrár með takmarkanir á skattaskráningu skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**.
1. Veldu nauðsynlegt ferli.
1. Veldu **POS skrár með takmarkanir á fjárhagslegum ferli** flipa.
1. Bættu við skrám með takmörkunum á ríkisfjármálum eftir þörfum.

### <a name="validate-the-fiscal-registration-process"></a>Staðfestu fjárhagsskráningarferlið

Mælt er með því að þú staðfestir fjárhagsskráningarferlið í eftirfarandi tilvikum:

- Þú hefur lokið við allar stillingar fyrir nýtt skráningarferli. Þessar stillingar fela í sér úthlutun skráningarferla á POS virknisnið og vélbúnaðarsnið.
- Þú hefur gert breytingar á núverandi fjárhagsskráningarferli og þær breytingar gætu valdið því að annað fjárhagslegt tengi sé valið á keyrslutíma. (Til dæmis hefurðu breytt tengihópnum fyrir fjárhagsskráningarferlisþrep, virkjað virkt tengisnið í tengihópi eða bætt nýju virkusniði tengi við tengihóp.)
- Þú hefur gert breytingar á úthlutun tækniprófíla tengis á vélbúnaðarsnið.

Til að staðfesta fjárhagsskráningarferlið skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum Commerce, farðu á **Skráningarferli í ríkisfjármálum** síða (**Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Skráningarferli í ríkisfjármálum**).
1. Veldu **Staðfesta** til að staðfesta skattskráningarferlið.
1. Á síðunni **Dreifingaráætlun** skal keyra verkin **1070** og **1090** til að flytja gögn til gagnagrunns rásarinnar.

## <a name="set-up-fiscal-texts-for-discounts"></a>Setja upp fjárhagstexta fyrir afslætti

Í sumum tilfellum verður að prenta sérstakan texta á fjárhagskvittun ef afsláttur er notaður. Hægt er að setja upp fjárhagstexta fyrir afslætti á síðunni **Fjárhagstenglahópur** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Fjárhagstenglahópar**).

- Fyrir handvirka afslætti sem eru notaðir á sölustað ætti að stilla fjárhagstexta fyrir upplýsingakóðann eða flokk upplýsingakóða sem er tilgreindur sem upplýsingakóðinn **Afurðarafsláttur** í virknireglu sölustaðar.

    1. Á síðunni **Flokkur fjárhagstengils** skal velja **Texti fyrir fjárhagskvittun**.
    1. Í flipanum **Upplýsingakóðar** skal velja **Bæta við** og velja upplýsingakóða eða flokk upplýsingakóða.
    1. Í reitnum **Númer upplýsingakóða** skal velja gildi.
    1. Í reitnum **Númer undirkóða** skal velja gildi ef krafist er undirkóða fyrir valinn upplýsingakóða.
    1. Í reitnum **Texti fyrir fjárhagskvittun** skal tilgreina fjárhagstexta sem á að prenta á fjárhagskvittun.
    1. Stilltu valkostinn **Prenta innslátt notanda á fjárhagskvittun** á **Já** til að hnekkja textanum á fjárhagskvittun með upplýsingum sem notandi slær inn handvirkt á sölustaðnum. Þessi valkostur gildir aðeins um upplýsingakóða sem eru með gerð innsláttar sem **Texti**.

    > [!NOTE]
    > Hægt er að tilgreina fjárhagstexta fyrir ýmsa upplýsingakóða til að styðja við aðstæður þar sem flokkar upplýsingakóða, tengdir upplýsingakóðar og ræstir upplýsingakóðar eru notaðir. Við þessar aðstæður mun fjárhagskvittunin innihalda fjárhagstexta fyrir alla upplýsingakóða sem eru tengdir við færslulínuna þar sem afslátturinn var notaður.

- Fyrir afslætti sem miðast við rásir skal skilgreina fjárhagstexta fyrir afsláttarkennið.

    1. Á síðunni **Flokkur fjárhagstengils** skal velja **Texti fyrir fjárhagskvittun**.
    1. Í flipanum **Afslættir** skal velja **Bæta við** og velja afsláttarkenni.
    1. Í reitnum **Texti fyrir fjárhagskvittun** skal tilgreina fjárhagstexta sem á að prenta á fjárhagskvittun.

    > [!NOTE]
    > Ef nokkrir afslættir eru notaðir fyrir sömu færslulínuna mun fjárhagskvittunin innihalda fjárhagstexta frá öllum afsláttum sem eru tengdir við þessa færslulínu.

## <a name="set-error-handling-settings"></a>Velja stillingar villumeðhöndlunar

Valkostir villumeðhöndlunar sem eru í boði í samþættingu fjárhags eru stilltir í skráningarferli fjárhags. Nánari upplýsingar um villumeðhöndlun í samþættingu fjárhags er að finna í [Villumeðhöndlun](fiscal-integration-for-retail-channel.md#error-handling).

Til að stilla villumeðferðarstillingar skaltu fylgja þessum skrefum.

1. Á síðunni **Skráningarferli fjárhags** (**Retail og Commerce \> Uppsetning rásar \> Samþætting fjárhags \> Skráningarferli fjárhags**) er hægt að stilla eftirfarandi færibreytur fyrir hvert skref í skráningarferli fjárhags:

    - **Leyfa að sleppa** - Þessi færibreyta virkjar valkostinn **Sleppa** í svarglugga villumeðhöndlunar.
    - **Leyfa að merkja sem skráð** - Þessi færibreyta virkjar valkostinn **Merkja sem skráð** í svarglugga villumeðhöndlunar.
    - **Leyfa fresta** – Þessi breytu gerir kleift að **Fresta** valmöguleika í villumeðferðarglugganum.
    - **Halda áfram á villu** - Ef þessi færibreyta er virkjuð getur ferli fjárhagsskráningar haldið áfram í afgreiðslukassa ef fjárhagsskráning færslu eða tilviks mistekst. Annars, til að keyra fjárhagsskráningu á næstu færslu eða tilviki, verður notandi að reyna misheppnuðu fjárhagsskráninguna aftur, sleppa henni eða merkja færsluna eða tilvikið sem skráð. Frekari upplýsingar er að finna í [Valfrjáls fjárhagsskráning](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Ef færibreytan **Halda áfram á villu** er virkjuð eru færibreyturnar **Leyfa að sleppa** og **Leyfa að merkja sem skráð** sjálfkrafa gerðar óvirkar.

1. The **Sleppa** og **Merktu sem skráð** valkostir í villumeðferðarglugganum krefjast þess að **Leyfa að sleppa skráningu eða merkja sem skráð** leyfi vera virkt. Til að virkja þessa heimild skaltu fara á **Leyfishópar** síða (**Verslun og verslun \> Starfsmenn \> Leyfishópar**), og stilltu **Leyfa að sleppa skráningu eða merkja sem skráð** valmöguleika til **Já**.
1. The **Fresta** valkostur í villumeðferðarglugganum krefst þess að **Leyfa fresta** leyfi vera virkt. Til að virkja heimildina skaltu fara á **Leyfishópar** síða (**Verslun og verslun \> Starfsmenn \> Leyfishópar**), og stilltu **Leyfa fresta** valmöguleika til **Já**.
1. The **Sleppa**, **sem skráð**, og **Fresta** valkostir leyfa rekstraraðilum að slá inn viðbótarupplýsingar þegar fjárhagsskráning mistekst. Til að gera þessa virkni aðgengilega ættirðu að tilgreina **Sleppa**, **sem skráð**, og **Fresta** upplýsingakóðar á fjárhagstengihópi. Upplýsingarnar sem notendur slá inn eru síðan vistaðar sem færsla upplýsingakóða sem er tengd við fjárhagsfærsluna. Nánari upplýsingar um upplýsingakóða er að finna í [Upplýsingakóðar og upplýsingakóðaflokkar](../info-codes-retail.md).

    > [!NOTE]
    > Virkniræsingin **Afurð** er ekki studd fyrir upplýsingakóðana sem eru notaðir fyrir **Sleppa** og **Merkja sem skráð** í fjárhagstenglaflokkum.

    - Á **Fjárhagstengingarhópur** síðu, á **Upplýsingakóðar** flipann, veldu upplýsingakóða eða upplýsingakóðahópa í **Sleppa**, **sem skráð**, og **Fresta** sviðum.

    > [!NOTE]
    > Hægt er að búa til eitt fjárhagsskjal og eitt skjal sem er ekki fjárhagsskjal í hvaða skrefi sem er í skráningarferli fjárhags. Viðbót fjárhagsskjalaveitu ber kennsl á allar gerðir af færslum eða tilvikum sem tengdar við fjárhagsskjal eða skjals sem ekki er fjárhagsskjal. Eiginleiki villumeðhöndlunar á aðeins við um fjárhagsskjöl.
    >
    > - **Fjárhagsskjal** - Áskilið skjal sem ætti að skrá (t.d. fjárhagskvittun).
    > - **Skjal sem ekki er fjárhagsskjal** - Viðbótarskjal fyrir færsluna eða tilvikið (t.d. gjafakort).

1. Ef notandinn verður að geta haldið áfram til að vinna úr fyrirliggjandi aðgerð (t.d. stofnun eða frágang á færslu) eftir að villa í ástandsskoðun kemur upp, ættir þú virkja heimildina **Leyfa að sleppa villu í ástandsskoðun** á síðunni **Heimildaflokkar** (**Retail og Commerce \> Starfsmenn \> Heimildaflokkar**). Frekari upplýsingar um ástandsskoðunarferli er að finna í [Ástandsskoðun fjárhagsskráningar](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Setja upp X/Z-skýrslur fjárhags úr POS

Til að gera kleift að keyra X/Z-skýrslur úr POS ættir þú að bæta nýjum hnöppum við POS-útlit.

- Á síðunni **Hnappahnit** skal fylgja leiðbeiningunum í [Bæta sölustaðaraðgerðum við POS-útlit með hnappahnitshönnuði](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) til að setja upp hönnuðinn og uppfæra POS-útlit.

    1. Veldu útlitið til að uppfæra. 
    1. Bættu við nýjum hnapp og stilltu eiginleika hnappsins **Prenta fjárhag X**.
    1. Bættu við nýjum hnapp og stilltu eiginleika hnappsins **Prenta fjárhag Z**.
    1. Á síðunni **Dreifingaráætlun** skal keyra verkið **1090** til að flytja breytingar til gagnagrunns rásarinnar.

## <a name="enable-manual-execution-of-deferred-fiscal-registration"></a>Virkja handvirka framkvæmd á frestað fjárhagsskráningu

Til að virkja handvirka framkvæmd á frestað fjárhagsskráningu ættir þú að bæta nýjum hnappi við POS útlit.

- Á síðunni **Hnappahnit** skal fylgja leiðbeiningunum í [Bæta sölustaðaraðgerðum við POS-útlit með hnappahnitshönnuði](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) til að setja upp hönnuðinn og uppfæra POS-útlit.

    1. Veldu útlitið til að uppfæra.
    1. Bættu við nýjum hnapp og stilltu eiginleika hnappsins **Ljúka skráningarferli fjárhags**.
    1. Á síðunni **Dreifingaráætlun** skal keyra verkið **1090** til að flytja breytingarnar þínar til gagnagrunns rásarinnar.

## <a name="view-connection-parameters-and-other-information-in-pos"></a>Skoðaðu tengibreytur og aðrar upplýsingar í POS

Til að skoða tengifæribreytur og aðrar upplýsingar í POS skaltu fylgja þessum skrefum.

1. Opnaðu Modern POS (MPOS) eða Cloud POS (CPOS).
1. Veldu **Stillingar**. Ef fjárhagsleg samþætting er virkjuð, **Samþætting ríkisfjármála** kafla til hægri mun sýna eftirfarandi upplýsingar:

    - Staða ríkisskráningar
    - Staða síðustu ríkisfjármálaviðskipta
    - Fjöldi endurskoðunarviðburða sem bíða

1. Veldu **Upplýsingar** til að skoða eftirfarandi upplýsingar:

    - Skref skráningarferlisins
    - Færibreytur tengingar
    - Endurskoðun viðburða upplýsingar
 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
