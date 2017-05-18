---
title: "Tilföng verks"
description: "Þessi efnisatriði gefur upplýsingar um tilföng verka."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 11755e4ab4b3c1f55da80e57ff96e0b13c84c697
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="project-resourcing"></a>Tilföng verks

[!include[banner](../includes/banner.md)]


Þessi efnisatriði gefur upplýsingar um tilföng verka.

Ein áskorun fyrir verkefnastjóra og forðastjóra meðan á áætlunargerð stendur er forðaúthlutun, þar sem þeir þurfa að ákvarða og taka frá rétt tilföng til vinnu á verk. Í Microsoft Dynamics 365 for Operations gerir tilfangageta verkefna kleift að skilgreina hlutverk sem eru meðhöndluð sem tímabundin tilföng sem hægt er að taka frá fyrir sérstaka úttekt eða sem hluta af úttekt. Þessi tegund tilfanga gerir verkefnisstjórum og stjórnendum tilfanga kleift að ljúka eftirfarandi verkum:

-   Skilgreina hlutverk sem hefur nauðsynlega hæfni til að gera auðvelt að samsvara tilföng.
-   Nota hlutverk til að skilgreina upphaflega úttekt sem er byggð á fráteknum tilföngum.
-   Gera kostnaðarmat og ákvarða upphaflega fjárhagsáætlun, byggt á úthlutuðum hlutverkum og tilföngum fyrir verk.
-   Hlutverk eru notuð til að áætla fjölda úttekta tilfanga sem krafist er fyrir hverja úttekt.
-   Áætla fjölda tilfanga sem krafist er fyrir allan líftíma verksins.
-   Gera drög að sundurliðun verkþátta (WBS) með því að nota upphaflega tilfangaúthlutun.

[![Líftími afurðar](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Eftir því sem áætlunargerð er haldið áfram, er hægt að skipta út áætluðum tilföngum fyrir mönnuð tilföng. Verkefnisstjóri getur einnig farið til baka og uppfært tilfangafrátektir á öllum verkstigum.

## <a name="set-up-project-resources"></a>Setja upp verktilföng.
Þú þarft að setja upp dagatal og tengja það við starfsmann eða starfskraft. Dagatalið er notað til að áætla verkið og vinnutíma þeirra tilfanga sem eru frátekin fyrir verkið. Við uppsetningu dagatals geta verkefnisstjórar framkvæmt sléttun á tilföngum sem hluta af fínstillingu tilfanga. Samkvæmt áætlun dagatals geta takmarkanir verið settar á tilföng. Hægt er að setja upp dagatal sem á síðunni **Dagatöl**. 

Þegar starfsmaður er settur upp sem tilföng verks er hægt að velja úr starfsmönnum sem vinna í fyrirtækinu þar sem verið er að setja upp tilföng eða hægt er að velja starfsmenn úr öðrum fyrirtækjum innan fyrirtækisins. Þetta eru samstæðutilföng. Eftirfarandi ferli útskýra hvernig setja á upp starfsmanns sem tilföng verks innan fyrirtækisins og hvernig á að setja upp samstæðuverk tilfanga.

### <a name="set-up-a-worker-as-a-project-resource"></a>Setja upp starfmann sem verktilfang.

1.  Á síðunni **Starfsmenn**, í listanum **Starfsfólk**, veljið starfsmann sem verið er að bæta við sem tilfang verks og opnið skrá starfsmannsins.
2.  Á Aðgerðasvæðinu skal smella á **Verk** &gt; **Uppsetning** &gt; **Verkuppsetning**.
3.  Velja skal Dagatal og loka svo síðunni.

Einnig er hægt að tilgreina sjálfgefið verk fyrir tilföng sem gerð áætlaðs verkefnis. Hægt er að nota áætlaðar úthlutanir þegar tilfangastjórnandi eða verkstjóri veit hvaða verk tilfangið verður að vinna að fyrirfram. Einnig er hægt að byggja áætlaðar úthlutanir á beiðni kostunaraðila verks eða viðskiptavinar. Til að úthluta verki fyrirfram: Á síðunni **Úthluta verkum**, á flipanum **Verk**, á listanum **Eftirstandandi verk** skal velja viðeigandi verk.

### <a name="set-up-an-intercompany-resource"></a>Setja upp samstæðutilföng

Þegar starfsmaður er settur upp sem samstæðutilföng verður að ljúka uppsetningunni í útlánafyrirtækinu og lántökufyrirtækisinu. 

**Í útlánafyrirtækinu:**

1.  Í Dynamics 365 for Operations, staðfesta að útlánafyrirtækið sé valið, og ljúka síðan ferlinu hér að framan, "Setja upp starfsmann sem tilfang verks".
2.  Fara í ** Fjárhag **&gt; ** Bókunaruppsetning **&gt;**Samstæðubókhald**. Smellt er á **Nýtt**.
3.  Í svæðinu ** Kenni lögaðila ** skal velja útlánafyrirtæki. Fyllið út eftirstandandi svæði eftir þörfum og smellið síðan á **Vista**.
4.  Farið í **Verkefnastjórnun og bókhald **&gt; **Uppsetning **&gt;**Verðlag ** &gt; **Flutningsverð**** **.
5.  Í skjámyndinni ** flutningsverð ** er smellt á **Nýtt**, og í svæðinu ** Lögaðili sem fær Lánað ** skal velja viðeigandi fyrirtæki.
6.  Ef þú vilt aðeins lána lántökufyrirtækinu þau tilföng sem voru stofnuð í upphafi þessa hluta í svæðinu **Tilföng** skal velja nafn tilfanganna sem voru stofnuð. Ef óskað er að gera öll tilföng í fyrirtækinu tiltæk lántökufyrirtæki skal skilja svæðið ** Tilföng ** eftir autt.
7.  Fara í ** Verkefnastjórnun og bókhald **&gt; ** Uppsetningu **&gt;**Verkefnastjórnun og bókhaldsfæribreytur**, og á flipanum ** Samstæðu ** skal stilla svæðið ** Virkja samstæðuröðun tilfanga og tímablöð ** á **Já**.

**Í lántökufyrirtækinu:**

1.  Fara skal í **Verkefnastjórnun og bókhald** &gt; **Verktilföng** &gt; **Tilfangalisti**.
2.  Í leitarsíu færið inn heiti tilfanga sem þú stofnaðir í fyrra ferli fyrir útlánafyrirtækið til að staðfesta að heitið sé innifalið í lista yfir tilföng lántökufyrirtækis.

## <a name="manage-resource-competencies"></a>Umsjón með hæfni tilfanga
Skilgreiningar á hæfni tilfanga eru mikilvægur hluti af stjórnun tilfanga. Hæfni er hægt að nota sem grunnlínu til að ákvarða tilföng sem eru með rétt jafnvægi hvað varðar hæfni, menntun, réttindi og verkreynslu. Rétt er að setja þessar upplýsingar upp fyrir hvert tilfang og uppfæra þær reglulega. Á þennan hátt er hægt að hámarka getu þegar tiltekin hæfni tilfanga er borin saman við úthlutun verks til tilfanga. [![Dæmi um hæfni, réttindi, menntun og verkreynslu](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Eftirfarandi aðgerðir útskýra hvernig á að setja upp ákveðna hæfni fyrir tilfang. 

Til að setja upp hæfni starfsmanns, er hægt að nota annað hvort listasíðuna **Starfsmenn** í Mannauði eða listasíðuna **Tilföng** í Verkefnastjórnun og bókhald. Fyrir eftirfarandi ferla notum við listasíðuna **Starfsmenn** í Mannauði.

### <a name="set-up-competencies-certificates"></a>Setja upp hæfni: Réttindi

1.  Á listasíðunni **Starfsmenn** veljið línu þess starfsmanns sem verið er að bæta við upplýsingum um réttindi fyrir.
2.  Í Aðgerðasvæði, á flipanum **Starfsmaður** í flokknum **Hæfni** er smellt á **Réttindi**.
3.  Smellt er á **Nýtt**.
4.  Í svæðinu **Tegund réttinda**, veljið **PMP**.
5.  Í svæðinu **Upphafsdagsetning**, veljið **1/10/2015**.
6.  Smellið á **Vista** og lokið síðan skjámyndinni.

### <a name="set-up-competencies-skills"></a>Setja upp hæfni: Færni

1.  Á listasíðunni **Starfsmenn** skal tryggja að starfsmaðurinn sem notaður var í fyrra ferli sé enn valinn. Í Aðgerðasvæði, á flipanum **Starfsmaður** í flokknum **Hæfni** er smellt á **Færni**.
2.  Smellt er á **Nýtt**.
3.  Á svæðinu **Færni** skal velja **Verkefnastjórnun**.
4.  Á svæðinu **Stig** skal velja **5 Expert**.
5.  Á svæðinu **Dagsetning stigs**, veljið **14/1/2014**.
6.  Á svæðinu **Reynsla í árum** færið inn **10**.
7.  Smellið á **Vista** og lokið síðan skjámyndinni.

## <a name="create-a-new-project"></a>Stofna nýtt verk
1.  Smellt er á **Verkefnastjórnun og bókhald** &gt; **Vinnusvæði** &gt; **Verkefnastjórnun**.
2.  Smelltu á **Nýtt verk** og færðu síðan eftirfarandi gildi inn:
    -   **Gerð verks** - Tími og efni
    -   **Verkheiti** - XYZ Uppfærsla þrep 2
    -   **Verkflokkur** - TM\_VÍV
    -   **Auðkenni verksamnings**  - 00000002
3.  Smella á **Stofna verk**.

### <a name="assign-a-resource-to-a-project"></a>Úthluta tilfangi á verk

1.  Smellt er á **Mannauður** &gt; **Starfsmenn** &gt; **Starfsmenn**.
2.  Í listanum **Starfsmenn**, skal velja skrá starfsmanns sem hefur áður verið sett upp hæfni fyrir og opna skrá starfsmanns.
3.  Á Aðgerðarrúðunni, á flipanum **Verk** í flokkinum **Uppsetning** smellið á **Úthluta verkum**.
4.  Á síðunni **Úthlutanir villuleitartegundar tilfanga** er smellt á flipann **Verk**.
5.  Í síunni **Bæta verki við valin verk**, afmarkið verkið, XYZ Uppfærsla þrep 2
6.  Í rúðunni **Eftirstandandi verk**, veljið verk og smellið síðan á ör til að bæta því við í **Valin verk** rúðunni.
7.  Lokið síðunni.

Ef þörf krefur, er einnig hægt að úthluta tegundum fyrir tilföng. Gerð tegundar er annað hvort Kostnaður eða Tekjur. Þetta er ákvarðað af fyrirtækinu. Ef engar úthlutaðar tegundir eru fyrir tilföngin mun Dynamics 365 for Operations fletta upp sjálfgefinni tegund á verð á klukkustund fyrir kostnað og tekjur.

### <a name="set-up-project-resource-and-role-characteristics"></a>Setja upp verk tilfanga og einkenni verks

Verkefnastjóri getur notað aðgerðir verktilfanga til að stofna hlutverk sem krafist er fyrir verkið. Hægt er að nota hlutverk þegar staðfest tilföng eru enn óþekkt við frátekt tilfanga. Hægt er að taka hlutverk tímabundið frá sem áætluð tilföng, svo hægt sé að halda áfram verkáætlun. 

[![Dæmi um hlutverk](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Aðstæður:** Contoso var ráðinn til að ljúka við Tíma- og efnisverk sem hefur samþykkta skipulagsskrá verks. Undirverkefnastjóri er enn að ljúka við umfang verksins. Tilfangastjórnandi er sem stendur að auðkenna tiltekin tilföng sem eru frátekin til að vinna í hinu nýja verki. Eitt hlutverk sem var umbeðið af kostunaraðila verksins, vegna mikilvægs eðlis verksins, var Yfirverkefnastjóri. Stjórnandi tilfanga verður að fá nýtt tilfang og skilgreinir hlutverkið í kerfinu ef undirverkefnastjóri krefst tilfangaupplýsingar meðan á verkáætlun stendur. 

Eftirfarandi skref sýna hvernig stjórnandi tilfanga getur sett upp hlutverkið Yfirverkefnastjóri og tengt eiginleika tilfanga við það. Síðar er hægt að nota hlutverkið til að leita að lausum tilföngum sem samsvara áskildri hæfni tilfangsins.

1.  Smellt er á **Verkefnastjórnun og bókhald** &gt; **Setja upp** &gt; **Tilföng** &gt; **Uppsetning hlutverka**.
2.  Smelltu á **Nýtt** og færðu síðan eftirfarandi gildi inn:
    -   **Kenni hlutverks** - Yfirverkefnastjóri
    -   **Lýsing:** - Yfirverkefnastjóri
3.  Smellið á **Stofna**.
4.  Velja skal hlutverkið **Yfirverkefnastjóri** og smellið svo á **Skilgreina einkenni**.
5.  Í reitnum **Gerð einkenna** skal velja **Hæfni**.
6.  Í reitnum **Tiltæk einkenni** skal færa inn hæfni sem verið er að leita að.
7.  Í reitnum **Gerð einkenna** skal velja **Réttindi**.
8.  Í reitnum **Tiltæk einkenni** skal færa inn tegund réttinda sem verið er að leita að.
9.  Smellið á **OK** og lokið síðunni.

### <a name="assign-a-project-resource-to-a-project"></a>Úthlutið verktilföngum á verk

1.  Smellið á **Verkefnastjórnun og bókhald** &gt; **Algengt** &gt; **Verk** &gt; **Öll verk** og opnið verkið **XYZ Uppfærsla þrep 2**.
2.  Á flipanum **Verkhópur og áætlun**, smellið á **Bæta við**.
3.  Á svæðinu **Hlutverk**, veljið **Meðlimur**.
4.  Smellið á **Bóka úr dagatali**.
5.  Á síðunni **Tilföng til ráðstöfunar** er smellt á **Skoða stillingar**.
6.  Á síðunni **Breyta stillingum yfirlits** skal færa inn eftirfarandi gildi:
    -   **Snið fyrir dagsetningabil** - Dagur
    -   **Birta lýsingar á framboði** - Já
    -   **Sýna eftirstöðvar afkastagetu** - Já
7.  Í lista yfir tilföng, velja tilfang.
8.  Smellið á **Bundin bókun** &gt; **Full afkastageta**.
9.  Lokið síðunni.

### <a name="assign-a-resource-to-a-default-role"></a>Tengja tilfang við sjálfgefið hlutverk

Til að aðstoða verkefnastjóra eða tilfangastjórnendur, er hægt að kafa frekar niður á tilföng sem má tengja við verk. Hægt er að tengja sjálfgefið hlutverk við fyrirliggjandi tilfang eða nýlega áunnið tilfang. Til dæmis þegar Daniel var ráðinn hafði hann reynslu og hæfni til að fylla hlutverk viðskiptagreinis. Stjórnandi tilfanga úthlutaði þessu hlutverki sem sjálfgefin hlutverk Daniels í fyrirtækinu. Þess vegna bætti stjórnandi tilfanga Daniel við hóp viðskiptagreina sem eru tiltækir til að vinna verk. 

Meðan á frátekningu tilfanga stendur geta verkefnisstjórar síað hlutverkatilföng sem eru tiltæk til að vinna að verkum. Þeir geta notað þessar upplýsingar sem eitt skilyrði þegar þeir framkvæma ákvarðanagreiningu um mörg skilyrði við uppfyllingar tilfanga. Þeir get líka bætt öðrum eiginleika tilfanga við síuna til að leita að tilföngum sem hafa tiltekna hæfni, menntun og reynslu fyrir tiltekið verk. 

**Dæmi:** Samþykkt verk er hafið og hlutverk Yfirverkefnastjóra var frátekið sem áætluð tilföng í verkáætlunarferlinu. Stjórnandi tilfanga hefur nú fengið tilfang til að uppfylla hlutverkið Yfirverkefnastjóri.

1.  Smellt er á **Verkefnastjórnun og bókhald** &gt; **Tilföng Verks** &gt; **Tilfangalisti**.
2.  Í listanum **Tilföng**, veljið **Daniel Goldschmidt**.
3.  Smellt er á **Verktilfang** &gt; **Vinna með** &gt; **Tilfangahlutverk**.
4.  Smelltu á **Nýtt** og færðu síðan eftirfarandi gildi inn:
    -   **Gildir frá** - (Núgildandi dagsetning)
    -   **Lok gildistíma** - Aldrei
    -   **Hlutverk** - Yfirverkefnastjóri
5.  Smellið á **Vista** og lokið síðan skjámyndinni.
6.  Á flipanum **Hæfni**, bæta við **ProjectMgmt** hæfni og **PMP** réttindum.

## <a name="set-up-role-based-pricing"></a>Uppsetning verðlagningar byggðri á hlutverkum
Hægt er að setja allan kostnað, söluverð og flutningsverð upp fyrir hlutverk.

1.  Smellt er á **Verkefnastjórnun og bókhald** &gt; **Setja upp** &gt; **Verð** &gt; **Söluverð (klukkustund)**.
2.  Smellt er á **Nýtt**.
3.  Tilgreina gildisdagsetningu.
4.  Í **Hlutverk** dálki skal velja hlutverk.
5.  Í **Verðlagning** dálki skal slá inn verð fyrir valið tilfangahlutverk.

## <a name="form-a-project-team"></a>Búa til verkhóp
Til að nota hlutverk sem voru áður sett upp í verkefni verður verkefnastjóri að tengja hlutverk við verkið. Hægt er að tengja mörg hlutverk við verk og Dynamics 365 for Operations merkir sjálfvirkt þessi hlutverk við frátekningu til að koma í veg fyrir misskilning. Til dæmis, ef verkefnastjóri krefst þriggja hugbúnaðarverkfræðinga eru þrjú hlutverk hugbúnaðarverkfræðinga sem eru merktir sem hugbúnaðarverkfræðingur 1, hugbúnaðarverkfræðingur 2 og hugbúnaðarverkfræðingur 3, sjálfvirkt mynduð. Ef einkenni hlutverks hafa áður verið stillt fyrir hlutverkið, eru þau notuð sem sía við leit tilfanga. Hægt er að bæta frekari eiginleikum við sem þarf til að fínstilla leitina enn frekar. 

Einnig er hægt að sérsníða skoðun á stillingum til að gefa betra yfirlit yfir tiltæk tilföng. Það eru valkostir til að sýna tiltæki eftir klukkustund, daglega, vikulega, mánaðarlega, ársfjórðungslega og árlega. Það er einnig valkostur að sýna tiltæka og eftirstandandi afkastagetu á tilföng. Þessi valkostur er gagnleg fyrir tímastjórnun þegar verið er að meta tiltækan tíma fyrir verkþætti eða tiltæk tilföng. 

Verkefnastjórinn getur valið hlutverk á síðunni og, séu tiltæk tilföng sem hentar þörfinni, valið að taka frá tilfang til að fylla hlutverkið. Athugið að ekki þarf að taka tilföng frá á þessum tíma meðan á áætlunarferli stendur. Þegar Sundurliðun verkþátta (WBS) er stofnað er hægt að skipta út hlutverk með mönnuðum tilföngum fyrir verkið. Ef hlutverkum er skipt út fyrir mönnuð tilföng í WBS, uppfærir uppsetning tilfanga sjálfkrafa skráningar og röðun í verkhópinn. 

[![Verkhópur skráningar sem inniheldur bæði hlutverk og raunveruleg tilföng](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Verkefnastjórinn hefur mismunandi valkosti fyrir bókun tilfanga fyrir verk, eins og **Eftirstöðvar afkastagetu**, **Full afkastageta**, **Hlutfall Afkastagetu**, og **Tilgreina klukkustundir**. Hætta má við þessa bókunarvalkosti hvenær sem er ef úthlutun tilfanga breytist. Til eru tvær gerðir bókunar:

-   **Bundin bókun** – Frátekning tilfanga var samþykkt og staðfest að vinna í úttekt fyrir tilgreinda tímalengd.
-   **Óbundin bókun** – Frátekningar á tilföngum var með fyrirvara stillt á að vinna í úttekt fyrir tilgreinda tímalengd.

Notið eftirfarandi aðferðir til þess að stofna verkhóp.

### <a name="create-a-project-team"></a>Stofna verkhóp

1.  Á listasíðunni **Öll verk** veldu verk og smellið síðan á **Breyta**.
2.  Á flipanum **Verkhópur Og áætlun**, á svæðinu **Áætluð lokadagsetning**, færið inn áætlaða upphafsdagsetningu plús einn mánuður. Til dæmis, ef áætluð upphafsdagsetning er 24. Júní, 2017 (24/06/2017), færa inn **24/07/2017**.
3.  Smellið á **Bæta við**.
4.  Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk**, veljið **Yfirverkefnastjóri**.
5.  Smellið á **Áskilin hæfni**.
6.  Á síðunni **Velja eiginleika**, eru þeir eiginleikar sem þú stilltir áður á hlutverk Yfirverkefnastjóra valdir sjálfkrafa. Smelltu á **Í lagi**.
7.  Á síðunni **Bæta hlutverkum við verk**, í svæðinu **Fjöldi tilfanga** skal færa inn **1**.
8.  Í svæðinu **Tilföng** sýnir uppfletting öll tilföng sem hafa áskilda hæfni. Velja **Daniel Goldschmidt**, og smellið síðan á **Stofna**.
9.  Á síðunni **Verk** síðunni er smellt á **Bæta við**.
10. Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk** veljið **Meðlimur**. Í svæðinu **Fjöldi tilfanga** skal slá inn **5**.
11. Smellið á **Stofna**.
12. Á síðunni **Verk** er smellt á **Uppfylla tilföng**.

## <a name="resource-capacity-synchronization"></a>Samstilling afkastagetu fyrir tilfangið
Vinnslur fyrir samstillingu tilfanga hjálpar til við að tryggja að upplýsingar í dagatali og grunndagatali seytli niður í röðun tilfanga verks. Ef dagatali er breytt gera ferlin nauðsynlegar uppfærslur á áætlun tilfanga verks. Ferlin hjálpa einnig til með að bæta afköst, þar sem tilfangaupplýsingar á dagatalinu eru samstilltar fyrirfram, þannig að uppfærslur á upplýsingum tilfanga gerast hraðar. Mælt er með er skipuleggja ferlin sem runuvinnslu í stað þess að skipuleggja einn í einu. Annars er hætta á að einhver gleymi sameiginlegum dagsetningum þegar upplýsingarnar voru síðast samstilltar. Ef ekki eru notaðar sameiginlegar dagsetningar geta eyður komið fram við samstillingu á dagsetningu.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Samstilling dagatals](./media/projectresourcing04-1024x471.jpg)

**Samstilla tilfangagetu samantekta**

Samstillingarferlið er hannað til að samstilla upplýsingar um öll dagatöl tilfanga. Þessar upplýsingar innihalda grunnupplýsingar dagatals um allar breytingar á Töflu yfir afkastagetu tilfangadagatals.verksins. Ef nýjum tilföngum er bætt við verkið, hjálpar samstilling við að tryggja að uppfærðu dagatalsupplýsingarnar séu tiltækar. Þessa samstillingu er hægt að gera hvenær sem er. 

Mælt er með því að nota runuvinnslu. Valkostirnir eru tiltækar í samstillingu frátekinnar afkastagetu.

-   Smellt er á **Verkefnastjórnun og bókhald** &gt; **Reglubundið** &gt; **Samstilling afkastagetu** &gt; **Samstilla afkastagetu samantekta**.

| Valkostur | lýsing                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Já    | Samstilla öll tilfangagögn við dagatal og upplýsingar um grunndagatal og skrifa yfir allar upplýsingar í dagatali afkastagetu tilfanga í verkinu.                                                  |
| Nei     | Samstilla tilfangagögnin, samkvæmt tímabilskóðanum og tilgreindum upphafs- og lokadagsetningum. Þessi valkostur fjarlægir ekki fyrirliggjandi gögn og uppfærir upplýsingar aðeins fyrir nýlega viðbætt tilföng. |

[![Samstillingarferli](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Setja upp hlutverk á WBS-sniðmát
Verkefnisstjórar geta sett upp WBS-sniðmát sem hægt er að nota þegar þeir stofna WBS fyrir ný verk. Verkefnisstjórar geta bætt við hlutverkum þegar sniðmát er stofnað. Notið eftirfarandi ferli til að úthluta hlutverki til WBS-sniðmáts.** **

1.  Smellt er á **Verkefnastjórnun og bókhald** &gt; **Uppsetning** &gt; **Verk** &gt; **Sniðmát fyrir sundurliðun verkþátta**.
2.  Smellt er á **Upplýsingar** fyrir valið WBS-sniðmát.
3.  Velja verk í lista og síðan, í svæðinu **Hlutverk** skal velja hlutverk til að úthluta á verkefnið.

### <a name="work-with-a-wbs"></a>Vinna með WBS

Hægt er að stofna nýtt WBS eða afrita WBS úr fyrirliggjandi WBS-sniðmáti. Stjórnandi verks getur auðveldlega stjórnað tilföngum með því að úthluta hlutverkum á ný verk í WBS. Hægt er að skipta út hlutverkum eftir að tilfang er fengið, eða eftir að staðfest tilfang sem á að vinna við verkið er auðkennt. Þessi sveigjanleika gerir verkefnisstjórum kleift að framkvæma eftirfarandi verkefni:

-   Auðkennið fjölda tilfanga sem þarf fyrir WBS vinnupakka.
-   Áætla kostnað verks.
-   Stofna bráðabirgðafjárhagsáætlun.
-   Meta tímalengd verkþáttar, sem byggir á hlutverkum og tilföngum.
-   Þróa einhverjar verkstjórnunaráætlanir, byggt á upplýsingum um tiltæk verk.

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
<td>Bæta við áætluðum tilföngum sjálfkrafa með því að nota hlutverk sem eru tengd verkefni. Dynamics 365 for Operations stingur sjálfkrafa upp á áætluðum tilföngum með því að nota greiningu um ákvörðun um mörg skilyrði sem byggir á hlutverkum. Eftir að hlutverk og framlag (klukkustundir) hefur verið stillt fyrir verk í WBS og skipulag hefur verið losað er smellt á <strong>Búa Sjálfkrafa til hóp</strong>. Áskildum fjölda áætlaðra tilfanga er bætt við WBS og flipann <strong>Áætlun Verks og hóps</strong>.</td>
</tr>
<tr class="odd">
<td>Tilföng (fellilisti)</td>
<td>Á síðunni <strong>Ræsa úthlutun tilfanga </strong>er hægt að velja tilföng í bundna bókun eða óbundna bókun, á grundvelli tilgreindrar tímalengdar. Hægt er að breyta stillingum yfirlits til að sjá og stilla tímalengd verkþátta tilfanga. Hægt er að velja og úthluta tilföngum á stigi pakkavinnu með eftirfarandi valkostum:
<ul>
<li><strong>Samþykkja</strong> -Staðfesta breytingar á tilföngum sem er úthlutað á verkefni.</li>
<li><strong>Hætta við</strong> -Hætta við breytingar á tilföngum sem er úthlutað á verkefni.</li>
<li><strong>Úthluta sjálfkrafa</strong> – Þessi valkostur velur tiltæk mönnuð tilföng með samsvarandi hlutverki á valið verk.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Farið í **Verkefnastjórnun og bókhald** &gt; **Verkefni** &gt; **Öll verkefni**.
2.  Á listanum, veljið verkið **XYZ Uppfærsla þrep 2**.
3.  Smellið á **Áætlun** &gt; **Aðgerðir** &gt; **Sundurliðun verkþátta**.
4.  Smellið á **Nýtt** til að bæta eftirfarandi verkþætti af stigi eitt við WBS:
    -   Verið er að hefja
    -   Áætlun
    -   Í gangi
    -   Eftirlit og stjórn
    -   Loka

5.  Setja upp dagsetningar og framlag (klukkustundir), eins og sýnt er í eftirfarandi skjáskoti.[![Stilla dagsetningar og framlag](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Veljið verklínuna **Hefja** og síðan, í svæðinu **Hlutverk**, veljið **Yfirverkefnastjóri**.
7.  Smelltu á **Birta**.
8.  Í sömu línu í svæðinu **Tilfang**, veljið **Daniel Goldschmidt**.
9.  Smellið á **Samþykkja**.
10. Veljið verklínuna **Áætlanagerð** og síðan, í svæðinu **Hlutverk** veljið **Viðskiptagreinir**.
11. Smelltu á **Birta**, og smellið síðan á **Búa Sjálfkrafa til hóp**.
12. Í svarglugganum sem birtist smellirðu á **Já**.
13. Í svæðinu **Tilfang** skal staðfesta að gildið sé **Viðskiptagreinir 1**.
14. Fyrir tilfangið **Viðskiptagreinir 1**, opnið uppflettingu og smellið á **Ræsa skjámynd úthlutana tilfanga**.
15. Velja starfsmann fyrir verkið.
16. Smellið á **Óbundnar úthlutanir** &gt; **Full afkastageta**.
17. Smellið á **Vista** og lokið síðan skjámyndinni. 

> [!NOTE] 
> Það berst ekki viðvörun um að tilgreind viðföng séu nú 2, þar sem fjöldi tilfanga helst í 1.
18. Á síðunni **Sundurliðun Verkþátta** skal staðfesta úthlutun tilfanga á WBS og smellið síðan á **Vista**.

## <a name="resource-fulfillment-for-planned-resources"></a>Uppfylling tilfanga fyrir áætluð tilföng
Verkefnastjóri getur áætlað áskilið tilfangahlutverk  við verkið. Stjórnandi tilfanga sér þessi áætluðu tilföng sem beiðnir á síðunni **Uppfyllingar Tilfanga** og getur úthlutað raunverulegum tilföngum.

1.  Farið í **Verkefnastjórnun og bókhald** &gt; **Verkefni** &gt; **Öll verkefni**.
2.  Á listanum, veljið verkið **XYZ Uppfærsla þrep 2**.
3.  Smellið á **Verk**.
4.  Smellið á **Breyta**.
5.  Á flipanum **Verkhópur og áætlun**, ** **smellið á **Bæta við**.
6.  Í svarglugganum **Bæta við hlutverkum** veljið hlutverkið **Forritari**.
7.  Smellið á **Stofna**.
8.  Lokið verksíðunni.
9.  Smellið á **Verkefnastjórnun og bókhald** &gt; **Tilföng verks** &gt; **Uppfylling tilfanga**.
10. Veljið **Forritari 1** fyrir verkið **XYZ Uppfærsla verks þrep 2**.
11. Veljið notanda og smellið á **Úthluta**.
12. Staðfesta að lína fyrir **Forritara 1** hefur verið fjarlægð fyrir verkið **XYZ Uppfærslu verks þrep 2**.
13. Á flipanum **Verkhópur Og áætlun** fyrir verkið **XYZ Uppfærsla þrep 2**, skal staðfesta að starfsmanni sem valinn var í þrepi 11 hefur verið bætt við sem **Forritara**.

## <a name="requests-for-project-resources"></a>Beiðnir um verktilföng
Virknin Röðun verktilfanga styður aðeins stjórnendur tilfanga til að dreifa mönnuðum tilföngum á úttektir eða verk. Til að virkja þennan eiginleika skal ljúka eftirfarandi verkum eða að staðfesta að þeim sé lokið.

-   Setja upp númeraraðir.
-   Setja upp verkflæði fyrir verkefnastjórnun og bókhald
-   Virkja verkflæði tilfangabeiðni.

Eftir að hafa annað hvort staðfestir eða ljúka verkefnum ofan, er hægt að ljúka eftirfarandi verkum eftir þörfum.

-   Stofna beiðni tilfanga úr óbundið mönnuðum tilföngum.
-   Fylgjast með tilfangabeiðnum.
-   Uppfylla tilfangabeiðnir.
-   Biðja um mönnuð tilföng úr WBS.
-   Bóka tilföng á verk án beiðni um mönnuð tilföng.

## <a name="monitor-project-teams"></a>Fylgjast með verkhópum
1.  Farið í **Verkefnastjórnun og bókhald** &gt; **Verkefni** &gt; **Öll verkefni**.
2.  Í lista yfir verk, smellið á tengilinn **Verkkenni** fyrir verkið **XYZ Uppfærsla þrep 2**.
3.  Á flýtiflipanum **Verkhópur og áætlun** sakl ganga úr skugga um að tilföng verks sem eru talin upp séu rétt.





