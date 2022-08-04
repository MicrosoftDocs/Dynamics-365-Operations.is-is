---
title: Innfelld vinnuforrit frá Power Apps
description: Þessi grein útskýrir hvernig á að fella inn strigaforrit frá Microsoft Power Apps inn í viðskiptavininn til að auka virkni vörunnar.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: d7dc45e56c5fa616c288ebb4b919f039b7358794
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123655"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Innfelld vinnuforrit frá Power Apps

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Microsoft Power Apps er þjónusta sem gerir þróunaraðilum og öðrum notendum með litla tæknikunnáttu kleift að byggja upp sérsniðin viðskiptaforrit fyrir fartæki, spjaldtölvur og netið án þess að skrifa kóða. Fjármála- og rekstrarforrit styðja samþættingu við Power Apps. Hægt er að fella strigaforrit sem þú, fyrirtæki þitt eða víðtækara vistkerfi þróar inn í fjármála- og rekstrarforrit til að auka virkni vörunnar. Til dæmis gætirðu smíðað strigaforrit úr Power Apps að bæta við fjármála- og rekstrarapp með upplýsingum sem eru sóttar úr öðru kerfi.

Til að fræðast meira um innfellingu á vinnusvæðaforritum skal horfa á stutt myndband: [Hvernig á að innleiða vinnusvæðaforrit](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Innfelldu vinnusvæðaforriti bætt við úr Power Apps á síðu

Áður en vinnusvæðaforrit er fellt inn úr Power Apps í biðlarann, þarf að finna eða smíða forrit sem er með æskilegt viðmót eða virkni. Þessi grein inniheldur ekki nákvæma lýsingu á ferlinu við að búa til forrit. Ef þú hefur litla eða enga reynslu af Power Apps skaltu skoða [Power Apps fylgigögn](/powerapps/).

Það eru þrjár leiðir til að fella strigaforrit inn í fjármála- og rekstrarforrit. Þú getur notað þá aðferð sem passar best við þínar aðstæður. 

- Felldu vinnusvæðaforritið inn í hnappinn **Power Apps** á hefðbundnu aðgerðasvæði á síðu. Forrit sem þú bætir við á þennan hátt birtast sem atriði á valmyndarhnappnum **Power Apps** og forritin opnast í hliðarsvæðum. 
- Felldu vinnusvæðaforritið beint inn í fyrirliggjandi síðu sem síðu á nýjum flipa (snúningsflipa, flýtiflipa, blaði eða vinnusvæði).
- Búðu til nýja heilsíðuupplifun fyrir vinnusvæðaforritið úr stjórnborðinu.

Þegar innfellt vinnusvæðaforrit er skilgreint er hægt að velja einn reit sem ætlunin er að senda sem samhengi til forritsins. Þetta skref gerir forritinu kleift að geta brugðist við á grundvelli gagna sem verið er að skoða.

> [!NOTE]
> Ekki er hægt að nota þessa leið til að fella inn líkanadrifin forrit.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Innfella vinnusvæðaforrit á fyrirliggjandi síðu

Eftirfarandi ferli sýnir hvernig á að fella inn vinnusvæðaforrit í fyrirliggjandi síðu úr Power Apps.

1. Farið á síðuna þar sem á að fella inn vinnusvæðaforritið. Þessi síða mun innihalda gögn sem þarf að senda til forritsins sem inntak.
2. Opnaðu gluggann **Bæta við forriti frá Power Apps**:

    - Ef forritið verður fellt beint inn á síðuna skaltu velja **Valkostir** til að \> **Sérsníða þessa síðu** \> **Meira** og fylgja svo einu af eftirfarandi skrefum:

        - Ef kveikt er á eiginleikanum **Forrit á heilli síðu** skaltu velja **Bæta við síðu** og síðan velja svæðið þar sem þú vilt bæta við forritinu. Til að fella forritið inn í valmyndarhnappinn **Power Apps** skal velja aðgerðasvæðið. Til að fella forritið beint inn á síðuna skaltu velja viðeigandi flipa, flýtiflipa, blað eða hluta (ef þú ert á vinnusvæði). Því næst á svæðinu **Bæta við forriti** skaltu velja **Power Apps**.
        - Ef slökkt er á eiginleikanum **Forrit á heilli síðu** skaltu velja **Bæta við forriti af Power Apps** og síðan velja svæðið þar sem þú vilt bæta við forritinu. Til að fella forritið inn í valmyndarhnappinn **Power Apps** skal velja aðgerðasvæðið. Til að fella forritið beint inn á síðuna skaltu velja viðeigandi flipa, flýtiflipa, blað eða hluta (ef þú ert á vinnusvæði).

    - Ef hægt er að komast í forritið með því að nota valmyndarhnapp **Power Apps** geturðu valið valmyndarhnappinn **Power Apps** á staðlaða aðgerðasvæðinu og síðan valið **Bæta við forriti**.

3. Grunnstilla innfellt forrit. Fyrir frekari upplýsingar, sjá [Að stilla strigaforrit](#configuring-a-canvas-app) kafla síðar í þessari grein.
4. Eftir að þú hefur staðfest að stillingarnar séu réttar skaltu velja **Setja inn**.

    - Ef slökkt er á eiginleikanum **Vistuð yfirlit** er beðið um að endurhlaða vafranum til að geta séð innfellda forritið.
    - Ef kveikt er á eiginleikanum **Vistað yfirlit** verður þú að vista yfirlitið til að breytingin haldist.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Fella inn vinnusvæðaforrit sem heilsíðuupplifun úr stjórnborðinu

Þú gætir viljað fella inn strigaforrit frá mælaborðinu ef appið er ekki tengt núverandi síðu, eða ef þú vilt bara birta appið sem heilsíðuupplifun inni í fjármála- og rekstrarappinu.

> [!NOTE]
> Til að bjóða upp á þennan möguleika þarftu að kveikja á eiginleikanum **Forrit á heilli síðu** í eiginleikastjórnun. 

1. Opnið stjórnborð.
2. Veljið og haldið (eða hægrismellið) síðunni, veljið **Sérstilla** og veljið því næst **Bæta við síðu**.
3. Á svæðinu **Bæta við síðu** skal velja **Power Apps**.
4. Grunnstilla innfellt forrit. Fyrir frekari upplýsingar, sjá [Að stilla strigaforrit](#configuring-a-canvas-app) kafla síðar í þessari grein.
5. Veljið **Vista** til að bæta forritinu við stjórnborðið sem nýjan reit.
6. Veldu nýja reitinn á stjórnborðinu og staðfestu að vinnusvæðaforritið birtist eins og ætlast er til.

### <a name="configuring-a-canvas-app"></a>Vinnusvæðaforrit skilgreint

Þegar þú fellir inn vinnusvæðaforrit verður þú að stilla eftirfarandi færibreytur:

- **Heiti** – Færðu inn textann sem á að sýna fyrir hnappinn eða flipann sem mun innihalda innfellt forrit. Oft gætirðu viljað endurtaka heiti forritsins í þessum reit.
- **Forritskenni** – Tilgreindu altækt einkvæmt kennimerki (GUID) fyrir vinnusvæðaforritið sem á að fella inn. Til að sækja þetta gildi skaltu finna forritið á [make.powerapps.com](https://make.powerapps.com) og skoða síðan reitinn **Forritskenni** undir **Upplýsingar**.
- **Setja inn samhengi fyrir forritið** - hægt að velja valfrjálst reitinn sem inniheldur gögnin sem þú vilt flytja yfir í forritið sem inntak. Fyrir upplýsingar um hvernig appið getur nálgast gögnin sem eru send úr fjármála- og rekstraröppum, sjá [Að byggja upp app sem nýtir gögn sem send eru frá fjármála- og rekstraröppum](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) kafla síðar í þessari grein.

    Frá og með útgáfu 10.0.19 verður núgildandi lögaðili einnig sendur sem samhengi til vinnusvæðaforritsins í gegnum færibreytuvefslóðina **cmp**. Þessi hegðun hefur ekki áhrif á notkun vinnusvæðaforritsins fyrr en forritið notar þær upplýsingar.

- **Stærð forrits** – Veldu gerð forrits sem þú ert að fella inn. Veldu **Mjótt** fyrir forrit sem eru smíðuð fyrir fartæki og **Breitt** fyrir forrit sem eru smíðuð fyrir spjaldtölvur. Þessi færibreyta tryggir að nægu plássi sé úthlutað fyrir innfellda forritið.
- **Lögaðilar** – Þú getur valið þá lögaðila sem forritið ætti að vera fáanlegt fyrir. Forritið er sjálfgefið í boði fyrir alla lögaðila. Þessi valkostur er aðeins í boði þegar fellt er inn beint á fyrirliggjandi síðu og slökkt er á eiginleikanum **[Vistuð yfirlit](saved-views.md)**.

## <a name="sharing-an-embedded-app"></a>Að deila innfelldu forriti

Þegar vinnusvæðaforrit hefur verið fellt inn á síðu og staðfest að það virki á réttan hátt gætirðu viljað deila forritinu með öðrum notendum kerfisins. Til að deila innfelldu vinnusvæðaforriti skal fylgja þessum skrefum.

1. [Deildu vinnusvæðaforritinu í Power Apps](/powerapps/maker/canvas-apps/share-app) með viðeigandi notendum þannig að þeir geti fengið beinan aðgang að forritinu í Power Apps.
2. Deildu sérstillingunum sem tengjast innfellda forritinu með þeim notendum sem óskað er eftir. Hægt er að aðra hvora af eftirfarandi aðferðum:

    - **Birta yfirlitið (ráðlagt):** Ef kveikt er á eiginleikanum **[Vistuð yfirlit](saved-views.md)** er ráðlagða og æskilega leiðin að búa til yfirlit sem inniheldur innfellt vinnusvæðaforrit og síðan birta yfirlitið þeim notendum sem óskað er eftir. Þessi aðferð tryggir að allir notendur sem eru með öryggishlutverk sem birta yfirlitið beinist að komi til með að sjá vinnusvæðaforritið á síðunum.

        Einnig er hægt að birta vinnusvæðaforrit sem hefur verið fellt inn sem heilsíðuupplifun frá stjórnborðinu. Á stjórnborðinu skal velja og halda niðri (eða hægrismella) reitnum sem tengist forritinu, velja **Sérstilla** og síðan velja **Birta síðu**. Upplifun sem líkist *Birtingu yfirlita* er sýnd og þú getur valið öryggishlutverkin til að birta í. Í uppfærslu 10.0.21 eða nýrri, ef kveikt er á eiginleikanum **Bættur stuðningur lögaðila fyrir vistuð yfirlit**, getur þú einnig gefið forritið út í þeim lögaðilum sem þú vilt.

    - Ef slökkt er á eiginleikanum **Vistuð yfirlit** getur kerfisstjórinn gefið sérstillingu sem felur í sér vinnusvæðaforritið til viðeigandi hóps notenda í gegnum síðuna **Sérstilling**. Einnig er hægt að flytja út sérstillingar síðunnar og senda þær á einn eða fleiri notendur. Hver þessara notenda getur síðan flutt inn sérstillingarnar. Tækjastika sérstillinga er með hnappa sem gera þér kleift að flytja út og flytja inn sérstillingar.

> [!NOTE]
> Ef strigaforritinu hefur verið deilt með utanaðkomandi notendum geta þeir notendur ekki notað innfellda appið í fjármála- og rekstrarforritum. Hins vegar geta þeir nálgast forritið beint inni í Power Apps. Ytri notendur innihalda gesti og notendur sem tilheyra ekki Microsoft 365 Azure Directory þar sem fjármála- og rekstrarforritið er notað.

Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um sérstillingarvalkosti á vörunni og hvernig á að nota þá.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Að byggja upp strigaforrit sem notar gögn sem eru send frá fjármála- og rekstraröppum

Þegar þú smíðar strigaforrit sem verður fellt inn í fjármála- og rekstrarapp, er einn mikilvægur hluti af ferlinu að nota inntaksgögnin úr því fjármála- og rekstrarappi. Frá Power Apps þróunarreynslu er hægt að nálgast inntaksgögnin sem eru send frá fjármála- og rekstrarappi með því að nota **Param("EntityId")** breytilegt. Að auki mun núgildandi lögaðili frá og með útgáfu 10.0.19 einnig vera sendur til vinnusvæðaforritsins í gegnum breytuna **Param(„cmp“)**. 

Til dæmis, í OnStart aðgerð appsins, gætirðu stillt inntaksgögnin frá fjármála- og rekstrarforritum á breytu eins og þessa:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Vinnusvæðaforrit skoðað

Til að skoða innfellt strigaforrit á síðu í fjármála- og rekstrarforritum, farðu bara á síðu sem hefur innfellt app. Munið að hægt er að opna forrit með því að nota hnappinn **Power Apps** á staðlaða aðgerðasvæðinu. Að öðrum kosti geta þær birst beint á síðunni sem nýr flipi eða flýtiflipi eða blað eða sem nýr hluti á vinnusvæði. Þegar notendur reyna fyrst að hlaða forriti á síðu verða þeir beðnir um að skrá sig inn. Þetta skref tryggir að notendur hafi viðeigandi heimildir til að nota forritið.

## <a name="editing-an-embedded-app"></a>Breyta innfelldu forriti

Eftir að forrit hefur verið fellt inn á síðu getur verið að þú þurfir að gera nokkrar breytingar á grunnstillingu þessa forrits. Til dæmis viltu hugsanlega breyta merkingunni sem tengist innfelldu forriti eða ný útgáfa af forriti hefur verið búin til og þú þarft að uppfæra kenni forrits til að benda á það nýjasta.

Fylgdu þessum skrefum til að breyta grunnstillingu á innfelldu forriti:

1. Farðu á svæðið **Breyta forriti**.

    - Ef farið er í innfellt forrit í gegnum Power Apps valmyndarhnappinn skaltu velja og halda (eða hægrismella) á Power Apps valmyndarhnappinn og velja **Sérstilla**. Veldu forrit sem þú vilt grunnstilla úr fellivalmyndinni **Velja forrit**.
    - Ef innfellt forrit birtist beint á síðunni skaltu velja **Valkostir** og síðan velja **Sérstilla þessa síðu**. Með verkfærinu **Velja** skaltu smella á innfellt forrit.
    - Ef innfellda forritinu var bætt við af stjórnborðinu skaltu opna stjórnborðið, velja og halda niðri (eða hægrismella) reitnum sem tengist forritinu, velja **Sérstilla** og síðan velja **Breyta síðu**.

2. Gerðu nauðsynlegar breytingar á grunnstillingu forritsins og smelltu síðan á **Vista**.

## <a name="removing-an-app"></a>Forrit fjarlægt

Eftir að forrit hefur verið fellt inn á síðu eru til nokkrar leiðir til að fjarlægja það ef þörf krefur:

- Farðu í **Breyttu forriti** rúðu með því að nota leiðbeiningarnar frá [Að breyta innfelldu forriti](#editing-an-embedded-app) kafla fyrr í þessari grein. Staðfestu að svæðið birti upplýsingar um innbyggða forritið sem þú vilt fjarlægja og smelltu síðan á hnappinn **Eyða**.
- Ef innfellda forritinu var bætt við af stjórnborðinu skaltu opna stjórnborðið, velja og halda niðri (eða hægrismella) reitnum sem tengist forritinu, velja **Sérstilla** og síðan velja **Fjarlægja síðu**. 
- Vegna þess að innfellt forrit er vistað sem sérstillt gögn, mun hreinsun á sérstillingum síðunnar einnig fjarlægja innfelld forrit á þessari síðu. Athugaðu að hreinsun á sérstillingum síðunnar er varanleg og ekki hægt að afturkalla. Til að fjarlægja sérstillingar þínar á síðu skaltu velja **Valkostir** og smella síðan á **Sérsníða þessa síðu** og að lokum á hnappinn **Hreinsa**. Allar fyrri sérstillingar fyrir þessa síðu verða fjarlægðar þegar vafrinn er uppfærður. Sjá [Sérstilla notandaupplifun](personalize-user-experience.md) til að fá frekari upplýsingar um hvernig á að fínstilla síður með sérstillingu.

## <a name="appendix"></a>Viðauki

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Þróunaraðili] Vinnusvæðaforrit smíðað í skjámynd

Þó að þessi grein beinist að því að fella inn strigaforrit með sérstillingu, þá hafa forritarar einnig möguleika á að bæta strigaforriti við eyðublað með því að nota Visual Studio reynslu af þróun. Til að gera þetta skal einfaldlega bæta PowerAppsHostControl við skjámyndina. Lýsigagnaeiginleikarnir sem eru í boði í stýringunni bjóða upp á sömu möguleika og sérstillingarleiðin.

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

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

