---
title: Yfirlit yfir fjárhagssamstæður og umreikning gjaldmiðla
description: Þetta efnisatriði lýsir fjármálasamstæðum og umreikningi gjaldmiðils í Fjárhag.
author: aprilolson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: c4561a1193971b131ab2b6c8d64f848d8155c1fc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975765"
---
# <a name="financial-consolidations-and-currency-translation-overview"></a>Yfirlit yfir fjárhagssamstæður og umreikninga gjaldmiðils

[!include [banner](../includes/banner.md)]

Þetta efnisatriði fer með þér í gegnum nálgunina sem bæði Microsoft Dynamics 365 Finance og fjárhagsskýrslugerð nota fyrir samstæður. Það lýsir aðstæðum sem fela í sér skýrslugerð fyrir mörg fyrirtæki, uppsöfnun, losun og hlutdeild minnihluta. Það útskýrir einnig hvernig skal takast á við sérstakar aðstæður, svo sem aðstæður þar sem lögaðilar eru með mismunandi fjárhagstímabil eða mismunandi bókhaldslykla.

Þetta efnisatriði var skrifað fyrir notendur og hagnýta ráðgjafa og gerir ráð fyrir að lesendur hafi almennan skilning á Finance og fjárhagsskýrslugerð. Ekki er fjallað um grunnuppsetningu.

> [!NOTE]
> Hugtakið *lögaðili* er notað í Finance og hugtakið *fyrirtæki* er notað í Financial reporting. Bæði hugtökin eru notuð í þessu efnisatriði. Í þessu efnisatriði hafa þau hins vegar sömu merkinguna.

## <a name="audience"></a>Notendahópur
Þetta efnisatriði er ætlað fjármála- og bókhaldsnotendum og hugbúnaðarráðgjöfum sem vilja nota Finance and Reporting og Financial reporting til að sameina gögn margra fyrirtækja og margra gjaldmiðla.

## <a name="approach"></a>Nálgun
Finance notar aðskilinn lögaðila til að vinna úr samstæðu. Það virkjar eins-tilviks samstæðu en veitir möguleika á því að taka inn gögn frá öðrum uppruna. Samstæðuferlið verður að vera keyrt í hvert skipti sem breytingar eru gerðar á lögaðilum upprunans.

Financial reporting getur sameinað mörg fyrirtæki við skýrslugerð. Þótt gögnin séu geymd í gagnaskemmu, útgáfu þeirra breytt og hægt sé að flytja þau út, er hvert upprunafyrirtæki samt sem áður geymsluaðili gagnanna. Skýrsluna er hægt að keyra hvenær sem er, jafnvel á mínútu fresti (til dæmis). Það býður upp á marga fleiri kosti, svo sem getuna til þess að kafa ofan í öll fyrirtæki og víddir.

Notendur geta notað Consolidate Online, Financial reporting eða bæði. Val þeirra fer eftir þörfum fyrirtækisins og óskir endurskoðenda þeirra.

## <a name="consolidations"></a>Samstæður
Einingin **Samstæður** felur í sér möguleika á því að sameina marga lögaðila í samstæðuferlinu, og til að flytja inn eða flytja út stöðu fyrirtækisins. Þú getur einnig sett upp losanir og bókað losunarbækur.

## <a name="benefits-of-using-consolidate-online"></a>Kostir þess að nota Consolidate á netinu
Fyrir viðskiptavini sem nota eininguna **Samstæður** fylgja ýmsir kostir:

- **Dýpt gagna** - Þú getur búið til samstæðuskýrslur sem sameina raungögn og fjárhagsáætlunargögn bæði á bókahaldsstigi og víddarstigi.
- **Gagnvirkar samstæður** - Hægt er að vinna úr samstæðum mörgum sinnum.
- **Endurskoðunargeta** - Víddum og lyklum er viðhaldið fyrir greiningar og endurskoðun og stöður eru búnar til eftir dagsetningu.
- **Umreikningur gjaldmiðils** - Þú getur sett upp lyklasvið og gengi til að umreikna bókhaldsgjaldmiðil upprunafyrirtækis yfir í bókhaldsgjaldmiðil samstæðufyrirtækis.
- **Vinna úr losunum í samstæðu- eða losunarfyrirtæki** - Hægt er að vinna úr og bóka losun sem eitt ferli í samstæðuferli. Einnig er hægt að keyra tillögu sér.

## <a name="supported-consolidation-scenarios"></a>Studdar aðstæður samstæðu
Hér eru nokkrar samstæðuaðstæður sem Consolidate á netinu styður:

- Eins stigs samstæður yfir lögaðila
- Samstæður sem fela í sér losun
- Hlutdeild minnihluta (Í þessari atburðarás verður að nota handvirkan útreikning og innslátt í fyrirtækinu.)
- Margar bókhaldslyklar yfir lögaðila
- Mismunandi fjárhagsdagatöl yfir marga lögaðila
- Samstæður sem fela í sér marga skýrslugjaldmiðla

## <a name="legal-entity-setup"></a>Uppsetning lögaðila
Áður en þú vinnur úr samstæðu verður þú að setja upp lögaðila. Hægt er að keyra samstæðu eins oft og þörf krefur og öll gögn verða umreiknuð úr bókhaldsgjaldmiðli upprunafyrirtækis yfir í gjaldmiðilinn sem er skilgreindur fyrir samstæðufyrirtækið. Fyrir eftirfarandi skipulagseiningar fyrirtækis, ef þú verður fyrst að umreikna öll norður-amerísk fyrirtæki í Bandaríkjadali (USD) og síðan í evrur (EUR), gjaldmiðil móðurfyrirtækis, verður þú þar af leiðandi að hafa að minnsta kosti tvö samstæðufyrirtæki.

![Skipulag fyrirtækis](./media/organizational-structure.png "Skipulag fyrirtækis")

Í fyrri skipulagseiningum fyrirtækis verður þú að hafa lögaðili fyrir norður-amerísku samstæðuna, vegna þess að samstæður sameinast alltaf út frá bókhaldsgjaldmiðli upprunafyrirtækisins til gjaldmiðils samstæðufyrirtækisins. Í dæminu, ef öll fyrirtæki eru hluti af einni samstæðu, verður mexíkóska dótturfélagið umreiknað úr mexíkóskum pesóum (MXN) yfir í EUR, ekki frá MXN til USD til EUR.

Þegar þú býrð til lögaðilann getur þú tilgreint hvort fyrirtækið sé notað fyrir bæði samstæðuferlið og losunarferlið, eða notað aðeins fyrir einn af þessum ferlum. Í eftirfarandi skýringarmynd er fyrirtækið notað fyrir báða ferlana. Athugaðu að þú getur ekki sent daglegar færslubækur í samstæðufyrirtæki, en þú getur bókað þær í losunarfyrirtæki. Því gætirðu viljað hafa losunarfyrirtæki sér.

![Lögaðili sem er notaður bæði til sameiningar og útrýmingar](./media/sep-elimination-company.png "Lögaðili sem er notaður bæði til sameiningar og útrýmingar")

## <a name="main-accounts-and-consolidation-account-groups"></a>Flokkar aðallykla og samstæðulykla
Eitt sem þú þarft að ákveða er hvernig þú vilt sameina bókhaldslyklana þína. Í samstæðuferlinu hefur þú þrjá möguleika til að sameina aðallykla.

Fyrsta kosturinn er að nota aðallykla frá upprunafyrirtækjum. Í þessu tilfelli verður allir lyklar frá öllum fyrirtækjum steyptir saman. Til dæmis, ef Cash er lykill 100000 í USMF-fyrirtækinu og lykill 1100 í DEMF-fyrirtækinu, mun samstæðufyrirtækið innihalda báða lyklana. Hver lykil mun hafa sína eigin stöðu.

Önnur kosturinn er að tilgreina sjálfgefinn samstæðulykil á síðunni **Aðallykill**. Lyklinum verður síðan varpað á samstæðulykilinn. Þessi valkostur getur verið gagnlegur þegar þú ert með mismunandi bókhaldslykla eða verður að varpa á töflu sem er skilgreind af höfuðstöðvunum.

![Sjálfgefinn samstæðulykill sem tilgreindur er á Aðalreikningssíðunni](./media/main-accounts.png "Sjálfgefinn samstæðulykill sem tilgreindur er á Aðalreikningssíðunni")

Þriðji kosturinn er að nota flokka samstæðulykla. Hægt er að skilgreina eins marga flokka samstæðulykla eftir þörfum. Síðan á síðunni **Viðbótarupplýsingar um samstæðulykla** varpar þú bara aðallyklinum frá bókhaldslyklunum yfir á lykilinn sem þú þarfnast fyrir þann flokk.

![Vörpun á síðunni Viðbótarupplýsingar samstæðureikninga](./media/additional-consolidation-accounts.png "Vörpun á síðunni Viðbótarupplýsingar samstæðureikninga")

## <a name="consolidating-online"></a>Samþætting á netinu
Til að læra hvernig á að slá inn upplýsingar um samstæðu á netinu skal sjá [Sameiningar fjárhags á netinu](./consolidate-online.md).

## <a name="managing-consolidation-transactions"></a>Stjórnun samstæðufærslna
Þú hefur margar leiðir til að skoða niðurstöður samstæðunnar:

- Búðu til fjárhagsskýrslu á móti samstæðufyrirtækinu.
- Endurskoða listasíðuna **Prófjöfnuður** í samstæðufyrirtækinu.
- Í listanum yfir samstæðufærslur á síðunni **Samstæður** skal skoða stður sem eru búnar til eftir dagsetningu fyrir hvert upprunafyrirtæki fyrir hvert tímabil.

    ![Sameiningarfærslur á síðunni Sameiningar](./media/managing-consolidation-transactions.png "Sameiningarfærslur á síðunni Sameiningar")

Til að keyra samstæðuna aftur er einfaldlega hægt að vinna úr samstæðunni. Einnig er hægt að velja fyrst **Fjarlægja færslur** á síðunni **Samstæður**.
Í tilvikinu eru stöður á samstæðureikningnum þínum ekki rétt, hægt er að leiðrétta þessar stöður með því að nota síðuna **Leiðréttingar á lokunartímabili**.

## <a name="consolidate-with-import"></a>Taka með í innflutning
Samstæðan með innflutningsvirkni virkar eins og samstæðuvirknin á netinu. Þegar þú velur lögaðila muntu fletta upp á upprunalegu skránni sem inniheldur gögnin.

## <a name="export-company-balances"></a>Flytja út stöðu fyrirtækis
Útflutningsvirkni á stöðu fyrirtækis virkar einnig eins og samstæðuvirknin á netinu. Þegar þú velur lögaðilana býrðu til skráarslóð fyrir úttakið.

## <a name="elimination-rules"></a>Niðurfellingarreglur
Til að fella niður færslur innan samstæðu er hægt að búa til niðurfellingarreglu. Einnig er hægt að gera handvirka niðurfellingarfærslu í fyrirtæki sem er útnefnt sem losunarfyrirtæki. Ef þú býrð til niðurfellingarreglu hefur þú tvo valkosti fyrir niðurfellingaraðferðina: **Nettóbreyting** og **Fast**.

### <a name="set-up-elimination-rules"></a>Setja upp losunarreglur
Þegar þú setur upp losunarreglur í Finance getur þú búið til fjárhagsvídd sem er sérstaklega notuð fyrir losun. Flestir viðskiptavinir nefna þessa fjárhagsvídd **Trading Partner** eða eitthvað svipað. Ef þú ákveður að nota ekki fjárhagsvídd skaltu gæta þess að hafa aðallykla sem eru aðeins notaðir fyrir færslur innan samstæðu.

Hægt er að finna uppsetningu fyrir losanir á svæðinu **Setja upp** í einingunni **Samstæður**. Eftir að þú slærð inn lýsingu fyrir regluna þarftu að velja fyrirtækið sem losunarbókin mun vera bókuð í. Fyrirtækið sem þú valdir ætti að hafa **Nota fyrir losunarferli fjárhags** valið í uppsetningu lögaðila.

Þú getur stillt dagsetninguna þegar losunarreglan tekur gildi og dagsetninguna þegar hún rennur út, eins og þú þarfnast. Ef þú vilt að losunarreglan sé aðgengileg í losunartillöguferlinu verður þú að stilla valkostinn **Virk** á **Já**. Veldu heiti færslubókar af gerðinni **Losun**.

![Grunneiginleikar brotthvarfsreglu](./media/ledger-elimination-rule-journal.png "Grunneiginleikar brotthvarfsreglu")

Þegar þú hefur skilgreint grunneiginleika skaltu velja **Línur** til að skilgreina raunverulegar úrvinnslureglur. Þú hefur tvo kosti í boði fyrir losun, að losa upphæð nettóbreytingar eða skilgreina fasta upphæð.

Veldu upprunalykla. Þú getur notað stjörnu (\*) sem algildistaf. Til dæmis velur **1\**_alla lykla sem byrja á_* 1** sem gagnagjafa fyrir úthlutunina.

Þegar þú hefur valið upprunalykil skaltu nota reitinn **Lýsing á lykli** til að tilgreina lykilinn sem er notaður í viðtökufyrirtæki. Veldu **Uppruni** til að nota sama aðallykilinn sem er skilgreindur í upprunalegum lykli. Ef þú velur **Notandaskilgreint** verður þú að tilgreina viðtökulykil.

![Síðan Losunarreglulína fjárhags](./media/ledger-elimination-rule-line.png "Síðan Losunarreglulína fjárhags")

Reiturinn **Víddarskilgreining** virkar eins og reiturinn **Lýsing á lykli**. Veldu **Uppruni** til að nota sömu víddir í viðtökufyrirtækinu og í upprunafyrirtækinu. Ef þú velur **Notandaskilgreint** þarftu að tilgreina víddir í viðtökufyrirtæki með því að velja **Víddir viðtökustaðar**. Veldu síðan upprunavíddir og fjárhagsvíddir og gildi sem eru notuð sem uppruni losunar.

### <a name="process-elimination-transactions"></a>Vinna Losunarfærslur
Það eru tvær leiðir til að vinna losunarfærslur. Hægt er að vinna úr færslunni í samstæðuferlinu á netinu, eða þú getur búið til losunarbók og keyrt losunartillöguferlið. Þessi hluti einblínir á seinni valkostinn.

Í fyrirtæki sem er skilgreint sem losunarfyrirtæki skal velja **Losunarbók** í einingunni **Samstæður**. Þegar þú hefur valið heiti færslubókar skaltu velja **Línur**. Til að keyra tillöguna skaltu velja **Tillögur** \> **Losunartillaga**.

Veldu fyrirtækið sem er uppruni sameinuðu gagnanna og veldu svo regluna sem á að vinna með. Sláðu inn upphafs- og lokadagsetningar til að skilgreina dagsetningabilið þar sem leitað er að losunarupphæðum. Reiturinn **Bókunardagsetning fjárhags** tilgreinir þann dag sem er notaður til að bóka færslubókina í fjárhag. Þegar valið er **Í lagi** er hægt að endurskoða upphæðirnar og bóka færslubókina.

> [!NOTE]
> Losunarbókin sýnir upphæðirnar fyrir lyklagildi í gjaldmiðli upprunalegra færslna, ekki í bókhaldsgjaldmiðlinum. Þegar þú endurskoðar upphæðirnar í losunarbókinni gæti þér fundist þessi hegðun ruglingsleg.

Nánari upplýsingar og dæmi er að finna í [Losunarreglur](./elimination-rules.md).

## <a name="currency-revaluation-in-a-consolidation-company"></a>Endurmat á gjaldmiðli í samstæðufyrirtæki
Þegar gögn frá einum bókhaldsgjaldmiðill til annars eru sameinuð, verður samt að keyra gjaldmiðilsendurmatið ef gengi breytast, þannig að lykilsstöður þínar séu rétt endurmetnar. Þegar gögn eru sameinuð í upphafi skal nota flipann **Umreikningur gjaldmiðils** til að velja fyrstu gengin sem á að nota fyrir umreikning í samstæðuferlinu. Eftir að nýtt gengi er fært inn (til dæmis í næsta mánuð), verður að endurmeta stöðu lykils. Óinnleystur hagnaður eða tap er síðan uppfærð á grundvelli nýju gengis og dagsetningu.

Nánari upplýsingar um endurmat gjaldmiðils í samstæðufyrirtæki er að finna í [Endurmat á gjaldmiðli í samstæðufyrirtæki](currency-revaluation-consolidation-company.md).

Frekari upplýsingar um hvernig endurmat á gjaldmiðli virkar í einingunni **Fjárhagur** er að finna í [Endurmat á erlendum gjaldmiðli fyrir fjárhag](./foreign-currency-revaluation-general-ledger.md).

### <a name="additional-information"></a>Viðbótarupplýsingar
- Öll bókunarlög eru sameinuð þegar unnið er úr samstæðunni.
- Aðeins er hægt að bóka losunarbækur í núverandi lagi.
- Aðeins virkar stöður eru sameinaðar. Til þess að sjá opnunarstöður verður þú því enn að keyra árslokalokun í samstæðufyrirtækinu.
- Þú getur bókað daglega færslubók í losunarfyrirtæki, en ekki í samstæðufyrirtæki.
- Leiðréttingar á stöðu í samstæðufyrirtæki er aðeins hægt að gera með því að nota síðuna **Leiðréttingar á lokunartímabili** . 

## <a name="benefits-of-using-financial-reporting-for-financial-consolidations-and-currency-translation-or-to-complement-consolidate-online-for-consolidated-reporting"></a>Kostir þess að nota Financial reporting fyrir fjárhagssamstæður og umreikning gjaldmiðils, eða til viðbótar við samstæðu á netinu fyrir samstæðuskýrslugerð
Viðskiptavinir sem nota Financial reporting fyrir fjárhagssamstæður og umreikning gjaldmiðils, eða til viðbótar við samstæðu á netinu fyrir samstæðuskýrslugerð munu geta nýtt sér ýmsa kosti:

- **Dýpt gagna** - Þú getur búið til samstæðuskýrslur sem sameina raungögn og fjárhagsáætlunargögn bæði á bókahaldsstigi og víddarstigi. Fyrir Finance innihalda gögnin bæði gögn frá fjárhagsáætlunarstýringu og fjárhagsáætlunargerð.
- **Gagnvirkar samstæður** - Hægt er að skapa samstæður hvenær sem er og á hvaða stigi sem er í stigveldi fyrirtækis.
- **Full endurskoðunargeta** - Öllum víddum, lyklum og færsluupplýsingum er viðhaldið fyrir greiningu og endurskoðun. Að auki veitir Financial reporting fulla köfun til baka í upprunalegu færsluna í einhverjum lögaðila sem hefur verið sameinaður.
- **Einfaldaður umreikningur gjaldmiðils** - Eftir lágmarksuppsetningu í Finance getur þú umreiknað allar skýrslur Financial reporting yfir í hvaða skýrslugjaldmiðil sem er sem hefur verið settur upp. Að auki getur þú sett upp ótakmarkaðan fjölda skýrslugjaldmiðla.
- **Bóka losanir í uppruna** - Þú getur búið til og prentað losunarskýrslu til að staðfesta losunarfærslur. Þú getur síðan bókað allar nýjar losanir sem staðlaðar færslur innan samstæðu. Þú getur einnig notað losunarlögaðila fyrir hvaða færslu sem er sem þú vilt ekki hafa í lögaðilum þínum.

## <a name="supported-consolidation-scenarios"></a>Studdar aðstæður samstæðu
Hér eru nokkrar samstæðuaðstæður sem Financial reporting styður:

- Samstæður á einu eða mörgum stigum yfir lögaðila
- Samstæður sem nota skipulag fyrirtækis sem er búið til út frá lögaðilum
- Samstæður sem fela í sér losun
- Hlutdeild minnihluta
- Margar bókhaldslyklar yfir lögaðila
- Mismunandi fjárhagsdagatöl yfir marga lögaðila
- Samstæður sem fela í sér marga skýrslugjaldmiðla
- Samstæður viðskiptaeiningar

## <a name="generating-consolidated-financial-statements"></a>Býr til samstæðureikningsskil
Nánari upplýsingar um aðstæður þar sem þú gætir búið til samstæðureikningsskil er að finna í [Búa til samstæðureikningsskil](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]