---
title: Dynamics 365 Commerce Staðsetningarleiðbeiningar fyrir rafræn viðskipti
description: Þessi grein lýsir því hvernig á að staðfæra a Microsoft Dynamics 365 Commerce e-verslunarsíðu yfir á fleiri tungumál og stilltu síðuna til að styðja við margar rásir.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 955a85340f6d35f1e203d74920d07b5dc6ff8654
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873385"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Dynamics 365 Commerce Staðsetningarleiðbeiningar fyrir rafræn viðskipti

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að staðfæra a Microsoft Dynamics 365 Commerce e-verslun síða í fleiri tungumál og stilla síðuna til að styðja margar rásir, og einnig nær yfir hugtök og hugtök sem tengjast ferlinu.

Rafræn verslunarmöguleikar í Dynamics 365 Commerce hafa verið hönnuð til að gera upplifun á netinu kleift sem hægt er að sníða að sérstökum löndum og tungumálum, en á sama tíma leyfa hámarks endurnotkun á sniðmátum, síðum, efni og miðlum. Þú getur líka búið til grunnsíðu og stækkað síðan inn á nýja markaði með því að bæta við stuðningi fyrir fleiri lönd og tungumál með tímanum.

## <a name="definitions"></a>Skilgreiningar

**Staðbundin, staðarauðkenni** : Staðbundin (einnig þekkt sem staðarauðkenni) skilgreinir tungumál sem er tengt landi eða svæði. Til dæmis er staðarauðkennið „fr-ca“ tengt við kanadíska frönsku.

**Grunnmál** : Tungumálið sem þú þróar síðuna þína á áður en þú flytur það út til staðsetningar.

**Rás, netverslun** : Rás (einnig þekkt sem netverslun) skilgreinir greiðslumáta, verðflokka, vörustigveldi, úrval og vörur fyrir netverslun á netinu.

## <a name="concepts"></a>Hugtök

### <a name="url-driven-experience"></a>URL-drifin upplifun

Dynamics 365 Commerce Netverslunarsíður veita viðskiptavinum einstaka markaðsvædda og staðbundna upplifun í gegnum rásir og staðsetningarauðkenni. Rásir skilgreina einstöku vörur, flokka, gjaldmiðla og greiðslumáta fyrir markað og staðsetningarauðkenni ákvarða tungumál efnisins sem viðskiptavinir sjá. Rafræn viðskiptasíða notar vefslóðir til að greina á milli markaðssettrar og staðbundinnar upplifunar. Vefslóðir fyrir þessar einstöku rásar- og staðsetningarupplifanir eru skilgreindar fyrir síðu á **Vefstillingar \> Rásir** síðu inn Dynamics 365 Commerce vefsmiður.

Í vefsíðugerð er vefslóð sambland af léni og slóð sem skilgreinir inngangspunkt fyrir einstaka samsetningu rásar og staðsetningar. Í eftirfarandi dæmi skilgreinir gervi netverslun sem heitir Fabrikam Inc. fjórar einstakar samsetningar rásar og staðsetningar og kortleggur hverja samsetningu á einstaka vefslóð sem þjónar efni til viðskiptavina.

| Lén                     |  Slóð      | Rás       |   Staður     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Fabrikam útbreidd netverslun | is  |
| `https://fabrikam.com` | /es    | Fabrikam útbreidd netverslun | es     |
| `https://fabrikam.ca`  | /      | Contoso netverslun    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso netverslun    | en-ca  |

#### <a name="domain"></a>Lén

Lén eru stofnuð þegar þú setur upp netverslunarsíðuna þína í Microsoft Dynamics Lífsferilsþjónusta (LCS). Eftir að rafræn viðskiptaumhverfi þitt hefur verið útvegað geturðu bætt við fleiri lénum með því að opna þjónustubeiðni. Fyrir frekari upplýsingar um hvernig á að setja upp lén fyrir netverslunarsíðuna þína, sjá [Lén í Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Slóð

- Slóð er handahófskenndur strengur sem, ásamt léninu, er varpað á einstaka samsetningu rásar og staðsetningar. Í dæminu á undan samsvarar strengurinn sem er notaður sem slóð staðsetningarauðkennið sem slóðin er varpað á. Hins vegar geturðu notað aðra nálgun.
- Hægt er að varpa samsetningu rásar og staðsetningar á lén og tóma slóð ("/"). Í dæminu á undan eru viðskiptavinir sem heimsækja`https://fabrikam.ca/` mun fá vörurnar og úrvalið fyrir kanadíska markaðinn á kanadískri frönsku.
- Viðskiptasíðugerð kemur í veg fyrir að þú búir til tvíteknar samsetningar af léni og slóð. Hins vegar geturðu kortlagt tvíteknar samsetningar rásar og staðsetningar á aðra samsetningu af léni og slóð.

#### <a name="channel"></a>Rás

- Rásir (einnig þekktar sem netverslanir) skilgreina greiðslumáta, verðflokka, vörustigveldi, úrval og vörur fyrir netverslun á netinu.
- Rásir eru skilgreindar, stilltar og birtar í Dynamics 365 Commerce höfuðstöðvar.
- Vefsmiður getur greint netverslanir sem hafa verið stilltar í höfuðstöðvum Commerce og hægt er að kortleggja þær á síðu.

Fyrir frekari upplýsingar um rásir, sjá [Yfirlit yfir rásir](channels-overview.md). Fyrir frekari upplýsingar um hvernig á að setja upp netrás, sjá [Settu upp netrás](channel-setup-online.md).

#### <a name="locale"></a>Staður

- Staðsetningin er raunverulegt auðkenni sem notað er þegar þú afhendir XML Localization Interchange File Format (XLIFF) skrár til staðsetningar. Staðsetningar eru skilgreindar og birtar fyrir hverja rás í höfuðstöðvum Commerce. Fyrir upplýsingar um hvernig á að stilla tungumál og rásir í vefsvæðisgerðinni, sjá næsta kafla.
- Hægt er að kortleggja sama svæði á margar rásir. Þannig er hægt að bjóða upp á sameiginlegt tungumál á mörgum mörkuðum.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Stilltu tungumál og rásir fyrir netverslunarsíðuna þína

Upp úr kassanum, allt Dynamics 365 Commerce Netverslunarsíður eru stilltar til að nota eina netrás og eitt tungumál, óháð því hvort þú byrjar á Fabrikam kynningarsíðunni eða býrð til nýja síðu frá grunni.

Í þessari uppsetningu þróa viðskiptavinir og samstarfsaðilar venjulega allar eignir sem verða notaðar á milli landa og tungumála. Þessar eignir innihalda sniðmát, síður, brot, efni og fjölmiðla. Allt efni síðunnar er þróað á fyrsta tungumálinu sem þú valdir fyrir síðuna þína, eða ef þú ert að nota Fabrikam kynningarsíðuna verður efni síðunnar þróað á ensku.

![Út fyrir kassann Dynamics 365 Commerce rafræn viðskipti síða](media/loc-guide-1.png)

> [!NOTE]
> Þú getur stillt kynningarsíðuna fyrir Fabrikam fyrir viðbótartungumál þannig að hægt sé að þróa efni á því tungumáli. Fyrir upplýsingar um hvernig á að bæta nýju tungumáli við síðu og rás, sjáðu [Stilltu viðbótartungumál fyrir síðuna þína](#configure-an-additional-language-for-your-site) kafla síðar í þessari grein.

Hins vegar er vefumsjónarkerfi (CMS) og síðulíkan fyrir Dynamics 365 Commerce Netverslunarsíður hafa verið hannaðar til að gera kleift að stækka inn á nýja markaði og staði. Þess vegna, í gegnum eina netverslunarsíðu, geturðu stjórnað eignum fyrir netverslun sem spannar marga markaði og tungumál.

![Dynamics 365 Commerce Netverslunarsíða sem spannar marga markaði og tungumál](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Stilltu viðbótartungumál fyrir síðuna þína

Ferlið við að stilla nýtt tungumál fyrir netverslunarsíðu hefur þrjú skref.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>Skref 1: Bættu tungumálinu við rásina þína (netverslun) í höfuðstöðvum Commerce

1. Í höfuðstöðvum Commerce, farðu á rásina sem þú vilt bæta nýja tungumálinu við. Til að finna lista yfir rásir sem þú hefur stillt í höfuðstöðvum Commerce skaltu fara á **Verslun og verslun \> Rásir \> Netverslanir**.
1. Opnaðu netverslunina sem er kortlögð á síðuna þína með því að velja hana **Auðkenni smásölurásar** gildi. Þú getur staðfest netverslunina sem er kortlögð á síðuna þína með því að opna **Rásir** síða stillingar í Commerce site builder og skoða nafn netverslunarinnar í **Rásir** dálki. 
1. Á flýtiflipanum **Tungumál** velurðu **Bæta við**. Í **Tungumál** reit, veldu staðarkóða fyrir nýja tungumálið. Veldu síðan **Vista**.
1. Fara til **Verslun og verslun \> Upplýsingatækni í smásölu og viðskiptum \> Dreifingaráætlun**, og keyra starf **1070 Rásar stillingar**. Þegar verkinu er lokið geturðu haldið áfram í skref 2 og bætt tungumálinu við rás fyrir síðuna þína í Site builder.

![Tungumál flýtiflipi netverslunar í höfuðstöðvum Commerce](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>Skref 2: Bættu tungumálinu við rás í Site builder

Til að bæta tungumáli við rás í vefsvæðisgerð skaltu fylgja þessum skrefum.

1. Í Commerce site builder, opnaðu síðuna þína og opnaðu síðan **Rásir** síðu í stillingum vefsvæðisins.
1. Veldu nafn rásarinnar sem þú vilt bæta tungumálinu við.
1. Í hægri glugganum velurðu **Bættu við svæði**.
1. Í **Bættu við svæði** svargluggi, undir **Bættu við svæði** veldu svæði fyrir tungumálið sem þú bættir áður við rásina í höfuðstöðvum Commerce.
1. Veldu lénið og slóðina sem viðskiptavinir munu biðja um til að skoða síðuna þína á þessari rás og tungumáli.
1. Ef þú vilt að tungumálið sé sjálfgefið tungumál til að skoða, búa til og uppfæra síður og brot vefsíðnagerðar skaltu velja **Notaðu sem sjálfgefið tungumál höfundarrásar** gátreit. 
    > [!NOTE]
    > Þessi stilling hefur aðeins áhrif á vefsíðugerð. Það hefur ekki áhrif á birta síðuupplifun viðskiptavina þinna.
1. Veldu **Í lagi**.
1. Veldur **Vista og birta**.

#### <a name="step-3-localize-your-site-content"></a>Skref 3: Staðfærðu innihald vefsvæðisins þíns

Þegar þú kemur aftur til **Síður** skoða í Commerce site builder, nýja tungumálið verður fáanlegt í rásinni og staðarvalsvalinu efst til hægri. Þú getur nú búið til staðbundnar útgáfur af síðum á grunntungumálinu þínu.

Farið er yfir ferlið við að staðfæra innihald síðna þinna og brota í [Staðfærðu innihald rafrænna viðskiptasíðunnar](#localize-e-commerce-site-content) kafla síðar í þessari grein.

### <a name="configure-a-new-channel-for-your-site"></a>Stilltu nýja rás fyrir síðuna þína

Dynamics 365 Commerce Rafræn viðskipti geta þjónað upplifunum sem eru skilgreindar á mörgum netrásum sem eru stilltar í höfuðstöðvum Commerce. Vefsvæði notar margar rásir til að sýna viðskiptavinum einstaka uppsetningu á greiðslumáta, verðflokkum, vörustigveldi, úrvali og vöruflokki. Rás er venjulega notuð til að stilla þessar stærðir þannig að þær henti kröfum og óskum fyrir upplifunina sem tengist einstökum löndum. Hins vegar er þessi nálgun viðskiptaákvörðun sem viðskiptavinurinn tekur. Það er ekki krafa.

Forsendur og verkefni sem tengjast uppsetningu rásar (netverslun) eru utan gildissviðs þessa skjals. Fyrir frekari upplýsingar um hvernig á að setja upp netrás í höfuðstöðvum Commerce, sjá [Grunnatriði rásaruppsetningar](channels-overview.md#channel-setup-basics). Fyrir upplýsingar um skref og kröfur sem eru sértækar fyrir netrásir, sjá [Settu upp netrás](channel-setup-online.md).

Fylgdu þessum skrefum til að bæta við rás á síðuna þína í Site builder.

1. Í Commerce site builder, farðu á **Vefstillingar \> Rásir**. 
1. Veldu **Bættu við rás**.
1. Í **Bættu við rás** svargluggi, undir **Rás** veldu rásina sem þú vilt bæta við. 
    > [!NOTE]
    > Þú getur aðeins bætt við rásum sem hefur ekki þegar verið bætt við síðuna þína.
1. Veldu sjálfgefið svæði fyrir rásina. Ef þú bætir nýjum tungumálum við rásina geturðu breytt sjálfgefna tungumálinu í eitt þeirra.
1. Tilgreindu lénið og slóðina sem mun mynda vefslóðina sem þjónar efni og upplifun fyrir þessa samsetningu rásar og tungumáls.
1. Veldu **Í lagi**.
1. Veldur **Vista og birta**.

## <a name="localize-e-commerce-site-content"></a>Staðfærðu innihald rafrænna viðskiptasíðunnar

### <a name="xliff-basics"></a>XLIFF grunnatriði

XLIFF er iðnaðarstaðlað skráarsnið til að senda staðfæranlegt efni á milli efnisstjórnunartækja. Viðskiptasíðugerð notar XLIFF skráarsniðið til að flytja út lýsigögn síðu, brota og myndefnis svo hægt sé að staðfæra það og flytja það aftur inn.

Microsoft Dynamics viðskiptavinir vinna venjulega með staðsetningarframleiðendum þriðja aðila eins og [Translated.com](https://translated.com/welcome) að þýða XLIFF skrárnar sínar á þau tungumál sem þeir þurfa.

### <a name="localize-assets-in-site-builder"></a>Staðsetja eignir í síðugerð

Hægt er að staðsetja eftirfarandi eignir fyrir rafræn viðskipti í vefsmiði:

- Síður
- Brot
- Fjölmiðlaeignir
- Einingar

Allar nýjar síður, bútar og fjölmiðlaeignir eru búnar til í samhengi við rásina og tungumálið sem er valið í rásar- og staðarvalinu. Þetta tungumál er venjulega "grunntungumálið þitt", að því tilskildu að þú hafir ekki stillt fleiri tungumál eða rásir. Á síðum þar sem margar rásir og tungumál eru stilltar er „grunntungumálið“ skilgreint af rásinni og staðsetningum sem þú hefur stillt sem sjálfgefið á **Rásir** síðu í stillingum vefsvæðisins.

Skrefin til að staðfæra efni fyrir síður, brot og fjölmiðlaeignir eru svipuð. Bent verður á undantekningar og mismun í köflum hér á eftir. Hins vegar eru skrefin til að staðsetja innihald eininga mismunandi. Fyrir frekari upplýsingar, sjá [Staðsetja einingar](#localize-modules) kafla síðar í þessari grein.

#### <a name="step-1-export-an-xliff-file"></a>Skref 1: Flyttu út XLIFF skrá

Fylgdu þessum skrefum til að flytja út XLIFF skrá fyrir síðu, brot eða mynd í vefsíðugerð.

1. Opnaðu eignina sem þú vilt flytja út grunnmálsefni fyrir svo hægt sé að staðfæra hana.
1. Veldu á skipanastikunni **Staðfærsla \> Flytja út XLIFF**.
    > [!NOTE]
    > The **Staðfærsla** valkostur er aðeins sýnilegur þegar eignin er í **Breyta** ríki.

XLIFF skrá sem heitir **\<assetname\> .xlf** verður hlaðið niður í niðurhalsmöppu vafrans þíns. Þessi XLIFF-skrá á sérstaklega við eignina sem verið er að staðfæra. Þú verður að flytja út XLIFF-skrá fyrir hverja eign sem á að staðsetja.

#### <a name="step-2-localize-the-xliff-file"></a>Skref 2: Staðfærðu XLIFF skrána

Í flestum tilfellum muntu vinna með staðfærslusala til að þýða XLIFF skrárnar þínar. Hins vegar, ef verið er að staðfæra eignir innbyrðis, eða ef þú vilt bara prófa staðfærsluferlið, verður þú að gera eftirfarandi breytingar á XLIFF skrá:

- Bættu við eigind marktungumáls við /xliff/skráareininguna og stilltu gildið á staðbundið kenni tungumálsins sem verið er að staðfæra á. 
    > [!NOTE]
    > Þetta kenni landsstaðals verður að samsvara kenni landsstaðalsins frá **síðunni Rásir** í stillingum setursins.
- Fyrir hverja //upprunaeiningu skal bæta við markeiningarsystkini þar sem textagildið er staðfærð útgáfa af innihaldi þeirrar frumeiningar.

Upplýsingar um skemað sem stjórnar XLIFF-skrám er að finna í [XLIFF 1.2 Specification](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html).

> [!NOTE]
> Til að staðfæra eign á mörg tungumál verður að búa til staðfærða XLIFF-skrá fyrir hvert þessara tungumála.

#### <a name="step-3-import-the-localized-xliff-file"></a>Skref 3: Flytja inn staðfærðu XLIFF skrána

Til að flytja inn XLIFF-skrá fyrir eign skal fylgja þessum skrefum.

1. Í Commerce site builder skal opna eignina sem á að flytja inn XLIFF-skrá fyrir.
1. Í rásinni og staðbundnu tínslunni efst til hægri skal velja rásina og tungumálið sem verið er að flytja inn staðfært efni fyrir.
1. Á skipanastikunni skal velja **Staðfæra innflutning \> XLIFF**. Flettu síðan að og veldu staðfærðu XLIFF-skrána fyrir valda eign og tungumál.

Eftir að XLIFF-skráin hefur verið flutt inn er búið til "afbrigði" af síðunni, brotinu eða eigninni. Frá þeim tímapunkti munu allar breytingar sem gerðar eru á staðfærða afbrigðinu aðeins hafa áhrif á það afbrigði. Þeir munu ekki hafa áhrif á grunneignina sem afbrigðið var dregið af. Sömuleiðis munu breytingar á grunneigninni ekki hafa áhrif á afbrigði þeirrar eignar. 

Hins vegar, ef um síður er að ræða, er hægt að gera breytingar á milli afbrigða með því að breyta sniðmátinu eða útlitinu sem þessar síður eru bundnar við. Sömuleiðis munu breytingar á broti hafa áhrif á allar síður sem taka háð á því afbrigði.

### <a name="images"></a>Myndir

Myndir er aðeins hægt að gera á síðu eða einingarafbrigði ef lýsigögn innihalds sem tengjast þessum myndum eru staðfærð. Eins og er eru eftirfarandi lýsigögn í miðilseign staðfærð:

- Baktexti
- Lýsing
- Titill

Eins og er er ekki hægt að staðsetja tvíundina fyrir stafræna eign eins og mynd eða myndband. Vöruteymið Dynamics 365 Commerce vinnur nú að þessari getu.

### <a name="localize-modules"></a>Staðfæra einingar

Strengir sem eru gerðir sem hluti af einingunni sjálfri (til dæmis "Fyrri" og "Áfram" í hringekjueiningu) eru staðfærðir sérstaklega frá innihaldi eininga. Leiðbeiningar er að finna í [Staðfæra kerfiseiningu](e-commerce-extensibility/localize-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Orðalisti blaðsíðna](page-elements-overview.md)

[Samnýting milli rása](cross-channel-sharing.md)

[Staðfæra einingu](e-commerce-extensibility/localize-module.md)

[Skilgreiningarskrá einingar](e-commerce-extensibility/module-definition-file.md)

[Staðfæra tilföng og merkjaskrár í Commerce-viðbót](dev-itpro/extension-resource-localization.md)

[Altækar einingar með klasanum CultureInfoFormatter](e-commerce-extensibility/globalize-modules.md)

[Stillingar forrita: Þemu](e-commerce-extensibility/app-settings.md#themes-section)
