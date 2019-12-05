---
title: Fella inn Power Apps
description: Þetta efnisatriði lýsir því hvernig á að fella Power Apps inn í biðlarann til að auka virkni vörunnar.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 755a30f89725ca0a7e1c14252984c617d6ba280e
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824494"
---
# <a name="embed-microsoft-power-apps"></a>Fella inn Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Verkvangsuppfærsla 14 styður samþættingu við Microsoft Power Apps, þjónustu fyrir þróunaraðila og aðra ekki tæknilega notendur til að byggja upp sérsniðin viðskiptaforrit fyrir fartæki, spjaldtölvur og netið án þess að skrifa kóða. Power Apps þróað af þér, fyrirtæki þínu eða breiðara vistkerfi er síðan hægt að fella inn í forritum Finance and Operations til að auka virkni vörunnar. Til dæmis gætir þú byggt upp Power Apps til að bæta við forrit Finance and Operations með upplýsingum sem eru sótt úr öðru kerfi.

Til að fræðast meira um innfellingu á Power Apps skal horfa á stutt myndband [Hvernig á að innleiða Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-power-app-to-a-page"></a>Bætir við innfelldu Power Apps á síðu

### <a name="overview"></a>Yfirlit

Áður en Power Apps er fellt inn í biðlara þarftu fyrst að finna eða byggja upp Power Apps með viðkomandi myndefni og/eða virkni. Við munum ekki lýsa í smáatriðum ferlinu um hvernig skuli byggja upp Power Apps hér. Efnisatriðið [Inngangur að Power Apps](https://docs.microsoft.com/powerapps/getting-started) er góður upphafsstaður ef þú hefur ekki reynslu af Power Apps.

Þegar þú ert tilbúin/n til að fella inn ákveðið Power Apps getur þú valið á milli tveggja leiða til að fá aðgang að Power Apps á síðu, fer eftir því hvor leiðin hentar betur. Fyrsta leiðin er í gegnum hnappinn Power Apps sem hefur verið bætt við staðlaða aðgerðasvæðið. Power Apps bætt við með þessari aðferð mun birtast sem valmyndaratriði inni í Power Apps valmyndarhnappnum. Þegar valið, þá opnar hvert þessara valmyndaratriða hliðarsvæði sem inniheldur innfellt Power Apps. Að öðrum kosti getur þú valið að sýna Power Apps beint á síðu sem nýjan flipa, flýtiflipa, blað eða sem nýjan hluta á vinnusvæði.

Þegar þú grunnstillir innfellt Power Apps er hægt að velja stakan reit sem þú vilt senda sem inntak í Power Apps. Þetta gerir Power Apps kleift að svara á grundvelli gagna sem þú ert að skoða á þeirri stundu.

### <a name="details"></a>Upplýsingar

Eftirfarandi leiðbeiningar sýna hvernig á að fella Power Apps inn í vefbiðlara.

1. Farðu á síðuna þar sem þú vilt fella inn Power Apps. Þetta verður sama síðan og sú sem inniheldur allar þær upplýsingar sem þarf að flytja yfir til Power Apps sem inntak.
2. Opnaðu svæðið **Setja inn Power Apps**:

    - Smelltu á **Valkostir** og veldu síðan **Sérstilla þessa skjámynd**. Undir valmyndinni **Setja inn** skal velja **Power Apps**. Að lokum skal velja svæðið þar sem þú vilt bæta við Power Apps. Ef þú vilt fella Power Apps inn í valmyndarhnapp Power Apps skaltu velja aðgerðasvæðið. Ef þú vilt fella Power Apps beint inn á síðuna skaltu velja viðeigandi flipa, flýtiflipa, blað eða hluta (ef þú ert á vinnusvæði).
    - Ef hægt er að komast í Power Apps með því að nota valmyndarhnapp Power Apps geturðu einnig smellt á valmyndarhnappinn **Power Apps** á staðlaða aðgerðasvæðinu og síðan valið **Setja inn Power Apps**.

3. Grunnstilla innfellt Power Apps:

    - Reiturinn **Heiti** gefur til kynna textann sem er sýndur fyrir hnappinn eða flipann sem mun innihalda innfellt Power Apps. Oft getur verið að þú viljir endurtaka heiti Power Apps í þessum reit.
    - **Kenni forrits** er GUID fyrir Power Apps sem þú vilt fella inn. Til að sækja þetta gildi skaltu finna Power Apps á [web.powerapps.com](https://web.powerapps.com) og finna síðan reitinn **Kenni forrits** undir **Upplýsingar**.
    - Fyrir **Setja inn gögn fyrir Power Apps** er valfrjálst hægt að velja reitinn sem inniheldur gögnin sem þú vilt flytja yfir í Power Apps sem inntak. Sjá kaflann síðar í þessu efnisatriði undir heitinu [Búa til Power Apps sem nýtir gögn úr forritum Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps) til að fá upplýsingar um hvernig Power Apps getur nálgast gögn sem send eru úr forritum Finance and Operations.
    - Veldu **Stærð forrits** sem passar við Power Apps-gerðina sem þú ert að fella inn. Veldu **Mjótt** fyrir Power Apps byggt fyrir fartæki og **Breitt** fyrir Power Apps byggt fyrir spjaldtölvur. Þetta tryggir að nægilegt magn af plássi sé úthlutað fyrir innfellt Power Apps.
    - Flýtiflipinn **Lögaðilar** veitir möguleika á að velja lögaðilana sem Power Apps er í boði fyrir. Sjálfgefið er að sýna Power Apps í öllum lögaðilum.

4. Eftir að hafa staðfest að grunnstillingarnar séu réttar skal smella á **Setja inn** til að fella inn Power Apps á síðunni. Þú verður beðinn um að uppfæra vafrann til að geta séð innfellt Power Apps.

## <a name="sharing-an-embedded-power-app"></a>Að deila innfelldu Power Apps

Eftir að þú hefur fellt Power Apps inn á síðu og staðfest að það virki rétt með hvaða gagnasamhengi sem kemur frá síðunni, gætirðu viljað deila þessu innfelllda Power Apps með öðrum notendum í kerfinu. Þetta er hægt að framkvæma á tvenns konar hátt með því að nota sérstillingarvalkosti vörunnar:

- Ráðlögð atburðarás er í gegnum kerfisstjóra sem getur ýtt sérstillingu til allra notenda eða undirhóps notenda.
- Einnig er hægt að flytja út sérstillingu síðunnar, senda þær á einn eða fleiri notendur og fá hvern notanda til að flytja inn þessar breytingar. Stjórna valkosturinn á tækjastiku sérstillinga gerir þér kleift að flytja út og flytja inn sérstillingar.

Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um sérstillingarvalkosti á vörunni og hvernig á að nota þá.

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Búa til Power Apps sem nýtir gögn sem eru send úr forriti Finance and Operations

Mikilvægur þáttur í því að byggja upp Power Apps sem verður fellt inn í forrit Finance and Operations er að nýta inntaksgögnin úr forritum Finance and Operations. Inni í Power Apps er hægt að nálgast þessi inntaksgögn með því að nota Param("EntityId") breytuna.

Til dæmis, í OnStart aðgerðinni í Power Apps getur þú stillt inntaksgögnin úr forritum Finance and Operations sem í breytu eins og þessa:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Skoða innfellt Power Apps

Til að skoða innfellt Power Apps á síðu í forritum Finance and Operations skal einfaldlega fara á síðu með innfellt Power Apps. Munið að hægt er að komast í Power Apps í gegnum hnappinn Power Apps á staðlaða aðgerðasvæðinu, eða það getur birst beint á síðunni sem nýr flipi, flýtiflipi, blað eða sem nýr hluti á vinnusvæði. Þegar notandi reynir fyrst að hlaða inn Power Apps á síðu verður hann eða hún beðinn um að skrá sig inn í Power Apps til að tryggja að notandinn hafi viðeigandi heimildir til að nota Power Apps.

## <a name="editing-an-embedded-power-app"></a>Breyta innfelldu Power Apps

Eftir að Power Apps hefur verið fellt inn á síðu getur verið að þú þurfir að gera nokkrar breytingar á grunnstillingu þessa Power Apps. Til dæmis viltu hugsanlega breyta merkingunni sem tengist innfelldu Power Apps eða ný útgáfa af Power Apps hefur verið búin til og þú þarft að uppfæra kenni forrits til að benda á nýjasta Power Apps.

Fylgdu þessum skrefum til að breyta grunnstillingu á innfelldu Power Apps:

1. Farðu á svæðið **Breyta Power Apps**.

    - Ef farið er í innfellt Power Apps í gegnum Power Apps valmyndarhnappinn skaltu hægrismella á Power Apps valmyndarhnappinn og velja **Sérstilla**. Veldu Power Apps sem þú vilt grunnstilla úr fellivalmyndinni **Velja Power Apps**.
    - Ef innfellt Power Apps birtist beint á síðunni skaltu velja **Valkostir** og síðan velja **Sérstilla þessa skjámynd**. Með verkfærinu **Velja** skaltu smella á innfellt Power Apps.

2. Gerðu nauðsynlegar breytingar á grunnstillingu Power Apps og smelltu síðan á **Vista**.

## <a name="removing-an-embedded-power-app"></a>Fjarlægja innfellt Power Apps

Eftir að Power Apps hefur verið fellt inn á síðu eru tvær leiðir til að fjarlægja það ef þörf krefur:

- Farðu á svæðið **Breyta Power Apps** samkvæmt leiðbeiningunum úr kaflanum [Breyta innfelldu Power Apps](#editing-an-embedded-powerapp) fyrr í þessu efnisatriði. Staðfestu að svæðið birti upplýsingar um innbyggða Power Apps sem þú vilt fjarlægja og smelltu síðan á hnappinn **Eyða**.
- Vegna þess að innfellt Power Apps er vistað sem sérstillt gögn, mun hreinsun á sérstillingum síðunnar einnig fjarlægja innfelldu Power Apps á þessari síðu. Athugaðu að hreinsun á sérstillingum síðunnar er varanleg og ekki hægt að afturkalla. Til að fjarlægja sérstillingar þínar á síðu skaltu velja **Valkostir** og smella síðan á **Sérsníða þessa skjámynd**. Undir valmyndinni **Stjórna** skal velja hnappinn **Hreinsa**. Allar fyrri sérstillingar fyrir þessa síðu verða fjarlægðar þegar vafrinn er uppfærður. Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um hvernig á að fínstilla síður með sérstillingu.

## <a name="appendix"></a>Viðauki

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Stýring þróunaraðila á því hvar hægt er að fella inn Power Apps

Að sjálfgefnu geta notendur fellt Power Apps inn á hvaða síðu sem er, annaðhvort undir valmyndarhnappi Power Apps eða beint á síðuna sem flipa, flýtiflipa, blaði eða sem nýjum hluta á vinnusvæði. Hins vegar, ef þörf krefur, geta þróunaraðilar einnig skilgreint þennan eiginleika til að aðeins leyfa innfellingu á Power Apps á ákveðnum síðum með því að framkvæma eftirfarandi aðferðir:

- **isPowerAppPersonalizationEnabled** – Ef þessi aðferð skilar röngu fyrir tiltekna síðu, þá birtist ekki valmyndarhnappur Power Apps og notendur geta ekki fellt inn Power Apps hvar sem er á þessari síðu, þar á meðal sem flipa.
- **isPowerAppTabPersonalizationEnabled** – Ef þessi aðferð skilar röngu fyrir tiltekna síðu þá geta notendur ekki fellt Power Apps beint inn á síðuna sem flipa, flýtiflipa eða víðmyndarhluta. Notendur geta samt fellt inn Power Apps í gegnum valmyndarhnapp Power Apps ef innfelling er leyfileg á síðunni.

Eftirfarandi dæmi sýnir nýja tegund með þeim tveimur aðferðum sem þarf til að skilgreina hvar hægt er að fella Power Apps inn.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
