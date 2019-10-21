---
title: Innfella PowerApps-forrit
description: Þetta efnisatriði lýsir því hvernig á að fella PowerApps inn í biðlarann til að auka virkni vörunnar.
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
ms.openlocfilehash: 37faf2a7a880c384f6f01d06ef5c9f28055d5006
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191179"
---
# <a name="embed-powerapps-apps"></a>Innfella PowerApps-forrit

[!include [banner](../includes/banner.md)]

Verkvangsuppfærsla 14 styður samþættingu við Microsoft PowerApps, þjónustu fyrir þróunaraðila og aðra ekki tæknilega notendur til að byggja upp sérsniðin viðskiptaforrit fyrir fartæki, spjaldtölvur og netið án þess að skrifa kóða. PowerApps þróað af þér, fyrirtæki þínu eða breiðara vistkerfi er síðan hægt að fella inn í forritum Finance and Operations til að auka virkni vörunnar. Til dæmis gætir þú byggt upp PowerApp til að bæta við forrit Finance and Operations með upplýsingum sem eru sótt úr öðru kerfi.

Til að fræðast meira um innfellingu á PowerApps skal horfa á stutt myndband [Hvernig á að innleiða PowerApps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Bætir við innfelldu PowerApp á síðu

### <a name="overview"></a>Yfirlit

Áður en PowerApp er fellt inn í biðlara þarftu fyrst að finna eða byggja upp PowerApp með viðkomandi myndefni og/eða virkni. Við munum ekki lýsa í smáatriðum ferlinu um hvernig skuli byggja upp PowerApp hér. Efnisatriðið [Inngangur að PowerApps](https://docs.microsoft.com/powerapps/getting-started) er góður upphafsstaður ef þú hefur ekki reynslu af PowerApps.

Þegar þú ert tilbúin/n til að fella inn ákveðið PowerApp getur þú valið á milli tveggja leiða til að fá aðgang að PowerApp á síðu, fer eftir því hvor leiðin hentar betur. Fyrsta leiðin er í gegnum hnappinn PowerApps sem hefur verið bætt við staðlaða aðgerðasvæðið. PowerApps bætt við með þessari aðferð mun birtast sem valmyndaratriði inni í PowerApps valmyndarhnappnum. Þegar valið, þá opnar hvert þessara valmyndaratriða hliðarsvæði sem inniheldur innfellt PowerApp. Að öðrum kosti getur þú valið að sýna PowerApp beint á síðu sem nýjan flipa, flýtiflipa, blað eða sem nýjan hluta á vinnusvæði.

Þegar þú grunnstillir innfellt PowerApp er hægt að velja stakan reit sem þú vilt senda sem inntak í PowerApp. Þetta gerir PowerApp kleift að svara á grundvelli gagna sem þú ert að skoða á þeirri stundu.

### <a name="details"></a>Upplýsingar

Eftirfarandi leiðbeiningar sýna hvernig á að fella PowerApp inn í vefbiðlara.

1. Farðu á síðuna þar sem þú vilt fella inn PowerApp. Þetta verður sama síðan og sú sem inniheldur allar þær upplýsingar sem þarf að flytja yfir til PowerApp sem inntak.
2. Opnaðu svæðið **Setja inn PowerApp**:

    - Smelltu á **Valkostir** og veldu síðan **Sérstilla þessa skjámynd**. Undir valmyndinni **Setja inn** skal velja **PowerApp**. Að lokum skal velja svæðið þar sem þú vilt bæta við PowerApp. Ef þú vilt fella PowerApp inn í valmyndarhnapp PowerApps skaltu velja aðgerðasvæðið. Ef þú vilt fella PowerApp beint inn á síðuna skaltu velja viðeigandi flipa, flýtiflipa, blað eða hluta (ef þú ert á vinnusvæði).
    - Ef hægt er að komast í PowerApp með því að nota valmyndarhnapp PowerApps geturðu einnig smellt á valmyndarhnappinn **PowerApps** á staðlaða aðgerðasvæðinu og síðan valið **Setja inn PowerApp**.

3. Grunnstilla innfellt PowerApp:

    - Reiturinn **Heiti** gefur til kynna textann sem er sýndur fyrir hnappinn eða flipann sem mun innihalda innfellt PowerApp. Oft getur verið að þú viljir endurtaka heiti PowerApp í þessum reit.
    - **Kenni forrits** er GUID fyrir PowerApp sem þú vilt fella inn. Til að sækja þetta gildi skaltu finna PowerApp á [web.powerapps.com](https://web.powerapps.com) og finna síðan reitinn **Kenni forrits** undir **Upplýsingar**.
    - Fyrir **Setja inn gögn fyrir PowerApp** er valfrjálst hægt að velja reitinn sem inniheldur gögnin sem þú vilt flytja yfir í PowerApp sem inntak. Sjá kaflann síðar í þessu efnisatriði undir heitinu [Búa til PowerApp sem nýtir gögn úr forritum Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps) til að fá upplýsingar um hvernig PowerApp getur nálgast gögn sem send eru úr forritum Finance and Operations.
    - Veldu **Stærð forrits** sem passar við PowerApp-gerðina sem þú ert að fella inn. Veldu **Mjótt** fyrir PowerApps byggt fyrir fartæki og **Breitt** fyrir PowerApps byggt fyrir spjaldtölvur. Þetta tryggir að nægilegt magn af plássi sé úthlutað fyrir innfellt PowerApp.
    - Flýtiflipinn **Lögaðilar** veitir möguleika á að velja lögaðilana sem PowerApp er í boði fyrir. Sjálfgefið er að sýna PowerApp í öllum lögaðilum.

4. Eftir að hafa staðfest að grunnstillingarnar séu réttar skal smella á **Setja inn** til að fella inn PowerApp á síðunni. Þú verður beðinn um að uppfæra vafrann til að geta séð innfellt PowerApp.

## <a name="sharing-an-embedded-powerapp"></a>Að deila innfelldu PowerApp

Eftir að þú hefur fellt PowerApp inn á síðu og staðfest að það virki rétt með hvaða gagnasamhengi sem kemur frá síðunni, gætirðu viljað deila þessu innfelllda PowerApp með öðrum notendum í kerfinu. Þetta er hægt að framkvæma á tvenns konar hátt með því að nota sérstillingarvalkosti vörunnar:

- Ráðlögð atburðarás er í gegnum kerfisstjóra sem getur ýtt sérstillingu til allra notenda eða undirhóps notenda.
- Einnig er hægt að flytja út sérstillingu síðunnar, senda þær á einn eða fleiri notendur og fá hvern notanda til að flytja inn þessar breytingar. Stjórna valkosturinn á tækjastiku sérstillinga gerir þér kleift að flytja út og flytja inn sérstillingar.

Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um sérstillingarvalkosti á vörunni og hvernig á að nota þá.

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps"></a>Búa til PowerApp sem nýtir gögn sem eru send úr forriti Finance and Operations

Mikilvægur þáttur í því að byggja upp PowerApp sem verður fellt inn í forrit Finance and Operations er að nýta inntaksgögnin úr forritum Finance and Operations. Inni í PowerApp er hægt að nálgast þessi inntaksgögn með því að nota Param("EntityId") breytuna.

Til dæmis, í OnStart aðgerðinni í PowerApp getur þú stillt inntaksgögnin úr forritum Finance and Operations sem í breytu eins og þessa:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a>Skoða innfellt PowerApp

Til að skoða innfellt PowerApp á síðu í forritum Finance and Operations skal einfaldlega fara á síðu með innfellt PowerApp. Munið að hægt er að komast í PowerApps í gegnum hnappinn PowerApps á staðlaða aðgerðasvæðinu, eða það getur birst beint á síðunni sem nýr flipi, flýtiflipi, blað eða sem nýr hluti á vinnusvæði. Þegar notandi reynir fyrst að hlaða inn PowerApp á síðu verður hann eða hún beðinn um að skrá sig inn í PowerApps til að tryggja að notandinn hafi viðeigandi heimildir til að nota PowerApp.

## <a name="editing-an-embedded-powerapp"></a>Breyta innfelldu PowerApp

Eftir að PowerApp hefur verið fellt inn á síðu getur verið að þú þurfir að gera nokkrar breytingar á grunnstillingu þessa PowerApp. Til dæmis viltu hugsanlega breyta merkingunni sem tengist innfelldu PowerApp eða ný útgáfa af PowerApp hefur verið búin til og þú þarft að uppfæra kenni forrits til að benda á nýjasta PowerApp.

Fylgdu þessum skrefum til að breyta grunnstillingu á innfelldu PowerApp:

1. Farðu á svæðið **Breyta PowerApp**.

    - Ef farið er í innfellt PowerApp í gegnum PowerApps valmyndarhnappinn skaltu hægrismella á PowerApps valmyndarhnappinn og velja **Sérstilla**. Veldu PowerApp sem þú vilt grunnstilla úr fellivalmyndinni **Velja PowerApp**.
    - Ef innfellt PowerApp birtist beint á síðunni skaltu velja **Valkostir** og síðan velja **Sérstilla þessa skjámynd**. Með verkfærinu **Velja** skaltu smella á innfellt PowerApp.

2. Gerðu nauðsynlegar breytingar á grunnstillingu PowerApps og smelltu síðan á **Vista**.

## <a name="removing-an-embedded-powerapp"></a>Fjarlægja innfellt PowerApp

Eftir að PowerApp hefur verið fellt inn á síðu eru tvær leiðir til að fjarlægja það ef þörf krefur:

- Farðu á svæðið **Breyta PowerApp** samkvæmt leiðbeiningunum úr kaflanum [Breyta innfelldu PowerApp](#editing-an-embedded-powerapp) fyrr í þessu efnisatriði. Staðfestu að svæðið birti upplýsingar um innbyggða PowerApp sem þú vilt fjarlægja og smelltu síðan á hnappinn **Eyða**.
- Vegna þess að innfellt PowerApp er vistað sem sérstillt gögn, mun hreinsun á sérstillingum síðunnar einnig fjarlægja innfelldu PowerApps á þessari síðu. Athugaðu að hreinsun á sérstillingum síðunnar er varanleg og ekki hægt að afturkalla. Til að fjarlægja sérstillingar þínar á síðu skaltu velja **Valkostir** og smella síðan á **Sérsníða þessa skjámynd**. Undir valmyndinni **Stjórna** skal velja hnappinn **Hreinsa**. Allar fyrri sérstillingar fyrir þessa síðu verða fjarlægðar þegar vafrinn er uppfærður. Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um hvernig á að fínstilla síður með sérstillingu.

## <a name="appendix"></a>Viðauki

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Stýring þróunaraðila á því hvar hægt er að fella inn PowerApp

Að sjálfgefnu geta notendur fellt PowerApps inn á hvaða síðu sem er, annaðhvort undir valmyndarhnappi PowerApps eða beint á síðuna sem flipa, flýtiflipa, blaði eða sem nýjum hluta á vinnusvæði. Hins vegar, ef þörf krefur, geta þróunaraðilar einnig skilgreint þennan eiginleika til að aðeins leyfa innfellingu á PowerApps á ákveðnum síðum með því að framkvæma eftirfarandi aðferðir:

- **isPowerAppPersonalizationEnabled** – Ef þessi aðferð skilar röngu fyrir tiltekna síðu, þá birtist ekki valmyndarhnappur PowerApps og notendur geta ekki fellt inn PowerApps hvar sem er á þessari síðu, þar á meðal sem flipa.
- **isPowerAppTabPersonalizationEnabled** – Ef þessi aðferð skilar röngu fyrir tiltekna síðu þá geta notendur ekki fellt PowerApps beint inn á síðuna sem flipa, flýtiflipa eða víðmyndarhluta. Notendur geta samt fellt inn PowerApps í gegnum valmyndarhnapp PowerApps ef innfelling er leyfileg á síðunni.

Eftirfarandi dæmi sýnir nýja tegund með þeim tveimur aðferðum sem þarf til að skilgreina hvar hægt er að fella PowerApps inn.

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
