---
title: Verkstjórnun
description: Þessi grein útskýrir verkefnastjórnunarvirknina sem er fáanleg í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c567f6d74e6ff87a72ff3b8663ca3a291dff3abb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897865"
---
# <a name="task-management"></a>Verkstjórnun

[!INCLUDE [PEAP](../includes/peap-1.md)]

Verkefnastjórnun gerir þér kleift að búa til verkefni sem þarf að ljúka til að ráða (um borð), segja upp (fyrir utan) og flytja (skipti) starfsmenn. Verkefnastjórnun notar hugtakið gátlista. Gátlisti er yfir lista yfir verkefni um borð, brottför eða umskipti. Verkefnastjórnun notar gátlista til að flokka verkefni saman og úthluta þeim á einstaklinga eða hópa. Virkni gátlistans fyrir um borð, brottför og umskipti er svipuð.

## <a name="checklist-overview"></a>Yfirlit yfir gátlista

Gátlisti er hópur verkefna. Gátlistar gefa þér sveigjanlega leið til að flokka verkefni og þá er hægt að endurnýta þá (til dæmis þegar þú ræður fleiri starfsmenn). Þú getur búið til eins marga gátlista og þú þarft og þú getur úthlutað sömu verkefnum á marga gátlista.

### <a name="examples"></a>Dæmi

Eftirfarandi dæmi sýna hvernig gátlista er hægt að nota í inngönguferlinu. Hins vegar, vegna þess að virkni gátlistans fyrir um borð, brottför og umskipti er svipuð, eiga upplýsingarnar einnig við um brottför og umskipti.

Sem hluti af inngönguferlinu geta starfsmenn mannauðs (HR) búið til verkefni sem fylgjast með framvindu komandi og nýráðinna starfsmanna. Vegna þess að inngönguferlið gæti verið breytilegt, eftir staðsetningu starfsmanns eða landfræðilegri staðsetningu, geturðu búið til marga gátlista um borð til að koma til móts við mismunandi ráðningaraðstæður.

**Dæmi 1**

Sérhver starfsmaður sem er ráðinn í Bandaríkjunum verður að ljúka verkefnum eins og að fylla út eyðublöð fyrir staðgreiðslu skatta. Hins vegar gætu verkefni eins og úthlutun fyrirtækjabíls aðeins átt við um starfsfólk á stjórnendastigi. Í þessu tilviki er hægt að búa til tvo gátlista um borð: **Starfsmenn með aðsetur í Bandaríkjunum** og **Aðeins stjórnendur**. Síðan, þegar miðstigsstjóri er ráðinn í Bandaríkjunum, þá **Starfsmenn með aðsetur í Bandaríkjunum** gátlisti er valinn. Hins vegar, þegar framkvæmdastjóri er ráðinn til starfa í Bandaríkjunum, eru báðir gátlistarnir valdir til að tryggja að öll tilskilin verkefni um borð séu unnin.

**Dæmi 2**

Í fyrirtæki eru bæði árstíðabundnir starfsmenn og fastir starfsmenn í fullu starfi. Þótt sum verkefni (eins og að sannreyna komutíma nýja starfsmannsins) eigi við um starfsmenn af báðum gerðum, þá eiga sum viðbótarverkefni aðeins við um venjulega starfsmenn í fullu starfi. Í þessu tilviki geturðu búið til tvo gátlista. Báðir gátlistarnir innihalda þau verkefni sem eiga við um bæði árstíðabundið og venjulegt fullt starf, en aðeins einn gátlisti inniheldur þau verkefni sem eru sértæk fyrir fasta starfsmenn í fullu starfi.

## <a name="task-management-workspace"></a>Verkefnastjórnun vinnusvæði

The **Verkefnastjórnun** vinnusvæði listar öll verkefni sem hafa verið úthlutað einstaklingum í inngöngu-, brottför- og umbreytingarferlum. Til að skoða verkefnin fyrir ferli skaltu velja viðeigandi flipa í efra vinstra horninu: **Um borð**, **·**, eða **Umskipti**. Sjálfgefið er að aðeins HR sérfræðingar hafa aðgang að **Verkefnastjórnun** vinnurými.

The **Um borð** flipinn inniheldur a **Byrjar bráðum** listi sem sýnir komandi starfsmenn og a **Nýlegar ráðningar** lista sem sýnir nýráðna starfsmenn. Í báðum listum er aðeins hægt að velja einn starfsmann. Þegar starfsmaður er valinn birtast öll verkefni sem tengjast inngöngu þess starfsmanns hægra megin á síðunni. The **Um borð** flipinn inniheldur einnig **Öll verkefni** listi sem sýnir öll verkefni fyrir alla komandi eða nýlega ráðna starfsmenn. Að lokum inniheldur það lista yfir tímabær verkefni og lista yfir verkefni sem eru úthlutað til núverandi notanda.

The **Útför** flipinn inniheldur lista yfir starfsmenn sem eru að hætta hjá fyrirtækinu og lista yfir starfsmenn sem þegar hafa hætt í fyrirtækinu. Í báðum listum er aðeins hægt að velja einn starfsmann. Þegar starfsmaður er valinn birtast öll verkefni sem tengjast brottför viðkomandi starfsmanns. The **Útför** flipinn inniheldur einnig **Öll verkefni** listi sem sýnir öll verkefni fyrir alla starfsmenn sem hætta eða hætta. Að lokum inniheldur það lista yfir tímabær verkefni og lista yfir verkefni sem eru úthlutað til núverandi notanda.

The **Umskipti** flipi inniheldur **Öll verkefni** listi sem sýnir öll verkefni fyrir alla starfsmenn sem munu skipta um stöðu eða hafa nýlega skipt um stöðu. Það er líka listi yfir tímabær verkefni og listi yfir verkefni sem eru úthlutað til núverandi notanda.

Á öllum þremur flipunum geta starfsmannaaðstoðarmenn og stjórnendur lokið eftirfarandi verkefnum:
- Notaðu gátlista fyrir starfsmann
- Uppfærðu stöðu verkefnis
- Endurúthlutaðu verkefni
- Uppfærðu gjalddaga verks

> [!NOTE]
> Sjálfgefið er **Um borð** flipinn sýnir starfsmenn sem voru ráðnir á síðustu sjö dögum. Til að breyta þessari stillingu, á **Stærðir mannauðs** síðu, á **Almennt** flipa, í **Nýlegar ráðningar** reit, sláðu inn tímaramma. Upplýsingarnar í **Nýlegar ráðningar** Listi er hægt að sýna fyrir ákveðinn fjölda daga, mánaða eða ára. Til dæmis, til að skoða lista yfir starfsmenn sem voru ráðnir á síðustu 14 dögum skaltu stilla **Tímabil** sviði til **14** og **Eining** sviði til **Dagar**.
> Á **Stærðir mannauðs** síðu geturðu einnig uppfært tímabil fyrir lista yfir starfsmenn sem hætta og hætta sem eru sýndir á **Útför** flipa. Þessar stillingar eiga einnig við um **Starfsmannastjórnun** vinnurými.

## <a name="setting-up-tasks"></a>Að setja upp verkefni

Þú getur búið til verkefni fyrir sig og síðan endurnýtt þau í mörgum gátlistum. Til að búa til verkefni, á **Uppsetning um borð** síðu, á **Verkefni** flipa, veldu **Nýtt**.

Að öðrum kosti geturðu bætt verkefnum beint við gátlista. Til að bæta verkefni við gátlista, á **Uppsetning um borð** síðu, á **Tékklisti** flipa, búðu til annað hvort nýjan gátlista til að bæta verkefninu við eða bæta verkefninu við núverandi gátlista.

> [!NOTE]
> Ef þú bætir verkefni beint á gátlista geturðu ekki endurnýtt það í öðrum gátlistum.

Eftirfarandi tafla lýsir reitunum sem eru tiltækir þegar þú býrð til verkefni með annarri hvorri aðferð.

| Reitur           | Lýsing |
|-----------------|-------------|
| Verk            | Sláðu inn heiti verkefnisins. |
| Lýsing     | Sláðu inn lýsingu á verkefninu. |
| Valfrjálst        | Tilgreindu hvort verkefnið sé valfrjálst og sé eingöngu til upplýsinga. |
| Verkefnatengill       | Sláðu inn vefslóð ytri vefsíðu eða tiltekinnar síðu í appinu þar sem notandinn ætti að klára verkefnið. Fyrir frekari upplýsingar, sjá [Verkefnistenglar](#task-links) kafla. |
| Úthlutunargerð | Hægt er að úthluta verkefnum til ákveðins starfsmanns, stöðu eða hóps staða, yfirmanns viðkomandi starfsmanns (þ.e. starfsmannsins sem er hluti af inngöngu-, brottför- eða breytingaferlinu) eða viðkomandi starfsmanns. Veldu tegund verkefnis. Fyrir frekari upplýsingar, sjá [Verkefnagerðir](#assignment-types) kafla. |
| Úthlutað til     | Veldu tiltekinn starfsmann, stöðu eða hóp af stöðum til að úthluta verkefninu til. |
| Tengiliður  | Tilgreindu þann sem á að hafa samband við ef spurningar vakna um verkefnið. |
| Gjalddagajöfnun | Tilgreindu fjölda daga fyrir eða eftir inngöngu-, uppsagnar- eða umbreytingardagsetningu sem verkefnið á að skila. Fyrir frekari upplýsingar, sjá [Gjalddagar verks og reiturinn Gjalddagajöfnun](#task-due-dates-and-the-due-date-offset-field) kafla. |
| Leiðbeiningar    | Sláðu inn leiðbeiningar til að klára verkefnið. Fyrir frekari upplýsingar, sjá [Leiðbeiningar](#instructions) kafla. |

### <a name="task-links"></a>Verkefnistenglar

Verkatengill veitir tengil á ytri vefsíðu eða síðu í Dynamics 365 appinu. Þú getur tilgreint verktengil ef sá sem er úthlutað verki ætti að fara á tiltekna vefsíðu eða ákveðna síðu í Dynamics 365 appinu til að klára það verkefni. Þegar þú býrð til verktengil geturðu valið einn af eftirfarandi valkostum:

- **Valmyndaratriði** – Ef þú velur þennan valkost birtist listi yfir allar síður í Dynamics 365 appinu. Veldu síðu á listanum.
- **URL** – Ef þú velur þennan valkost skaltu slá inn vefslóð vefsíðunnar sem þú vilt að sá sem er úthlutað verkefninu fari á. Tilgreind síða getur verið síða sem er ekki hluti af Dynamics 365 appinu.
- **Upplýsingar um starfsmann** – Ef þú velur þennan valkost skaltu velja einn af eftirfarandi valkostum:

    - **Sjálfsafgreiðsluaðgerðir starfsmanna** – Þessi valkostur sýnir lista yfir síður sem eru tiltækar á **Sjálfsafgreiðsla starfsmanna**. Notaðu það ef verkefnið sem var úthlutað starfsmanni um borð þarf að vera lokið í **Sjálfsafgreiðsla starfsmanna**. Til dæmis, ef þú vilt að starfsmaðurinn slær inn persónulegar tengiliðaupplýsingar sínar skaltu velja **Sjálfsafgreiðsluaðgerðir starfsmanna**, og veldu síðan **Persónulegar upplýsingar&gt; Persónuupplýsingar**.
    - **Aðgerðir starfsmannastjórnunar** – Þessi valkostur sýnir lista yfir síður sem tengjast skráningu starfsmanns, en eru ekki aðgengilegar starfsmanninum. Til dæmis, ef þú vilt að eigandi verkefna setji inn upplýsingar sem eru sérstakar fyrir starfsmann um borð, svo sem upplýsingar um launakjör, veldu **Aðgerðir starfsmannastjórnunar**, og veldu síðan **Bætur&gt; Fastar bætur**.

### <a name="assignment-types"></a>Verkefnagerðir

Þegar starfsmaður er ráðinn, sagt upp eða fluttur til er hægt að velja einn eða fleiri gátlista. Eftir að gátlisti hefur verið valinn og ráðningar-, uppsagnar- eða flutningsferlinu er lokið eru verkefni búin til og þeim úthlutað til notenda til að fylgjast með framförum.

Þegar verkefni er búið til er því úthlutað til ákveðins notanda. Notandinn sem verkefni er úthlutað á fer eftir úthlutunargerðinni sem er valin fyrir það verkefni. Eftirfarandi gildi eru fáanleg í **Tegund verkefnis** reit:

- **Vinnumaður** – Úthlutaðu verkefninu til ákveðins starfsmanns. Eftir að þú hefur valið þetta gildi skaltu velja starfsmanninn í **Úthlutað til** sviði.
- **Staða** – Úthlutaðu verkefninu á ákveðna stöðu. Eftir að þú hefur valið þetta gildi skaltu velja staðsetningu í **Úthlutað til** sviði.

    Til dæmis mun upplýsingatæknifræðingur alltaf sjá um að útbúa fartölvu fyrir nýjan starfsmann. Í þessu tilviki, þegar þú býrð til fartölvustillingarverkefnið skaltu velja **Staða** sem úthlutunartegund og veldu síðan **upplýsingatæknifræðingur** sem staða. Síðan, þegar starfsmaður er ráðinn, og gátlistinn er úthlutað, er fartölvustillingarverkefninu úthlutað til hvaða starfsmanns sem er í upplýsingatækniverkfræðingsstöðu á þeim tíma þegar ráðningaraðgerðin er slegin inn.

- **Hópur** – Úthlutaðu verkefninu í hóp staða (verkefnahópur). Eftir að þú hefur valið þetta gildi skaltu velja hópinn í **Úthlutað til** sviði. Fyrir frekari upplýsingar, sjá [Uppsetning verkefnahópa (valfrjálst)](#setting-up-assignment-groups-optional) kafla.
- **Framkvæmdastjóri** – Úthlutaðu verkefninu til yfirmanns starfsmanns sem verið er að ráða, segja upp eða flytja til.

    > [!IMPORTANT]
    > Þegar gátlisti er notaður, ef engin staða er í augnablikinu úthlutað starfsmanni sem ráðinn var, sagt upp eða fluttur, er ekki hægt að ákvarða yfirmanninn. Í þessu tilviki er verkefninu úthlutað eiganda gátlistans. Fyrir frekari upplýsingar, sjá [Að setja upp gátlista](#setting-up-checklists) kafla.

- **Starfsmaður** – Úthluta starfsmanninum sem verið er að ráða, segja upp eða flytja til.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Gjalddagar verks og reiturinn Gjalddagajöfnun

Gjalddagar verkefna eru byggðir á upphafsdegi ráðningar, uppsagnardegi eða umbreytingardagsetningu. Sumum verkefnum þarf að ljúka fyrir upphafsdag starfsmanns, en öðrum verkefnum er hægt að ljúka eftir. Þegar þú skilgreinir verkefni stillirðu **Gjalddagajöfnun** reit til að tilgreina gjalddaga sem er miðað við upphafsdag, uppsagnardagsetningu eða umbreytingardagsetningu. Til dæmis þarf upplýsingatæknifræðingur að útbúa fartölvu fyrir nýjan starfsmann tveimur dögum fyrir upphafsdag þess starfsmanns. Í þessu tilviki, þegar þú býrð til fartölvustillingarverkefnið skaltu stilla **Gjalddagajöfnun** sviði til **-2**. Síðan, ef upphafsdagur starfsmanns er 5. maí, á verkefnið að skila 3. maí.

> [!NOTE]
> Gjalddaga er hægt að breyta eftir að verkefnið er búið til.

Gjalddagar eru reiknaðir út frá dagatalinu sem tengist gátlistanum. Fyrir frekari upplýsingar, sjá [Að setja upp gátlista](#setting-up-checklists) kafla.

### <a name="instructions"></a>Leiðbeiningar

Flókin verkefni gætu þurft mörg skref eða sá sem framkvæmir verkefnið gæti þurft að veita frekari upplýsingar. Í **Leiðbeiningar** reit geturðu slegið inn leiðbeiningar eða viðbótarupplýsingar til að hjálpa þeim sem er úthlutað til að klára það.

## <a name="setting-up-checklists"></a>Að setja upp gátlista

Gátlisti er hópur verkefna. Þú getur búið til eins marga gátlista og þú þarft og þú getur úthlutað sömu verkefnum á marga gátlista. Þegar þú býrð til gátlista tilgreinir þú eiganda og dagatal.

Ef **Tegund verkefnis** reit fyrir verkefni er stillt á **Staða**, **·**, eða **Hópur**, en enginn ákveðinn einstaklingur er hægt að leiða af verkefnagerðinni, verður verkefninu úthlutað til eiganda gátlistans. Hér eru nokkur dæmi um aðstæður þar sem verkefnum verður úthlutað til eiganda gátlistans:

- Engin staða er skipuð þeim starfsmanni sem verið er að ráða eða segja upp. Vegna þess að starfsmaðurinn hefur ekki úthlutun í stöðu er ekki hægt að ákvarða yfirmann hans.
- The **Tegund verkefnis** reiturinn er stilltur á **Staða**, en engum starfsmanni er úthlutað í stöðuna á þeim tíma þegar verkefnið er stofnað. Til dæmis, the **Uppsetning fartölvu** verkefni er úthlutað stöðunúmeri 000876 (**Sérfræðingur í tækniaðstoð**). Á þeim tíma sem starfsmaður er ráðinn er enginn starfsmaður skipaður í stöðu 000876. Þess vegna verður verkefni búið til fyrir eiganda gátlistans.
- The **Tegund verkefnis** reiturinn er stilltur á **Hópur**, en enginn starfsmaður er skipaður í stöðurnar í hópnum á þeim tíma þegar verkefnið er stofnað.

Dagatalið sem er tilgreint fyrir gátlista er notað til að reikna út gjalddaga verkefna sem eru hluti af þeim gátlista. Virkir og óvirkir dagar eru skilgreindir í uppsetningu dagatalsins. Virkir dagar eru teknir með þegar gjalddagi verkefna er reiknaður og óvirkir dagar eru undanskildir. Óvirkir dagar telja helgar og frídaga. 

Eftir að dagatal er sett upp er það tengt við gátlistasniðmát. Þannig er gjalddagi hvers verks á gátlistanum reiknaður út á sama hátt. Þú getur sett upp mörg dagatöl, en aðeins eitt dagatal getur verið tengt hverjum gátlista.

## <a name="setting-up-assignment-groups-optional"></a>Setja upp verkefnahópa (valfrjálst)

Stundum ber hópur einstaklinga ábyrgð á verkefni. Til dæmis gæti hópur upplýsingatæknistarfsmanna verið ábyrgur fyrir því að undirbúa fartölvur fyrir nýráðningar.

Til að setja upp verkefnahóp skaltu fylgja þessum skrefum.

1. Á **Hópverkefni** síðu, veldu **Nýtt**.
1. Sláðu inn nafn (td **IT fartölva**) og lýsingu fyrir hópinn.
1. Veldu **Vista**.
1. Á **Meðlimir** Flýtiflipi, veldu **Bæta við**.
1. Í **Stöður** reit, veldu allar stöður sem bera ábyrgð á verkefninu.

Eftir að verkefnahópur er búinn til er hann tiltækur fyrir val þegar verkefni er búið til. Til að velja ákveðinn hóp fyrir verkefni verður þú að velja **Hópur** í **Tegund verkefnis**. Hópurinn sem þú bjóst til verður síðan tiltækur fyrir val í **Úthlutað til** sviði.

> [!IMPORTANT]
> Ef verkefni er úthlutað í hóp er verkefnið merkt sem **Lokið** þegar einn í hópnum klárar það. Verkefni eru búin til við ráðningu, uppsögn eða umskipti. Þær eru búnar til fyrir notendur sem eru úthlutaðir í stöður sem eru með í hópnum.

## <a name="setting-up-task-groups-optional"></a>Uppsetning verkefnahópa (valfrjálst)

Um borð, brottför eða umbreytingarferli geta falið í sér mörg verkefni. Til að auðvelda þér að úthluta öllum nauðsynlegum verkefnum á gátlista geturðu búið til valfrjálsa verkefnahópa til að flokka tengd verkefni. Til dæmis verða starfsmanna-, upplýsingatækni- og launadeildir hver um sig að ljúka sérstökum verkefnum til að ráða nýjan starfsmann. Þess vegna býrðu til eftirfarandi verkefnahópa: **HR**, **·**, og **Launaskrá**. Síðan, þegar þú býrð til verkefni, geturðu tengt einn af þessum verkhópum við það.

Þegar þú vilt bæta verki við gátlista geturðu síað verkefnalistann eftir verkefnahópnum sem viðkomandi verkefni er úthlutað. Til dæmis, þegar þú býrð til gátlistasniðmát geturðu síað listann þannig að aðeins upplýsingatækniverkefnum sem eru úthlutað til **ÞAÐ** verkefnahópar eru sýndir. Þess vegna getur þú tryggt að aðeins viðkomandi upplýsingatækniverkefni séu valin.

## <a name="using-checklists"></a>Notkun gátlista

Þegar starfsmaður er ráðinn, sagt upp eða fluttur er hægt að velja einn eða fleiri gátlista. Gjalddagar verkefna og úthlutun starfsmanna eru búnar til eftir að ráðningar-, uppsagnar- eða umbreytingarferli er lokið. Til dæmis, þegar þú velur **Ráða** eða **Leigðu og bættu við upplýsingum** hnappinn eru verkefni búin til fyrir einstaklinga, byggt á verkefnagerð.

Gjalddagi er úthlutað á hvert verkefni með því að bæta við eða draga frá gjalddagajöfnun frá upphafsdegi starfsmanns. Fyrir frekari upplýsingar, sjá [Gjalddagar verks og reiturinn Gjalddagajöfnun](#task-due-dates-and-the-due-date-offset-field) kafla.

Ef þú ert að nota starfsmannaaðgerðir eru verkefnin búin til þegar **Heill** hnappur er valinn eða aðgerðin er samþykkt.

Í **Verkefnastjórnun** vinnusvæði, þú getur sett gátlista á starfsmann með því að velja starfsmann á einföldu listasíðunni eða upplýsingasíðunni og velja síðan **Notaðu gátlista**. Verðmæti **Áætluð dagsetning** reiturinn verður notaður til að reikna út gjalddaga verkefna. Venjulega ætti markdagsetningin að passa við ráðningar-, uppsagnar- eða breytingadag starfsmanns.

Einnig er hægt að setja gátlista fyrir starfsmann með því að opna þeirra **Vinnumaður** síðu og velja **Gátlistar** á matseðlinum.

## <a name="completing-tasks"></a>Að klára verkefni

**Á síðunni Sjálfsafgreiðsla** starfsmanns getur starfsmaður skoðað öll verk sem þeim er úthlutað. Fyrir hvert úthlutuð verk **eru gildi verks**, **lýsingar**, **leiðbeininga** og **tengiliðar** sýnd. Að auki, fyrir hvert verk, getur starfsmaðurinn opnað tengda ytri vefsíðu eða tengda síðu í forritinu Dynamics 365.

Einnig er hægt að birta verk á sjálfgefna mælaborðinu. Verk birt á sjálfgefna mælaborðinu:
1. Fara í **notendavalkosti – Kjörstillingar – Verkefnastjórnun** 
2. Velja skal skjáverkin **á sjálfgefnu mælaborði** í **Á**.  

>[!Note] 
>**Kveikja verður á eiginleikanum Verkstjórnun** í **Eiginleikastjórnun** til að hægt sé að birta valkostinn í **valkostum** notanda.

Hægt er að merkja verk sem **Í vinnslu**, **Hætt við** eða **Lokið**. Ef verki var úthlutað á flokk verður það merkt sem **Lokið** þegar einn aðili í hópnum lýkur því.

Einnig er hægt að endurúthluta verkefnum.
