---
title: Sending lítilla pakka
description: Í þessari grein er að finna upplýsingar um eiginleika lítilla pakkasendinga (SPS). Þessi eiginleiki gerir Microsoft Dynamics 365 Supply Chain Management kleift að senda inn upplýsingar um pakkaða gáma til flutningsaðila og fá síðan merkimiða, flutningstaxta og rakningarnúmer aftur frá flutningsaðila.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b2adde2b81ed881a3c81193a2220fbe569069c7c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336156"
---
# <a name="small-parcel-shipping"></a>Sending lítilla pakka

[!include [banner](../../includes/banner.md)]

Eiginleiki lítilla pakkasendinga (SPS) gerir Microsoft Dynamics 365 Supply Chain Management kleift að eiga bein samskipti við farmflytjendur með því að bjóða upp á samskiptaramma í gegnum API flutningsaðila. Þessi virkni er gagnleg þegar einstakar sölupantanir eru sendar í gegnum flutningsfyrirtæki í stað þess að nota gámaflutning eða sendingar sem eru minni en fullhlaðinn trukkur (LTL).

SPS-eiginleikinn á samskipti við farmflytjandann í gegnum sérstaka *taxtavél*. Fyrirtækið verður að þróa þessa taxtavél í samstarfi við flutningsaðilann eða miðstöð flutningsþjónustunnar. Þessi taxtavél gerir Supply Chain Management kleift að senda inn upplýsingar um pakkaða gáma til flutningsaðila og fá síðan merkimiða, flutningstaxta og rakningarnúmer aftur frá flutningsaðila.

Flutningstaxtanum sem er skilað er bætt við viðeigandi sölupöntun sem gjaldi. Merkimiðanum sem er skilað er síðan hægt að prenta með því að nota prentara Zebra-forritunarmáls (ZPL) og nota hann fyrir sendinguna. Flutningsaðilinn mun skanna þennan merkimiða þegar hann sækir pakkana í vöruhúsinu.

## <a name="prepare-your-system-to-support-sps"></a>Undirbúa kerfið fyrir stuðning við SPS

Áður en hægt er að byrja að nota SPS-virkni þarf að kveikja á SPS-eiginleikanum í eiginleikastjórnun, bæta við taxtavélinni og setja upp einingarnar **Flutningsstjórnun** og **Vöruhúsakerfi** til að styðja við hana.

### <a name="turn-the-sps-feature-on-or-off"></a>Kveikir eða slekkur á SPS eiginleikanum

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Sending lítilla pakka* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="deploy-and-set-up-rate-engines"></a>Nota og setja upp taxtavélar

Supply Chain Management inniheldur engar taxtavélar. Sækja þarf eða stofna nauðsynlegar taxtavélar og síðan bæta þeim við kerfið. Hins vegar býður Microsoft upp á sýnitaxtavél sem hægt er að nota til prófunar.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Hlaða niður og nota prufutaxtavél

Fylgið þessum skrefum til að fá sýniútgáfu af taxtavél.

1. Í GitHub skal sækja [DLL fyrir sýniútgáfu taxtavélar](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).
1. Á Supply Chain Management-þjóninum skal vista DLL í möppunni **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.

#### <a name="create-and-deploy-functional-rate-engines"></a>Stofna og nota virkar taxtavélar

Upplýsingar um hvernig á að stofna og setja upp virkar taxtavélar þannig að hægt sé að nota þær í framleiðslu- eða prófunarumhverfi er að finna í eftirfarandi greinum:

- [Stofna nýja flutningsstjórnunarvél](../transportation/create-new-transportation-management-engine.md)
- [Setja upp flutningsstjórnunarvélar](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

Frekari upplýsingar um hvernig á að búa til SPS-taxtavél er að finna í eftirfarandi bloggfærslu: [Sending lítilla pakka: Hvernig á að nýta sér virkni lítilla pakkasendinga í Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Setja upp taxtavél í Supply Chain Management

Þegar búið er að stofna og virkja taxtavél fyrir SPS skal fylgja þessum skrefum til að setja hana upp.

1. Opnið **Flutningsstjórnun \> Uppsetning \> Vélar \> Taxtavél**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi reiti:

    - **Taxtavél** – Sláið inn einkvæmt heiti fyrir taxtavél. Ef sýniútgáfa taxtavélar er notuð skal slá inn *Sýniútgáfa taxtavélar*.
    - **Heiti** – Færa skal inn stutta lýsingu á taxtavélinni. Ef sýniútgáfa taxtavélar er notuð skal slá inn *Sýniútgáfa taxtavélar*.
    - **Lýsigagnakenni fyrir taxta** – Veljið grunninn sem á að nota til að reikna út taxtann. Til dæmis gæti gengi notanda verið reiknað út frá vegalengd. Ef verið er að nota prufutaxtavélina er hægt að skilja þennan reit eftir auðan.
    - **Vélarsamsetning** – Færið inn skráarheiti DLL-pakkans sem var virkjaður. Ef prufutaxtavél er notuð skal færa inn *TMSSmallParcelShippingEngine.dll*.
    - **Vélarklasi** – Færið inn klasaheitið sem var komið upp fyrir taxtavélina. Ef sýniútgáfa taxtavélar er notuð skal færa inn *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.

## <a name="example-scenario"></a>Dæmi

Þetta dæmi sýnir hvernig á að setja upp og nota SPS eftir að búið er að undirbúa kerfið eins og lýst var hér á undan. Þessar aðstæður nota áðurnefnda sýniútgáfu taxtavélar.

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/fin-ops/get-started/demo-data.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

### <a name="set-up-the-scenario"></a>Setja upp aðstæður

Fyrir þetta dæmi þarf að vera með sýnidæmi um flutningsaðila, flutningsflokk, pökkunarreglu og pökkunarforstillingu. Eftirfarandi undirkaflar útskýra hvernig á að undirbúa færslurnar sem eru nauðsynlegar fyrir aðstæðurnar. Í framleiðsluaðstæðum líkist uppsetningarferlið yfirleitt ferlinu sem er lýst hér. Hins vegar skal stilla önnur gildi.

#### <a name="set-up-carriers"></a>Setja upp flutningsaðila

Fylgið þessum skrefum til að setja upp flutningsaðila.

1. Opnið **Flutningsstjórnun \> Uppsetning \> Flutningsaðilar \> Farmflytjendur**.
1. Á aðgerðasvæðinu skal velja **Nýr** til að bæta við flutningsaðila.
1. Stillið eftirfarandi gildi í hausnum:

    - **Farmflytjandi:** *Sýnidæmi flutningsaðila*
    - **Heiti:** *Sýnidæmi flutningsaðila*
    - **Stilling:** *Landflutningur*

1. Stilltu eftirfarandi gildi á **Yfirlit** flipanum:

    - **Virkja farmflytjanda:** *Já*
    - **Virkja einkunn flutningsaðila:** *Já*

1. Á flýtiflipanum **Línur** skal velja **Ný** til að bæta línu við hnitanetið.
1. Stillið eftirfarandi gildi fyrir nýju þjónustuna:

    - **Flutningsþjónusta:** *Sýnidæmi flutningsþjónustu*
    - **Heiti:** *Sýnidæmi flutningsþjónustu*
    - **Flutningsaðferð:** *Jörð*

    Sláið inn handahófskennd gildi fyrir alla aðra reiti, eins og nauðsynlegt er. (Þegar ný færsla farmflytjanda er vistuð verður nýr flutningsmáti stofnaður og reiturinn **Flutningsmáti** verður stilltur sjálfkrafa.)

1. Í flýtiflipanum **Taxtaforstillingar** skal velja **Ný** til að bæta taxtaforstillingu við hnitanetið.
1. Stillið eftirfarandi gildi fyrir nýju forstillinguna:

    - **Matsforstilling:** *Sýnidæmi flutningsþjónustu*
    - **Heiti:** *Sýnidæmi flutningsþjónustu*
    - **Taxtavél:** *Sýniútgáfa taxtavélar*

    Sláið inn handahófskennd gildi fyrir alla aðra reiti, eins og nauðsynlegt er.

1. Í aðgerðarúðunni skal velja **Vista**.

Frekari upplýsingar um hvernig á að setja upp flutningsaðila er að finna í [Setja upp flutningsaðila](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Setja upp reikninga flutningsþjónustu

Fylgið þessum skrefum til að setja upp reikning flutningsþjónustu.

1. Opnið **Flutningsstjórnun \> Uppsetning \> Taxti \> Reikningur flutningsþjónustu**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta við flutningsþjónustureikningi.
1. Stillið eftirfarandi gildi fyrir nýja reikninginn:

    - **Farmflytjandi:** *Sýnidæmi flutningsaðila*
    - **Flutningsþjónusta:** *Sýnidæmi flutningsþjónustu*
    - **Númer viðskiptavinalykils flutningsaðila:** Númer viðskiptavinalykils flutningsaðila sem er notað til að sannprófa og auðkenna tenginguna við farmflytjandann. Flutningsaðilinn mun gefa upp þetta gildi. Hægt er að færa inn handahófskennt gildi ef þú ert að nota prufuþjónustuna.
    - **Svæði:** *6*
    - **Vöruhús:** *62*

    > [!NOTE]
    > Oft er gildið **Númer viðskiptavinalykils flutningsaðila** er eina gildið sem þarf til að sannvotta tenginguna. Hins vegar ef flutningsaðilinn krefst frekari færibreyta sannvottunar ætti fyrirtækið að sérstilla þessa síðu til að bæta við viðbótarreitum eftir þörfum.

#### <a name="set-up-a-container-packing-policy"></a>Setja upp pökkunarreglur gáms

Fylgið þessum skrefum til að setja upp pökkunarreglur gáms.

1. Ef ekki hefur þegar verið sett upp skilgreining ZPL-prentara skal nota forritið Document Routing Agent til að setja hana upp. Frekari upplýsingar er að finna í [Yfirlit skjalaprentunar](../../fin-ops-core/dev-itpro/analytics/print-documents.md) og tengdum greinum.
1. Fara í **Vöruhúsakerfi \> Uppsetning \> Gámar \> Pökkunarreglur gáms**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta við pökkkunarreglu gáms.
1. Í haus nýju reglunnar skal stilla eftirfarandi gildi:

    - **Pökkunarregla gáms:** *Sýnidæmi pökkunarreglu*
    - **Lýsing:** Lýsing á reglunni

1. Stilltu eftirfarandi gildi á **Yfirlit** flipanum:

    - **Vöruhús:** *62*
    - **Sjálfgefin staðsetning lokasendingar:** *Útskot*
    - **Þyngdareining:** *kg*
    - **Lokunarregla geymis:** *Sjálfvirk losun*
    - **Losunarregla geymis:** *Gera tiltækt á endanlegum sendingarstað*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Skrá geymis**:

    - **Sjálfvirk skrá við lokun geymis:** *Já*
    - **Skráarkröfur fyrir gám:** *Flutningsstjórnun*
    - **Prenta innihald gámsins:** *Nei*

1. Í flýtiflipanum **Prentun merkimiða flutningsaðila** skal stilla eftirfarandi gildi:

    - **Prenta merkimiða gáms:** *Alltaf*
    - **Prentaraheiti:** Heiti ZPL-prentarans sem á að prenta merkimiða

#### <a name="set-up-a-packing-profile"></a>Setja upp forstillingu umbúða

Fylgið þessum skrefum til að setja upp forstillingu umbúða.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Forstillingar umbúða**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta forstillingu umbúða við hnitanetið.
1. Stillið eftirfarandi gildi fyrir nýju forstillinguna:

    - **Forstillingarkenni umbúða:** *Sýnidæmi umbúðaforstillingar*
    - **Lýsing:** Lýsing á forstillingunni
    - **Pökkunarregla gáms:** *Sýnidæmi pökkunarreglu*
    - **Auðkennisstilling gáms:** *Sjálfvirkt*
    - **Gámagerð:** *SmallBox*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>Setja upp viðskiptavin til að nota SPS-flutningsaðila

Fylgdu þessum skrefum til að setja viðskiptavin upp þannig að hann geti notað flutningsaðilann sem var stofnaður.

1. Farið í **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**.
1. Í hnitanetinu skal finna og velja viðskiptavinur *US-027*.
1. Á aðgerðasvæðinu, í flipanum **Almennt**, í flokknum **Setja upp**, skal velja **Viðskiptavinalyklar flutningsaðila**.
1. Á síðunni **Viðskiptavinalyklar flutningsaðila**, á aðgerðasvæðinu, skal velja **Nýr** til að bæta nýjum lykli við hnitanetið.
1. Stillið eftirfarandi gildi fyrir nýja reikninginn:

    - **Farmflytjandi:** *Sýnidæmi flutningsaðila*
    - **Númer viðskiptavinalykils flutningsaðila:** *12345* (Gildið er ekki mikilvægt fyrir þessar aðstæður, en það verður vísað í það í næsta hluta.)

### <a name="go-through-the-example-scenario"></a>Farið í gegnum sýnidæmið

Þegar búið er að setja upp öll sýnigögn eins og lýst var í hlutanum hér á undan er hægt að fara í gegnum sýnidæmið.

#### <a name="create-a-sales-order-and-process-the-work"></a>Stofna sölupöntun og vinna verk

Fylgdu þessum skrefum til að búa til sölupöntun.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Smellið á **Nýtt** til að stofna nýja sölupöntun.
1. Í svarglugganum **Stofna sölupöntun** skal stilla reitinn **Reikningur viðskiptavinar** á *US-027* .
1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Í flýtiflipanum **Sölupöntunarhaus** skal stilla reitinn **Númer viðskiptavinalykils flutningsaðila** á gildið sem var valið fyrir þennan viðskiptavin hér á undan (*12345*).
1. Í hlutanum **Sölupöntunarlínur** skal bæta við sölulínu og stilla eftirfarandi gildi fyrir hana:

    - **Vörunúmer:** *A0002*
    - **Magn:** *1*
    - **Svæði:** *6*
    - **Vöruhús:** *62*

1. Skiptið yfir í **Hausa** yfirlitið.
1. Í flýtiflipanum **Afhending** skal stilla eftirfarandi gildi:

    - **Farmflytjandi:** *Sýnidæmi flutningsaðila*
    - **Flutningsþjónusta:** *Sýnidæmi flutningsþjónustu*

1. Skiptið aftur yfir í yfirlitið **Línur**. Ef beðið er um að uppfæra afhendingarmáta fyrir sölulínurnar skal velja **Já**.
1. Í hlutanum **Sölupöntunarlínur** skal velja pöntunarlínuna sem var sett upp hér á undan og síðan velja **Birgðir \> Frátekning**.
1. Á síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Vinna er stofnuð til að færa vörur úr tiltektarstaðsetningu og yfir á pökkunarstöð.

1. Í hlutanum **Sölupöntunarlínur** skal velja **Vöruhúsa \> Upplýsingar sendingar**.
1. Á síðunni **Upplýsingar sendingar** skal skrifa hjá sér sendingarkennið. Þörf er á því þegar sending er pökkuð á pökkunarstöðinni.
1. Lokið síðunni **Upplýsingar sendingar** til að fara aftur í sölupöntunina.
1. Skráið hjá ykkur sölupöntunarnúmerið og farið síðan í **Vöruhúsakerfi \> Vinna \> Öll vinna**.
1. Notið sölupöntunarnúmerið til að finna og velja vinnu sem var stofnuð fyrir pöntunina.
1. Á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Ljúka vinnu**.
1. Á síðunni **Vinnulok**, í reitnum **Notandakenni**, skal velja notandakenni. Veldu **Villuleita verk** á aðgerðasvæðinu.
1. Ef verk stenst sannvottun skal velja **Ljúka vinnu** á aðgerðasvæðinu.

    Vinnan er merkt sem lokið til að herma eftir flutningi varanna á pökkunarstöðina.

#### <a name="pack-the-shipment"></a>Sending pökkuð

Fylgið þessum skrefum til að pakka sendingunni.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Starfsmaður** og gangið úr skugga um að notandareikningurinn sé tengdur reikningi starfsmanns fyrir vöruhúsakerfi.
1. Farið í **Vöruhúsakerfi \> Tiltekt og gámun \> Pakka**.
1. Í svarglugganum **Velja pökkunarstöð** skal stilla eftirfarandi gildi:

    - **Svæði:** *6*
    - **Vöruhús:** *62*
    - **Staðsetning:** *Pakka*
    - **Forstillingarkenni umbúða:** *Sýnidæmi umbúðaforstillingar*

1. Veljið **Í lagi**.
1. Síðan **Pakka** birtist. Í framleiðsluaðstæðum mun starfskraftur skanna númeraplötu eða sendingarauðkenni. Fyrir þessar aðstæður skal hins vegar opna síðuna **Allar sendingar** og leita að sendingarnúmerinu fyrir sendinguna sem var stofnuð rétt í þessu. Færið síðan þetta gildi inn í reitinn **Númeraplata eða sending** á síðunni **Pakka**. Einnig er hægt að færa inn sendingarkennið sem var skrifað niður hér á undan.
1. Á aðgerðasvæðinu skal velja **Nýr gámur**.
1. Svarglugginn sem birtist sýnir upplýsingar um nýja gáminn. Haldið sjálfgefnu gildunum óbreyttum og veljið síðan **Í lagi**.
1. Á síðunni **Pakka**, í flýtiflipanum **Vörupökkun**, í reitnum **Auðkenni**, skal velja *A0002* til að pakka þeirri vöru. Vörunni er bætt við gáminn.
1. Á aðgerðasvæðinu skal velja **Gámar fyrir sendingu**.

    Síðan **Gámar til sendingar** sem birtist er með línu fyrir gáminn sem var stofnuð hér á undan. Hins vegar er reiturinn **Skráarkenni gáms** í þeirri línu auður eins og er vegna þess að ekki er búið að móttaka merkimiðann og rakningarnúmerið frá flutningsaðilanum.

1. Á aðgerðasvæðinu skal velja **Loka gámi**.
1. Í svarglugganum **Loka gámi** skal stilla reitinn **Brúttóþyngd** á *1 kg* og síðan velja **Í lagi**.

    Nú ætti að prenta merkimiðann á ZPL-prentaranum sem var valinn hér áður. Niðurstaðan ætti að líkjast eftirfarandi dæmi.

    ![Dæmi um merkimiða.](media/sps-label-example.png "Dæmi um merkimiða")

1. Takið eftir að gildunum **Skráarkenni gáms** og **Heildarfarmur** hefur verið bætt við sem mótteknum frá flutningsaðila.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]