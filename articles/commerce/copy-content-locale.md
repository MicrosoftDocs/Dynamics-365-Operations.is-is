---
title: Afrita efni á annan landsstaðal
description: Þessi grein lýsir því hvernig á að afrita fyrirliggjandi efni á annan stað innan vefsvæðis í Microsoft Dynamics 365 Commerce vefsmiður.
author: josaw1
ms.date: 07/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 6afa871048bde22133ae083b8d56b6e99e49c401
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269262"
---
# <a name="copy-content-to-another-locale"></a>Afrita efni á annan landsstaðal

[!include[banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að afrita fyrirliggjandi efni á annan stað innan vefsvæðis í Microsoft Dynamics 365 Commerce vefsmiður.

Þegar þú býrð til efni í Commerce site builder er það alltaf tengt við staðsetningarauðkenni, eins og „en-us“. Þú getur afritað einstakar síður og eignir á annan stað innan sömu netverslunarsíðu með því að skipta um svæði þegar þú breytir efnisatriði og býr síðan til nýtt afbrigði af hlutnum. Í sumum tilfellum, eins og þegar þú ert að setja af stað alveg nýjan stað á verslunarglugganum þínum, er skynsamlegt að afrita öll efnisatriðin á núverandi svæði yfir á nýja staðinn. Ef nýja staðsetningin er með sama grunntungumál og eitt af núverandi staðsetningum geturðu notað núverandi svæði sem upprunastað fyrir afritunaraðgerðina. (Til dæmis, "en-us" og "en-au" staðsetningarnar nota báðar enska tungumálið.) Þannig hjálpar þú til við að draga úr fyrirhöfninni sem þarf til að staðfæra efnið á nýja staðnum.

Eftirfarandi aðferðir útskýra hvernig á að bæta nýjum stað við núverandi rás, afrita öll efnisatriði frá núverandi svæði yfir á nýjan stað og fylgjast með stöðu svæðisafritunaraðgerðar.

## <a name="add-a-new-locale"></a>Bættu við nýjum stað

Fylgdu þessum skrefum til að bæta við nýjum stað í Commerce site builder.

1. Farðu á síðuna þína í Site Builder.
1. Í vinstri yfirlitsrúðunni, veldu **Vefstillingar**, og veldu síðan **Rásir**.
1. Undir **Rás**, veldu rásina til að bæta nýju svæði við.
1. Í rásarglugganum sem birtist hægra megin velurðu **Bættu við svæði**.
1. Í **Bættu við svæði** valmynd, í **Staðsetning til að styðja** reit, veldu svæði.
1. Staðfestu að **Lén** gildi er rétt.
1. Undir **Leið**, sláðu inn einstaka vefslóð (til dæmis, **en-okkur** eða **ensku-okkur**).
1. Veldu **Í lagi**.
1. Lokaðu rásarglugganum.
1. Undir **Rás**, staðfestu að nýja staðsetningin sé skráð við hliðina á réttri rás.
1. Veljið **Vista og birta**.

> [!NOTE]
> Áður en hægt er að stilla nýja staðsetninguna í vefsvæðisgerð verður að bæta honum við tengda netverslunarrás í höfuðstöðvum Commerce.

## <a name="copy-all-content-items-to-a-new-locale"></a>Afritaðu öll efnisatriði á nýjan stað

Fylgdu þessum skrefum til að afrita öll efnisatriði á nýjan stað í Commerce site builder.

1. Farðu á síðuna þína í Site Builder.
1. Í vinstri yfirlitsrúðunni, veldu **Vefstillingar**, og veldu síðan **Rásir**.
1. Veldu á skipanastikunni **Búðu til staðsetningarafrit frá**.
1. Í **Búðu til staðsetningarafrit** svargluggi sem birtist hægra megin, undir **Heimildasíða**, staðfestu að rétt síða sé valið.
1. Í **Upprunarás** reit, veldu upprunarásina.
1. Í **Áfangarrás** reit, veldu sömu upprunarás.
1. Í **Heimildarstaður** reit, veldu upprunastaðinn.
1. Í **Áfangastaður** reit, veldu nýjan stað.
1. Veldu **Afritaðu staðarval**. Tilkynning staðfestir að staðsetningarafritunaraðgerðin hafi hafist.

> [!NOTE]
> Þú getur líka afritað efni á milli mismunandi rása.

## <a name="monitor-the-status-of-the-locale-copy"></a>Fylgstu með stöðu staðsetningarafritsins

Fylgdu þessum skrefum til að fylgjast með stöðu afritunaraðgerðar.

1. Farðu á síðuna þína í Site Builder.
1. Í vinstri yfirlitsrúðunni, veldu **Vefstillingar**, og veldu síðan **Störf**.
1. Undir **Núverandi störf**, veldu verkið til að fylgjast með. Upplýsingar um starf eru sýndar í glugganum sem birtist hægra megin.
