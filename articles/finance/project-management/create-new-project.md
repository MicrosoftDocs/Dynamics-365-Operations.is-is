---
title: Stofna nýtt verk
description: Þetta efnisatriði gefur upplýsingar um hvernig á að búa til nýtt verk.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760573"
---
# <a name="create-a-new-project"></a>Stofna nýtt verk

[!include [banner](../includes/banner.md)]

Ljúkið eftirfarandi skrefum til að stofna nýtt verk.

1. Á **Verkefnastjórnun** skal velja **Nýtt verk** og færa eftirfarandi gildi inn:

    - **Gerð verks:** Tími og efni
    - **Verkheiti:** XYZ Uppfærsla þrep 2
    - **Verkflokkur:** TM\_WIP
    - **Auðkenni verksamnings:** 00000002

2. Velja **Stofna verk**.

## <a name="assign-a-resource-to-a-project"></a>Úthluta tilfangi á verk

1. Á síðunni **Starfskraftar** í listanum **Starfskraftar**, skal velja skrá starfskrafts sem hefur áður verið sett upp hæfni fyrir og opna starfskrafts.
2. Á Aðgerðarrúðunni, á flipanum **Verk** í flokkinum **Uppsetning** veljið **Úthluta verkum**.
3. Á **Úthlutanir tilfanga fyrir villuleit í verki** síðunni á **Verk** flipanum í **Bæta verki við valin verk** reitnum skal sía eftir **XYZ Uppfærsla þrep 2** verki.
4. Í rúðunni **Eftirstandandi verk**, veljið verk og smellið síðan á örvarhnappur til að bæta því við í **Valin verk** rúðunni.

Einnig er hægt að úthluta tegundum fyrir tilföng eftir þörfum. Gerð tegundar er annað hvort **Kostnaður** eða **Tekjur**. Gerð tegundar er ákvörðuð af fyrirtækinu. Ef engin tegund er fyrir tilfönginmun Finance fletta upp sjálfgefinni tegund á verð á klukkustund fyrir kostnað og tekjur.

## <a name="set-up-project-resource-and-role-characteristics"></a>Setja upp verk tilfanga og einkenni verks

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

## <a name="assign-a-project-resource-to-a-project"></a>Úthlutið verktilföngum á verk

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

## <a name="assign-a-resource-to-a-default-role"></a>Tengja tilfang við sjálfgefið hlutverk

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
