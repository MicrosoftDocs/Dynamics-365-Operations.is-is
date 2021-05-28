---
title: Skilgreina gagnaveitu uppflettingar til að nota færibreytur sem eru sértækar fyrir rafræna skýrslugerð
description: Þetta efnisatriði útskýrir hvernig hægt er að skilgreina gagnaveitur uppflettingar í rafrænum skýrslugerðarsniðum til að forritstengdar færibreytur rafrænnar skýrslugerðar.
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 131d14f1f1aa329bd71b1f8a4015192736bd8e44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022576"
---
# <a name="configure-lookup-data-sources-to-use-er-application-specific-parameters"></a>Skilgreina gagnaveitu uppflettingar til að nota færibreytur sem eru sértækar fyrir rafræna skýrslugerð 

[!include[banner](../includes/banner.md)]

Eiginleikinn fyrir forritstengdar færibreytur [Rafrænnar skýrslugerðar](general-electronic-reporting.md) gerir þér kleift að skilgreina gagnasíun í sniði rafrænnar skýrslugerðar þannig að hún byggi á safni sértækra reglna. Hægt er að stilla þetta reglusafn til að nota gagnaveitu af gerðinni **Uppfletting** sem er í boði í sniði rafrænnar skýrslugerðar. Þá er hægt að tilgreina raunverulegar reglur umfram þætti rafrænnar skýrslugerðar með því að nota notandaviðmótið sem sjálfkrafa búið til samkvæmt stillingunum á gagnaveitunni **Uppfletting** í samsvarandi sniði rafrænnar skýrslugerðar og núverandi gögnum lögaðilans. Að lokum verða tilgreindar reglur aðgengilegar gagnaveitu **Uppflettingar** fyrir snið rafrænnar skýrslugerðar þegar þetta snið rafrænnar skýrslugerðar er keyrt.

> [!NOTE]
> Notið skilgreindar gagnaveitur fyrir breytanlegt snið rafrænnar skýrslugerðar til að tilgreina hvaða forritsgögn eru notuð til að skilgreina raunverulegar reglur.

Notið [Aðgerðarhönnuð rafrænnar skýrslugerðar](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) til að flytja gagnaveitu af gerðinni **Uppfletting** inn í snið rafrænnar skýrslugerðar. Skilgreina þarf gagnaveituna til að lýsa því hvernig sértæku reglurnar líta út, þ.m.t. eftirfarandi:

   - Færibreytusafn af ákveðinni gagnagerð þar sem gildin eru gefin upp til að tilgreina eina reglu.
   - Gerð gildis ákveðinnar gagnagerðar sem er skilað með einni reglu þegar þessi regla er talin henta best.

Hægt er að skilgreina eftirfarandi gerðir af gagnaveitu **Uppflettingar** eftir því hvers konar gildi er skilað af einhverri skilgreindri reglu:

   - Notið gerðina **Data model\Lookup** þegar skila verður tölusetningargildi líkans.
   - Notið gerðina **Dynamics 365 Operations\Lookup** þegar þarf að skila tölusetningargildi forrits eða forritsgildinu [aukin gagnagerð](../extensibility/extensible-edts.md).
   - Notið gerðina **Format enumeration\Lookup** þegar skila þarf tölusetningargildi sniðs.

Eftirfarandi skýringarmynd sýnir hvernig hægt er að skilgreina tölusetningarsniði í sýnidæmi rafræns skýrslugerðarsniðs.

   ![Sýnir tölusetningu sniðs sem grunn fyrir skilgreinda gagnaveitu uppflettingar](./media/er-lookup-data-sources-img1.gif)

Eftirfarandi skýringarmynd sýnir þætti sniðs sem voru skilgreindir til að tilkynna um mismunandi gerðir af sköttum í mismunandi hlutum myndaðrar skýrslu.

   ![Sýnir sniðshlutana til að tilkynna hverja mismunandi skattgerð út af fyrir sig](./media/er-lookup-data-sources-img2.png)

Eftirfarandi skýringarmynd sýnir hvernig aðgerðarhönnuður rafrænnar skýrslugerðar leyfir að bæta við gagnaveitu af gerðinni **Format enumeration\Lookup**.  Viðbætt gagnaveita er skilgreind til að skila gildi á tölusetningarsniði `List of taxation levels`.

   ![Gagnaveitu rafrænnar skýrslugerðar af gerðinni Format enumeration\Lookup bætt við](./media/er-lookup-data-sources-img3.gif)

Eftirfarandi mynd sýnir hvernig viðbætt gagnaveita er skilgreind til að nota reitinn **Kóði** í færslulistanum **Model.Data.Tax** í gagnaveitunni **Líkan** sem færibreytu sem þarf að tilgreina fyrir hverja skilgreinda reglu.

![Færibreytur viðbættrar gagnaveitu skilgreindar fyrir gerðina Format enumeration\Lookup](./media/er-lookup-data-sources-img4.gif)

Viðbætt `Model.Data.Tax` gagnaveita er skilgreind til að tilgreina skattkóða fyrir hverja skilgreinda reglu með því opna færslur forritstöflunnar **TaxTable**.

   ![Yfirferð á gagnaveitu uppflettingar í einu fyrirtæki af gerðinni Format enumeration\Lookup](./media/er-lookup-data-sources-img5.gif)

Hægt er að setja upp reglur uppflettingar fyrir valið snið rafrænnar skýrslugerðar með því að nota notandaviðmótið sem er sjálfkrafa stillt upp með skipulagi skilgreindrar gagnaveitu. Sem stendur krefst þetta notandaviðmót fyrir hverja reglu að skilaða gildið sé tilgreint sem tölusetningargildi `List of taxation levels` sniðs ásamt skattkóðanum sem færibreytu.

   ![Setja upp reglur fyrir skilgreinda gagnaveitu](./media/er-lookup-data-sources-img6.gif)

Eftirfarandi skýringarmynd sýnir hvernig hægt er að skilgreina `Model.Data.Summary.LevelByLookup` gagnaveitu af gerðinni **Reiknaður reitur** til að kalla á skilgreinda gagnaveitu **Uppflettingar** sem gefur upp nauðsynlegar færibreytur. Til að vinna úr þessu kalli á keyrslutíma fer rafræn skýrslugerð í gegnum listann yfir skilgreindar reglur í skilgreindri röð til að hafa upp á fyrstu reglunni sem uppfyllir uppgefin skilyrði. Í þessu dæmi er það reglan sem inniheldur skattkóðann sem samsvarar þeirri sem gefin er upp. Þar af leiðandi finnst hentugasta reglan og tölusetningargildinu sem er skilgreint fyrir fundnu regluna er skilað af þessari gagnaveitu.

> [!NOTE]
> Undantekning á sér stað þegar engin viðeigandi regla finnst. Til að koma í veg fyrir þessar undanþágur skal skilgreina frekari reglur neðst í reglulistanum til að sjá um tilfelli þegar óskilgreint gildi eða ekkert gildi er gefið upp. Notið valkostina **\*Ekki autt\*** og **\*Autt\***.  
>
> ![Bæta við gagnaveitu til að kalla á skilgreinda gagnaveitu uppflettingar](./media/er-lookup-data-sources-img7.png)

Þegar valkosturinn **Milli fyrirtækja** er stilltur á **Já** fyrir breytanlega gagnaveitu uppflettingar er nýrri áskildri færibreytu **Fyrirtækis** bætt við færibreytusafn þessarar gagnaveitu. Gildi færibreytunnar **Fyrirtæki** verður að vera tilgreint við keyrslutíma þegar kallað er á gagnaveitu uppflettingar. Þegar kóði fyrirtækisins er tilgreindur við keyrslutíma eru reglur sem skilgreindar eru fyrir þetta fyrirtæki notaðar til að finna hentugustu regluna og samsvarandi gildi er skilað. Eftirfarandi mynd sýnir hvernig hægt er að gera þetta og hvernig færibreytusafn breytanlegrar gagnaveitu er breytt.

   ![Yfirferð á gagnaveitu uppflettingar milli fyrirtækja af gerðinni Format enumeration\Lookup](./media/er-lookup-data-sources-img8.gif)

> [!NOTE]
> Veljið hvert fyrirtæki út af fyrir sig til að skilgreina reglusafnið fyrir þessa gagnaveitu uppflettingar á breytanlegu sniði rafrænnar skýrslugerðar. Undanþága kemur upp við keyrslutíma þegar kallað er á uppflettingu milli fyrirtækja með kóða fyrirtækisins þar sem stilling uppflettingar var ekki lokið.
>
> Gangið úr skugga um veittar séu heimildir þeim notanda sem keyrir rafrænt skýrslugerðarsnið með gagnaveitu **Uppflettingar** milli fyrirtækja til að fá aðgang að gögnum úr öllum fyrirtækjum sem eru innan sviðs þessarar gagnaveitu. Annars er undantekning notuð á keyrslutíma.

Frá og með útgáfu 10.0.19 eru auknir möguleikar fyrir gagnaveitu **Uppflettingar** í boði. Þegar valkosturinn **Stækkað** er stilltur á **Já** fyrir breytanlegan gagnagjafa uppflettingar, er skilgreindri gagnaveitu uppflettingar breytt í skipulagða gagnaveitu sem býður upp á frekari möguleika til að greina skilgreint reglusafn. Eftirfarandi mynd sýnir þessa umbreytingu.

   ![Yfirferð á skipulagðri gagnaveitu uppflettingar af gerðinni Format enumeration\Lookup](./media/er-lookup-data-sources-img9.gif)

- Undirliðurinn **Uppfletting** er hannaður sem aðgerð til að finna hentugust regluna úr safni af skilgreinanlegum reglum út frá uppgefnu færibreytusafni.
- Undirliðurinn **IsLookupResultSet** er hannaður sem aðgerð til að samþykkja uppgefið gildi gagnaveitu grunntölusetningar og skila *Boole-gildinu* **Satt** þegar reglusafnið inniheldur að minnsta kosti eina reglu þar sem uppgefið tölusetningargildi var skilgreint sem skilagildi. Þessi aðgerð skilar *Boole-gildinu* **Ósatt** þegar engar reglur er skilgreindar til að skila uppgefnu tölusetningargildi.
- Undirliðurinn **Stilling** er hannaður sem aðgerð sem skilar safni af skilgreindum reglum sem færslum í færslulista. Skiluð gildi og færibreytusafn skilgreindra reglna eru sýndar í öllum skiluðum færslum sem reitir af viðeigandi gagnagerðum:

    - Skilað gildi er sýnt sem reiturinn **Niðurstaða uppflettingar**.
    - Skilgreindu færibreyturnar eru sýndar sem reitir sem bera nafn færibreyta (**Kóði** reiturinn í þessu dæmi).

Frekari upplýsingar um hvernig á að skilgreina gagnaveitu **Uppflettingar** er að finna í [Grunnstilla rafrænt skýrslugerðarsnið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md). Til að komast að því hvernig á að stilla uppflettingarreglurnar skal skoða [Setja upp færibreytur á sniði rafrænnar skýrslugerðar fyrir hvern lögaðila](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Grunnstilla ER-snið til að nota færibreytur sem eru tilgreindar fyrir hvern lögaðila](er-app-specific-parameters-configure-format.md)

[Setja upp færibreytur á sniði rafrænnar skýrslugerðar fyrir hvern lögaðila](er-app-specific-parameters-set-up.md)
