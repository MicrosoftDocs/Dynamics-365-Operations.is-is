---
title: Algengar spurningar um flipa umsjónar hönnunarbreytinga
description: Í þessu efnisatriði verða veitt svör við algengum spurningum um eiginleika hönnunarbreytingastjórnunar.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba489358ef2d74e816186f29956aea5538a2432825c7d949e7c9cc23d947b997
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714379"
---
# <a name="engineering-change-management-faq"></a>Algengar spurningar um flipa umsjónar hönnunarbreytinga

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði verða veitt svör við algengum spurningum um eiginleika hönnunarbreytingastjórnunar.

## <a name="should-i-track-the-version-in-transactions"></a>Á ég að rekja útgáfuna í færslum?

Þegar stofnaður er flokkur hönnunarbreytinga býður síðan **Upplýsingar um flokk hönnunarbreytingar** upp á valkost sem kallast **Rekja útgáfu í færslum**. Hvað er þessi stilling og hvað gerir hún?

- Ef valkosturinn **Rekja útgáfu í færslum** er stilltur á *Já* er reiturinn **Víddaflokkur** síaður þannig að hann sýnir aðeins vídarflooka þar sem útgáfa er virk vídd.
- Ef valkosturinn **Rekja útgáfu í færslum** er stilltur á *Nei* er reiturinn **Víddaflokkur** síaður þannig að hann sýnir aðeins vídarflooka þar sem útgáfuvíddin er **ekki** virk vídd.

### <a name="if-you-track-the-version-in-transactions"></a>Ef þú rekur útgáfuna í færslum

Fyrir hönnunarflokka þar sem þú hefur valið víddaflokk þar sem útgáfa er virk vídd muntu rekja útgáfur í færslum fyrir vörur í þeim flokki. Í þessu tilfelli verður hönnunarafurðin afurðarsniðmát og hver útgáfa afurðarinnar verður afurðarafbrigði sem notar vídd útgáfunnar. Hægt er að nota aðra víddir með útgáfuvíddinni.

Í þessu tilfelli verður litið á hverja hönnunarútgáfu sem afbrigði í öllum ferlum. Þess vegna, ef þú ert með ákveðið afbrigði í færslu (þannig að þú getir ákvarðað hvaða afbrigði var selt eða keypt), þarftu að hafa umsjón með birgðum fyrir hverja útgáfu, aðaláætlanagerð mun skipuleggja birgðir fyrir hverja útgáfu og svo framvegis. Ef útgáfa er tekin af markaði verður að breyta gildistíma hennar handvirkt - frá og til gildistíma - þannig að breytingin endurspeglist. Þú verður einnig að hafa umsjón með birgðum til að tryggja að ekki séu ónotaðar útgáfur af vörum í vöruhúsunum.

Þótt þessi valkostur geri kröfu um meiri stjórnun er samt mælt með honum ef þörf er á hárri rakningargetu á tilteknum útgáfum sem eru notaðar í hverri færslu.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Ef útgáfan er ekki rakin í færslum

Fyrir hönnunarflokka þar sem þú hefur valið víddaflokk þar sem útgáfa er **ekki** virk vídd muntu **ekki** rekja útgáfur í færslum fyrir afurðir í þeim flokki. Ef þú notar ekki neina aðra vídd, verður hönnunarafurðin aðgreind afurð í þessu tilviki. Afurðinni verður úthlutað útgáfu og hægt verður að hafa umsjón með upplýsingum um tilteknar útgáfur (til dæmis uppskriftum \[þeirra] og leið), en ekki verður hægt að rekja hvaða tiltekna útgáfa var notuð í hverri færslu. Gildistími hverrar útgáfu er tilgreindur í frá og til gildistímanum.

Mun auðveldar er að hafa umsjón með þessum valkosti vegna þess að ef ætlunin er að breyta úr einni útgáfu í aðra þarf eingöngu að gera nauðsynlegar breytingar á breytingaröð og því næst uppfæra til og frá dagsetningar gildistíma í hönnunarútgáfunni. Framleiðsluferlin munu síðan taka upp nauðsynlega uppskrift og leið fyrir afurðina (og tiltekna útgáfu hennar).

Flest fyrirtæki velja þennan valkost þar sem hann býður upp á útgáfu- og breytingastjórnun en bætir ekki við aukakostnaði við rakningu útgáfunnar í hverri færslu, í birgðastjórnun og við aðaláætlanagerð.

## <a name="which-fields-are-copied-from-the-released-item-template"></a>Hvaða reitir eru afritaðir úr útgefna atriðasniðmátinu?

Þegar hönnunarfyrirtæki stofnar hönnunarafurð er afurðin stofnuð sem útgefin afurð í hönnunarfyrirtækinu. Útgefin afurð sem er stofnuð er byggð á *útgefnum vörusniðmátum* sem eru valin. (Sniðmátið fyrir útgefna afurð er sjálft fyrirliggjandi losuð afurð.) Sniðmát útgefinnar afurðar er einnig notað þegar afurðin er losuð til rekstrarfyrirtækis. Í hverju tilviki skilgreinir útgefið vörusniðmát flest reitargildin fyrir útgefna afurð og þessi gildi koma frá tengdu síðunni **Upplýsingar um útgefnar afurðir**.

Eftirfarandi töflur sýna svæðin sem eru afrituð meðan á ferlunum stendur.

| Flýtiflipi | Reitir sem afritaðir eru við vörusköpun í hönnunarfyrirtækinu | Reitir sem eru afritaðir við losun til rekstrarfyrirtækis |
|---|---|---|
| **Almennt** | Allir reitir í hlutanum **Stjórnun** | Sömu reitir og eru afritaðir fyrir hönnunarfyrirtækið |
| **Innkaup** | Öll svæði | Allir reitir nema **Eining** |
| **Sala** | Allir reitir í eftirfarandi hlutum: **Sölupöntun**, **Stjórnun**, **Skattlagning**, **Uppfærsla á verði**, **Grunnsöluverð**, **Gjöld**, **Afslættir** og **Önnur afurð** | Allir sömu reitir sem eru afritaðir fyrir verkfræðifyrirtækið, nema **Eining** |
| **Erlend viðskipti** | Öll svæði | Öll svæði |
| **Stjórna birgðum** | Öll svæði og kaflar *nema* **Efnislegar víddir** og **Framleiðsluþyngd** | Allir sömu reitir sem eru afritaðir fyrir verkfræðifyrirtækið, nema **Eining** |
| **Hanna**, **Áætla**, **Umsjón með kostnaði**, **Umsjón verka**, **Fjárhagsvíddir** og **Vöruhús** | Öll svæði | Allir reitir nema **Uppskriftareining** |
| **Afurðarafbrigði** | Allir reitir í hlutanum **Sjálfgefið afurðarafbrigði** | Sömu reitir og eru afritaðir fyrir hönnunarfyrirtækið |

Auk reitanna sem sýndir eru í fyrri töflunni eru allar sjálfgefnar pöntunarstillingar afritaðar úr útgefnu vörusniðmáti, bæði þegar afurðin er búin til í hönnunarfyrirtækinu og þegar hún er gefin út í fyrirtæki í rekstri. (Til að skoða sjálfgefnar pöntunarstillingar fyrir útgefið vörusniðmát skal opna viðeigandi síðuna **Upplýsingar um útgefnar afurðir** og því næst, á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, skal velja **Sjálfgefnar pöntunarstillingar**.)

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Á ég að stofna sérstakan lögaðila fyrir hönnunarafurðir eða nota fyrirliggjandi lögaðila?

Viðskiptakröfur þínar ákvarða hvort stofna eigi nýjan lögaðila fyrir hönnunarafurðir.

Með því að búa til aðskilið hönnunarfyrirtæki er hægt að halda hönnunargögnum aðskildum og síðan bæta við breytingum þegar á þarf að halda fyrir staðbundna rekstrarfyrirtækið. Á þennan hátt er hægt að ná eftirfarandi markmiðum:

- Halda aðskildri einingu þar sem hönnunarafurðir eru stofnaðar og þeim stjórnað.
- Komið í veg fyrir að hönnunarafurðir birtist saman með hinum útgefnu afurðunum þar til þær eru tilbúnar og útgefnar.
- Aðskiljið á greinilegan hátt gögn sem er stýrt af hönnun og staðbundin gögn.

Á hinn bóginn ætti sennilega að nota fyrirliggjandi lögaðila sem hönnunarfyrirtæki ef eftirfarandi skilyrði eiga við um þig:

- Þú ert aðeins með einn lögaðila í kerfinu þínu og/eða þú þarft ekki að gera greinarmun á vörum sem verið er að hanna.
- Þú vilt ekki afrita sum gögn, svo sem tilfangaflokka, tilföng, aðgerðir og (kannski) svæði.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Hver er flokkurinn fyrir hönnunarútgáfur og afbrigði?

Nafnakerfið fyrir hönnunarafurðir og afurðarafbrigði virkar á eftirfarandi hátt:

- Fyrir hönnunarafurðir (þ.e. einkvæmu afurðina ef engar víddir eru notaðar eða afurðarsniðmátið ef einhverjar víddir eru notaðar) er nafnakerfi númerareglunnar skilgreint í flokki hönnunarafurðar. Þar er hægt að nota töluröð, textafasta og heiti eiginda og gildi.
- Fyrir hvert afbrigði hönnunarafurðar (ef hönnunarafurðin er afurðarsniðmát, eru afbrigði sett upp í flokki hönnunarafurðar þar sem víddaflokkur er tilgreindur) er nafnakerfi númerareglunnar fyrir hvert afbrigði skilgreint í víddaflokknum. Í því tilviki er hægt að nota afurðarkenni aðalsniðmátsins og víddargildin og heitin.
