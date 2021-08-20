---
title: Úrræðaleita birgðaaðgerðir
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með birgðaaðgerðir.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 1198bc12830afa2ae2c5eb8e77413a9d8ef70c625823f676ab1965ff250c2443
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730394"
---
# <a name="troubleshoot-inventory-operations"></a>Úrræðaleita birgðaaðgerðir

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með birgðaaðgerðir.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Ekki er hægt að finna felligluggann „Verkflæði“ fyrir birgðabækur.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ekki er hægt að **Verkflæði** felligluggann á færslusíðunni eða tengdar verkflæðisaðgerðir eru ekki í boði.

Þrjár ástæður geta verið fyrir þessu vandamáli eins og lýst er í eftirfarandi undirköflum.

### <a name="issue-resolution-1"></a>Úrlausn úrlausnaratriðis 1

Ef vandamálið á við alla notendur kann það að koma upp vegna þess að samþykktarverkflæði hefur ekki verið úthlutað á færslubókarheitið. Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Farið í **Birgðastjórnun &gt; Uppsetning &gt; Færslubókarheiti &gt; Birgðir**.
1. Veljið heiti færslubókar úr listadálknum til að opna stillingasíðuna.
1. Á flipanum **Almennt** skal stilla **Samþykktarverkflæði** valkostinn á *Já*. Ef notandi er beðinn um að staðfesta breytinguna skal velja **Já**.
1. Í reitnum **Verkflæði** skal velja verkflæðið sem á að nota fyrir valið heiti færslubókar.

### <a name="issue-resolution-2"></a>Úrlausn úrlausnaratriðis 2

Ef verkflæðið notar sérsniðinn kóða gætu vandamál komið upp eftir uppfærslu á kerfinu. Í verkflæði færslubókar gæti til dæmis hnappurinn **Senda inn** verið skyggður þannig að ekki er hægt að velja hann til að samþykkja innsendingu.

Ef hnappurinn **Senda inn** er skyggður gæti verkflæðið hafa verið sérstillt, sem þýðir að aðferð verkflæðisins, `canSubmitToWorkflow()` í `FormDataUtil`, hafi verið stækkuð. Til að laga þetta vandamál skal breyta því hvernig aðferð er stækkuð fyrir `canSubmitToWorkflow()` til að nota skipulagið í eftirfarandi dæmi.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Úrlausn úrlausnaratriðis 3

Ef vandamálið á aðeins við fáa tiltekna notendur gætu þessir notendur ekki haft þau öryggisréttindi sem krafist er til að keyra verkflæðisaðgerðir á birgðabókum. Gangið úr skugga um að hver og neinn notandi hafi öryggisréttindin *Vinna með verkflæði í birgðabók*. Sjálfgefið er að þessum réttindum sé úthlutað á skyldu sem er með sama heiti og skyldan er notuð í hlutverkunum *Starfsmaður í vöruhúsi* og *Vöruhúsastjórnandi*.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Birgðabókin mín er áfram í læstri stöðu og runuvinnsla verkflæðis virkar ekki.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ein af birgðabókum notanda er læst af einhverri aðgerð og ekki er verið að losa hana. Ef óþekkt villa kemur til dæmis upp við bókun (sem er aðgerð kerfislæsingar) gæti færslubókin áfram verið í læstri stöðu. Í þessu tilviki mun rekill vinnuliðar í verkflæði birta villu á meðan sannprófun á læsingu er gerð.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Skráið ykkur inn í SQL-þjónstilvik fyrir Supply Chain Management og athugið hvort **InventJournalTable.SystemBlocked** sé stillt á *1*. Ef svo er skal ganga úr skugga um að færslubókin eigi ekki að vera í læstri stöðu og síðan endurstilla **InventJournalTable.SystemBlocked** á *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Verkflæði fyrir birgðabókina mína klárast aldrei og hvorki er hægt að breyta færslubókinni né bóka hana.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar búið er að senda inn samþykktarverkflæði færslubókar hættir verkflæðisferli að svara og ekki verður hægt að breyta eða vinna úr færslubókunum.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ýmsar ástæður eru fyrir því að ekki er hægt að ljúka við verkflæðisferli. Kannið eftirfarandi vandamál:

- Opnið **Birgðastjórnun &gt; Uppsetning&gt; Verkflæði birgðastjórnunar**, og farið yfir skilgreininguna á verkflæðinu sem um ræðir. Fyrir frekari upplýsingar sjá [Samþykktarverkflæði birgðabókar](inventory-journal-workflow.md).
- Í verkflæðinu gæti hugsanlega hafa komið upp undantekning eða villa. Farið yfir feril vinnuliðar í verkflæðinu sem um ræðir til að sjá hvort í honum sé forritsvilla sem stöðvar verkflæðið.
- Aðeins er hægt að uppfæra birgðabókina eða breyta henni ef hún er samþykkt. Ef afturköllun er virk er hægt að reyna að afturkalla færslubókina. Ekki er hægt að fresta keyrslu á runuvinnslunni af mörgum ástæðum. Sumar af þessum ástæðum gætu stafað af vandamáli varðandi verkflæðisrammann.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Skilyrði verkflæðis birgðabókar gilda aðeins á færslubókarstigi, ekki á línustigi

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál gæti komið upp ef til dæmis reynt er að setja upp skilyrði fyrir verkflæði birgðabókar í kostnaðarupphæðinni. Skilyrði er sett upp þannig að skref 1 er aðeins keyrt þegar kostnaðarupphæðin er lægri en 100. Síðan er sett upp annað skilyrði þannig að skref 2 er aðeins keyrt þegar kostnaðarupphæðin er hærri en eða jöfn og 100. Því næst, þegar verkflæðið er keyrt, sýnir verkflæðissagan aðeins eina línu og fyrsta skilyrðið er alltaf metið sem *satt* burtséð frá gildinu sem er sent inn.

### <a name="issue-workaround"></a>Lausn á vandamálinu

Í núverandi útgáfu eiga skilyrði í verkflæði birgðabókar aðeins við á færslubókarstigi, ekki á línustigi. Þessi hegðun er samkvæmt hönnuninni. Mælt er með því að skilyrðið sé aðeins sett á fyrir eigindir á færslubókarstigi.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>Síusvæðið á listasíðu lagers síar ekki niðurstöður eins og ég geri ráð fyrir.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Síurnar á síusvæðinu á **Listasíða lagers** síðunni sía ekki niðurstöður eins og þú gerir ráð fyrir.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni.

Síðan  **Lagerlisti**  er sett saman úr ítarlegri töflu yfir lagerbirgðir sem inniheldur allar tiltækar víddir. Listinn á þessari síðu er hins vegar samantekt. Hann gæti þar af leiðandi sameinað línur úr upprunatöflunni með því að leggja saman gildi samkvæmt víddunum sem eru sýndar.

Síur sem eru settar upp á síusvæðinu eiga við upprunatöfluna, ekki uppsafnaðan lista. Þessi hegðun getur stundum leitt til óvæntrar niðurstöðu eins og lýst er í [þessum dæmum](inventory-on-hand-list.md#examples).

 [Síurnar sem gefnar eru upp í hnitanetinu](inventory-on-hand-list.md#grid-filters)  *eiga*  hinsvegar við samanlagða listann. Þessar síur fela í sér bæði QuickFilter efst í hnitanetinu og síuna fyrir hvern dálkahaus.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Eining og magn einingar virka ekki á réttan hátt í birgðabókinni.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Annað eða bæði þessi vandamál gætu komið upp þegar unnið er með einingar og magn í birgðabók:

- Ekki er hægt að breyta einingum eða magni í birgðabókinni á meðan umreikningseining er sett upp fyrir útgefna afurð og ekki er hægt að skipta um einingu í birgðabókinni.
- Reitirnir **Magn** og **Eining** sjást í birgðabókinni, en reiturinn **Magn einingar** sést ekki. Ef einingunni er breytt skal færa inn magn og bóka færslubókina, færslubókin sýnir enn upprunalega mælieininguna fyrir það magn.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Til að laga þetta vandamál skal fylgja þessum skrefum.

1. Á vinnusvæðinu **Eiginleikastjórnun** skal ganga úr skugga um að kveikt sé á eiginleikanum *Notkun mælieiningar og einingarmagns í birgðabókum*. Þessi eiginleiki bætir reitunum **Eining** og **Magn einingar** við færslubókina.
1. Þegar kveikt hefur verið á eiginleikanum skal nota reitina **Magn**, **Magn einingar** og **Eining** á eftirfarandi hátt:

    - **Magn** – Tilgreinið magnið með því að nota sjálfgefna einingu sem er skilgreind fyrir útgefna afurð. Sjálfgefin eining er hins vegar ekki sýnd hér. Ef umreikningur er uppsettur milli sjálfgefinnar einingar og einingarinnar sem er valin í reitnum **Eining** verður reiturinn **Magn** uppfærður sjálfkrafa út frá því sem er valið í reitunum **Magn einingar** og **Eining**.
    - **Magn einingar** – Tilgreinið magnið með því að velja eininguna sem er valin í reitnum **Eining**.
    - **Eining** – Veljið eininguna sem á að nota fyrir gildið í reitnum **Magn einingar**.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Ég fæ eftirfarandi villuskilaboð: „Hámarksfjöldi aukastafa fyrir birgðahaldseininguna er 0.“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar reynt er að bóka birgðafærslu eða birgðafrátekningu koma upp eftirfarandi villuboð: „Hámarksfjöldi aukastafa fyrir birgðahaldseininguna er 0.“

Þetta vandamál kemur upp þegar magn birgðafærslunnar er tilgreint sem gildi í aukastöfum sem er undir nákvæmnismörkunum sem reiturinn styður. Til dæmis *hefur magn 0,5* verið tilgreint fyrir birgðafærsluna en aðeins heiltölumagn er stutt. Þess vegna ætti gildið að vera *1* í stað *0,5*.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

1. Keyrið eftirfarandi forskrift í tilviki SQL Server til að slétta magn í birgðafærslum. Þessi forskrift mun leiðrétta gildi í töflunni **inventTrans** .

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Keyra skal samræmisathugun á birgðum þar sem kveikt er á valkostinum **Leiðrétta villu**. Þessi athugun mun leiðrétta gildi í tölfunni **inventSum**.

> [!IMPORTANT]
> Sérstaklega er mælt með því að fara gætilega þegar forskriftinni er breytt samkvæmt þörfum umhverfisins, prófið hana í prófunarumhverfi og athugið síðan niðurstöðurnar áður en forskriftin er keyrð í framleiðsluumhverfi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]