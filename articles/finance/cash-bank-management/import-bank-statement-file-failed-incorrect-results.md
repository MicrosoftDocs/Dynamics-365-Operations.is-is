---
title: Úrræðaleit vegna innflutnings bankayfirlitsskrár
description: Þessi grein útskýrir hvernig á að laga vandamál vegna lítils mismunar í bankayfirlitsskránni.
author: angelad116
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44658ea48b9f7dae76c34c5f3d8828c9e8c4ac32
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151761"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Úrræðaleit vegna innflutnings bankayfirlitsskrár

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Þessi virkni verður afskráð í september 2022, nýir notendur ættu að nota rafræn skýrslugerð.

Það er mikilvægt að bankayfirlitsskránni frá bankanum samsvari útliti sem Microsoft Dynamics 365 Finance styður. Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt. Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður. Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni. Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu.

## <a name="what-is-the-error"></a>Hver er villan?

Þegar þú hefur reynt að flytja inn bankayfirlitsskránni, skaltu fara í vinnslusögu gagnastjórnunar og í Gögn og upplýsingar um framkvæmd til að finna villuna. Villan getur hjálpað til með því vísa til yfirlits, stöðu eða uppgjörslínu. Hins vegar er ólíklegt að hún veiti nægar upplýsingar til að auðvelda að auðkenna svæði eða einingu sem veldur vandamálinu.

> [!NOTE]
> Innflutt bankayfirlit geta aðeins skarast fyrir einn tímapunkt.  Ef uppgjöri lýkur til dæmis klukkan 12:00 þann 1. janúar, 2021 þá er upphafsdagsetningin fyrir næsta uppgjör kl. 12:00 þann 1. janúar, 2021 12:00:00.

## <a name="what-are-the-differences"></a>Hver er munurinn?
Berðu saman skilgreiningu útlits bankaskrár við innflutningsskilgreiningu Finance og taktu eftir öllu misræmi í reitum og einingum. Berðu saman bankayfirlitsskrána við tengda sýnisskrá Finance. Í ISO20022 skrárnar ætti að vera auðvelt að sjá mismun.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Munur á tímabelti á innfluttum bankayfirliti
Gildin á dagsetningunni í innflutningsskránni geta verið önnur en gildistíminn sem birtist í fjármálum- og rekstri. Til að koma í veg fyrir þetta misræmi, sláðu inn tímabelti sem valinn er á síðunni **Stilla gagnaveitur**. Frekari upplýsingar um að slá inn tímabeltisval má finna á [Setja upp þróaða innflutningsferli banka](set-up-advanced-bank-reconciliation-import-process.md).

## <a name="transformations"></a>Umbreytingar
Yfirleitt, verður að framkvæma breytinguna í einni af þremur umbreytingum. Hver umbreyting er skrifuð fyrir tiltekna staðla.

| Nafn tilfangs                                         | Skrárnafn                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_í\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_í\_Afstemming\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_í\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Kembing umbreytinga
### <a name="adjust-the-bai2-and-mt940-files"></a>Leiðrétta BAI2 og MT940 skrár

BAI2 og MT940 skrár eru skrár byggðar á texta og þarfnast leiðréttingar til að virkja kembingu Extensible Stylesheet Language-Umbreytinga (XSL-umbreyting). Forritið gerir þessa leiðréttingu þegar skrá er innflutt.

1.  Stofna xml-skrá, og afrita eftirfarandi texta í það.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Afrita innihald bankayfirlitsskrár og líma þau í xml-skrána þannig að þær skipta út **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>Kemba XSL-umbreytingu

Frekari upplýsingar er að finna í <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Ræsa Microsoft Visual Studio.
2.  Stofnið nýtt stjórnborðsforrit.
3.  Opnið viðeigandi XSL-umbreytingu.
4.  Smellt er á XLS-umbreytingu og skilgreiningarsíðu hennar.
5.  Stilltu ílagið á staðsetningu bankayfirlitsskrár.
6.  Skilgreina staðsetningu og skrárnafn fyrir úttak.
7.  Stilltu nauðsynlega rofpunkta.
8.  Á valmyndinni, smelltu á **XML** &gt; **Byrja XSLT kembingu**.

### <a name="format-the-xslt-output"></a>Sníða XLST-úttak

Þegar umbreytingin er keyrð, stofnar hún úttaksskrá sem hægt er að skoða í Visual Studio. Notið Ctrl + A, Ctrl + K og Ctrl + D til að sníða til úttaksskránni á fjótlegan hátt.

### <a name="adjust-the-transformation"></a>Stilla umbreytingu

Stilla umbreytingu til að fá viðeigandi svæði eða einingu í bankayfirlitsskránni. Varpaðu svo þeim reit eða einingu á viðeigandi einingu Finance.

### <a name="debitcredit-indicator"></a>Vísir fyrir debet/kredit

Stundum gætu debet verið flutt inn sem kredit og kredit verið flutt inn sem debet. Til að leysa þetta vandamál verður að breyta viðkomandi XSL-umbreytingu. Ef bankayfirlit koma úr mörgum bönkum, skal tryggja að þau noti allir sama nálgun fyrir debet/kredit, eða stofna aðskilinn umbreytingar.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-sniðmát
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit-sniðmát
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-sniðmát

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Dæmi um bankayfirlitssnið og tæknilegar útlit
Hér að neðan eru dæmi um skilgreiningar tæknilegs útlits fyrir innflutningsskrár ítarlegrar bankaafstemmingar og þriggja tengdum skrám bankayfirlits: Þú getur hlaðið niður skáardæmum og tæknilegum útlitum hér: [Flytja inn skráardæmi](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Skilgreining tæknilegs útlits                             | Dæmi bankayfirlitsskránni          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

