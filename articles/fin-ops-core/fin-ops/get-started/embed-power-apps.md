---
title: Fella inn Power Apps
description: Þetta efnisatriði lýsir því hvernig á að fella Power Apps inn í biðlarann til að auka virkni vörunnar.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
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
ms.openlocfilehash: 9585d5a399ebf45b0ad7640f3c4e48d8afc46cd8
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017729"
---
# <a name="embed-microsoft-power-apps"></a>Fella inn Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Finance and Operations styður samþættingu við Microsoft Power Apps, þjónustu fyrir þróunaraðila og aðra ekki tæknilega notendur til að byggja upp sérsniðin viðskiptaforrit fyrir fartæki, spjaldtölvur og netið án þess að skrifa kóða. Power Apps þróað af þér, fyrirtæki þínu eða breiðara vistkerfi er síðan hægt að fella inn í forritum Finance and Operations til að auka virkni vörunnar. Til dæmis gætir þú byggt upp forrit úr Power Apps til að auka við forrit Finance and Operations með upplýsingum sem eru sóttar úr öðru kerfi.

Til að fræðast meira um innfellingu á Power Apps skal horfa á stutt myndband [Hvernig á að innleiða Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Bætir við innfelldu forriti Power Apps á síðu

### <a name="overview"></a>Yfirlit

Áður en forrit úr Power Apps er fellt inn í biðlara þarftu fyrst að finna eða byggja upp forrit með viðkomandi myndefni og/eða virkni. Við munum ekki lýsa í smáatriðum ferlinu um hvernig skuli byggja upp forrit hér. Efnisatriðið [Inngangur að Power Apps](https://docs.microsoft.com/powerapps/getting-started) er góður upphafsstaður ef þú hefur ekki reynslu af Power Apps.

Þegar þú ert tilbúin/n til að fella inn ákveðið forrit getur þú valið á milli tveggja leiða til að fá aðgang að forriti á síðu, fer eftir því hvor leiðin hentar betur. Fyrsta leiðin er í gegnum hnappinn Power Apps sem hefur verið bætt við staðlaða aðgerðasvæðið. Forrit sem bætt við með þessari aðferð mun birtast sem valmyndaratriði inni í Power Apps valmyndarhnappnum. Þegar valið, þá opnar hvert þessara valmyndaratriða hliðarsvæði sem inniheldur innfellt forrit. Að öðrum kosti getur þú valið að fella forrit beint inn á síðu sem nýjan flipa, flýtiflipa, blað eða sem nýjan hluta á vinnusvæði.

Þegar þú grunnstillir innfellt forrit er hægt að velja stakan reit sem þú vilt senda sem samhengi í forritinu. Þetta gerir forritinu kleift að svara á grundvelli gagna sem þú ert að skoða á þeirri stundu.

### <a name="details"></a>Upplýsingar

Eftirfarandi leiðbeiningar sýna hvernig á að fella forrit úr Power Apps inn í vefbiðlara.

1. Farðu á síðuna þar sem þú vilt fella forritið inn. Þetta verður sama síðan og sú sem inniheldur allar þær upplýsingar sem þarf að flytja yfir til forritsins sem inntak.
2. Opnaðu gluggann **Bæta við forriti frá Power Apps**:

    - Smelltu á **Valkostir** og veldu síðan **Sérstilla þessa síðu**. Undir valmyndinni **Setja inn** skal velja **Power Apps**. Að lokum skal velja svæðið þar sem þú vilt bæta við forriti. Ef þú vilt fella forrit inn í valmyndarhnapp Power Apps skaltu velja aðgerðasvæðið. Ef þú vilt fella forritið beint inn á síðuna skaltu velja viðeigandi flipa, flýtiflipa, blað eða hluta (ef þú ert á vinnusvæði).
    - Ef hægt er að komast í forritið með því að nota valmyndarhnapp Power Apps geturðu einnig smellt á valmyndarhnappinn **Power Apps** á staðlaða aðgerðasvæðinu og síðan valið **Bæta við forriti**.

3. Grunnstilla innfellt forrit:

    - Reiturinn **Heiti** gefur til kynna textann sem er sýndur fyrir hnappinn eða flipann sem mun innihalda innfellt forrit. Oft getur verið að þú viljir endurtaka heiti forritsins í þessum reit.
    - **Kenni forrits** er GUID fyrir forritið sem þú vilt fella inn. Til að sækja þetta gildi skaltu finna forritið á [web.powerapps.com](https://web.powerapps.com) og finna síðan reitinn **Kenni forrits** undir **Upplýsingar**.
    - Fyrir **Setja inn samhengi fyrir forritið** er valfrjálst hægt að velja reitinn sem inniheldur gögnin sem þú vilt flytja yfir í forritið sem inntak. Sjá kaflann síðar í þessu efnisatriði undir heitinu [Búa til forrit sem nýtir gögn úr forritum Finance and Operations](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) til að fá upplýsingar um hvernig forritið getur nálgast gögn sem send eru úr forritum Finance and Operations.
    - Veldu **Stærð forrits** sem passar við forritsgerðina sem þú ert að fella inn. Veldu **Mjór** fyrir forrit byggt fyrir fartæki og **Breiður** fyrir forrit byggt fyrir spjaldtölvur. Þetta tryggir að nægilegt magn af plássi sé úthlutað fyrir innfellt forrit.
    - Flýtiflipinn **Lögaðilar** veitir möguleika á að velja lögaðilana sem forritið er í boði fyrir. Sjálfgefið er að gera forritið aðgengilegt í öllum lögaðilum. Þessi valkostur er aðeins í boði þegar aðgerðin [Vistaðar skoðanir](saved-views.md) er óvirk. 

4. Eftir að hafa staðfest að grunnstillingarnar séu réttar skal smella á **Setja inn** til að fella inn Power Apps á síðunni. Þú verður beðinn um að uppfæra vafrann til að geta séð innfellt forrit.

## <a name="sharing-an-embedded-app"></a>Að deila innfelldu forriti

Eftir að þú hefur fellt forrit inn á síðu og staðfest að það virki rétt með hvaða gagnasamhengi sem kemur frá síðunni, gætirðu viljað deila þessu forriti með öðrum notendum í kerfinu. Þetta er hægt að framkvæma á tvenns konar hátt með því að nota sérstillingarvalkosti vörunnar:

- Ráðlögð atburðarás er í gegnum kerfisstjóra sem getur ýtt sérstillingu til allra notenda eða undirhóps notenda.
- Einnig er hægt að flytja út sérstillingu síðunnar, senda þær á einn eða fleiri notendur og fá hvern notanda til að flytja inn þessar breytingar. Tækjastika sérstillinga er með aðgerðir sem gera þér kleift að flytja út og flytja inn sérstillingar.

Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um sérstillingarvalkosti á vörunni og hvernig á að nota þá.

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Búðu til forrit sem nýtir gögn sem send eru úr forritum Finance and Operations

Mikilvægur liður í því að byggja upp forrit úr Power Apps sem verður fellt inn í forrit Finance and Operations er að nota innsláttargögn úr því forriti. Úr þróunarupplifun Power Apps er hægt að fara í innsláttargögn send úr forriti Finance and Operations með Param-breytunni („EntityId“).

Til dæmis, í OnStart aðgerðinni í forritinu getur þú stillt inntaksgögnin úr forritum Finance and Operations sem í breytu eins og þessa:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Að skoða forrit

Til að skoða innfellt forrit á síðu í forritum Finance and Operations skal einfaldlega fara á síðu með innfellt forrit. Munið að hægt er að komast í forrit í gegnum hnappinn Power Apps á staðlaða aðgerðasvæðinu, eða það getur birst beint á síðunni sem nýr flipi, flýtiflipi, blað eða sem nýr hluti á vinnusvæði. Þegar notandi reynir fyrst að hlaða inn forriti á síðu verður hann eða hún beðinn um að skrá sig inn til að tryggja að notandinn hafi viðeigandi heimildir til að nota forritið.

## <a name="editing-an-embedded-app"></a>Breyta innfelldu forriti

Eftir að forrit hefur verið fellt inn á síðu getur verið að þú þurfir að gera nokkrar breytingar á grunnstillingu þessa forrits. Til dæmis viltu hugsanlega breyta merkingunni sem tengist innfelldu forriti eða ný útgáfa af forriti hefur verið búin til og þú þarft að uppfæra kenni forrits til að benda á það nýjasta.

Fylgdu þessum skrefum til að breyta grunnstillingu á innfelldu forriti:

1. Farðu á svæðið **Breyta forriti**.

    - Ef farið er í innfellt forrit í gegnum Power Apps valmyndarhnappinn skaltu hægrismella á Power Apps valmyndarhnappinn og velja **Sérstilla**. Veldu forrit sem þú vilt grunnstilla úr fellivalmyndinni **Velja forrit**.
    - Ef innfellt forrit birtist beint á síðunni skaltu velja **Valkostir** og síðan velja **Sérstilla þessa síðu**. Með verkfærinu **Velja** skaltu smella á innfellt forrit.

2. Gerðu nauðsynlegar breytingar á grunnstillingu forritsins og smelltu síðan á **Vista**.

## <a name="removing-an-app"></a>Forrit fjarlægt

Eftir að forit hefur verið fellt inn á síðu eru tvær leiðir til að fjarlægja það ef þörf krefur:

- Farðu á svæðið **Breyta forriti** samkvæmt leiðbeiningunum úr kaflanum [Breyta innfelldu forriti](#editing-an-embedded-power-app) fyrr í þessu efnisatriði. Staðfestu að svæðið birti upplýsingar um innbyggða forritið sem þú vilt fjarlægja og smelltu síðan á hnappinn **Eyða**.
- Vegna þess að innfellt forrit er vistað sem sérstillt gögn, mun hreinsun á sérstillingum síðunnar einnig fjarlægja innfelld forrit á þessari síðu. Athugaðu að hreinsun á sérstillingum síðunnar er varanleg og ekki hægt að afturkalla. Til að fjarlægja sérstillingar þínar á síðu skaltu velja **Valkostir** og smella síðan á **Sérsníða þessa síðu** og að lokum á hnappinn **Hreinsa**. Allar fyrri sérstillingar fyrir þessa síðu verða fjarlægðar þegar vafrinn er uppfærður. Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um hvernig á að fínstilla síður með sérstillingu.

## <a name="appendix"></a>Viðauki

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Stýring þróunaraðila á því hvar hægt er að fella inn forrit

Að sjálfgefnu geta notendur fellt forrit inn á hvaða síðu sem er, annaðhvort undir valmyndarhnappi Power Apps eða beint á síðuna sem flipa, flýtiflipa, blaði eða sem nýjum hluta á vinnusvæði. Hins vegar, ef þörf krefur, geta þróunaraðilar einnig skilgreint þennan eiginleika til að aðeins leyfa innfellingu á forritum á ákveðnum síðum með því að framkvæma eftirfarandi aðferðir:

- **isPowerAppPersonalizationEnabled** – Ef þessi aðferð skilar röngu fyrir tiltekna síðu, þá birtist ekki valmyndarhnappur Power Apps og notendur geta ekki fellt inn forrit hvar sem er á þessari síðu, þar á meðal sem flipa.
- **isPowerAppTabPersonalizationEnabled** – Ef þessi aðferð skilar röngu fyrir tiltekna síðu þá geta notendur ekki fellt forrit beint inn á síðuna sem flipa, flýtiflipa eða víðmyndarhluta. Notendur geta samt fellt inn forrit í gegnum valmyndarhnapp Power Apps ef innfelling er leyfileg á síðunni.

Eftirfarandi dæmi sýnir nýja tegund með þeim tveimur aðferðum sem þarf til að skilgreina hvar hægt er að fella inn forrit.

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
