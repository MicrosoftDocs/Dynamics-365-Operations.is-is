---
title: Skilgreina rafrænna reikningsfærslu í Regulatory Configuration Services (RCS)
description: Þetta efnisatriði útskýrir hvernig skilgreina á rafræna reikningsfærslu í Dynamics 365 Regulatory Configuration Services (RCS).
author: gionoder
ms.date: 05/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6c1d309744c4c8dd0d17f5259551d31c257ede61
ms.sourcegitcommit: 633d51834d7d29b745824924315a3898dc471f1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2021
ms.locfileid: "6075144"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>Skilgreina rafrænna reikningsfærslu í Regulatory Configuration Services (RCS)

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um skilgreiningarmöguleika fyrir rafræna reikningsfærslu í Dynamics 365 Regulatory Configuration Services (RCS).

Það er í gegnum skilgreiningarmöguleikana sem rafræn reikningsfærsla auðveldar þér að uppfylla kröfur fyrirtækis og reglugerða fyrir rafræna reikningsfærslu án þess að þurfa að gera einhverja kóðun. Og í aðstæðunum þar sem rafrænir reikningar verða að vera samþykktir rafrænt af vefþjónustu auðvelda skilgreiningarmöguleikarnir þér einnig að uppfylla kröfur um samskipti í gegnum skilaboð við vefþjónustur án þess að gera einhverja kóðun.

## <a name="electronic-reporting"></a>Rafræn skýrslugerð

Rafræn skýrslugerð styður rafræna reikningsfærslu.

Vörpun og snið gagnalíkansins eru skilgreininalegir þættir sem eru búnir til og unnið með í gegnum rafræna skýrslugerð og notaðir í rafrænni reikningsfærslu. Sniðshönnuður rafrænnar skýrslugerðar er verkfærið til að búa til og vinna með skráarsnið. Hann er notaður til að skilgreina eiginleika rafrænnar reikningsfærslu.

Frekari upplýsingar eru í [Yfirlit yfir rafræna skýrslugerð (ER)](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Eiginleikar rafrænnar reikningsfærslu

Eiginleikar rafrænnar reikningsfærslu bera ábyrgð á að mynda rafræna reikninga í gegnum rafræna reikningsfærslu. Þeir halda utan um skilgreiningarreglur og nota þær til að vinna úr gögnum sem Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management senda til rafrænnar reikningsfærslu og rafrænna reikninga.

Eiginleikarnir styðja líka aðstæður þar sem reglufylgni við forskriftir skráarsniðs er nauðsynleg og útkoman er sjálfstæð rafræn skrá. Í flestum tilfellum eru forskriftir skráarsniðs birt af skattyfirvöldum.

Að lokum styðja eiginleikarnir samskipti með skilaboðum við ytri vefþjónustur sem eru hýstar annaðhvort af skattyfirvöldum eða viðurkenndum aðila, og beiðnir um heimild eða samþykktarstimpil í rafrænum reikningi.

### <a name="availability-of-electronic-invoicing-features"></a>Framboð á eiginleikum rafrænnar reikningsfærslu

Framboð á eiginleikum rafrænnar reikningsfærslu fer eftir landinu eða svæðinu. Þótt sumir eiginleikar séu almennt í boði eru aðrir í forútgáfu.

#### <a name="generally-available-features"></a>Almennt tiltækir eiginleikar

Eftirfarandi tafla sýnir eiginleika rafrænnar reikningsfærslu sem eru almennt í boði.

| Land/svæði | Heiti eiginleika                         | Viðskiptaskjal |
|----------------|--------------------------------------|-------------------|
| Egyptaland          | Egypskur rafrænn reikningur (EG) | Sölureikningar og verkreikningar |

#### <a name="preview-features"></a>Forskoðunareiginleikar

Eftirfarandi tafla sýnir eiginleika rafrænnar reikningsfærslu sem eru í forútgáfu sem stendur.

| Land/svæði | Heiti eiginleika                         | Viðskiptaskjal |
|----------------|--------------------------------------|-------------------|
| Austurríki        | Rafrænir reikningar í Austurríki (AT)    | Sölureikningar og verkreikningar |
| Belgía        | Belgískur rafrænn reikningur (BE)      | Sölureikningar og verkreikningar |
| Brasilía         | Brasilískt NF-e (BR)                  | Fjárhagsskjalalíkan 55, leiðréttingarbréf, afturkallanir og fleygingar |
| Brasilía         | Brasilískt NFS-e ABRASF Curitiba (BR) | Fjárhagsskjöl þjónustu |
| Danmörk        | Danskur rafrænn reikningur (DK)       | Sölureikningar og verkreikningar |
| Eistland        | Eistneskur rafrænn reikningur (EE)     | Sölureikningar og verkreikningar |
| Finnland        | Finnskur rafrænn reikningur (FI)      | Sölureikningar og verkreikningar |
| Frakkland         | Franskur rafrænn reikningur (FR)       | Sölureikningar og verkreikningar |
| Þýskaland        | Þýskur rafrænn reikningur (DE)       | Sölureikningar og verkreikningar |
| Ítalía          | FatturaPA (IT)                       | Sölureikningar og verkreikningar |
| Mexíkó         | Mexíkóskt CFDI (MX)                    | Sölureikningar, fylgiseðlar, birgðaflutningar, greiðsluuppfyllingar og afturkallanir |
| Holland    | Hollenskur rafrænn reikningur (NL)        | Sölureikningar og verkreikningar |
| Noregur         | Norskur rafrænn reikningur (NO)    | Sölureikningar og verkreikningar |
| Spánn          | Spænskur rafrænn reikningur (ES)      | Sölureikningar og verkreikningar |
| Evrópa         | PEPPOL rafrænn reikningur            | PEPPOL sölureikningar og verkreikningar |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Skilgreinanlegir þættir fyrir eiginleika rafrænnar reikningsfærslu

Eiginleikar rafrænnar reikningsfærslu samanstanda af eftirfarandi flokkum skilgreinanlegra þátta:

- **Snið** – Snið gera þér kleift að skilgreina hvað rafrænnar reikningsfærslu verður að mynda þegar rafrænt skjal verður að rafrænum reikningi. Snið fela í sér skilgreiningu sniðs fyrir rafrænan reikning og fyrir skrár og skilaboð sem eru notuð til að senda inn beiðnir og taka við svörum þegar samskipti við ytri vefþjónustu eru nauðsynleg.
- **Aðgerðir** – Aðgerðir gera þér kleift að skilgreina hvernig rafræn reikningsfærsla myndar umbreytingu á rafrænu skjali sem Finance and Supply Chain Management sendu inn í rafrænan reikning.
- **Gildissviðsreglur** – Gildissviðsreglur gera þér kleift að skilgreina samhengið sem rafræn reikningsfærsla verður að hafa í huga til að vinna úr eiginleika rafrænnar reikningsfærslu.
- **Breytur** – Breytur gera þér kleift að skilgreina stuðninginn við smíði á rökum skilgreiningar. Breytur geta virkað sem innsláttur gilda til að framkvæma tiltekna aðgerð. Þær geta líka virkað sem skipti á gildum milli Finance and Supply Chain Management og rafrænnar reikningsfærslu.
- **Líkanavörpun rafræns skjals** – Líkanavörpun rafræns skjals gerir þér kleift að skilgreina líkanavörpun rafrænnar skýrslugerðar. Líkanavörpunin skilgreinir gagnavörpun á útdrætti reiknings sem er felldur inn í rafræna reikningsfærslu þegar rafræn skjöl eru send inn.
- **Samhengislíkan reiknings** – Samhengislíkan reiknings gerir þér kleift að skilgreina samhengislíkan reiknings í rafrænni skýrslugerð og ákveða samhengi eiginleika rafrænnar reikningsfærslu.
- **Svargerðir** – Svargerðir gera þér kleift að skilgreina hvað rafræn reikningsfærsla þarf að uppfæra í Finance and Supply Chain Management eftir úrvinnslu á rafræna reikningnum.

### <a name="formats"></a>Snið

Eftirfarandi listar sýna skilgreiningar rafræns skýrslugerðarsniðs sem eru í boði fyrir eiginleika rafrænnar reikningsfærslu.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Austurríki (AT) rafrænn reikningur: Sölu- og verkreikningar fyrir Austurríki

- OIOUBL sölureikningur
- OIOUBL verkreikningur
- OIOUBL sölukreditnóta
- OIOUBL kreditnóta verks

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgískur (BE) rafrænn reikningur: Sölu- og verkreikningar fyrir Belgíu

- UBL sölureikningur BE
- UBL verkreikningur BE
- UBL kreditnóta verks BE
- UBL sölukreditnóta BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brasilískt (BR) NF-e: NF-e Federal (Brasilía)

- Útflutningssnið NF-e-innsendingar (BR)
- Útflutningssnið NF-e-leiðréttingarbréfs (BR)
- Útflutningssnið NF-e-afturköllunar (BR)
- NF-e fleygja útflutningssniði (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brasilískt NFS-e (BR): NFS-e ABRASF Curitiba-borg

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF Inquire Curitiba (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Danmörk (DK) rafrænn reikningur: Sölu- og verkreikningar fyrir Danmörku

- OIOUBL sölureikningur
- OIOUBL verkreikningur
- OIOUBL sölukreditnóta
- OIOUBL kreditnóta verks

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Hollenskur (NL) rafrænn reikningur: Sölu- og verkreikningar fyrir Holland

- UBL sölureikningur NL
- UBL verkreikningur NL
- UBL kreditnóta verks NL
- UBL sölukreditnóta NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Egypskur (EG) rafrænn reikningur: Sölu- og verkreikningar fyrir Egyptaland

- Sölureikningur (EG)(Reikningsfærsla)
- Verkreikningur (EG)(Reikningsfærsla)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Eistland (EE) rafrænn reikningur: Sölu- og verkreikningar fyrir Eistland

- Sölureikningur (EE)
- Verkreikningur (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Finnland (FI) rafrænn reikningur: Sölu- og verkreikningar fyrir Finnland

- Sölureikningur (FI)
- Verkreikningur (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Frakkland (FR) rafrænn reikningur: Sölu- og verkreikningar fyrir Frakkland

- UBL sölureikningur FR
- UBL verkreikningur FR
- UBL kreditnóta verks FR
- UBL sölukreditnóta FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Þýskaland (FR) rafrænn reikningur: Sölu- og verkreikningar fyrir Þýskaland

- Sölureikningur (DE)
- Verkreikningur (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Ítalía (IT) rafrænn reikningur: Sölu- og verkreikningar fyrir Ítalíu

- Sölureikningur (IT)
- Verkreikningur (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Mexíkó (MX) CFDI: CFDI fyrir Mexíkó

- CFDI-reikningssnið (MX)
- CFDI-fylgiseðill (MX)
- CFDI-birgðaflutningur (MX)
- CFDI-greiðslusnið (MX)
- Afturköllunarsnið CFDI-reiknings (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Noregur (NO) rafrænn reikningur: Sölu- og verkreikningar fyrir Noreg

- OIOUBL sölureikningur
- OIOUBL verkreikningur
- OIOUBL sölukreditnóta
- OIOUBL kreditnóta verks

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL rafrænn reikningur: PEPPOL sölu- og verkreikningar

- PEPPOL sölureikningur
- PEPPOL verkreikningur
- PEPPOL sölukreditnóta
- PEPPOL kreditnóta verks

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Spánn (ES) rafrænn reikningur: Sölu- og verkreikningar fyrir Spán

- Sölureikningur (ES)
- Verkreikningur (ES)

Auk tilbúinna skilgreininga á rafrænu skýrslugerðarsniði sem eru í boði í rafrænu reikningsfærsluþjónustunni, er einnig hægt að búa til sínar eigin skilgreiningar á rafrænu skýrslugerðarsniði. Hins vegar styðja sniðsskilgreiningarnar, sem eru gerðar til að nota með eiginleikum rafrænnar reikningsfærslu, ekki beina tilvísun í töflur Finance og Supply Chain Management eða samsvarandi lýsigögn. Aðeins tilvísanir í vörpun ER-líkans eru studdar.

### <a name="actions"></a>Aðgerðir

Eftirfarandi tafla sýnir tiltækar aðgerðir og hvort þær eru almennt í boði sem stendur eða enn í forútgáfu.

| Aðgerð                                        | lýsing                                                                  | Til ráðstöfunar         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Breyta skjali                            | Keyrið rafrænt skýrslugerðarsnið til að breyta skjalinu.                   | Almennt tiltækt  |
| Skrifa undir xml-skjal                             | Undirritið XML-skjöl með stafrænni undirskrift.                                   | Í kynningarútgáfu           |
| Undirrita JSON-skjal fyrir egypsk skattyfirvöld | Undirritið JSON-skjöl með stafrænni undirskrift fyrir egypsk skattyfirvöld.       | Almennt tiltækt  |
| Samþætta við egypska ETA-þjónustu           | Hefjið samskipti við egypsk skattyfirvöld.                                     | Almennt tiltækt  |
| Hringja í SEFAZ-þjónustu í Brasilíu                  | Samþættið við brasilíska SEFAZ-þjónustu fyrir innsendingu fjárhagsskjals.       | Í kynningarútgáfu           |
| Hringja í PAC-þjónustu í Mexíkó                      | Samþættið við mexíkóska PAC-þjónustu fyrir innsendingu CFDI.                      | Í kynningarútgáfu           |
| Vinna úr svari                              | Greinið svarið sem var móttekið frá vefþjónustukalli.                     | Almennt tiltækt  |
| Nota MS Power Automate                         | Samþættið við ferli sem er byggt inn í Microsoft Power Automate.                       | Í kynningarútgáfu           |

### <a name="applicability-rules"></a>Gildissviðsreglur

Gildissviðsreglur eru stillanleg ákvæði sem eru skilgreind á stigi rafræns reikningsfærslueiginleika. Reglurnar eru stilltar til að gefa samhengi fyrir framkvæmd rafrænna reikningsfærslueiginleika í gegnum safn af möguleikum rafrænnar reikningsfærslu.

Þegar viðskiptaskjal úr Finance eða Supply Chain Management er sent inn til rafrænnar reikningsfærslur, inniheldur viðskiptaskjalið ekki neina beina tilvísun sem gerir safni af möguleikum rafrænnar reikningsfærslu kleift að kalla á ákveðinn eiginleika rafrænnar reikningsfærslu til að vinna úr innsendingunni.

Engu að síður, þegar viðskiptaskjalið er skilgreint á viðeigandi hátt, inniheldur það nauðsynlega þætti sem gera rafrænni reikningsfærslu kleift að finna út hvaða eiginleika rafrænnar reikningsfærslu þarf að velja og síðan mynda rafrænan reikning.

Gildissviðsreglur gerir safni af möguleikum rafrænnar reikningsfærslu kleift að finna nákvæmlega þá eiginleika rafrænnar reikningsfærslu sem þarf að nota til að vinna úr innsendingunni. Það er gert með því að samsvara innihald innsenda skjalsins við ákvæðin í gildissviðsreglunum.

Til dæmis eru tveir eiginleikar rafrænnar reikningsfærslu með tengdum gildissviðsreglum settir upp í safn af möguleikum rafrænnar reikningsfærslu.

| Eiginleiki rafrænnar reikningsfærslu | Gildissviðsreglur        |
|------------------------------|--------------------------- |
| A                            | <p>Land = BR</p><p>og</p><p>Lögaðili = BRMF</p>  |
| V                            | <p>Land = MX</p><p>og</p><p>Lögaðili = MXMF</p>  |

Ef viðskiptaskjal úr Finance eða Supply Chain Management er sent inn í safn af möguleikum rafrænnar reikningsfærslu inniheldur viðskiptaskjalið eftirfarandi eigindir sem fylltar eru út sem:

- Land = BR
- Lögaðili = BRMF

Safn rafrænna reikningsfærslumöguleika mun velja rafrænan reikningsfærslueiginleika **A** til að vinna úr innsendingunni og mynda rafrænan reikning.

Á sama hátt, ef viðskiptaskjalið inniheldur:

- Land = MX
- Lögaðili = MXMF

Rafrænn reikningsfærslueiginleiki **B** er valinn til að mynda rafrænan reikning.

Stilling á gildissviðsreglum má ekki vera tvíræð. Þetta þýðir að tveir eða fleiri eiginleikar rafrænnar reikningsfærslu mega ekki vera með sama ákvæðið, annars leiðir það til þess að ekkert er valið. Ef upp kemur tvítekning á eiginleikum rafrænnar reikningsfærslu, til að forðast tvíræðni, skal nota frekari ákvæði til gera safni rafrænna reikningsfærslumöguleika kleift að sjá muninn milli rafrænu reikningsfærslueiginleikanna.

Skoðið t.d. rafræna reikningsfærslueiginleikann **C**. Þessi eiginleiki er afrit af rafrænum reikningsfærslueiginleika **A**.

| Eiginleiki rafrænnar reikningsfærslu | Gildissviðsreglur        |
|------------------------------|--------------------------- |
| A                            | <p>Land = BR</p><p>og</p><p>Lögaðili = BRMF</p>  |
| K                            | <p>Land = BR</p><p>og</p><p>Lögaðili = BRMF</p>  |

Í þessu dæmi er eiginleiki **C** fyrir framan innsendingu viðskiptaskjals sem inniheldur eftirfarandi:

- Land = BR
- Lögaðili = BRMF

Rafrænn reikningsmöguleiki getur ekki fundið út hvorn rafrænan reikningsfærslueiginleikann á að nota til að vinna úr innsendingunni vegna þess að innsendingarnar innihalda nákvæmlega sömu ákvæðin.

Til að aðgreina eiginleikana tvo í gegnum gildissviðsreglur þarf að bæta nýju ákvæði við einn af eiginleikunum til að gera safni rafræns reikningsfærslumöguleika kleift að velja viðeigandi eiginleika rafrænnar reikningsfærslu.

| Eiginleiki rafrænnar reikningsfærslu | Gildissviðsreglur        |
|------------------------------|--------------------------- |
| A                            | <p>Land = BR</p><p>og</p><p>Lögaðili = BRMF</p>  |
| K                            | <p>Land = BR</p><p>og</p><p>Lögaðili = BRMF</p><p>og</p><p>Model=55</p>  |

Til að styðja fleiri flóknari ákvæði eru eftirfarandi tilföng í boði:

Röklegir virkjar:
- Og
- Eða

Gerðir virknitákna:
- Equal
- Not equal
- Greater than
- Less than
- Stærra en eða jafnt og
- Minna en eða jafnt og
- Contains
- Byrjar á

Gagnagerðir:
- Strengur
- Númer
- Boole
- Dagsetning
- UUID

Geta til að flokka og afflokka ákvæði.
Dæmið lítur þannig út.

| Eiginleiki rafrænnar reikningsfærslu | Gildissviðsreglur        |
|------------------------------|--------------------------- |
| K                            | <p>Land = BR</p><p>og</p><p>( Lögaðili = BRMF</p><p>eða</p><p>Model=55)</p>  |


## <a name="configuration-providers"></a>Skilgreiningarveitur

Skilgreiningarveitur bjóða upp á eiginleika rafrænnar reikningsfærslu og rafræna skýrslugerðarþætti þeirra, svo sem líkanavörpun, skilgreiningu sniðs og samhengislíkan. Þær gefa út eiginleika rafrænnar reikningsfærslu og rafræna skýrslugerðarþætti í tengdri altækri geymslu. Þaðan geta önnur fyrirtæki sótt þá.

Áður en eiginleikar rafrænnar reikningsfærslu eru skilgreindir í gegnum RCS þarf að skilgreina eigið fyrirtæki sem skilgreiningarveitu í einingunni **Rafræn skýrslugerð**. Frekari upplýsingar um hvernig á að stilla skilgreiningarveitu á **Virk** er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Eiginleikar rafrænnar reikningsfærslu skoðaðir í altækri geymslu

Til að fletta í gegnum eiginleika rafrænnar reikningsfærslu sem eru í boði í altækri geymslu fyrir tiltekna skilgreiningarveitu skal samstilla RCS-tilvik fyrirtækisins. Að samstillingu lokinni verður listi yfir tiltæka eiginleika rafrænnar reikningsfærslu uppfærður.

## <a name="importing-electronic-invoicing-features"></a>Flytja inn eiginleika rafrænnar reikningsfærslu

Áður en eiginleikar rafrænnar reikningsfærslu eru notaðir eða skilgreindir þarf að flytja þá inn í RCS-tilvik fyrirtækisins. Innflutningsaðgerðin býr til staðbundið afrit af eiginleikunum og afritar allar gervingar rafrænnar skýrslugerðar sem eiginleikarnir nota (til dæmis skilgreiningar sniðs og líkanaskilgreiningar) við RCS-tilvik fyrirtækisins.

Hægt er að flytja inn eiginleikar rafrænnar reikningsfærslu úr hvaða skilgreiningarveitu sem er.

## <a name="creating-electronic-invoicing-features"></a>Eiginleikar rafrænnar reikningsfærslu búnir til

Hægt er að búa til eiginleika rafrænnar reikningsfærslu frá grunni eða út frá öðrum eiginleika rafrænnar reikningsfærslu.

Þegar eiginleiki rafrænnar skýrslugerðar er búinn til frá grunni þarf að bæta við handvirkt þáttum rafrænnar skýrslugerðar (t.d. skilgreiningarútgáfu eiginleika og öðrum skilgreiningum á borð við uppsetningu eiginleikaútgáfu og uppsetningu forrits). Þegar eiginleiki er búinn til út frá öðrum eiginleika erfir nýi eiginleikinn allar skilgreiningar frá þeim upprunalega. 

## <a name="electronic-invoicing-feature-version"></a>Eiginleikaútgáfa rafrænnar reikningsfærslu

Eiginleikar rafrænnar reikningsfærslu fá úthlutað útgáfu. Þegar ný útgáfa er búin til hækkar útgáfunúmerið sjálfkrafa. Hægt er að skilgreina „gildir frá“ dagsetningu fyrir nýju útgáfuna.

Eiginleikaútgáfur rafrænnar reikningsfærslu fylgja stuðningstíma sem er með allt að þrjár stöður:

- **Drög** – Ef útgáfa eiginleika er í þessari stöðu er hægt að breyta skilgreiningareigindum og öllum gervingum hennar (til dæmis skilgreiningum skráarsniðs).
- **Lokið** – Ef útgáfa eiginleika er í þessari stöðu hefur hún verið birt í altækri geymslu sem tengist fyrirtækinu. Ekki er lengur hægt að breyta eiginleikaútgáfunni eða einhverjum þáttum rafrænnar skýrslugerðar.
- **Birt** – Ef útgáfa eiginleika er í þessari stöðu hefur hún verið birt í rafrænni reikningsfærslu. Ekki er lengur hægt að breyta eiginleikaútgáfunni eða einhverjum þáttum rafrænnar skýrslugerðar.

### <a name="feature-configurations"></a>Eiginleikastillingar

Eiginleikaskilgreiningar halda öllum skilgreiningum rafræns skýrslugerðarsniðs sem eiginleikar rafrænnar reikningsfærslu nota. Allar rafrænar skrár sem eiginleikar rafrænnar reikningsfærslu nota við vinnslu koma úr skilgreiningum sniðs sem bætt hefur verið við eiginleikaskilgreiningar fyrir þennan eiginleika.

Úr skilgreiningum eiginleika er hægt að fá aðgang að sniðshönnuði rafrænnar skýrslugerðar, sem er verkfæri rafrænnar skýrslugerðar sem er notað til að búa til skilgreiningar sniðs.

### <a name="feature-setup"></a>Uppsetning eiginleika

Uppsetningar eiginleika eru notaðar í bland við skilgreiningar eiginleika. Sérhver uppsetning eiginleika nær utan um safn aðgerða, gildissviðsreglur og breytur sem bjóða upp á væntanlega hegðun þannig að eiginleiki rafrænnar reikningsfærslu getur uppfyllt tiltekna kröfu rafræna reikningsins.

### <a name="application-setup"></a>Uppsetning forrits

Uppsetning forrits verður að vera tengd við tengt forrit sem var áður stofnað.

Í gegnum uppsetningu forrits er hægt að skilgreina hluta rafræns reikningsfærslueiginleika sem þarf að gera í Finance and Supply Chain Management. Að minnsta kosti þrír skilgreinanlegir þættir eru áskildir burtséð frá eiginleika rafrænnar reikningsfærslu:

- **Töfluheiti** – Einingin í Finance and Supply Chain Management sem geymir bókaða reikninga og sem eiginleiki rafrænnar reikningsfærslu byggir á.
- **Samhengi** – Heiti samhengislíkans reiknings sem var skilgreint í gegnum rafræna skýrslugerð.
- **Vörpun viðskiptaskjals** – Heiti vörpunarlíkans reiknings sem var skilgreint í gegnum rafræna skýrslugerð.

> [!IMPORTANT]
> Skilgreiningin sem er færð inn í uppsetningu forritsins er hægt að skoða í Finance and Supply Chain Management. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreyta rafrænna skjala**. Í flipanum **Rafrænt skjal** skal velja **Nota** og síðan velja valkostinn **Tengt forrit**.

### <a name="deploying-feature-versions"></a>Eiginleikaútgáfur notaðar

Í RCS er skipunin **Nota** notuð til að birta ákveðna eiginleikaútgáfu rafrænnar reikningsfærslu. Veljið **Nota** og veljið síðan einn af eftirfarandi valkostum til að skilgreina markmið uppsetningarinnar: 

- **Þjónustuumhverfi** – Þegar markmið uppsetningarinnar er þjónustuumhverfið er útgáfa rafræns reikningsfærslueiginleika birt í þjónustuumhverfinu. Rafræn reikningsfærsla er þá tilbúin til að taka við og vinna úr rafrænum skjölum sem Finance and Supply Chain Management senda.
- **Tengt forrit** – Þegar markmið uppsetningarinnar er tengda forritið verður skilgreiningin sem gefin er upp af uppsetningu forritsins skrifuð í tilviki Finance and Supply Chain Management sem var tengt við hana á undan.

Aðeins eiginleikaútgáfur rafrænnar reikningsfærslu sem eru með stöðuna **Lokið** er hægt að setja upp í annaðhvort þjónustuumhverfi eða tengt forrit.

### <a name="removing-feature-versions"></a>Fjarlægir eiginleikaútgáfu

Í RCS er skipunin **Hætta að nota** notuð til að fjarlægja tiltekna eiginleikaútgáfu rafrænnar reikningsfærslu úr þjónustuumhverfi í rafrænni reikningsfærslu.

> [!IMPORTANT]
> Skipunin **Hætta að nota** virkar aðeins í þjónustuumhverfum. Það fjarlægir ekki eiginleikaútgáfur fyrir rafrænar reikningsfærslur úr tengdum forritum.

### <a name="rebasing-electronic-invoicing-features"></a>Eiginleikar rafrænnar reikningsfærslu endurreiknaðir

Þegar einn eiginleiki rafrænnar reikningsfærslu er tekinn frá öðrum, uppfærir skipunin **Endurreikna grunn** afleiddan eiginleika með breytingunum sem hafa verið gerðar á upprunalega eiginleikanum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gefa út rafræna reikninga í Finance and Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
