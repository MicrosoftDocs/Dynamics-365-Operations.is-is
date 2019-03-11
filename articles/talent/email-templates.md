---
title: Sniðmát fyrir tölvupóst
description: Þetta umræðuefni veitir upplýsingar um sniðmátin fyrir tölvupóst sem þú getur búið til og notað í Microsoft Dynamics 365 for Talent - Attract.
author: josaw
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e02912ad242186fe3e2dd8d7a4cc7312aec6015e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "304885"
---
# <a name="email-templates"></a>Sniðmát tölvupósts
[!include[banner](../includes/banner.md)]

Með því að nota sniðmátasafnið fyrir tölvupóst geta stjórnendur búið til samræmda þema og vörumerki fyrir öll tölvupóst sem eru send með Microsoft Dynamics 365 for Talent: Attract. Stjórnendur geta einnig stýrt sniðmátum fyrir efni tölvupósts sem aðrir notendur geta notað. Ráðningarteymið getur notað þessi sniðmát í verkflæði sínu til að senda tölvupóst á skilvirkan hátt. Sumir tölvupóstar í Attract eru stilltir til að senda sjálfkrafa, og stjórnandinn getur notað sniðmátasafnið fyrir tölvupóst til að sérsníða efni fyrir þessi tölvupóst.

> [!NOTE]
> Til að nota sniðmát fyrir tölvupóst verður fyrirtækið þitt að vera með Viðbót við alhliða ráðningar.

## <a name="global-template-configurations"></a>Stillingar á altæku sniðmáti

Til að búa til samræmd vörumerki fyrir öll tölvupóstssamskipti, verður stjórnandinn fyrst að setja altæka hausinn og fótinn fyrir öll sniðmátin fyrir tölvupóst. Í stjórnendamiðstöð getur stjórnandi hlaðið inn mynd sem á að nota sem haus eða borða fyrir allan tölvupóst í flipanum **Stillingar fyrir sniðmát tölvupósts** í **Haus** kaflanum. Myndin gæti verið fyrirtækjamerki, bréfshaus eða önnur auðkennandi mynd. Við mælum með að breiddin sé á milli 25 og 800 pixlar og að hæðin sé á milli 25 og 150 pixlar, því þessi mál eru ákjósanleg fyrir flesta tölvupóstbiðlara, svo sem Microsoft Outlook. Myndin verður að vera JPEG, JPG, PNG eða SVG skrá og skráarstærðin verður að vera minni en 1 megabæti (MB). Eftir að mynd hefur verið hlaðið upp er sýnishorn af hausnum búið til og sýnt. Ef hausmyndin verður að fjarlægja eða skipta út, getur stjórnandinn notað **Fjarlægja** valkostinn fyrir ofan forskoðunina.

Í **Fótur** kafla getur stjórnandinn veitt tengla við persónuverndarstefnu fyrirtækisins varðandi samskipti og skilmálana. Þessir tenglar eru felldir inn í fót sem er sjálfkrafa myndaður. Forskoðun á þessum fót er þá sýnd.

Vertu viss um að vista breytingarnar áður en þú lokar stjórnendamiðstöðinni.

> [!NOTE] 
> Höfuð og fótur eru altækar stillingar fyrir allan tölvupóst. Þess vegna munu þeir birtast í öllum tölvupóstum sem eru sendir í gegnum Attract. Ef stillingarnar eru ekki skilgreindar verður hausinn og fóturinn skilinn út úr öllum tölvupósti.

## <a name="email-template-library"></a>Sniðmátasafn fyrir tölvupóst 

Eftir að altæku sniðmátsskilgreiningarnar hafa verið settar upp, getur stjórnandinn byrjað að búa til og stýra sniðmátum fyrir allan tölvupóst sem er sendur frá Attract. Sniðmátasafn fyrir tölvupóst er aðeins aðgengilegt fyrir stjórnendur. Til að opna safnið velurðu **Sniðmát fyrir tölvupóst** flipann á aðalvalmyndinni. Safnið er flokkað af hinum ýmsu verkþáttum í Attract að tölvupóstur þarf að senda til, svo sem áætlunargerð, mati og búa til starf. Stjórnandi getur valið hvaða flokk sem er til að skoða allar tölvupóstgerðir sem tengjast verkþættinum. Til dæmis, veldu **Áætlunargerð** til að skoða mismunandi gerðir af tölvupósti sem eru sendar í áætlunargerðarferlinu og öllum sniðmátunum sem eru tiltækar fyrir hverja gerð tölvupósts. Hver undirflokkur í flokki táknar gerð tölvupósts.

Sumar tegundir af tölvupósti geta haft fleiri en einn viðtakanda. Til dæmis, í flokknum **Áætlunargerð** eru sendir tölvupóstar þegar þörf er á samantekt á viðtalsáætlun, bæði til umsækjenda og spyrla. Hver hluti hefur tvö aðal dálka: **Titill sniðmáts** og **Viðtakandi**. Hver röð í hluta stendur fyrir eitt sniðmát fyrir gerð tölvupósts. Fyrst birtist lástákn í röðinni fyrir hvert sniðmát. Þetta tákn gefur til kynna að sniðmátið sé staðlað sniðmát sem fylgir með Attract og að því sé ekki hægt að eyða. Fyrir hvaða sniðmát sem er, getur stjórnandinn notað þrípunktahnappinn (**...**) til að afrita sniðmátið, setja það sem sjálfgefið sniðmát eða eyða því. Þegar sniðmát er valið sem sjálfgefið sniðmát getur eitt af tveimur atferlum komið fram. Atferlið er táknað með merkinu eða merkjum sem birtast í röðinni fyrir sniðmátið:

- **Sjálfgefið** - Þetta merki gefur til kynna að sniðmátið sé sjálfgefið sniðmát fyrir tölvupóst sem er sendur og að upplýsingar verða slegnar inn þegar notandi sendir tölvupóst af þeirri tilteknu tegund.
- **Sjálfgefið** + **Sent sjálfkrafa** - Þessi samsetning af merkjum gefur til kynna að sniðmátið sé virka sniðmátið fyrir kerfismyndaðan tölvupóst sem sendur er sjálfkrafa.

Til að breyta sniðmáti skaltu velja röðina og gera breytingar á sniðmátinu.

> [!NOTE]
> Hver viðtakandi tiltekinnar tegundar tölvupósts hefur sjálfgefið sniðmát. Öll hefðbundin Attract sniðmát eru settar sem sjálfgefna sniðmát þar til stjórnandinn býr til nýtt sniðmát fyrir tiltekna tegund af tölvupósti og setur það sem sjálfgefið sniðmát.

## <a name="create-a-template"></a>Búa til sniðmát

Til að búa til sniðmát skaltu velja **+ Nýtt sniðmát** í efra hægra horninu í sniðmátasafninu fyrir tölvupóst. Til að velja gerð tölvupósts sem þú ert að búa til sniðmátið fyrir skaltu velja viðtakandann, ferlið og viðburðurinn sem tölvupósturinn verður sendur fyrir. Veldu síðan **Búa til**.

Sniðmátið er opnað í breytingaskoðun og þú getur nefnt sniðmátið. Til dæmis, ef sniðmátið er ætlað til umsækjenda frá bandarískum háskóla, en efnið er skrifað á frönsku, gætir þú slegið inn **University\_US\_Francais** sem titilinn. Titillin, efnislínan og meginmálið fyrir hvaða sniðmát sem er, getur stutt tungumál fyrir utan ensku.

Ekki er hægt að breyta reitnum **Til** fyrir sniðmát vegna þess að þú hefur þegar valið viðtakandann þegar þú bjóst til sniðmátið fyrst.

Þú getur bætt við einstaklingum eins og **Ráðningaraðila** eða **Mannauðsstjóra** í afrit (Cc) línuna. Þegar tölvupósturinn er sendur er þessum hlutverkum sjálfkrafa skipt út fyrir viðeigandi notendur, byggt á samhengi starfsins.

Efnislínan og meginmálið styðja staðgengla. Þú getur sett inn staðgengla með því að slá inn **\#** og síðan velja viðeigandi staðgengla í fellilistanum fyrir sjálfvirka útfyllingu. Listi yfir tiltæka staðgengla birtist hægra megin á síðunni. Þegar tölvupósturinn er sendur eru staðgenglum sjálfkrafa skipt út frá samhengi starfsins og viðtakandans. Til dæmis inniheldur sniðmát fyrir tölvupóst sem sendur er til umsækjenda staðgengilinn \#{Umsækjandi\_Nafn}. Þegar tölvupósturinn er sendur til umsækjanda sem heitir Cameron verður þeim staðgengli skipt út fyrir nafnið Cameron.

Ritill meginmálsins er textaritill fyrir sniðinn texta sem leyfir þér að forma og sníða texta. Það leyfir þér einnig að setja inn tengla og akkeri.

Eftir að sniðmát er búið til fyrir tiltekna tegund af tölvupósti skaltu velja þrípunktahnappinn (**...**) í röðinni fyrir sniðmátið og stilla það sem sjálfgefið sniðmát.

## <a name="consume-templates"></a>Nota sniðmát

Þegar ráðningarteymið sendir tölvupóst, getur það notað sniðmát sem stjórnandinn bjó til. Ef mörg sniðmát hafa verið búin til fyrir tölvupóstinn sem notandi er að senda birtist fellilistinn í verkflæði tölvupóstssamsetningar. Sjálfgefið sniðmát er slegið inn sjálfkrafa, en notandinn getur valið annað sniðmát.

> [!NOTE] 
> Fyrir tölvupósta sem eru sendir sjálfkrafa er hægt að búa til mörg sniðmát. Hins vegar er aðeins hægt að velja eitt sniðmát sem virkt sniðmát. Vegna þess að þetta ferli kviknar af tilvikum getur aðeins stjórnandi ákveðið hvaða sniðmát ætti að nota, byggt á samsetningunni **Sjálfgefið** og **Sent sjálfkrafa** merkin í sniðmátasafninu.
