---
title: Innfelld vinnuforrit frá Power Apps
description: Þetta efnisatriði útskýrir hvernig á að innleiða vinnusvæðisforrit úr Microsoft Power Apps og í biðlarann til að auka virkni vörunnar.
author: jasongre
manager: AnnBe
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: fbdd4dd1bb0b850319b12e55b0e68d6fdc516ad6
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798378"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Innfelld vinnuforrit frá Power Apps

[!include [banner](../includes/banner.md)]

Microsoft Power Apps er þjónusta sem gerir þróunaraðilum og öðrum notendum með litla tæknikunnáttu kleift að byggja upp sérsniðin viðskiptaforrit fyrir fartæki, spjaldtölvur og netið án þess að skrifa kóða. Finance and Operations-forrit styðja samþættingu við Power Apps. Vinnusvæðaforrit sem þú, fyrirtækið þitt eða samfélagið þróar er hægt að fella inn í Finance and Operations-forrit til að auka virkni vörunnar. Til dæmis gætir þú smíðað vinnusvæðaforrit úr Power Apps til að bæta við Finance and Operations-forrit með upplýsingum sem sóttar eru úr öðru kerfi.

Til að fræðast meira um innfellingu á Power Apps skal horfa á stutt myndband [Hvernig á að innleiða Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Innfelldu vinnusvæðaforriti bætt við úr Power Apps á síðu

### <a name="overview"></a>Yfirlit

Áður en vinnusvæðaforrit er fellt inn úr Power Apps í biðlarann, þarf að finna eða smíða forrit sem er með æskilegt viðmót eða virkni. Í þessu efnisatriði er ekki að finna nákvæma lýsingu á ferlinu við að smíða forrit. Ef þú hefur litla eða enga reynslu af Power Apps skaltu skoða [Power Apps fylgigögn](https://docs.microsoft.com/powerapps/).

Tvær leiður eru í boði til að opna tiltekið vinnusvæðaforrit á síðu þegar þú ert tilbúin(n) að fella inn forritið. Hægt er að velja aðra hvora nálgunina eftir því sem hentar þínum aðstæðum. Fyrsta leiðin notar hnappinn **Power Apps** sem hefur verið bætt við hefðbundna aðgerðasvæðið. Forritum sem bætt er við með því að nota þessa aðferð líta út eins og atriði á valmyndarhnappnum **Power Apps**. Þegar eitt þessara atriða er valið, birtist hliðargluggi sem inniheldur innfellda forritið. Að öðrum kosti er hægt að fella inn forrit beint á síðu sem nýjan flipa, flýtiflipa eða blaði, eða sem nýjum hluta á vinnusvæði.

Þegar innfellt vinnusvæðaforrit er skilgreint er hægt að velja einn reit sem ætlunin er að senda sem samhengi til forritsins. Þetta skref gerir forritinu kleift að geta brugðist við á grundvelli gagna sem verið er að skoða.

> [!NOTE]
> Sem stendur er ekki hægt að nota þessa virkni til að fella inn þróuð forrit.  

### <a name="details"></a>Upplýsingar

Eftirfarandi ferli sýnir hvernig á að fella inn vinnusvæðaforrit úr Power Apps í vefbiðlarann.

1. Farið á síðuna þar sem á að fella inn vinnusvæðaforritið. Þessi síða verður sú síða sem inniheldur gögn sem þarf að senda til forritsins sem inntak.
2. Opnaðu gluggann **Bæta við forriti frá Power Apps**:

    - Smelltu á **Valkostir** og veldu síðan **Sérstilla þessa síðu**. Undir valmyndinni **Setja inn** skal velja **Power Apps**. Að lokum skal velja svæðið þar sem þú vilt bæta við forriti. Ef þú vilt fella forrit inn í valmyndarhnapp Power Apps skaltu velja aðgerðasvæðið. Ef þú vilt fella forritið beint inn á síðuna skaltu velja viðeigandi flipa, flýtiflipa, blað eða hluta (ef þú ert á vinnusvæði).
    - Ef hægt er að komast í forritið með því að nota valmyndarhnapp Power Apps geturðu einnig smellt á valmyndarhnappinn **Power Apps** á staðlaða aðgerðasvæðinu og síðan valið **Bæta við forriti**.

3. Grunnstilla innfellt forrit:

    - Reiturinn **Heiti** gefur til kynna textann sem er sýndur fyrir hnappinn eða flipann sem mun innihalda innfellt forrit. Oft getur verið að þú viljir endurtaka heiti forritsins í þessum reit.
    - Reiturinn **Forritskenni** gefur til kynna altækt einkvæmt kennimerki fyrir vinnusvæðaforritið sem á að fella inn. Til að sækja þetta gildi skaltu finna forritið á [make.powerapps.com](https://make.powerapps.com) og skoða síðan reitinn **Forritskenni** undir **Upplýsingar**.
    - Fyrir **Setja inn samhengi fyrir forritið** er valfrjálst hægt að velja reitinn sem inniheldur gögnin sem þú vilt flytja yfir í forritið sem inntak. Sjá kaflann síðar í þessu efnisatriði undir heitinu [Búa til forrit sem nýtir gögn úr forritum Finance and Operations](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) til að fá upplýsingar um hvernig forritið getur nálgast gögn sem send eru úr forritum Finance and Operations.
    - Veldu **Stærð forrits** sem passar við forritsgerðina sem þú ert að fella inn. Veldu **Mjór** fyrir forrit byggt fyrir fartæki og **Breiður** fyrir forrit byggt fyrir spjaldtölvur. Þetta tryggir að nægilegt magn af plássi sé úthlutað fyrir innfellt forrit.
    - Flýtiflipinn **Lögaðilar** veitir möguleika á að velja lögaðilana sem forritið er í boði fyrir. Sjálfgefið er að gera forritið aðgengilegt í öllum lögaðilum. Þessi valkostur er aðeins í boði þegar aðgerðin [Vistaðar skoðanir](saved-views.md) er óvirk. 

4. Eftir að hafa staðfest að grunnstillingarnar séu réttar skal smella á **Setja inn** til að fella inn Power Apps á síðunni. Þú verður beðinn um að uppfæra vafrann til að geta séð innfellt forrit.

## <a name="sharing-an-embedded-app"></a>Að deila innfelldu forriti

Þegar vinnusvæðaforrit hefur verið fellt inn á síðu og staðfest að það virki á réttan hátt í hvaða gagnasamhengi sem er sem er sent frá síðunni, gætirðu viljað deila forritinu með öðrum notendum kerfisins. Til að deila innfelldu vinnusvæðaforriti skal fylgja þessum skrefum.

1. [Deilið vinnusvæðaforritinu](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) með viðeigandi notendum þannig að þeir geti fengið aðgang að forritinu í Power Apps. 

2. Gangið úr skugga um að þessi notendur séu með viðeigandi sérstillingar þannig að innfellda forritið birtist þegar þessi notendur skoða síðuna. Hægt er að aðra hvora af eftirfarandi aðferðum:

    - Ráðlagt: Notið eiginleikann [Vistuð yfirlit](saved-views.md) til að búa til og birta yfirlit sem inniheldur innfellda forritið. Þessi aðferð tryggir að allir notendur sem eru með öryggishlutverk sem birta yfirlitið beinist að komi til með að sjá forritið í Finance and Operations-forritum. 
    - Ef ekki er kveikt á eiginleikanum Vistað yfirlit er hægt að fá kerfisstjórann til að senda út sérstillingu sem inniheldur innfellt forrit á alla notendur eða undirhóp notenda. Einnig er hægt að flytja út sérstillingar síðunnar og senda þær á einn eða fleiri notendur. Hver þessara notenda getur síðan flutt inn sérstillingarnar. Tækjastika sérstillinga er með aðgerðir sem gera þér kleift að flytja út eða flytja inn sérstillingar. 
    
> [!NOTE]
> Ef vinnusvæðaforritinu hefur verið deilt með ytri notendum, geta þessir notendur ekki notað innfellda forritið í Finance and Operations-forritum. Hins vegar geta þeir nálgast forritið beint inni í Power Apps. Ytri notendur eru gestir eða notendur sem tilheyra ekki Microsoft 365 Azure Directory þar sem Finance and Operations-forritið er sett upp.

Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um sérstillingarvalkosti á vörunni og hvernig á að nota þá.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Vinnusvæðaforrit smíðað sem notar gögn sem eru send úr Finance and Operations-forritum

Þegar vinnusvæðaforrit er smíðað sem mun fella inn Finance and Operations-forrit, er mikilvægur hluti ferlisins að nota inntaksgögnin úr þessu Finance and Operations-forriti. Úr þróunarreynslu Power Apps er hægt að fá aðgang að inntaksgögnunum sem koma frá Finance and Operations-forritinu með því að nota breytuna **Param("EntityId")**.

Til dæmis, í OnStart aðgerðinni í forritinu getur þú stillt inntaksgögnin úr forritum Finance and Operations sem í breytu eins og þessa:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Vinnusvæðaforrit skoðað

Til að skoða innfellt vinnusvæðaforrit á síðu í Finance and Operations-forritum skal einfaldlega fara á síðu sem er með innfellt forrit. Munið að hægt er að opna forrit með því að nota hnappinn **Power Apps** á staðlaða aðgerðasvæðinu. Að öðrum kosti geta þær birst beint á síðunni sem nýr flipi eða flýtiflipi eða blað eða sem nýr hluti á vinnusvæði. Þegar notendur reyna fyrst að hlaða forriti á síðu verða þeir beðnir um að skrá sig inn. Þetta skref tryggir að notendur hafi viðeigandi heimildir til að nota forritið.

## <a name="editing-an-embedded-app"></a>Breyta innfelldu forriti

Eftir að forrit hefur verið fellt inn á síðu getur verið að þú þurfir að gera nokkrar breytingar á grunnstillingu þessa forrits. Til dæmis viltu hugsanlega breyta merkingunni sem tengist innfelldu forriti eða ný útgáfa af forriti hefur verið búin til og þú þarft að uppfæra kenni forrits til að benda á það nýjasta.

Fylgdu þessum skrefum til að breyta grunnstillingu á innfelldu forriti:

1. Farðu á svæðið **Breyta forriti**.

    - Ef farið er í innfellt forrit í gegnum Power Apps valmyndarhnappinn skaltu hægrismella á Power Apps valmyndarhnappinn og velja **Sérstilla**. Veldu forrit sem þú vilt grunnstilla úr fellivalmyndinni **Velja forrit**.
    - Ef innfellt forrit birtist beint á síðunni skaltu velja **Valkostir** og síðan velja **Sérstilla þessa síðu**. Með verkfærinu **Velja** skaltu smella á innfellt forrit.

2. Gerðu nauðsynlegar breytingar á grunnstillingu forritsins og smelltu síðan á **Vista**.

## <a name="removing-an-app"></a>Forrit fjarlægt

Eftir að forit hefur verið fellt inn á síðu eru tvær leiðir til að fjarlægja það ef þörf krefur:

- Farðu á svæðið **Breyta forriti** samkvæmt leiðbeiningunum úr kaflanum [Breyta innfelldu forriti](#editing-an-embedded-app) fyrr í þessu efnisatriði. Staðfestu að svæðið birti upplýsingar um innbyggða forritið sem þú vilt fjarlægja og smelltu síðan á hnappinn **Eyða**.
- Vegna þess að innfellt forrit er vistað sem sérstillt gögn, mun hreinsun á sérstillingum síðunnar einnig fjarlægja innfelld forrit á þessari síðu. Athugaðu að hreinsun á sérstillingum síðunnar er varanleg og ekki hægt að afturkalla. Til að fjarlægja sérstillingar þínar á síðu skaltu velja **Valkostir** og smella síðan á **Sérsníða þessa síðu** og að lokum á hnappinn **Hreinsa**. Allar fyrri sérstillingar fyrir þessa síðu verða fjarlægðar þegar vafrinn er uppfærður. Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um hvernig á að fínstilla síður með sérstillingu.

## <a name="appendix"></a>Viðauki

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Þróunaraðili] Tilgreint hvar hægt er að fella inn forrit

Að sjálfgefnu geta notendur fellt forrit inn á hvaða síðu sem er, annaðhvort undir valmyndarhnappi Power Apps eða beint á síðuna sem flipa, flýtiflipa, blaði eða sem nýjum hluta á vinnusvæði. Hins vegar, ef þörf krefur, geta þróunaraðilar einnig skilgreint þennan eiginleika til að aðeins leyfa innfellingu á forritum á ákveðnum síðum með því að framkvæma eftirfarandi aðferðir:

- **isPowerAppPersonalizationEnabled** – Ef þessi aðferð skilar röngu fyrir tiltekna síðu, þá birtist ekki valmyndarhnappur Power Apps og notendur geta ekki fellt inn forrit hvar sem er á þessari síðu, þar á meðal sem flipa.
- **isPowerAppTabPersonalizationEnabled** – Ef þessi aðferð skilar röngu fyrir tiltekna síðu þá geta notendur ekki fellt forrit beint inn á síðuna sem flipa, flýtiflipa eða víðmyndarhluta. Notendur geta samt fellt inn forrit í gegnum valmyndarhnapp Power Apps ef innfelling er leyfileg á síðunni.

Eftirfarandi dæmi sýnir nýja tegund með þeim tveimur aðferðum sem þarf til að skilgreina hvar hægt er að fella inn forrit.

```powerapps
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
