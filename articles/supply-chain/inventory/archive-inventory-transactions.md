---
title: Safnvista birgðafærslur
description: Þessi grein lýsir því hvernig á að safnvista birgðafærslugögn til að hjálpa við að auka afköst kerfisins.
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c63cdee862e2e22649a3eb58ae37597741770e14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874102"
---
# <a name="archive-inventory-transactions"></a>Safnvista birgðafærslur

[!include [banner](../../includes/banner.md)]

Með tímanum mun birgðafærslutaflan (`InventTrans`) vaxa og nota meira pláss í gagnagrunni. Þess vegna verða fyrirspurnir þar sem sækja þarf upplýsingar úr töflunni smám saman hægari. Þessi grein lýsir því hvernig hægt er að nota *Safnvistun á birgðafærslum* eiginleikann til að safnvista gögn um birgðafærslur til að aðstoða við að auka afköst kerfisins.

> [!NOTE]
> Aðeins er hægt að safnvista fjárhagslega uppfærðum birgðafærslum á völdu lokuðu fjárhagstímabili. Til að vera safnvistað verða fjárhagslega uppfærðar birgðafærslur að vera með úthreyfingarstöðuna *Selt* og birgðafærslur á innleið verða að vera með nnhreyfingarstöðuna *Keypt*.

Þegar birgðafærslur eru safnvistaðar eru allar tengdar færslur færðar í `InventTransArchive`-töfluna. Úthreyfingarfærslur birgða og færslur á innhreyfingarskjali eru safnvistaðar sérstaklega, samkvæmt samsetningu vörukennisins (`itemId`) og birgðavíddaauðkenninu (`inventDimId`), og þær eru settar í samantektarfærslur og samanteknar innhreyfingarhreyfingar.

Ef `itemId` `inventDimId` samsetningin inniheldur aðeins eina kvittun eða úthreyfingafærslu, verður færslan ekki safnvistuð.

## <a name="turn-on-the-feature-in-your-system"></a>Kveikja á eiginleikanum í kerfinu

Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessari grein skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Safnvistun á birgðafærslum*. Ekki er hægt að slökkva á þessum eiginleika þegar hann hefur verið gerður virkur.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Það sem þarf að hafa í huga áður en birgðafærslur eru safnvistaðar

Áður en birgðafærslur eru safnvistaðar ætti að hafa í huga eftirfarandi viðskiptaaðstæður vegna þess að þær verða fyrir áhrifum af aðgerðinni:

- Við endurskoðun á birgðafærslum úr tengdum skjölum, svo sem innkaupapöntunarlínum, birtast færslurnar sem safnvistaðar. Til að yfirfara safnvistaðar færslur þarf að fara í **Birgðastjórnun \> Reglubundin verk \> Hreinsun \> Safnvistun á birgðafærslum**.
- Ekki er hægt að hætta við birgðalokun fyrir safnvistuð tímabil. Áður en hægt er að hætta við birgðalokun verður að bakfæra birgðafærslusafnið fyrir viðkomandi tímabil.
- Ekki er hægt að umreikna staðalkostnað fyrir safnvistuð tímabil. Áður en hægt er að umreikna staðalkostnað verður að bakfæra birgðafærslusafnið fyrir viðkomandi tímabil.
- Safnvistun hefur áhrif á birgðaskýrslur sem eru færðar úr birgðafærslum. Þessar skýrslur innihalda aldursgreiningarskýrslu birgða og birgðavirðisskýrslur.
- Þetta kann að hafa áhrif á birgðaspár ef þær eru keyrðar meðan hámarkstími safnvistaðar tímabila er í gangi.

## <a name="prerequisites"></a>Forkröfur

Aðeins er hægt að safnvista birgðafærslur á tímabilum þar sem eftirfarandi skilyrði eru uppfyllt:

- Fjárhagstímabilið verður að vera lokað.
- Keyra verður birgðalokun á eða eftir lokatímabils safnsins.
- Tímabilið verður að vera að minnsta kosti einu ári frá upphafsdagsetningu safnsins.
- Engir endurútreikningar birgða mega vera til staðar.

## <a name="archive-inventory-transactions"></a>Safnvista birgðafærslur

Fylgið eftirfarandi skrefum til að halda áfram að safnvista birgðafærslur.

1. Farið í **Birgðastjórnun** \> **Reglubundin verk** \> **Hreinsun** \> **Safnvistun á birgðafærslum**.

    Síðan **Safnvistun á birgðafærslum** birtist og sýnir lista yfir eldri safnferlisfærslur.

    ![Safnvistunarsíða birgðafærslna.](media/archive-inventory-empty.png "Safnvistunarsíða birgðafærslna")

1. Í aðgerðasvæði skal velja **Safnvistun á birgðafærslum** til að safnvista birgðafærslur.
1. Í svarglugganum **Safnvistun á birgðafærslum** á **Færibreytur** flýtiflipanum, skal stilla eftirfarandi reiti:

    - **Upphafsdagsetning í lokuðu fjárhagstímabili** – Veljið fyrstu dagsetningu færslu sem á að taka með í safninu.
    - **Lokadagsetning í lokuðu fjárhagstímabili** – Veljið síðustu dagsetningu færslu sem á að taka með í safninu.

    ![Svargluggi safnvistunar á birgðafærslum.](media/archive-inventory-dates.png "Svargluggi safnvistunar á birgðafærslum")

    > [!NOTE]
    > Aðeins er hægt að velja tímabil sem uppfylla [Skilyrði](#prerequisites).

1. Í flýtiflipanum **Keyra í bakgrunni** skal stilla upplýsingar runuvinnslu eins og þörf er á. Fylgið venjulegum skrefum fyrir runuvinnslur í Microsoft Dynamics 365 Supply Chain Management.
1. Veljið **Í lagi**.
1. Þú færð skilaboð þar sem þú þarft að staðfesta á að þú viljir halda áfram. Lestu skilaboðin vandlega og veldu svo **Já** ef þú vilt halda áfram.

    Þú færð skilaboð sem segja til um að safnvistun birgðafærsla hafi verið bætt við runubiðröðina. Vinnslan hefur nú safnvistun birgðafærsla á völdu tímabili.

## <a name="view-archived-inventory-transactions"></a>Skoða safnvistaðar birgðafærslur

**Safnvistun á birgðafærslum** sýnir allan safnvistunarferil þinn. Hver lína í hnitanetinu sýnir upplýsingar á borð við dagsetninguna þegar safnið var búið til, notandann sem stofnaði það og stöðu þess.

![Safnvistunarferill á síðunni Safnvistun á birgðafærslum.](media/archive-inventory-full.png "Safnvistunarferill á síðunni Safnvistun á birgðafærslum")

Í fellilistanum efst á síðunni skal velja eitt af eftirfarandi gildum til að sía safnvistanir sem eru sýndar í hnitanetinu:

- **Virkur** – Sýna aðeins virk söfn, ekki bakfærð söfn.
- **Allt** – Sýna öll söfn, bæði virk og bakfærð.

Fyrir hvert safn í hnitanetinu eru eftirfarandi upplýsingar veittar:

- **Virkt** – Gátmerki sýnir að safnið sé virkt.
- **Dagsetning frá** – Dagsetning elstu færslunnar sem hægt er að taka með í safninu.
- **Til dagsetningar** – Dagsetning nýjustu færslunnar sem hægt er að taka með í safninu.
- **Áætlað af** – Notandareikningurinn sem stofnaði safnið.
- **Keyrt** – Dagsetningin þegar safnið var stofnað.
- **Bakfæra** – Gátmerki gefur til kynna að safnið hafi verið bakfært.
- **Stöðva gildandi uppfærslu** – Gátmerki gefur til kynna að safnið sé í vinnslu en að hlé hafi verið gert á henni.
- **Staða** – Staða safnsins. Möguleg gildi eru *Í bið*, *Í vinnslu* og *Lokið*.

Tækjastikan fyrir ofan hnitanetið býður upp á eftirfarandi hnappa sem hægt er að nota til að vinna með valda safnvistun:

- **Safnvistaðar færslur** – Skoða allar upplýsingar um valið safn. Síðan **Safnvistaðar færslur** sem birtist sýnir allar færslurnar í safninu.

    ![Síða safnvistaðra færslna.](media/archive-inventory-transactions.png "Síða safnvistaðra færslna")

    Til að skoða frekari upplýsingar um tiltekna færslu á síðunni **Safnvistaðar færslur** skal velja hana í hnitanetinu og síðan á aðgerðasvæðinu skal velja **Upplýsingar um safnvistaða færslu**. Síðan **Upplýsingar um safnvistaða færslu** sem birtist sýnir upplýsingar á borð við fjárhagsbókun, tengdar tilvísanir undirbókar og fjárhagsvíddir.

- **Gera hlé á safnvistun** – Gera hlé á valdri safnvistun sem er verið að vinna úr. Aðeins er gert hlé eftir að safnvistunarverk hefur verið myndað. Þess vegna gæti liðið stuttur tíma áður en hlé er gert. Þegar búið er að gera hlé birtist gátmerki í reitnum **Stöðva gildandi uppfærslu**.
- **Halda áfram safnvistun** – Halda áfram safnvistun fyrir valda safnvistun sem gert var hlé á.
- **Bakfæra** – Bakfæra valið safn. Aðeins er hægt að bakfæra safn ef **Staða** þess er stillt á *Lokið*. Ef safn hefur verið bakfært birtist gátmerki í reitnum **Bakfæra**.

## <a name="extend-your-code-to-support-custom-fields"></a>Útvíkkaðu kóðann til að styðja sérstillta reiti

Ef `InventTrans` taflan inniheldur einn eða fleiri sérsniðna reiti gætirðu þurft að framlengja kóðann til að styðja þá, allt eftir því hvernig þeir eru nefndir.

- Ef sérsniðnu reitirnir í `InventTrans` töflunni hafa sömu heiti og í `InventtransArchive` töflunni, þýðir það að þeir eru 1:1 kortlagðir. Þar af leiðandi er einfaldlega hægt að setja sérsniðnu reitina í `InventoryArchiveFields` reitarhópinn í `inventTrans` töflunni.
- Ef sérsniðnu reitanöfnin í `InventTrans` töflunni passa ekki við reitanöfnin í `InventtransArchive` töflunni, þá þarftu að bæta við kóða til að kortleggja þau. Ef þú ert til dæmis með kerfisreit sem kallast `InventTrans.CreatedDateTime` þá þarftu að búa til reit í `InventTransArchive` töflunni með öðru heiti (t.d. `InventtransArchive.InventTransCreatedDateTime`) og bæta viðbótum við `InventTransArchiveProcessTask` og `InventTransArchiveSqlStatementHelper` klasana eins og sýnt er í eftirfarandi sýnikóða.

Eftirfarandi sýnishornskóði sýnir dæmi um hvernig á að bæta nauðsynlegri viðbót við `InventTransArchiveProcessTask` flokkinn.

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

Eftirfarandi sýnishornskóði sýnir dæmi um hvernig á að bæta nauðsynlegri viðbót við `InventTransArchiveSqlStatementHelper` flokkinn.

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```
