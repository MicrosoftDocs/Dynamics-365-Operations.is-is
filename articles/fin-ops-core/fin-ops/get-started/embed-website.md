---
title: Innfella forrit þriðja aðila
description: Þessi grein útskýrir hvernig á að fella inn forrit frá þriðja aðila til að auka virkni vörunnar.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3c07befc7150ff0a121fd3aaa0b5233df9f431e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868609"
---
# <a name="embed-third-party-apps"></a>Innfella forrit þriðja aðila

[!include [banner](../includes/banner.md)]

Margir viðskiptavinir nota ýmis forrit til að reka fyrirtæki sín. Sum þessara forrita eru vefforrit þriðja aðila sem virka í tengslum við Finance and Operations forrit. Til að veita hnökralausri notendaupplifun geturðu notað **Heilsíðuforrit** eiginleika til að fella þessi þriðju aðila öpp beint inn í fjármála- og rekstraröppin þín (að því gefnu að þriðju aðila öppin leyfi sér að vera felld inn). Á þennan hátt geta notendur fengið aðgang að vefsvæðum og forritum sem þeir þurfa án þess að þurfa að skipta um flipa eða glugga.

Áður en hægt er að fella forrit þriðja aðila inn í afurðina þarf að kveikja á eiginleikanum **Heilsíðuforrit** í eiginleikastjórnun. Síðan er hægt að nota eina af eftirfarandi aðferðum til að fella inn forrit eða vefsvæði þriðja aðila. Þessar aðferðir eru hliðstæðar aðferðunum sem eru notaðar til að fella inn strigaforrit frá Microsoft Power Apps inn í Finance and Operations öpp.

- Fellið forritið eða vefsvæðið inn í fyrirliggjandi síðu sem síðu á nýjum flipa (snúningsflipa, flýtiflipa, blaði eða vinnusvæði).
- Búið til nýja heilsíðuupplifun fyrir forritið eða vefsvæðið úr stjórnborðinu.

## <a name="embed-a-website-on-an-existing-page"></a>Fella inn vefsíðu á fyrirliggjandi síðu

Notið þessa aðferð til að bæta við síðu sem er til í kerfinu með innfelldu forriti.

1. Farið á síðuna þar sem á að fella inn forritið.
2. Opnið gluggann **Bæta við forriti**:

    1. Veljið **Stillingar** og síðan **Sérstilla** til að opna tækjastikuna **Sérstilling**.
    2. Veljið **Meira \> Bæta við forriti**.

3. Veldu svæðið á síðunni sem bæta á forritinu við. Þetta svæði verður að vera *flipahólf* fyrir snúningsflipa, flýtiflipa, blað eða vinnusvæði.
4. Veljið **Vefsvæði**.
5. Grunnstilla innfellt forrit:

    - **Heiti** – Færið inn textann sem á að sýna fyrir flipann sem inniheldur innfellt forrit. Algengt er að vilja hafa þennan texta sem heiti forritsins.
    - **Vefslóð** – Tilgreinið staðsetningu forritsins.

    > [!IMPORTANT]
    > - Vefslóðin verður af öryggisástæðum að nota HTTPS (Hypertext Transfer Protocol Secure).
    > - Stilla þarf forritið eða vefsvæðið þannig að það leyfi innfellingu.

6. Veljið **Vista** til að fella forritið inn á síðuna. Forritinu er bætt við sem síðasta flipanum eða hlutanum í flokknum.
7. Staðfestið að forritið birtist eins og búist var við. Ef appið er ekki birt skaltu skoða [Bilanagreining](#troubleshooting) kafla síðar í þessari grein.
8. Opnið yfirlitsvalið og veljið annaðhvort **Vista** (ef forritið á að vera tengd við núverandi yfirlit) eða **Vista sem** (til að vista forritið í annað yfirlit).

    Ef síðan er ekki með yfirlitsval (t.d. ef síðan er svargluggi eða vinnusvæði) er hægt að sleppa þessu skrefi.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Fella inn vefsvæði sem heilsíðuupplifun úr stjórnborðinu

Notaðu þessa aðferð ef appið sem þú vilt fella inn er ekki tengt núverandi síðu eða ef þú vilt bara heilsíðuupplifun fyrir appið í Finance and Operations appinu.

1. Opnið stjórnborð.
2. Veljið og haldið inni stjórnborðinu (eða hægrismellið á það), veljið **Sérstilla** og veljið því næst **Bæta við síðu**.
3. Á svæðinu **Bæta við síðu** skal velja **Vefsvæði**.
4. Grunnstilla innfellt forrit:

    - **Heiti** – Færið inn textann sem á að sýna í reitnum sem bætt er við fyrir innfellda forritið á stjórnborðinu. Algengt er að vilja hafa þennan texta sem heiti forritsins.
    - **Vefslóð** – Tilgreinið staðsetningu forritsins.

    > [!IMPORTANT]
    > - Vefslóðin verður að nota HTTPS af öryggisástæðum.
    > - Stilla þarf forritið eða vefsvæðið þannig að það leyfi innfellingu.

5. Veljið **Vista** til að bæta forritinu við stjórnborðið sem nýjan reit.
6. Veljið nýja reitinn á stjórnborðinu og staðfestið að forritið birtist eins og búast má við. Ef ekki er verið að birta forritið skaltu skoða [Bilanagreining](#troubleshooting) kafla síðar í þessari grein.

## <a name="sharing-embedded-apps"></a>Deiling innfelldra forrita

Þegar forrit hefur verið innfellt með því að nota eina af aðferðunum sem lýst er í hlutunum hér á undan gæti verið góð hugmynd að deila yfirlitinu með öðrum notendum í kerfinu. Ein af eftirfarandi aðferðum er notuð til að deila innfelldu forriti:

- **Birta yfirlitið (ráðlagt):** Ef innfellda forritið hefur verið vistað í yfirlit, er ráðlagða og æskilega leiðin til að deila því sú að birta yfirlitið þeim notendum sem eru með tilskilin öryggishlutverk í lögaðilunum. Í þessu tilviki munu aðeins þeir notendur sem óskað er eftir sjá innfellt forrit á þeirri síðu. Frekari upplýsingar um hvernig á að birta yfirlit er að finna í [Yfirlit birt](saved-views.md#publishing-views).

    Einnig er hægt að birta forrit sem hefur verið fellt inn sem heilsíðuupplifun úr stjórnborðinu. Á stjórnborðinu skal velja og halda niðri (eða hægrismella) reitnum sem tengist forritinu, velja **Sérstilla** og síðan velja **Birta síðu**. Upplifun sem líkist *Birtingu yfirlita* er sýnd og þú getur valið öryggishlutverkin til að birta í. Í uppfærslu 10.0.21 eða nýrri, ef kveikt er á eiginleikanum **Bættur stuðningur lögaðila fyrir vistuð yfirlit**, getur þú einnig gefið forritið út í þeim lögaðilum sem þú vilt.

- **Afrita sérstillinguna:** Fyrir síður sem styðja ekki yfirlit (t.d. svargluggar eða vinnusvæði), eða fyrir upplifun heilsíðuforrits, er hægt að afrita sérstillinguna til viðeigandi notenda. Frekari upplýsingar eru í [Sérstillingar samnýttar](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Skoða innfelld forrit

Til að skoða innfellt forrit á síðu í Finance and Operations forritum skaltu opna síðuna sem hefur innfellda appið. Munið að á sumum síðum er hægt að opna forrit með því að nota hnappinn **Power Apps** á staðlaða aðgerðasvæðinu. Að öðrum kosti kunna þær að birtast beint á síðunni sem nýr flipi eða flýtiflipi eða blað eða sem nýr hluti á vinnusvæði.

## <a name="editing-or-removing-embedded-apps"></a>Breyta eða fjarlægja innfelld forrit

Þegar forrit hefur verið fellt inn í síðu gæti þurft að breyta grunnstillingum þess (t.d. með því að breyta kaflamerkinu eða vefslóðinni). Einnig gæti þurft að fjarlægja það af síðunni. Notið eina af eftirtöldum aðferðum til að breyta stillingum innfellds forrits eða til að fjarlægja það alveg.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Forrit sem eru felld inn á fyrirliggjandi síður

1. Opna síðuna þar sem forritið er innfellt.
2. Veljið **Stillingar** og síðan **Sérstilla** til að opna tækjastikuna **Sérstilling**.
3. Velja **Velja** verkfæriið og veljið svo innfellda forritið.
4. Til að breyta forritinu skal gera nauðsynlegar breytingar á stillingum þess og velja síðan **Vista**.

    Einnig er hægt að fjarlægja forritið með því að velja **Eyða**.

5. Vistið aftur eða endurútgefið yfirlitið. Athugið að ef farið er af síðunni án þess að vista yfirlitið verður engum aðgerðanna sem voru framkvæmdar á svæðinu **Breyta vefsvæði** haldið við.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Forrit sem eru felld inn úr stjórnborðinu

1. Opnið stjórnborð.
2. Veljið og haldið (eða hægrismellið) reitnum sem tengist innfelldu forriti og veljið síðan **Sérstilla**.
3. Veljið **Breyta síðu** til að breyta forritinu. Á svæðinu **Breyta vefsvæði** skal gera nauðsynlegar breytingar á grunnstillingu forritsins og því næst velja **Vista**.

    Annar kostur til að fjarlægja forritið er að velja **Fjarlægja síðu**.

## <a name="appendix"></a>Viðauki

### <a name="troubleshooting"></a>Úrræðaleit

Ef vefsvæði birtast ekki á réttan hátt eftir innfellingu í forriti Finance and Operation, eða ef villuboð eru móttekin sem gefa til kynna að tengingu á vefslóð hafi verið hafnað, er vefsvæðið líklega grunnstillt til að koma í veg fyrir að það geti verið fellt inn í iframe. Fylgið eftirfarandi skrefum til að ákvarða hvort hægt sé að fella inn vefsíðuna.

1. Opnaðu þróunartólin fyrir vafrann sem verið er að nota.
2. Í flipanum **Netkerfi** skal finna og velja svarið frá innfelldu svæði.
3. Í flipanum **Hausar**, undir **Síðuhausar svars**, skal leita að **x-frame-options**. Ef **x-frame-options** er til í síðuhausum svars og er með gildið **DENY** eða **SAMEORIGIN** er ekki hægt að fella inn vefsvæðið sem stendur. Þú þarft að vinna með eiganda forritsins til að hægt sé að fella það inn á öruggan hátt.

### <a name="developer-modeling-a-website-on-a-form"></a>[Þróunaraðili] Vefsvæði smíðað í skjámynd

Þrátt fyrir að þessi grein beinist að því að fella inn forrit eða vefsíður frá þriðja aðila með sérstillingu, geta verktaki einnig fellt þau inn í form með því að nota Visual Studio reynslu af þróun. Bætið einfaldlega stýringu **WebsiteHostControl** við skjámyndina. Lýsigagnaeiginleikarnir sem eru í boði fyrir stýringuna bjóða upp á sömu möguleika og sérstillingarleiðin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
