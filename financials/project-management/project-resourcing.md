---
title: "Tilföng verks"
description: "Þetta efni veitir upplýsingar um resourcing verks."
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
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Tilföng verks

Þetta efni veitir upplýsingar um resourcing verks.

Ein challenge verkefnisstjórar og stjórnendur tilföng verksins stig fjárhagsáætlunargerðar er úthlutun tilfanga, þar sem þeir þurfa að ákvarða og taka frá rétt tilfanga til að vinna í verki. Í Microsoft Dynamics 365 fyrir Aðgerðir, resourcing getu fyrir verk hægt er að skilgreina hlutverk eru meðhöndluð sem tímabundin tilföng sem hægt er að taka frá fyrir tiltekna skuldbindingarbréf eða hluta sem skuldbindingarbréf. Þessi tegund tilfanga gerir verkefnisstjórum og stjórnendum tilfanga kleift að ljúka eftirfarandi verkum:

-   Skilgreina hlutverk sem hefur nauðsynlega hæfni til að gera auðvelt að samsvara tilföng.
-   Hlutverk er notuð til að skilgreina fyrstu skuldbindingarbréf greiðsluáætlun sem byggð er á frátekin tilföng.
-   Gera kostnaðarmat og ákvarða upphaflega fjárhagsáætlun, byggt á úthlutuðum hlutverkum og tilföngum fyrir verk.
-   Hlutverk er notuð til að áætla fjölda tilfanga frátekningar er krafist fyrir hverja skuldbindingarbréf.
-   Áætla fjölda tilfanga sem krafist er fyrir allan líftíma verksins.
-   Gera drög að sundurliðun verkþátta (WBS) með því að nota upphaflega tilfangaúthlutun.

[![Líftími verks](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Sem haldið er áfram áætlanagerð verks, áætluð tilföng hægt skipta á út mannaðar tilföng. Stjórnanda verksins einnig er hægt til baka og uppfæra resourcing frátekningar við allar verkstig.

## <a name="set-up-project-resources"></a>Setja upp verktilföng.
Þú þarft að setja upp dagatal og tengja það við starfsmann eða starfskraft. Dagatalið er notað til að áætla verkið og vinnutíma yfir tilföng sem eru fráteknar fyrir verkið. Við uppsetningu dagatals geta verkefnisstjórar framkvæmt sléttun á tilföngum sem hluta af fínstillingu tilfanga. Samkvæmt áætlun dagatals geta takmarkanir verið settar á tilföng. Hægt er að setja upp dagatal sem á við **Dagatöl** síðu. 

Þegar sett er upp starfsmanns sem tilföng verks er hægt að velja úr starfsmönnum sem vinna í fyrirtækinu sem verið er að setja upp tilföng eða hægt er að velja starfsmenn úr öðrum fyrirtækjum innan fyrirtækisins. Þetta eru samstæðu tilföng. Eftirfarandi aðgerðum er útskýrt hvernig setja á upp starfsmanns sem tilföng verks innan fyrirtækisins og hvernig á að setja upp samstæðuverk tilfanga.

### <a name="set-up-a-worker-as-a-project-resource"></a>Setja upp starfmann sem verktilfang.

1.  Í í **Starfsmenn** síðunni, í **Starfsmenn** listanum skal velja starfsmanninn sem verið er að bæta við sem tilföng verks og opna færslu starfsmanns.
2.  Á Aðgerðasvæðinu skal smellt á **Verks**&gt;**Uppsetningu**&gt;**verkuppsetning**.
3.  Velja dagatal og loka síðan.

Einnig er hægt að tilgreina sjálfgefið verk fyrir tilföng sem gerð áætlaðs verkefnis. Hægt er að nota áætlaðar úthlutanir þegar tilfangastjórnandi eða verkstjóri veit hvaða verk tilfangið verður að vinna að fyrirfram. Einnig er hægt að byggja áætlaðar úthlutanir á beiðni kostunaraðila verks eða viðskiptavinar. Til að úthluta verki fyrirfram: Á síðunni **Úthluta verkum**, á flipanum **Verk**, á listanum **Eftirstandandi verk** skal velja viðeigandi verk.

### <a name="set-up-an-intercompany-resource"></a>Setja upp samstæðuröðun tilfanga

Þegar sett er upp starfsmanns sem samstæðuröðun tilfanga verður að ljúka uppsetningunni í eignaleigu fyrirtækis og lánað fyrirtækisins. 

**Í lögaðilanum fyrirtæki:**

1.  Í Dynamics 365 fyrir Aðgerðir, staðfesta eignaleigu fyrirtækisins er valinn, og þá ljúka leiðbeiningunum hér að framan, "Setja upp starfsmanns sem tilfang verk".
2.  Fara í ** fjárhags **&gt; ** Bókunaruppsetning **&gt;**samstæðubókhald**. Click **New**.
3.  Í því ** Kenni lögaðila ** skal velja eignaleigu fyrirtækisins. Fyllið út eftirstandandi svæði eftir þörfum og smellið síðan á **Vista**.
4.  Fara í ** verkefnastjórnun Og bókhald **&gt; ** Uppsetningu **&gt;**Verð ** &gt;**flutningsverð**.** **
5.  Í í ** flutningsverð ** er smellt á **Nýtt**, og í ** lögaðili sem fær Lánað ** skal velja viðeigandi fyrirtæki.
6.  Ef þú vilt aðeins lána fyrirtækisins lánað tilfangið sem var stofnuð í upphafi þessa hluta í í **Tilfanga** skal velja nafn tilfangið sem var stofnuð. Ef óskað er að gera öll tilföng í fyrirtækinu tiltæk fyrirtæki lánað skilja á ** Tilfanga ** autt.
7.  Fara ** verkefnastjórnun Og bókhald **&gt; ** Uppsetningu **&gt;**verkefnastjórnun Og bókhaldsfæribreytur**, og á við ** Samstæðu ** flipanum, skal stilla í ** Virkja samstæðuröðun tilfanga og tímablöð ** á **Já**.

**Lánað fyrirtæki:**

1.  Fara í **verkefnastjórnun Og bókhald**&gt;**tilföng Verks**&gt;**tilfangalista**.
2.  Færið inn heiti tilfanga sem stofnaði í fyrra ferli eignaleigu fyrirtækisins til að staðfesta að heiti tekinn með í lista yfir tilföng lánað fyrirtækis í síunni leit.

## <a name="manage-resource-competencies"></a>Umsjón með hæfni tilfanga
Hæfni tilfanga eru nauðsynlegar hluti stjórnun tilfanga. Hæfni er hægt að nota sem grunnlínu til að ákvarða tilföng sem eru með rétt jafnvægi hvað varðar hæfni, menntun, réttindi og verkreynslu. Rétt er að setja þessar upplýsingar upp fyrir hvert tilfang og uppfæra þær reglulega. Á þennan hátt er hægt að hámarka getu þegar tiltekin hæfni tilfanga er borin saman við úthlutun verks til tilfanga. [![Dæmi um hæfni, menntun vottanir og verkreynslu](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

Eftirfarandi aðgerðir útskýra hvernig á að setja upp ákveðna hæfni fyrir tilfang. 

Til að setja upp hæfni starfsmanns, er hægt að nota annað hvort listasíðuna **Starfsmenn** í Mannauði eða listasíðuna **Tilföng** í Verkefnastjórnun og bókhald. Fyrir eftirfarandi aðferðir í **Starfsmenn** listasíðu í mannauði er notað.

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
1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**Vinnusvæða**&gt;**Verk stjórnun**.
2.  Smelltu á **Nýtt verk** og færðu síðan eftirfarandi gildi inn:
    -   **Gerð** - Tími og efni
    -   **Heiti verksins** -Áfanga 2 XYZ
    -   **Verkflokkur** -TM\_VÍV
    -   **Kenni samnings verks** -00000002
3.  Smella á **Stofna verk**.

### <a name="assign-a-resource-to-a-project"></a>Úthluta tilfangi á verk

1.  Smellið á **mannauður**&gt;**Starfsmenn**&gt;**Starfsmenn**.
2.  Í listanum **Starfsmenn**, skal velja skrá starfsmanns sem hefur áður verið sett upp hæfni fyrir og opna skrá starfsmanns.
3.  Á Aðgerðarrúðunni, á flipanum **Verk** í flokkinum **Uppsetning** smellið á ** Úthluta verkum**.
4.  Á síðunni **Úthlutanir villuleitartegundar tilfanga** er smellt á flipann **Verk**.
5.  Í því **Bæta verki við valið verk**, síu á verk, Áfanga 2 XYZ
6.  Í rúðunni **Eftirstandandi verk**, veljið verk og smellið síðan á ör til að bæta því við í **Valin verk** rúðunni.
7.  Lokið síðunni.

Ef þörf krefur, er einnig hægt að úthluta tegundum fyrir tilföng. Gerð tegundar er annað hvort Kostnaður eða Tekjur. Þetta er ákvarðað af fyrirtækinu. Engin úthlutað tegundir fyrir tilföngin eru Dynamics 365 fyrir Aðgerðir verður fletta upp sem sjálfgefin tegund verð á klukkustund fyrir kostnað og tekjur á.

### <a name="set-up-project-resource-and-role-characteristics"></a>Setja upp verk tilfanga og einkenni verks

Verkefnastjóri getur notað aðgerðir verktilfanga til að stofna hlutverk sem krafist er fyrir verkið. Hægt er að nota hlutverk þegar staðfestar tilföng eru enn óþekkt þegar tilföng sem eru teknar frá. Hlutverk hægt tímabundið tekin áætluð tilföng sem svo að hægt er að halda áfram verki áætlunarstig. 

[![Dæmi um hlutverk](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Aðstæður:** Contoso var ráðinn til að ljúka við Tíma- og efnisverk sem hefur samþykkta skipulagsskrá verks. Undirverkefnastjóri er enn að ljúka við umfang verksins. Stjórnandi tilfangs auðkennir núna tiltekin tilföng sem verða teknar frá fyrir vinnu á í nýja verkið. Háttsettur verkstjóri eitt hlutverk beðið sponsor verk, vegna mikilvæg eðli þess verks sem er. Stjórnandi tilfanga verður öðlast nýja tilfanga og skilgreina hlutverk í kerfinu ef bókara verkstjóri krefst tilfangaupplýsingar meðan á verkáætlun. 

Eftirfarandi sýna hvernig stjórnanda tilfanga er sett upp Háttsettur verkhlutverk stjórnanda og tengja eiginleika tilfanga við það. Síðar er hægt að nota hlutverkið til að leita að lausum tilföngum sem samsvara áskildri hæfni tilfangsins.

1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**Uppsetningu**&gt;**Tilföng**&gt;**Uppsetning hlutverk**.
2.  Smelltu á **Nýtt** og færðu síðan eftirfarandi gildi inn:
    -   **Kenni hlutverk** -Skattur Stjórnanda Verks
    -   **Lýsing** -Skattur Stjórnanda Verks
3.  Smellið á **Stofna**.
4.  Velja skal hlutverkið **Yfirverkefnastjóri** og smellið svo á **Skilgreina einkenni**.
5.  Í reitnum **Gerð einkenna** skal velja **Hæfni**.
6.  Í reitnum **Tiltæk einkenni** skal færa inn hæfni sem verið er að leita að.
7.  Í reitnum **Gerð einkenna** skal velja **Réttindi**.
8.  Í reitnum **Tiltæk einkenni** skal færa inn tegund réttinda sem verið er að leita að.
9.  Smellið á **OK** og lokið síðunni.

### <a name="assign-a-project-resource-to-a-project"></a>Úthlutið verktilföngum á verk

1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**Algengar**&gt;**Verk**&gt;**Öll verk**, og opna í **Áfanga 2 XYZ** verks.
2.  Á flipanum **Verkhópur og áætlun**, smellið á **Bæta við**.
3.  Á svæðinu **Hlutverk**, veljið **Meðlimur**.
4.  Smellið á **Bóka úr dagatali**.
5.  Á síðunni **Tilföng til ráðstöfunar** er smellt á **Skoða stillingar**.
6.  Á síðunni **Breyta stillingum yfirlits** skal færa inn eftirfarandi gildi:
    -   **Snið fyrir dagsetningabil** - Dagur
    -   **Birta lýsingar á framboði** - Já
    -   **Birta eftirstöðvar afkastagetu** - Já
7.  Í lista yfir tilföng, velja tilfang.
8.  Smellið á **bundinni**&gt;**Full afkastageta**.
9.  Lokið síðunni.

### <a name="assign-a-resource-to-a-default-role"></a>Tengja tilfang við sjálfgefið hlutverk

Til að auðvelda stjórnendum verk eða tilföng, hægt er að kafa niður frekar á forða sem hægt er að taka frá fyrir verk. Hægt er að tengja sjálfgefið hlutverk við fyrirliggjandi tilfang eða nýlega áunnið tilfang. Til dæmis þegar Daniel var ráðinn hann hafði reynslu og hæfni til að fylla Business analyst hlutverk. Stjórnandi tilfanga úthlutað þessu hlutverki sem sjálfgefin hlutverk Daniel fyrirtækisins. Þess vegna er tilfangastjórnandi bætt Daniel hóp analysts viðskiptatengsl sem eru tiltækar til að vinna í verk. 

Við frátekningu tilfangs, verkefnisstjórar sía hlutverk tilföng sem eru tiltækar til að vinna í verk. Þeir geta notað þessar upplýsingar sem eitt skilyrði þegar þeir framkvæma ákvarðanagreiningu um mörg skilyrði við uppfyllingar tilfanga. Þeir get líka bætt öðrum eiginleika tilfanga við síuna til að leita að tilföngum sem hafa tiltekna hæfni, menntun og reynslu fyrir tiltekið verk. 

**Dæmi:** samþykkt verkið er byrjuð og Aðalbókara verkhlutverk stjórnanda var frátekin sem áætluð tilföng verksins stig fjárhagsáætlunargerðar. Stjórnandi tilfanga hefur nú fengið tilfang til að uppfylla hlutverkið Yfirverkefnastjóri.

1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**tilföng Verks**&gt;**tilfangalista**.
2.  Í listanum **Tilföng**, veljið **Daniel Goldschmidt**.
3.  Smellið á **Verk tilfanga**&gt;**Maintain**&gt;**Tilfanga hlutverk**.
4.  Smelltu á **Nýtt** og færðu síðan eftirfarandi gildi inn:
    -   **Raunveruleg** - (núgildandi dagsetningu)
    -   **Lokadagur** - Aldrei
    -   **Hlutverk** -Skattur Stjórnanda Verks
5.  Smellið á **Vista** og lokið síðan skjámyndinni.
6.  Á flipanum **Hæfni**, bæta við **ProjectMgmt** hæfni og **PMP** réttindum.

## <a name="set-up-role-based-pricing"></a>Uppsetning verðlagningar byggðri á hlutverkum
Hægt er að setja allan kostnað, söluverð og flutningsverð upp fyrir hlutverk.

1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**Uppsetningu**&gt;**Verð**&gt;**söluverð (klukkustund)**.
2.  Click **New**.
3.  Tilgreina gildisdagsetningu.
4.  Í **Hlutverk** dálki skal velja hlutverk.
5.  Í **Verðlagning** dálki skal slá inn verð fyrir valið tilfangahlutverk.

## <a name="form-a-project-team"></a>Skjámyndin við verkhópinn
Til að nota hlutverk sem voru áður settar upp í verki, stjórnanda verks verður að tengja hlutverk við verk. Hægt er að úthluta mörgum hlutverk fyrir verk og 365 Dynamics aðgerða labels sjálfvirkt þessum hlutverkum við frátekningu koma í veg fyrir misskilning. Til dæmis, ef verkefnastjóra krefst þrjár hugbúnað-milli, þrjár Hugbúnað vendismíða hlutverk sem hafa hugbúnað vendismíða 1, hugbúnað vendismíða 2 og vendismíða hugbúnað 3 og merkja þeirra myndaður sjálfkrafa. Ef einkenni hlutverks hafa áður verið stillt fyrir hlutverkið, eru þau notuð sem sía við leit tilfanga. Hægt er að bæta frekari eiginleikum við sem þarf til að fínstilla leitina enn frekar. 

Einnig er hægt að sérsníða skoðun á stillingum til að gefa betra yfirlit yfir tiltæk tilföng. Það eru valkostir til að sýna tiltæki eftir klukkustund, daglega, vikulega, mánaðarlega, ársfjórðungslega og árlega. Það er einnig valkostur að sýna tiltæka og eftirstandandi afkastagetu á tilföng. Þessi valkostur er gagnleg fyrir tímastjórnun þegar verið er að meta tiltækan tíma fyrir verkþætti eða tiltæk tilföng. 

Verkefnastjóra hægt að velja hlutverk á síðunni og, sé tiltæk tilföng sem hentar þörfum, veljið síðan til að taka frá tilfangs til að fylla á hlutverki. Athugið að tilföng vinnukortaheimild ekki á að taka frá á þessu stigi fjárhagsáætlunargerðar stigi. Þegar WBS er hægt að skipta út hlutverk með mannaðar tilföng fyrir verkið. Ef hlutverk er skipt út fyrir mannaðar tilföng í WBS, uppfærir uppsetning tilfangs sjálfvirkt verkhópur skráningar og röðun. 

[![Verkhópur skráningar sem inniheldur hlutverk og raunverulega tilföng](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Verkefnastjórinn hefur mismunandi valkosti fyrir bókun tilfanga fyrir verk, eins og **Eftirstöðvar afkastagetu**, **Full afkastageta**, **Hlutfall Afkastagetu**, og **Tilgreina klukkustundir**. Hætta má við þessa bókunarvalkosti hvenær sem er ef úthlutun tilfanga breytist. Til eru tvær gerðir bókunar:

-   **Bundinni** – frátekningar tilfanga var samþykkt og staðfest að vinna á skuldbindingarbréf fyrir tilgreinda tímalengd.
-   **Óbundinni** – frátekningar tilfanga var tentatively stillt til að vinna á skuldbindingarbréf fyrir tilgreinda tímalengd.

Notið eftirfarandi aðferðir til þess að stofna verkhóp.

### <a name="create-a-project-team"></a>Stofna verkhóp

1.  Á listasíðunni **Öll verk** veldu verk og smellið síðan á **Breyta**.
2.  Á við **verkhópur Og áætlun** flipanum, á **Áætluð lokadagsetning** svæðinu, færið inn upphafsdagsetningu í röðun plús einn mánuð. Til dæmis, ef upphafsdagsetning í röðun er 24 Júní 2017 (24/06/2017), færa inn **07/24/2017**.
3.  Click **Add**.
4.  Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk **, veljið **Yfirverkefnastjóri**.
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

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Samstilling dagatal](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Samstillingarferlið er hannað til að samstilla upplýsingar um öll dagatöl tilfanga. Þessar upplýsingar innihalda grunnupplýsingar dagatals um allar breytingar á Töflu yfir afkastagetu tilfangadagatals.verksins. Ef ný tilföng er bætt við verkið, samstillingu tryggir uppfærða dagatalsupplýsingum er tiltækt. Þessa samstillingu er hægt að gera hvenær sem er. 

Mælt er með því að nota runuvinnslu. Valkostirnir eru tiltækar í samstillingu frátekinnar afkastagetu.

-   Smellt er á **verkefnastjórnun Og bókhald**&gt;**Reglubundið**&gt;**Afkastagetu samstillingu**&gt;**Samstilla tilföng afkastagetu taka saman-ups**.

| Valkostur | lýsing                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Já    | Samstilla öll tilfangagögn við dagatal og upplýsingar um grunndagatal og skrifa yfir allar upplýsingar í dagatali afkastagetu tilfanga í verkinu.                                                  |
| Nei     | Samstilla tilfangagögnin, samkvæmt tímabilskóðanum og tilgreindum upphafs- og lokadagsetningum. Þessi valkostur fjarlægir ekki fyrirliggjandi gögn og uppfærir upplýsingar aðeins fyrir nýlega viðbætt tilföng. |

[![Samstilling](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Setja upp hlutverk á WBS-sniðmát
Verkefnisstjórar geta sett upp WBS-sniðmát sem hægt er að nota þegar þeir stofna WBS fyrir ný verk. Verkefnisstjórar hægt að bæta við hlutverkum þegar sniðmát er stofnað. Notið eftirfarandi ferli til að úthluta hlutverki WBS template.* * **

1.  Smellt er á **verkefnastjórnun Og bókhald**&gt;**Uppsetningu**&gt;**Verk**&gt;**Sniðmát fyrir sundurliðun verkþátta**.
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
<td>Bæta við áætluðum tilföngum sjálfkrafa með því að nota hlutverk sem eru tengd verkefni. Dynamics 365 aðgerða stingur sjálfkrafa áætluð tilföng með því að nota mörg skilyrði ákvörðun analysis sem byggir á hlutverkum. Eftir að hlutverk og framlag (klukkustundir) hefur verið stillt fyrir verk í WBS og skipulag hefur verið losað er smellt á <strong>Búa Sjálfkrafa til hóp</strong>. Áskildum fjölda áætlaðra tilfanga er bætt við WBS og flipann <strong>Áætlun Verks og hóps</strong>.</td>
</tr>
<tr class="odd">
<td>Tilföng (fellilisti)</td>
<td>Á síðunni <strong>Ræsa úthlutun tilfanga </strong>er hægt að velja tilföng í bundna bókun eða óbundna bókun, á grundvelli tilgreindrar tímalengdar. Hægt er að breyta stillingum yfirlits til að sjá og stilla tímalengd verkþátta tilfanga. Hægt er að velja og úthluta tilföngum á stigi pakkavinnu með eftirfarandi valkostum:
<ul>
<li><strong>Samþykkja</strong> -Staðfesta breytingar á tilföngum sem er úthlutað á verkefni.</li>
<li><strong>Hætta við</strong> -Hætta við breytingar á tilföngum sem er úthlutað á verkefni.</li>
<li><strong>Úthluta sjálfkrafa</strong> – velur Þennan valkost við tiltækar mannaðar tilföng með samsvarandi hlutverki á valið verk.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**Verk**&gt;**Öll verk**.
2.  Á listanum, veljið verkið ** XYZ Uppfærsla þrep 2**.
3.  Smellið á **Áætlun**&gt;**Verkþætti**&gt;**sundurliðun Verkþátta**.
4.  Smellið á **Nýtt** til að bæta eftirfarandi verkþætti af stigi eitt við WBS:
    -   Verið er að hefja
    -   Áætlun
    -   Í gangi
    -   Eftirlit og stjórn
    -   Loka

5.  Setja upp dagsetningar og framlags (klukkustundir), eins og sýnt er í eftirfarandi skjámyndir. [![Dagsetningar og framlags](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
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
16. Smellið á **Óbundnar úthluta**&gt;**Full afkastageta**.
17. Smellið á **Vista** og lokið síðan skjámyndinni. 

> [!NOTE] 
> Berst ekki viðvörun sem tilgreint er nú 2, þar sem fjöldi tilfanga eftir 1.
18. Á síðunni **Sundurliðun Verkþátta ** skal staðfesta úthlutun tilfanga á WBS og smellið síðan á **Vista**.

## <a name="resource-fulfillment-for-planned-resources"></a>Uppfylling tilfanga fyrir áætluð tilföng
Verkefnastjóri getur áætlað áskilið tilfangahlutverk  við verkið. Stjórnandi tilfanga sér þessi áætluðu tilföng sem beiðnir á síðunni **Uppfyllingar Tilfanga** og getur úthlutað raunverulegum tilföngum.

1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**Verk**&gt;**Öll verk**.
2.  Á listanum, veljið verkið ** XYZ Uppfærsla þrep 2**.
3.  Smellið á **Verk**.
4.  Smellið á **Breyta**.
5.  Á við **verkhópur Og áætlun** flipanum ** ** smellið **Bæta**.
6.  Í svarglugganum **Bæta við hlutverkum** veljið hlutverkið **Forritari**.
7.  Smellið á **Stofna**.
8.  Lokið verksíðunni.
9.  Smellið á **verkefnastjórnun Og bókhald**&gt;**tilföng Verks**&gt;**Tilfanga uppfyllingar**.
10. Veljið **Forritari 1** fyrir verkið **XYZ Uppfærsla verks þrep 2**.
11. Veljið notanda og smellið á **Úthluta**.
12. Staðfesta að lína fyrir **Forritara 1** hefur verið fjarlægð fyrir verkið **XYZ Uppfærslu verks þrep 2**.
13. Á flipanum **Verkhópur Og áætlun** fyrir verkið **XYZ Uppfærsla þrep 2**, skal staðfesta að starfsmanni sem valinn var í þrepi 11 hefur verið bætt við sem **Forritara**.

## <a name="requests-for-project-resources"></a>Beiðnir um tilföng verks
Röðun aðgerð tilfanga styður aðeins stjórnendur tilfanga til að dreifa mannaðar tilföngum á engagements eða verk. Til að virkja þennan eiginleika virkan skal ljúka eftirfarandi verkum eða að staðfesta að þeir hafa lokið.

-   Setja upp númeraraðir.
-   Setja upp verkefnastjórnun og verkflæði bókhalds.
-   Virkja verkflæði notandabeiðnar tilfanga.

Eftir að hafa annað hvort staðfestir eða ljúka verkefnum ofan, er hægt að ljúka eftirfarandi verkum eftir þörfum.

-   Stofna beiðni tilfanga úr óbundið mannaðar tilfanga.
-   Fylgjast með beiðnir um tilföng.
-   Uppfylla beiðnir um tilföng.
-   Biðja um mannaðar tilfanga úr wbs.
-   Bóka tilföngum á verk án beiðni um mannaðar tilfanga.

## <a name="monitor-project-teams"></a>Fylgjast með hópa verks
1.  Smellið á **verkefnastjórnun Og bókhald**&gt;**Verk**&gt;**Öll verk**.
2.  Í lista yfir verk, smellið á tengilinn **Verkkenni** fyrir verkið **XYZ Uppfærsla þrep 2**.
3.  Á flýtiflipanum **Verkhópur og áætlun** sakl ganga úr skugga um að tilföng verks sem eru talin upp séu rétt.



