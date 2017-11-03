---
title: "Tilföng verks"
description: "Þessi efnisatriði gefur upplýsingar um tilföng verka."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8139134ed230cc1525c698fadb20309afee0a68f
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="project-resourcing"></a>Tilföng verks

[!include[banner](../includes/banner.md)]

Þessi efnisatriði gefur upplýsingar um tilföng verka.

Ein áskorun fyrir verkefnastjóra og forðastjóra meðan á áætlunargerð stendur er forðaúthlutun, þar sem þeir þurfa að ákvarða og taka frá rétt tilföng til vinnu á verk. Í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition gerir tilfangageta verkefna kleift að skilgreina hlutverk sem eru meðhöndluð sem tímabundin tilföng sem hægt er að taka frá fyrir sérstaka úttekt eða sem hluta af úttekt. Þessi tegund tilfanga gerir verkefnisstjórum og stjórnendum tilfanga kleift að ljúka eftirfarandi verkum:

- Skilgreina hlutverk sem hefur nauðsynlega hæfni til að gera auðvelt að samsvara tilföng.
- Nota hlutverk til að skilgreina upphaflega úttekt sem er byggð á fráteknum tilföngum.
- Gera kostnaðarmat og ákvarða upphaflega fjárhagsáætlun, byggt á úthlutuðum hlutverkum og tilföngum fyrir verk.
- Hlutverk eru notuð til að áætla fjölda úttekta tilfanga sem krafist er fyrir hverja úttekt.
- Áætla fjölda tilfanga sem krafist er fyrir allan líftíma verksins.
- Gera drög að sundurliðun verkþátta (WBS) með því að nota upphaflega tilfangaúthlutun.

[![Líftími afurðar](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Eftir því sem áætlunargerð er haldið áfram, er hægt að skipta út áætluðum tilföngum fyrir mönnuð tilföng. Verkefnisstjóri getur einnig farið til baka og uppfært tilfangafrátektir á öllum verkstigum.

## <a name="set-up-project-resources"></a>Setja upp verktilföng.
Þú þarft að setja upp dagatal og tengja það við starfsmann eða starfskraft. Dagatalið er notað til að áætla verkið og vinnutíma þeirra tilfanga sem eru frátekin fyrir verkið. Við uppsetningu dagatals geta verkefnisstjórar framkvæmt sléttun á tilföngum sem hluta af fínstillingu tilfanga. Samkvæmt áætlun dagatals geta takmarkanir verið settar á tilföng. Hægt er að setja upp dagatal sem á síðunni **Dagatöl**.

Þegar starfsmaður er settur upp sem tilföng verks er hægt að velja úr starfsmönnum sem vinna í fyrirtækinu þar sem verið er að setja upp tilföng. Einnig er hægt að velja starfskraftur úr öðrum fyrirtækjum innan fyrirtækisins þíns. Þessir starfskraftar eru þekktir sem samstæðutilföng.

Eftirfarandi ferli útskýra hvernig setja á upp starfsmanns sem tilföng verks innan fyrirtækisins og hvernig á að setja upp samstæðuverk tilfanga.

### <a name="set-up-a-worker-as-a-project-resource"></a>Setja upp starfmann sem verktilfang.

1. Á síðunni **Starfsmenn**, í listanum **Starfsfólk**, veljið starfsmann sem verið er að bæta við sem tilfang verks og opnið skrá starfsmannsins.
2. Á Aðgerðasvæðinu skal velja **Verk** &gt; **Uppsetning** &gt; **Verkuppsetning**.
3. Velja skal Dagatal og loka svo síðunni.

Einnig er hægt að tilgreina sjálfgefið verk fyrir tilföng sem gerð áætlaðs verkefnis. Hægt er að nota áætlaðar úthlutanir þegar tilfangastjórnandi eða verkstjóri veit hvaða verk tilfangið verður að vinna að fyrirfram. Einnig er hægt að byggja áætlaðar úthlutanir á beiðni kostunaraðila verks eða viðskiptavinar. Til að úthluta verki fyrirfram: Á síðunni **Úthluta verkum**, á flipanum **Verk**, á listanum **Eftirstandandi verk** skal velja viðeigandi verk.

### <a name="set-up-an-intercompany-resource"></a>Setja upp samstæðutilföng

Þegar starfsmaður er settur upp sem samstæðutilföng verður að ljúka uppsetningunni í bæði útlánafyrirtækinu og lántökufyrirtækinu.

**Í útlánafyrirtækinu:**

1. Í Finance and Operations skal staðfesta að útlánafyrirtækið sé valið, og ljúka síðan ferlinu hér að framan, „Setja upp starfsmann sem tilfang verks“.
2. Á síðunni **Samstæðulyklar** skal velja **Nýtt**.
3. Í svæðinu **Kenni lögaðila** skal velja útlánafyrirtæki. Fyllið út eftirstandandi svæði eftir þörfum og velja svo **Vista**.
4. Á síðunni **Innanhússverð** skal velja **Nýtt**.
5. Í **Lögaðili sem fær lánað** reitnum skal velja viðkomandi fyrirtæki.
6. Til að lána lántökufyrirtækinu aðeins þau tilföng sem voru stofnuð í upphafi þessa hluta í svæðinu **Tilföng** skal velja nafn tilfanganna sem voru stofnuð. Til að gera öll tilföng í fyrirtækinu tiltæk lántökufyrirtæki skal skilja svæðið **Tilföng** eftir autt.
7. Á **Verkefnastjórnun og bókhaldsfæribreytur** síðunni, á flipanum **Samstæða** Skal stilla **Virkja samstæðuröðun tilfanga og tímablöð** valkostinn á **Já**.

**Í lántökufyrirtækinu:**

- Á **Tilfangalisti** síðunni skal færa inn heiti tilfangs sem þú stofnaðir í útlánafyrirtækinu til að staðfesta að heitið sé innifalið í tilfangalistalántökufyrirtækis.

## <a name="manage-resource-competencies"></a>Umsjón með hæfni tilfanga
Skilgreiningar á hæfni tilfanga eru mikilvægur hluti af stjórnun tilfanga. Hæfni er hægt að nota sem grunnlínu til að ákvarða tilföng sem eru með rétt jafnvægi hvað varðar hæfni, menntun, réttindi og verkreynslu. Rétt er að setja þessar upplýsingar upp fyrir hvert tilfang og uppfæra þær reglulega. Á þennan hátt er hægt að hámarka getu þegar tiltekin hæfni tilfanga er borin saman við úthlutun verks til tilfanga.

[![Dæmi um hæfni, réttindi, menntun og verkreynslu](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Eftirfarandi aðgerðir útskýra hvernig á að setja upp ákveðna hæfni fyrir tilfang.

Til að setja upp hæfni starfsmanns, er hægt að nota annað hvort listasíðuna **Starfsmenn** í Mannauði eða listasíðuna **Tilföng** í Verkefnastjórnun og bókhald. Fyrir eftirfarandi ferla notum við listasíðuna **Starfsmenn** í Mannauði.

### <a name="set-up-competencies-certificates"></a>Setja upp hæfni: Réttindi

1. Á listasíðunni **Starfsmenn** skal velja línu þess starfsmanns sem verið er að bæta við upplýsingum um réttindi fyrir.
2. Í Aðgerðasvæði, á flipanum **Starfsmaður** í flokknum **Hæfni** skal velja **Réttindi**.
3. Veljið **Nýtt** og svo, í reitnum **Tegund réttinda**, veljið **PMP**.
4. Í svæðinu **Upphafsdagsetning**, veljið **1/10/2015** og svo **Vista**.

### <a name="set-up-competencies-skills"></a>Setja upp hæfni: Færni

1. Á listasíðunni **Starfsmenn** skal tryggja að starfsmaðurinn sem notaður var í fyrra ferli sé enn valinn. Svo, í Aðgerðasvæði, á flipanum **Starfsmaður** í flokknum **Hæfni** skal velja **Færni**.
2. Velja **Nýja**.
3. Á svæðinu **Færni** skal velja **Verkefnastjórnun**.
4. Á svæðinu **Stig** skal velja **5 Expert**.
5. Á svæðinu **Dagsetning stigs**, veljið **14/1/2014**.
6. Á svæðinu **Reynsla í árum** færið inn **10**.
7. Veljið **Vista** og lokið síðan skjámyndinni.

## <a name="create-a-new-project"></a>Stofna nýtt verk
1. Á **Verkefnastjórnun** skal velja **Nýtt verk** og færa eftirfarandi gildi inn:

    - **Gerð verks:**Tími og efni
    - **Verkheiti:** XYZ Uppfærsla þrep 2
    - **Verkflokkur:** TM\_WIP
    - **Auðkenni verksamnings:** 00000002

2. Velja **Stofna verk**.

### <a name="assign-a-resource-to-a-project"></a>Úthluta tilfangi á verk

1. Á síðunni **Starfskraftar** í listanum **Starfskraftar**, skal velja skrá starfskrafts sem hefur áður verið sett upp hæfni fyrir og opna starfskrafts.
2. Á Aðgerðarrúðunni, á flipanum **Verk** í flokkinum **Uppsetning** veljið **Úthluta verkum**.
3. Á **Úthlutanir tilfanga fyrir villuleit í verki** síðunni á **Verk** flipanum í **Bæta verki við valin verk** reitnum skal sía eftir **XYZ Uppfærsla þrep 2** verki.
4. Í rúðunni **Eftirstandandi verk**, veljið verk og smellið síðan á örvarhnappur til að bæta því við í **Valin verk** rúðunni.

Einnig er hægt að úthluta tegundum fyrir tilföng eftir þörfum. Gerð tegundar er annað hvort **Kostnaður** eða **Tekjur**. Gerð tegundar er ákvörðuð af fyrirtækinu. Ef engin tegund er fyrir tilfönginmun Finance and Operations fletta upp sjálfgefinni tegund á verð á klukkustund fyrir kostnað og tekjur.

### <a name="set-up-project-resource-and-role-characteristics"></a>Setja upp verk tilfanga og einkenni verks

Verkefnastjóri getur notað aðgerðir verktilfanga til að stofna hlutverk sem krafist er fyrir verkið. Hægt er að nota hlutverk þegar staðfest tilföng eru enn óþekkt við frátekt tilfanga. Hægt er að taka hlutverk tímabundið frá sem áætluð tilföng, svo hægt sé að halda áfram verkáætlun.

[![Dæmi um hlutverk](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Aðstæður:** Contoso var ráðinn til að ljúka við Tíma- og efnisverk sem hefur samþykkta skipulagsskrá verks. Undirverkefnastjóri er enn að ljúka við umfang verksins. Tilfangastjórnandi er sem stendur að auðkenna tiltekin tilföng sem eru frátekin til að vinna í hinu nýja verki. Vegna mikilvægis verkefnisins bað kostunaraðili verksins um Yfirverkefnastjóri í einu hlutverki. Stjórnandi tilfanga verður að fá nýtt tilfang og skilgreinir hlutverkið í kerfinu ef undirverkefnastjóri krefst tilfangaupplýsingar meðan á verkáætlun stendur.

Eftirfarandi skref sýna hvernig stjórnandi tilfanga getur sett upp hlutverkið Yfirverkefnastjóri og tengt eiginleika tilfanga við það. Síðar er hægt að nota hlutverkið til að leita að lausum tilföngum sem samsvara áskildri hæfni tilfangsins.

1. 'A **Uppsetning hlutverka** síðunni skal velja **Nýtt** og færa eftirfarandi gildi inn:

    - **Kenni hlutverks:** Yfirverkefnastjóri
    - **Lýsing:** Yfirverkefnastjóri

2. Velja **Stofna**.
3. Velja skal hlutverkið **Yfirverkefnastjóri** og veljið svo **Skilgreina einkenni**.
4. Í reitnum **Gerð einkenna** skal velja **Hæfni**.
5. Í reitnum **Tiltæk einkenni** skal færa inn færnina sem verið er að leita að.
6. Í reitnum **Gerð einkenna** skal velja **Réttindi**.
7. Í reitnum **Tiltæk einkenni** skal færa inn tegund réttinda sem verið er að leita að.

### <a name="assign-a-project-resource-to-a-project"></a>Úthlutið verktilföngum á verk

1. Á **Öll verk** síðunni skal velja verkið **XYZ Uppfærsla þrep 2**.
2. Á flipanum **Verkhópur og áætlun** skal velja **Bæta við**.
3. Á svæðinu **Hlutverk**, veljið **Meðlimur**.
4. Veljið **Bóka úr dagatali**.
5. Á síðunni **Forði til ráðstöfunar** er valið **Skoða stillingar**.
6. Á síðunni **Breyta stillingum yfirlits** skal færa inn eftirfarandi gildi:

    - **Snið fyrir dagsetningabil:** Dagur
    - **Birta lýsingar á framboði:** Já
    - **Sýna eftirstöðvar afkastagetu:** Já

7. Í lista yfir tilföng, velja tilfang.
8. Veljið **Bundin bókun** og **Full afkastageta**.


### <a name="assign-a-resource-to-a-default-role"></a>Tengja tilfang við sjálfgefið hlutverk

Til að aðstoða verkefnastjóra eða tilfangastjórnendur, er hægt að kafa frekar niður á tilföng sem má tengja við verk. Hægt er að tengja sjálfgefið hlutverk við fyrirliggjandi tilfang eða nýlega áunnið tilfang. Til dæmis þegar Daniel var ráðinn hafði hann reynslu og hæfni til að fylla hlutverk viðskiptagreinis. Stjórnandi tilfanga úthlutaði þessu hlutverki sem sjálfgefin hlutverk Daniels í fyrirtækinu. Þess vegna bætti stjórnandi tilfanga Daniel við hóp viðskiptagreina sem eru tiltækir til að vinna verk.

Meðan á frátekningu tilfanga stendur geta verkefnisstjórar síað hlutverkatilföng sem eru tiltæk til að vinna að verkum. Þeir geta notað þessar upplýsingar sem eitt skilyrði þegar þeir framkvæma ákvarðanagreiningu um mörg skilyrði við uppfyllingar tilfanga. Þeir get líka bætt öðrum eiginleika tilfanga við síuna til að leita að tilföngum sem hafa tiltekna hæfni, menntun og reynslu fyrir tiltekið verk.

**Dæmi:** Samþykkt verk er hafið og hlutverk Yfirverkefnastjóra var frátekið sem áætluð tilföng í verkáætlunarferlinu. Stjórnandi tilfanga hefur nú fengið tilfang til að uppfylla hlutverkið Yfirverkefnastjóri.

1. Í síðunni **Tilföng**, veljið **Daniel Goldschmidt**.
2. Á síðunni **Tilfangahlutverk** síðunni skal velja **Nýt** og færa eftirfarandi gildi inn:

    - **Gildistími:** Færið inn núgildandi dagsetningu.
    - **Lok gildistíma:** Færið inn **Aldrei**.
    - **Hlutverk:** Sláið inn **Yfirverkefnastjóri**.

3. Veljið **Vista** og lokið síðan skjámyndinni.
4. Á flipanum **Hæfni**, bæta við **ProjectMgmt** hæfni og **PMP** réttindum.

## <a name="set-up-role-based-pricing"></a>Uppsetning verðlagningar byggðri á hlutverkum
Hægt er að setja allan kostnað, söluverð og flutningsverð upp fyrir hlutverk.

1. Á **Söluverð (klukkustund)** síðunni skal velja **Nýtt** og slá inn gildisdagsetningu.
2. Í **Hlutverk** dálki skal velja hlutverk.
3. Í **Verðlagning** dálki skal slá inn verð fyrir valið tilfangahlutverk.

## <a name="form-a-project-team"></a>Búa til verkhóp
Til að nota hlutverk sem voru áður sett upp í verkefni verður verkefnastjóri að tengja hlutverk við verkið. Hægt er að tengja mörg hlutverk við verk. Finance and Operations merkir sjálfvirkt þessi hlutverk við frátekningu til að koma í veg fyrir misskilning. Til dæmis, ef verkefnastjóri krefst þriggja hugbúnaðarverkfræðinga eru þrjú hlutverk hugbúnaðarverkfræðinga sem eru merktir sem **hugbúnaðarverkfræðingur 1**, **hugbúnaðarverkfræðingur 2** og **hugbúnaðarverkfræðingur 3**, sjálfvirkt mynduð. Ef einkenni hlutverks hafa áður verið stillt fyrir hlutverkið, eru þau notuð sem sía við leit tilfanga. Hægt er að bæta frekari eiginleikum við sem þarf til að fínstilla leitina enn frekar.

Einnig er hægt að sérsníða skoðun á stillingum til að gefa betra yfirlit yfir tiltæk tilföng. Það eru valkostir til að sýna tiltæki eftir klukkustund, daglega, vikulega, mánaðarlega, ársfjórðungslega og árlega. Það er einnig valkostur að sýna tiltæka og eftirstandandi afkastagetu á tilföng. Þessi valkostur er gagnlegur fyrir tímastjórnun þegar verið er að meta tiltækan tíma fyrir verkþætti eða tiltæk tilföng.

Verkefnastjórinn getur valið hlutverk á síðunni og, séu tiltæk tilföng sem hentar þörfinni, valið að taka frá tilfang til að fylla hlutverkið. Athugið að ekki þarf að taka tilföng frá á þessum tíma meðan á áætlunarferli stendur. Þegar Sundurliðun verkþátta (WBS) er stofnað er hægt að skipta út hlutverk með mönnuðum tilföngum fyrir verkið. Ef hlutverkum er skipt út fyrir mönnuð tilföng í WBS, uppfærir uppsetning tilfanga sjálfkrafa skráningar og röðun í verkhópinn.

[![Verkhópur skráningar sem inniheldur bæði hlutverk og raunveruleg tilföng](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Verkefnastjórinn hefur mismunandi valkosti fyrir bókun tilfanga fyrir verk, eins og **Eftirstöðvar afkastagetu**, **Full afkastageta**, **Hlutfall Afkastagetu**, og **Tilgreina klukkustundir**. Hætta má við þessa bókunarvalkosti hvenær sem er ef úthlutun tilfanga breytist. Til eru tvær gerðir bókunar:

- **Bundin bókun** – Frátekning tilfanga var samþykkt og staðfest að vinna í úttekt fyrir tilgreinda tímalengd.
- **Óbundin bókun** – Frátekningar á tilföngum var með fyrirvara stillt á að vinna í úttekt fyrir tilgreinda tímalengd.

Notið eftirfarandi aðferðir til þess að stofna verkhóp.

### <a name="create-a-project-team"></a>Stofna verkhóp

1. Á listasíðunni **Öll verk** veldu verk og velja svo **Breyta**.
2. Á flipanum **Verkhópur Og áætlun**, á svæðinu **Áætluð lokadagsetning**, færið inn áætlaða upphafsdagsetningu plús einn mánuður. Til dæmis, ef áætluð upphafsdagsetning er 24. Júní, 2017 (24/06/2017), færa inn **24/07/2017**.
3. Veljið **Bæta við**.
4. Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk**, veljið **Yfirverkefnastjóri**.
5. Veljið **Áskilin hæfni**.
6. Á síðunni **Velja eiginleika**, eru þeir eiginleikar sem þú stilltir áður á hlutverk Yfirverkefnastjóra valdir sjálfkrafa. Veldu **Í lagi**.
7. Á síðunni **Bæta hlutverkum við verk**, í svæðinu **Fjöldi tilfanga** skal færa inn **1**.
8. Í svæðinu **Tilföng** sýnir uppfletting öll tilföng sem hafa áskilda hæfni. Velja **Daniel Goldschmidt**, og svo **Stofna**.
9. Á síðunni **Verk** síðunni er valið **Bæta við**.
10. Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk** veljið **Meðlimur**. Í svæðinu **Fjöldi tilfanga** skal slá inn **5**.
11. Velja **Stofna**.
12. Á síðunni **Verk** er valið **Uppfylla tilföng**.

## <a name="resource-capacity-synchronization"></a>Samstilling afkastagetu fyrir tilfangið
Vinnslur fyrir samstillingu tilfanga hjálpar til við að tryggja að upplýsingar fyrir dagatal og grunndagatal seytli niður í röðun tilfanga verks. Ef dagatali er breytt gera ferlin nauðsynlegar uppfærslur á áætlun tilfanga verks. Ferlin hjálpa einnig til með að bæta afköst, þar sem tilfangaupplýsingar á dagatalinu eru samstilltar fyrirfram. Því gerast uppfærslur á upplýsingum tilfanga hraðar. Mælt er með er skipuleggja ferlin sem runuvinnslu í stað þess að skipuleggja einn í einu. Annars er hætta á að einhver gleymi sameiginlegum dagsetningum þegar upplýsingarnar voru síðast samstilltar. Ef ekki eru notaðar sameiginlegar dagsetningar geta eyður komið fram við samstillingu á dagsetningu.

![Samstilling dagatals](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Samstilla tilfangagetu samantekta

Samstillingarferlið er hannað til að samstilla upplýsingar um öll dagatöl tilfanga. Þessar upplýsingar innihalda grunnupplýsingar dagatals um allar breytingar á Töflu yfir afkastagetu tilfangadagatals.verksins. Ef nýjum tilföngum er bætt við verkið, hjálpar samstilling við að tryggja að uppfærðu dagatalsupplýsingarnar séu tiltækar. Þessa samstillingu er hægt að gera hvenær sem er.

Mælt er með því að nota runuvinnslu. Valkostirnir er tiltækir í samstillingu frátekinnar afkastagetu.

1. Valið er **Verkefnastjórnun og bókhald** &gt; **Reglubundið** &gt; **Samstilling afkastagetu** &gt; **Samstilla afkastagetu samantekta**.
2. Stillið valkostina í eftirfarandi töflu.

    | Valkostur      | lýsing |
    |-------------|-------------|
    | Tímabilskóði | Einnig er hægt að velja kóða dagsetningabils í fjárhagi til að stilla upphafs og lokadag fyrir samstillingarferli fyrir tilfangagetu samantekta. |
    | Fyrsti vinnudagur  | Færa skal inn upphafsdag fyrir samstillingarferli fyrir tilfangagetu samantekta. |
    | Lokadagur    | Færa skal inn lokadag fyrir samstillingarferli fyrir tilfangagetu samantekta. |

[![Samstillingarferli](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Setja upp hlutverk á WBS-sniðmát
Verkefnisstjórar geta sett upp WBS-sniðmát sem hægt er að nota þegar þeir stofna WBS fyrir ný verk. Verkefnisstjórar geta bætt við hlutverkum þegar sniðmát er stofnað. Notið eftirfarandi ferli til að úthluta hlutverki til WBS-sniðmáts. 

1. Veljið **Verkefnastjórnun og bókhald** &gt; **Uppsetning** &gt; **Verk** &gt; **Sniðmát fyrir sundurliðun verkþátta**.
2. Veljið **Upplýsingar** fyrir valið WBS-sniðmát.
3. Velja verk í lista og síðan, í svæðinu **Hlutverk** skal velja hlutverk til að úthluta á verkefnið.

### <a name="work-with-a-wbs"></a>Vinna með WBS

Hægt er að stofna nýtt WBS eða afrita WBS úr fyrirliggjandi WBS-sniðmáti. Stjórnandi verks getur auðveldlega stjórnað tilföngum með því að úthluta hlutverkum á ný verk í WBS. Hægt er að skipta út hlutverkum eftir að tilfang er fengið eða eftir að staðfest tilfang sem á að vinna við verkið er auðkennt. Þessi sveigjanleika gerir verkefnisstjórum kleift að framkvæma eftirfarandi verkefni:

- Auðkennið fjölda tilfanga sem þarf fyrir WBS vinnupakka.
- Áætla kostnað verks.
- Stofna bráðabirgðafjárhagsáætlun.
- Meta tímalengd verkþáttar, sem byggir á hlutverkum og tilföngum.
- Þróa einhverjar verkstjórnunaráætlanir, byggt á upplýsingum um tiltæk verk.

Auka valkostum hefur verið bætt í WBS til að nýta betur virkni tilfanga.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valkostur</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Úthlutanir tilfanga</td>
<td>Skoða úthlutuð tilföng, dagsetningar, tímafjölda og bókunargerð fyrir verk í WBS.</td>
</tr>
<tr class="even">
<td>Mynda lið sjálfkrafa</td>
<td>Bæta við áætluðum tilföngum sjálfkrafa með því að nota hlutverk sem eru tengd verkefni. Finance and Operations stingur sjálfkrafa upp á áætluðum tilföngum með því að nota greiningu um ákvörðun um mörg skilyrði sem byggir á hlutverkum. Eftir að hlutverk og framlag (klukkustundir) hefur verið stillt fyrir verk í WBS og skipulag hefur verið losað skal velja <strong>Mynda lið sjálfkrafa</strong>. Áskildum fjölda áætlaðra tilfanga er bætt við WBS og flipann <strong>Áætlun Verks og hóps</strong>.</td>
</tr>
<tr class="odd">
<td>Tilföng (fellilisti)</td>
<td>Á síðunni <strong>Ræsa úthlutun tilfanga </strong>er hægt að velja tilföng í bundna bókun eða óbundna bókun, á grundvelli tilgreindrar tímalengdar. Hægt er að breyta stillingum yfirlits til að sjá og stilla tímalengd verkþátta tilfanga. Hægt er að velja og úthluta tilföngum á stigi pakkavinnu með eftirfarandi valkostum:
<ul>
<li><strong>Samþykkja</strong> -Staðfesta breytingar á tilföngum sem er úthlutað á verkefni.</li>
<li><strong>Hætta við</strong> -Hætta við breytingar á tilföngum sem er úthlutað á verkefni.</li>
<li><strong>Úthluta sjálfkrafa</strong> – Þessi valkostur velur tiltæk mönnuð tilföng með samsvarandi hlutverki og úthlutar á valið verk.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Á **Öll verk** síðunni skal velja verkið **XYZ Uppfærsla þrep 2**.
2. Veljið **Áætlun** &gt; **Aðgerðir** &gt; **Sundurliðun verkþátta**.
3. Veljið **Nýtt** til að bæta eftirfarandi verkþætti af stigi eitt við WBS:

    - Verið er að hefja
    - Áætlun
    - Í gangi
    - Eftirlit og stjórn
    - Lok

4. Setja upp dagsetningar og framlag (klukkustundir), eins og sýnt er á eftirfarandi mynd.

    [![Stilla dagsetningar og framlag](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Veljið verklínuna **Hefja** og síðan, í svæðinu **Hlutverk**, veljið **Yfirverkefnastjóri**.
6. Velja **Birta**.
7. Í sömu línu í svæðinu **Tilfang**, veljið **Daniel Goldschmidt** og svo **Samþykkja**.
8. Veljið verklínuna **Áætlanagerð** og síðan, í svæðinu **Hlutverk** veljið **Viðskiptagreinir**.
9. Veljið **Birta**, og smellið síðan á **Mynda lið sjálfkrafa**.
10. Smellt er á **Já** í glugganum sem birtist.
11. Í svæðinu **Tilfang** skal staðfesta að gildið sé **Viðskiptagreinir 1**.
12. Fyrir tilfangið **Viðskiptagreinir 1**, opnið uppflettingu og veljið **Ræsa skjámynd úthlutana**. Til að velja starfskraft fyrir verkið.
13. Veljið **Óbundnar úthlutanir** &gt; **Full afkastageta**.

    > [!NOTE] 
    > Það berst ekki viðvörun um að tilgreind viðföng séu nú 2, þar sem fjöldi tilfanga helst 1.

14. Á síðunni **Sundurliðun Verkþátta** skal staðfesta úthlutun tilfanga á WBS og velja svo **Vista**.

## <a name="resource-fulfillment-for-planned-resources"></a>Uppfylling tilfanga fyrir áætluð tilföng
Verkefnastjóri getur áætlað áskilið tilfangahlutverk  við verkið. Stjórnandi tilfanga sér þessi áætluðu tilföng sem beiðnir á síðunni **Uppfyllingar Tilfanga** og getur úthlutað raunverulegum tilföngum.

1. Á **Öll verk** síðunni skal velja verkið **XYZ Uppfærsla þrep 2**.
2. Veljið **Verk** og svo **Breyta**.
3. Á flipanum **Verkhópur og áætlun** skal velja **Bæta við**.
4. Í svarglugganum **Bæta við hlutverkum** veljið hlutverkið **Forritari**.
5. Veljið **Stofna** og lokið svo verksíðunni.
6. Á síðunni **Uppfylling tilfanga** skal velja **Forritari 1** fyrir verkið **XYZ Uppfærsla verks þrep 2**.
7. Veljið starfskraft og svo **Úthluta**.
8. Staðfesta að lína fyrir **Forritara 1** hefur verið fjarlægð fyrir verkið **XYZ Uppfærslu verks þrep 2**.
9. Á flipanum **Verkhópur Og áætlun** fyrir verkið **XYZ Uppfærsla þrep 2**, skal staðfesta að starfsmanni sem valinn var í fyrra þrepi hefur verið bætt við sem **Forritara**.

## <a name="requests-for-project-resources"></a>Beiðnir um verktilföng
Virknin fyrir röðun verktilfanga styður aðeins stjórnendur tilfanga til að dreifa mönnuðum tilföngum á úttektir eða verk. Til að virkja þennan eiginleika skal ljúka eftirfarandi verkum eða að staðfesta að þeim sé lokið:

- Setja upp númeraraðir.
- Setja upp verkflæði fyrir verkefnastjórnun og bókhald
- Virkja verkflæði tilfangabeiðni.

Eftir að fyrri verkefnum hefur verið lokið er hægt að ljúka eftirfarandi verkefnum eftir þörfum:

- Stofna beiðni tilfanga úr óbundið mönnuðum tilföngum.
- Fylgjast með tilfangabeiðnum.
- Uppfylla tilfangabeiðnir.
- Biðja um mönnuð tilföng úr WBS.
- Bóka tilföng á verk án þess að þurfa að biðja um mönnuð tilföng.

## <a name="monitor-project-teams"></a>Fylgjast með verkhópum
1. Á síðunni **Öll verk** skal velja **Verkkenni** tengilinn fyrir verkið **XYZ uppfærsla þrep 2** project.
2. Á flýtiflipanum **Verkhópur og áætlun** sakl ganga úr skugga um að tilföng verks sem eru talin upp séu rétt.

