---
title: Bylgjuúthlutun
description: Þetta efnisatriði lýsir hvernig á að setja upp skref bylgjuúthlutunar, þ.á.m. hvernig á að virkja hliðstæðu vinnslu fyrir hana.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9c534f5e10f5797543d56ff4a5a7ada937edcb017228ebe395ae8a45efa10886
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781322"
---
# <a name="wave-allocation"></a>Bylgjuúthlutun

[!include [banner](../includes/banner.md)]

Bylgjuvinnsla getur reynst tímafrek og meirihluti vinnslutímans fer í úthlutunarskrefið og stofnskref vinnunnar.

Nú er hægt að keyra skrefin samhliða, sem getur aukið afköst bylgjuvinnslunnar og opnað fyrir meira gegnumstreymi af bylgjum í sama vöruhúsið. Þetta efnisatriði útskýrir hvernig á að setja upp úthlutunaraðferð bylgjunnar til að keyra samhliða. Frekari upplýsingar um hvernig á að setja upp stofnun vinnu fyrir samhliða keyrslu er að finna í [Áætla stofnun vinnu í bylgju](configure-wave-schedule-work-creation.md).

Áður fyrr var aðeins hægt að úthluta einni bylgju í einu í vöruhúsi. Þessi takmörkun hefur verið fjarlægð og skipt út fyrir nýja takmörkun sem aðeins læsir vörunni og víddunum sem eru fyrir ofan staðsetninguna í frátekningarstigveldinu. Víddir fyrir ofan staðsetninguna eru alltaf með afurðarvíddir. Til dæmis ef vara er skilgreind með því að nota *Lit*, þá er hægt að vinna samhliða úr afbrigðum fyrir *Rauða*, *Bláa* og *Gula*.

Þetta þýðir að ef verið er að úthluta sömu vörunni með sömu víddirnar fyrir ofan staðsetninguna af einni bylgju þurfa aðrar bylgjur að bíða til að fá læsingu á sömu vöru og víddum. Ef ekki er hægt að fá læsinguna í tíma mun villa koma upp og bylgjuvinnslan mistakast.

Bylgjan verður að keyra í runu til að geta notað hliðstæða vinnslu.

## <a name="performance-improvements"></a>Bætt afköst

Ávinningur afkasta vegna hliðstæðrar vinnslu fellur í tvo flokka:

- **Bætt gegnumstreymi** – Gegnstreymi á bylgjum eykst yfirleitt jafnvel þótt hliðstæð vinnsla sé ekki skilgreind, sérstaklega í aðstæðum þar sem engin skörun á vörum innan bylgjanna.
- **Endurbætur á úthlutun fyrir eina bylgju** – Prófanir á gögnum viðskiptavina hafa sýnt nærri 50% bætingu á afköstum þegar skipt er yfir í hliðstæða úthlutun. Hliðstæða vinnslan er gerð eftir vörum og víddum fyrir ofan staðsetninguna þannig að bætingar fara eftir því hversu margar mismunandi vörur bylgja inniheldur, tiltæku tölvukerfi og tímalengd úthlutunar í samanburði við tímann sem tekur að stofna vinnu.

## <a name="configure-parallel-allocation"></a>Skilgreina hliðstæða úthlutun

### <a name="warehouse-management-parameters"></a>Færibreytur vöruhúsakerfis

Til að nota hliðstætt úthlutunarferli skal fara í **Vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis**, opna flipann **Bylgjuvinnsla** og stilla eftirfarandi:

- **Runuflokkur bylgjuvinnslu** – Veljið runuflokkinn sem upprunaleg vinnsla bylgjanna á að nota. Vinnsla úthlutunar sem fylgir í kjölfarið verður hægt að gera með því að nota mismunandi runuflokka.
- **Vinna bylgjur í runu** – Stillið þetta á *Já* til að nota hliðstæða vinnslu.
- **Bíða eftir læsingu (ms)** – Sláið inn tímann í millisekúndum sem úthlutunarskref mun bíða eftir tilfangi kerfis sem er læst af öðru úthlutunarskrefi. Þegar farið er yfir þennan tíma er ekki unnið úr bylgjunni og villuboð birtist. Mælt er með að láta a.m.k. nokkrar sekúndur líða til að leyfa úthlutun á einni röklegri einingu að klárast.

Frekari upplýsingar um þessa og aðra valkosti bylgjuvinnslu á síðunni **Færibreytur vöruhúsakerfis** er að finna í [Færibreytur vöruhúss fyrir bylgjuvinnslu](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Vinnsluaðferðir bylgju

Til að setja upp hliðstæða vinnslu:

1. Farið í **Vöruhúsakerfi > Uppsetning > Bylgjur > Aðferðir bylgjuvinnslu**.
1. Veljið `allocateWave` aðferðina í hnitanetinu.
1. Á aðgerðasvæðinu skal velja **Skilgreining verks**.
1. Þá opnast síðan **Skilgreining verks eftir bókunaraðferð bylgju**. Þetta hnitanet sýnir hvert vöruhús fyrir sig þar sem `allocateWave` aðferðin hefur verið skilgreind. Hliðstæð vinnsla verður aðeins notuð fyrir vöruhús sem eru skráð. Notið hnappa aðgerðasvæðisins til að bæta við eða fjarlægja vöruhús úr hnitanetinu eftir þörfum. 
1. Fyrir hvert vöruhús skaltu velja eftirfarandi stillingar:
    - **Hámarksfjöldi runuverka** – Tilgreinið fjölda runuverka sem á að nota fyrir úthlutunina fyrir valið vöruhús. Ákjósanlegur fjöldi runuverka fer eftir tölvukerfinu og öðrum runuvinnslum sem verið að vinna úr á þjóninum. Prófanir á fjögurra kjarna umhverfi sem einblíndi á bylgjuvinnslu sýndu fram á að góðar niðurstöður fengust með því að nota átta verk.
    - **Runuflokkur bylgjuvinnslu** – Hægt er að nota ákveðna runuflokka fyrir mismunandi vöruhús til að leyfa úthlutunarferlinu að laga sig að hverju vöruhúsi.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Kveikja eða slökkva á hliðstæðri vinnslu í öllum lögaðilum

Mælt er með að stilla `allocateWave` aðferðina á að keyra hliðstætt yfir alla lögaðila vegna þess að það stuðlar að auknum afköstum bylgjuvinnslunnar. Frá og með Supply Chain Management útgáfu 10.0.7 verður eiginleikinn *Hliðstæð vinnsla bylgju fyrir aðferð bylgjuúthlutunar* virkjaður að sjálfgefnu fyrir allar nýjar og uppfærðar uppsetningar og ekki verður hægt að slökkva á þeim aftur. Þegar þessi eiginleiki hefur verið virkjaður gerist eftirfarandi:

- Aðferð `allocateWave` er uppfærð til að hafa með stillingu verkskilgreiningar sem gerir kleift að nota síðuna **Aðferðir bylgjuvinnslu** til að skilgreina fjölda verka sem munu keyra samtímis, sem jafngildir fjölda hliðstæðra vinnsla. Fyrir vikið er tíminn sem notaður er í skrefi bylgjuúthlutunar (sem er yfirleitt 30% til 60% af heildarvinnslutímanum) styttur um því sem nemur í grófum dráttum fjölda verka. Einnig er hægt að velja hvaða runu verður úthlutað til að vinna úr þessum verkum. Mikilvægt er að hafa í huga að allir lögaðilar verða grunnstilltir til að vinna úr bylgjum í runu. Fyrir vöruhúsin sem eru þegar skilgreind til að vinna úr bylgjum í runu og fyrir vöruhúsin sem eru þegar skilgreind til að nota `allocateWave` aðferðina í hliðstæðri vinnslu, verður fyrirliggjandi skilgreiningu haldið.
- Sjálfgefið er að allir nýju lögaðilarnir séu grunnstilltar til að vinna úr bylgjum í runu. Öll ný vöruhús með valkostinn **Ferli vöruhúsakerfis** virkjaðan verða með `allocateWave` aðferðina skilgreinda til að keyra í hliðstæðri vinnslu að sjálfgefnu.
- Á síðunni **Færibreytur vöruhúsakerfis** er **Vinna úr bylgjum í runu** stillt á *Já* og **Bíða eftir læsingu (ms)** er stillt á 15 sekúndur að sjálfgefnu. Þetta þýðir að allar bylgjur verða keyrðar í runu. Þegar bylgja er keyrð fær hún læsingu á vörunni og víddunum fyrir ofan staðsetningu í úthlutunarskrefinu. Þegar annað bylgjuvinnsluverk reynir að fá sömu læsingu fyrir sömu færslu er lokað á það þar til núverandi vinnslu er lokið. Stillingarnar **Bíða eftir læsingu (ms)** setja á hámarkstíma sem kerfið mun bíða áður en læsingin er opnuð.

Samhliða úthlutunarferli krefst þess að bylgjuvinnsla keyri í runu. Þess vegna verða afköst bylgjuvinnslunnar minnkuð ef slökkt er á stillingunni **Vinna bylgjur í runu**, sérstaklega ef bylgjuvinnsla notar hliðstætt ferli eins og skilgreint er af verkskilgreiningunni fyrir viðeigandi bylgjuaðferðir.

Ef þörf krefur er hægt að afturkalla hverja sjálfgefna stillingu fyrir sig þegar eiginleikinn *Samhliða bylgja fyrir úthlutunaraðferð bylgju* er sjálfkrafa virkjaður fyrir tilvikið. Til að gera þetta:

- Farðu í **Vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**. Í flipanum **Bylgjuvinnsla** skal nota æskileg gildi fyrir **Vinna bylgjur í runu** og **Bíða eftir læsingu (ms)**.
- Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Vinnsluaðferðir bylgju**. Veljið `allocateWave` aðferðina. Á aðgerðasvæðinu skal velja **Skilgreining verks** til að opna síðu sem sýnir hvert vöruhús þar sem aðferðin er stillt á að keyra í hliðstæðri vinnslu. Breytið eða eyðið fjölda runuverka og úthlutuðum runuflokki fyrir hvert birt vöruhús eftir þörfum.

## <a name="troubleshooting"></a>Úrræðaleit

### <a name="troubleshoot-using-the-infolog"></a>Úrræðaleit með upplýsingaskránni

Þars sem runurammi er notaður verða villur sem koma upp í bylgjuvinnslu sóttar sem hluti af upplýsingaskrám runuvinnslanna. Til að lesa runuvinnslur sem tengjast bylgju:

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið bylgjuna sem á að skoða.
1. Á aðgerðasvæðinu skal opna flipann **Bylgja** og úr flokknum **Bylgja** skal velja **Runuvinnslur**.

Bylgjuvinnsla leiðréttir sig sjálf þannig að allar villur sem vinnslan greinir eiga að vera tilkynntar með upplýsingaskránni.

Dæmigerð villa sem tengist hliðstæðri vinnslu gæti verið að tvær bylgjur reyni að úthluta sömu vörunni samtímis og önnur þeirra klárast ekki þannig að hin bylgjan getur ekki fengið læsingu innan tiltekins tíma. Ef þetta kemur upp mun skrá runuvinnslanna innihalda upplýsingar sem gefa til kynna að ekki hafi verið hægt að sækja læsingu fyrir vöruna, sem þýðir að það þarf að vinna aftur bylgjuna sem tókst ekki.

Vegna þess að vinnslan er í gangi í hliðstæðri vinnslu þarf að viðhalda gögnum í öðrum töflum til að rekja stöðu vinnslunnar. Þetta þýðir skrárnar fyrir runuvinnslurnar gætu innihaldið villur á borð við tvítekinn lykil.

Villurnar í runuverkunum eru einnig hluti af skrá runuvinnslanna. Mikilvægustu upplýsingarnar eru yfirleitt neðst.

Í sjaldgæfum tilfellum, til dæmis ef SQL-tenging rofnaði, er möguleiki á að bylgjuvinnslan endi í ósamkvæmri stöðu þar sem runuvinnslan virðist vera í gangi en vinnslan hefur stöðvast. Bylgjan ræður ekki við villur á borð við þessa, þannig að tilraunir til að hreinsa upp mislukkaðar bylgjur er gerð þegar næsta bylgja er keyrð. Annars, ef núverandi bylgja er í ósamkvæmri stöðu, skal fara í gegnum eftirfarandi skref:

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið bylgjuna sem þarf að hreinsa.
1. Á aðgerðasvæðinu skal opna flipann **Bylgja** og í flokknum **Bylgja** skal velja **Hreinsa bylgjugögn**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Úrræðaleit með framvindukladda bylgju

Ef valkosturinn **Stofna kladda fyrir framvindu bylgju** er virkjaður á síðunni **Færibreytur vöruhúsakerfis**, þá er kladdafærsla búin til í hvert skipti sem úthlutun vöru og vídda hennar hefst og lýkur. Aðeins ætti að virkja þennan kladda þegar þess gerist þörf, til dæmis við fyrstu prófun eða fyrir úrræðaleit. Þegar þessi valkostur er virkjaður er hægt að skoða kladdann með því að gera eftirfarandi skref:

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið bylgjuna sem á að skoða.
1. Á aðgerðasvæðinu skal opna flipann **Bylgja** og í flokknum **Bylgja** skal velja **Framvinda**.
