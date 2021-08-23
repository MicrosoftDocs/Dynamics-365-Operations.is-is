---
title: Tæki, markaður og landfræðileg miðun
description: Þetta efnisatriði lýsir því hvernig á að búa til, breyta og stjórna notendahópum og markhópum í Microsoft Dynamics 365 Commerce vefsmiðnum með því að nota upplýsingar um tæki, markað og landfræðilega staðsetningu.
author: sushma-rao
ms.date: 07/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: 3ecc04c97b42b17f257aa40f665136c70de398748b9bda0da860c7000c062807
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730852"
---
# <a name="device-market-and-geolocation-targeting"></a>Tæki, markaður og landfræðileg miðun

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að búa til, breyta og stjórna notendahópum og markhópum í Microsoft Dynamics 365 Commerce vefsmiðnum með því að nota upplýsingar um tæki, markað og landfræðilega staðsetningu.

Dynamics 365 Commerce gerir þér kleift að sérsníða innihald síðunnar þinnar (sem kallast *markhópar*) fyrir tiltekna hópa viðskiptavina (sem kallast *notendahópar*) til að auka þátttöku og ánægju notenda. Hægt er að stofna notendahóp eða markhóp fyrst. Árangursrík markmiðasetning krefst hins vegar beggja þessara þátta.

Þú býrð til og hefur umsjón með notendahópum í vefsmið Commerce út frá gögnum viðskiptavinar, t.d. staðsetningu, upplýsingar um tæki, stöðu innskráningar og aðrar gagnvirkar afleiddar upplýsingar frá beiðnum viðskiptavina á netinu. Þú býrð einnig til og hefur umsjón með markhópum í einingum rafrænna viðskipta og brota í vefsmið Commerce.

**Fyrirvari:** Þú berð ábyrgð á því að nota þennan eiginleika í samræmi við öll viðeigandi lög og reglugerðir, þ.m.t. þau sem tengjast markmiðasetningu og prófílun. 

## <a name="audiences"></a>Markhópar

Notendahópur er hópur notenda og aðild að hópnum ræðst af gagnvirkum reglum. Þessar reglur eru einföld rökfræðileg próf sem eru keyrð gagnvart upplýsingum sem eru tiltækar í beiðnum viðskiptavina eða öðrum tiltækum hlutum. Þú getur sameinað margar reglur með því að nota OG/EÐA virknitáknið.

Commerce styður staðbundið grunnhluta á borð við tækjaupplýsingar, stöðu innskráningar, tilvísanda og færibreytur fyrirspurnarstrengs. Það styður einnig stækkanlega hluta í gegnum tengingar við veitur þriðja aðila.

### <a name="basic-segments"></a>Grunnhlutar

Eftirfarandi hlutar eru sjálfgefið í boði og geta verið með í skilgreiningum notendahópa:

- **Innskráningarstaða** – Prófaðu hvort notandi sé auðkenndur.
- **Verkvangur tækis** – Prófaðu fyrir eftirfarandi tegundir tækja:

    - Farsími
    - Skjáborð
    - Spjaldtölva
    - Annað

- **Stýrikerfi tækis** – Prófaðu fyrir eftirfarandi stýrikerfum:

    - Windows
    - Linux
    - iOS
    - Android, Annað

- **Færibreyta fyrirspurnarstrengs** – Prófaðu fyrir hvort par lyklagildis sé til staðar í færibreytu fyrirspurnarstrengs fyrir vefslóð beiðni. Til dæmis, fyrir vefslóðina `www.fabrikam.com/en-us/request?promo=true`, er hægt að skrifa reglu til að prófa að færibreyta **kynningar** hafi gildið **satt**.
- **Kaka** – Próf kökugildi sem er stillt fyrir lénið í vefslóð beiðninnar. Til dæmis gæti beiðni frá Fabrikam.com innihaldið köku sem hefur nafnið **CustomLayout** og gildið **1**. Kökuprófið athugar hvort til sé kaka en býr ekki til slíka sérstaklega. Í fyrra dæminu verður JavaScript að hafa áður stillt **CustomLayout** kökuna úr annarri einingu eða einhverju öðru viðskiptaferli.

    > [!NOTE]
    > Gættu þess að notkun þín á vefkökum sé í samræmi við gildandi lög.

- **Tilvísandi** – Ef notandi fylgir tengli til að biðja um síðuna er tilvísandinn vefslóð síðunnar sem hýsti tengilinn.

### <a name="extensible-segments"></a>Stækkanlegir hlutar

Commerce gerir þér kleift að stækka lista yfir tiltæka hluta með því að tengjast við þriðja aðila sem bjóða upp á hluta. Þjónustuaðili hlutar mun útskýra hlutagerðir sem eru í boði. Til að fá frekari upplýsingar um hvernig á að tengjast þjónustuveitu sem býður upp á landfræðilega staðsetningu eða hluta skal skoða [Skilgreina og virkja tengla](e-commerce-extensibility/connectors.md).

> [!NOTE]
> - Ef utanaðkomandi þjónustuveita er virkjuð gæti hún tengst við þjónustu sem er með afköst sem erfitt er að spá fyrir. Til að tryggja betri notandaupplifun, ef notandi biður um síðu sem inniheldur markmiðasetningu og sú síða vísar í notendahóp sem athugar þriðja aðila sem býður upp á þjónustuveitu fyrir hluta, er sjálfgefin útgáfa síðunnar sýnd.
> - Notandinn verður að samþykkja að leyfa kökur. Vafri notandans biður síðan um alla hluta frá viðeigandi þjónustuveitum og niðurstöðurnar eru settar í köku sem er skilað til notandans. Síðari beiðnir á síðuna munu nota þessar upplýsingar til að birta notandanum markvert efni. Frekari upplýsingar er að finna í [Reglufylgni köku](cookie-compliance.md).

**Fyrirvari:** Ef þú virkjar þennan eiginleika verður gögnum þínum deilt með kerfum þriðja aðila sem þú velur. Þú stjórnar því hvaða gögn, ef einhver eru, þú lætur þriðja aðilanum í té. Þú skilur að meðhöndlun gagna og fylgni við staðla þriðja aðila gæti verið frábrugðin stöðlum Microsoft Dynamics 365 Commerce. Persónuvernd þín skiptir Microsoft máli. Til að fá nánari upplýsingar skaltu lesa [Tilkynning um persónuvernd og kökur](https://privacy.microsoft.com/privacystatement).

### <a name="create-an-audience-in-site-builder"></a>Stofna notendahóp í vefsmið

Til að búa til notendahóp í vefsmið Commerce skal fylgja þessum skrefum.

1. Á yfirlitssvæðinu til vinstri skal velja **Notendahópar**.
1. Veljið **Nýtt**.
1. Færðu inn heiti fyrir notendahópinn. Þú getur einnig bætt við merkjum og lýsingu.
1. Veldu **Stofna** og síðan **Bæta við nýjum reglubálki**. Reglubálkur er safn af reglum sem eru sameinaðar með OG-skilyrðum. Þú getur líka búið til marga reglubálka sem eru með EÐA-skilyrðum á milli þeirra.
1. Veldu gagnaveitu fyrir hlutana þína og tilgreindu síðan heiti hlutans, virknitáknið og gildin. Þú getur búið til og eytt fleiri reglum í reglubálki eða þú getur búið til ðg eytt heilum reglubálkum. Þú getur einnig fært reglubálka upp eða niður eftir þörfum.

    > [!NOTE]
    > Þú getur verið með allt að 100 gildi í lista og hvert listaatriði getur innihaldið allt að 50 stafi.

1. Þegar skilgreiningu notendahópsins er orðin góð skaltu velja **Ljúka við breytingar**. Þú getur síðan valið **Birta** til að bjóða upp á notendahópinn til að nota í markhópi í rauntíma. Einnig geturðu birt notendahópinn ásamt markhópnum. 

Til að breyta notendahópi skaltu velja tengilinn fyrir hann í flipanum **Notendahópar** og síðan velja **Breyta** í ritli notendahópsins sem birtist. Til að skoða lista yfir markhópa og síður sem vísa í notendahóp skal velja notendahópinn í listayfirliti notendahópsins og síðan velja **Skoða úthlutanir**. Til að eyða notendahópi úr listayfirliti notendahópa eða ritli notendahóps skal taka hann úr birtingu ef hann var birtur og síðan velja **Eyða** á skipanastikunni.

> [!NOTE]
> Notendahópar eru hugmynd á svæðisstigi í vefsmið Commerce. Þú getur deilt sama notendahópnum í mörgum markhópum.

## <a name="targets"></a>Mark

Markhópur er notandaupplifun sem sýnir meðlimi í einum eða fleiri völdum notendahópum. Hann getur falið í sér breytingar á einni eða fleiri einingum á síðu eða í broti. 

Þú getur skilgreint áætlun fyrir markhópana þína til að tilgreina hversu lengi þeir eiga að haldast virkir. Athugaðu að þessi aðgerð er aðskilin frá þeirri aðgerð að skipuleggja birtingarhóp sem ákvarðar hvenær safn efnis verður birt. Þú getur einnig forskoðað markhópana þína til að sjá hvernig þeir munu líta út hjá meðlimum valinna notendahópa. Þú getur auk þess forgangsraðað markmiðum þínum til að tilgreina hvaða markmið ætti að sýna ef til árekstra kemur.

### <a name="create-a-target"></a>Búa til markhluta

Til að búa til ytra lag markhóps fyrir síðueiningar í vefsmið Commerce skal fylgja þessum skrefum.

1. Í vinstri stýriglugganum velurðu **Síður**. Veldu síðan tengilinn fyrir síðuna sem hefur einingarnar sem þú vilt miða á.
1. Veldu **Breyta** til að skoða síðuna fyrir breytingar.
1. Í valmyndinni **Markmið** skaltu velja **Nýtt markmið** til að stofna nýtt ytra lag markmiðs. Þú getur búið til mörg markmið á síðu eins og þú krefst.
1. Sláðu inn heiti og lýsingu fyrir markmiðið og veldu því næst **Áfram**.
1. Veldu **Bæta við** til að taka með þá notendahópa sem sjá markefnið eða til að útiloka notendahópa. Veljið síðan **Næst**.

    > [!NOTE]
    > Úthlutun notendahóps er valfrjálst skref þegar markmið er búið til. Áður en þú birtir markmiðið verður þú hins vegar að setja inn að minnsta kosti einn notendahóp til að tryggja að þeir hópar notenda sem stefnt er að sjái það efni sem miðað er á.

1. Skilgreindu tímagluggann fyrir birtingu markmiðsins með því að velja tímabeltið og upphafs- og lokadagsetningu og tíma. Þú getur stillt markið þannig að það birtist öllum stundum í glugganum eða þú getur valið tiltekna daga og tíma. Þegar þessu er lokið skal velja **Næst**.

    > [!NOTE]
    > Tímasetningar og tímabelti sem þú tilgreinir eru alþjóðleg. Ef þú vilt miða á mismunandi staðsetningar á ólíkum tímum eða í mismunandi tímabeltum þarf að búa til mismunandi markmið og skilgreina æskilega tímasetningu fyrir hverja staðsetningu.

1. Farðu yfir upplýsingarnar og þegar allt lítur rétt út skaltu velja **Búa til markupplifun** og því næst velja **Fara í markmið**. Ytra lag markmiðs er búið til. Núna geturðu bætt einingum við hana.
1. Veldu eininguna sem á að miða á, veldu úrfellingarmerkið (**...**) og veldu því næst **Bæta við núverandi markhluta**. Þegar þú miðar á yfireiningu verða allar undireiningar hennar hluti af markmiðinu. Einingar sem miðað er á eru sýndar í grænu.
1. Gerðu nauðsynlegar uppfærslur á efni fyrir einingar sem miðað er á og bætt fleiri einingum við markmiðið eftir þörfum. Veldu svo **Vista** til að vista breytingarnar.
1. Áður en þú birtir markmiðið skaltu velja **Forskoða** á skipanastikunni til að fara yfir það. Þú getur valið einn eftirfarandi valkosta:

    - **Einföld forskoðun** – Veldu þennan valkost til að aðeins forskoða valið afbrigði (sjálfgefin síða eða markmið) án tengdra notendahópa.
    - **Ítarleg forskoðun** – Veldu þennan möguleika ef þú ert með mörg markmið á síðu og vilt forskoða þau sem notandi sem tilheyrir ákveðnum notendahópi eða á tilteknum degi/tíma. Veldu **Næst** til að velja úr lista yfir viðeigandi notendahópa. Þú getur einnig fjarlægt síuna til að velja á milli allra notendahópa.

1. Þegar þú ert ánægð(ur) með stillingu markmiðs þarftu að birta síðuna til að markmiðið sé í rauntíma. Veldu **Birta** til að senda markmiðið í rauntíma strax. Þú getur einnig notað birtingarhóp til að tímasetja hvenær síðan fer í loftið. Upplýsingar um birtingarhópa er að finna í [Vinna með birtingarhópa](publish-groups.md).

Einnig er hægt miða á brot. Aðferðin er svipuð. Í skrefi 1 velur þú hins vegar **Brot** í staðinn fyrir **Síður** á yfirlitssvæðinu til vinstri.

> [!NOTE]
> Til að koma í veg fyrir neikvæð áhrif á mælingar geturðu annaðhvort gert tilraunir eða sett markmið á síðu eða síðubrot. Þú getur ekki bæði verið með tilraun og markmið.

### <a name="manage-targets"></a>Stjórna markhlutum

Til að breyta, afrita eða eyða markmiðum skaltu fara á sjálfgefnu síðuna eða síðubrotið og fylgja þessum skrefum.

1. Í fellivalmyndinni velur þú **Markmið** og velur svo **Stjórna markmiðum**.
1. Veljið mark til að breyta, afrita eða eyða.
1. Ef þú ert með mörg markmið í sömu einingu, eða ef mörg markmið eru tímasetningar sem stangast á skaltu velja **Forgangsraða markmiðum** til að tilgreina röðina sem á að sýna þau í. Ef þú bætir við fleiri en einu markmiði á síðu eða síðubrot birtist hnappurinn **Forgangsraða markmiðum** einnig í tilkynningastikunni til að minna þig á að forgangsraða markmiðunum. Ef enginn forgangur er tilgreindur er nýjasta markmiðið sjálfgefið valið.

### <a name="localize-targets"></a>Staðfæra markhluta

Markmið á síðum og í brotum eru sjálfkrafa tekin með þegar XLIFF-skrár eru fluttar út og fluttar inn fyrir staðfærslur. Ef hinsvegar ekki er þörf á staðfærslu getur þú eytt markmiðunum fyrir þau eftir að staðfærðar XLIFF-skrár hafa verið fluttar inn.

> [!NOTE]
> Markmiðum er stjórnað á hverri rás og staðsetningu. Breytingar sem þú gerir á markmiðum í einni rás eða staðsetningu eru ekki sjálfkrafa fluttar áfram í aðrar rásir eða staðsetningar.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
